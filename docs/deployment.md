# Deployment Guide

## Overview

daïmōnes is designed for sovereign deployment — your infrastructure, your data, your control. This guide covers single-node deployment suitable for academic institutions, research labs, and private deployments.

## Prerequisites

### Hardware Requirements
- **GPU**: NVIDIA L4 (24GB VRAM) or equivalent
- **CPU**: 8+ cores (Intel Xeon or AMD EPYC recommended)
- **RAM**: 64GB minimum
- **Storage**: 500GB SSD (1TB recommended for production)
- **Network**: Inbound HTTPS (port 443), no outbound required

### Software Requirements
- **OS**: Ubuntu 22.04 LTS or Debian 12+
- **NVIDIA Driver**: 535+ (with CUDA 12.2 support)
- **Docker**: 24.0+ (for containerized deployment)
- **Node.js**: 20 LTS (for manual deployment)
- **PostgreSQL**: 15+ with pgvector extension

## Quick Start (Docker)

### 1. Clone and Configure

```bash
git clone https://github.com/PowerHouse-Consulting-Group/daimones-community.git
cd daimones-community
cp .env.example .env
```

Edit `.env` with your configuration:
- `DATABASE_URL`: PostgreSQL connection string
- `DIRECTUS_URL`: CMS endpoint (or use bundled Directus)
- `JWT_SECRET`: Secure random string for authentication
- `LLM_API_URL`: llama.cpp server endpoint (default: http://localhost:8001)

### 2. Start Services

```bash
docker-compose up -d
```

This launches:
- **Frontend**: React app (port 3000)
- **Backend**: Node.js API (port 5000)
- **Database**: PostgreSQL + pgvector (port 5432)
- **CMS**: Directus (port 8055)
- **LLM**: llama.cpp server (port 8001)

### 3. Verify Deployment

```bash
# Check service health
docker-compose ps

# Test API endpoint
curl http://localhost:5000/api/health

# Access web interface
# Open https://your-domain.com (or http://localhost:3000 for local testing)
```

## Manual Deployment (Bare Metal)

### 1. Install Dependencies

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install NVIDIA drivers (if not already installed)
sudo apt install -y nvidia-driver-535

# Install build tools
sudo apt install -y build-essential cmake git

# Install Node.js 20
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs

# Install PostgreSQL with pgvector
sudo apt install -y postgresql-15 postgresql-15-pgvector
```

### 2. Build llama.cpp

```bash
# Clone llama.cpp
git clone https://github.com/ggerganov/llama.cpp.git
cd llama.cpp
git checkout v8940

# Build with CUDA support
mkdir build && cd build
cmake .. -DLLAMA_CUBLAS=ON
make -j$(nproc)

# Verify GPU detection
./bin/llama-server --list-gpus
```

### 3. Download Model

```bash
# Download Qwen3.6-27B-UD-Q5_K_XL quantization
wget -O models/Qwen3.6-27B-UD-Q5_K_XL.gguf \
  "https://huggingface.co/Qwen/Qwen3.6-27B-UD-GGUF/resolve/main/Qwen3.6-27B-UD-Q5_K_XL.gguf"
```

### 4. Start LLM Server

```bash
cd llama.cpp/build
./bin/llama-server \
  -m /path/to/models/Qwen3.6-27B-UD-Q5_K_XL.gguf \
  --port 8001 \
  -c 16384 \
  -ngl 65 \
  -b 512 \
  --ubatch-size 256 \
  --flash-attn on \
  --cache-type-k q4_0 \
  --cache-type-v q4_0 \
  --reasoning off \
  --mlock
```

### 5. Setup Database

```bash
# Create database and user
sudo -u postgres psql
CREATE USER daimones WITH PASSWORD 'your_secure_password';
CREATE DATABASE daimones OWNER daimones;
\c daimones
CREATE EXTENSION IF NOT EXISTS vector;
\q

# Import corpus (requires corpus data package)
psql -U daimones -d daimones -f data/corpus/aristotle_schema.sql
```

### 6. Build and Run Application

```bash
# Clone repository
git clone https://github.com/PowerHouse-Consulting-Group/daimones-community.git
cd daimones-community

# Install dependencies
npm install

# Build frontend and backend
npm run build

# Start production server
NODE_ENV=production npm start
```

### 7. Configure Reverse Proxy (Nginx)

```nginx
server {
    listen 443 ssl http2;
    server_name your-domain.com;

    ssl_certificate /etc/letsencrypt/live/your-domain.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/your-domain.com/privkey.pem;

    location / {
        proxy_pass http://localhost:5000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```

## Air-Gapped Deployment

For environments with no internet access:

### 1. Prepare Offline Package

On a connected machine:
```bash
# Download all dependencies
npm ci --prefer-offline
docker save daimones:latest | gzip > daimones-latest.tar.gz

# Download model
wget -O Qwen3.6-27B-UD-Q5_K_XL.gguf [model-url]

# Package everything
tar -czf daimones-offline-package.tar.gz \
  daimones-latest.tar.gz \
  Qwen3.6-27B-UD-Q5_K_XL.gguf \
  daimones-community/ \
  nvidia-driver-535.run
```

### 2. Transfer and Install

On the air-gapped machine:
```bash
# Extract package
tar -xzf daimones-offline-package.tar.gz

# Install NVIDIA driver
sudo ./nvidia-driver-535.run

# Load Docker image
docker load < daimones-latest.tar.gz

# Follow Docker deployment steps above
```

## Security Hardening

### Firewall Configuration
```bash
# Allow only HTTPS inbound
sudo ufw allow 443/tcp
sudo ufw allow 22/tcp  # SSH (restrict to your IP)
sudo ufw enable

# Block outbound (optional, for air-gapped)
sudo ufw default deny outgoing
sudo ufw allow out 53/udp  # DNS
sudo ufw allow out 80/tcp  # HTTP (for package updates)
sudo ufw allow out 443/tcp # HTTPS (for package updates)
```

### SSL/TLS Configuration
```bash
# Install Certbot
sudo apt install -y certbot python3-certbot-nginx

# Obtain certificate
sudo certbot --nginx -d your-domain.com

# Auto-renewal (cron job)
sudo crontab -e
# Add: 0 0 1 * * certbot renew --quiet
```

### Database Security
```bash
# Edit pg_hba.conf to restrict connections
sudo nano /etc/postgresql/15/main/pg_hba.conf

# Allow only localhost
local   all             all                                     peer
host    all             all             127.0.0.1/32            md5
host    all             all             ::1/128                 md5

# Restart PostgreSQL
sudo systemctl restart postgresql
```

## Monitoring and Logging

### Health Checks
```bash
# Check all services
curl http://localhost:5000/api/health

# Check LLM server
curl http://localhost:8001/health

# Check database
psql -U daimones -d daimones -c "SELECT 1"
```

### Logs
```bash
# Application logs
journalctl -u daimones -f

# LLM server logs
docker logs -f daimones-llm

# Database logs
tail -f /var/log/postgresql/postgresql-15-main.log
```

### Metrics (Optional)
Install Prometheus + Grafana for monitoring:
```bash
docker-compose -f docker-compose.monitoring.yml up -d
```

## Backup and Recovery

### Database Backup
```bash
# Create backup
pg_dump -U daimones daimones | gzip > backup-$(date +%Y%m%d).sql.gz

# Restore
gunzip < backup-20260612.sql.gz | psql -U daimones daimones
```

### Automated Backups (Cron)
```bash
# Add to crontab
0 2 * * * pg_dump -U daimones daimones | gzip > /backup/daimones-$(date +\%Y\%m\%d).sql.gz
```

## Troubleshooting

### LLM Server Won't Start
```bash
# Check GPU availability
nvidia-smi

# Verify CUDA installation
nvcc --version

# Check llama.cpp logs
docker logs daimones-llm
```

### Database Connection Issues
```bash
# Test connection
psql -U daimones -d daimones -h localhost

# Check PostgreSQL status
sudo systemctl status postgresql

# View logs
sudo tail -f /var/log/postgresql/postgresql-15-main.log
```

### High Memory Usage
- Reduce context window: `-c 8192` instead of 16384
- Use smaller quantization: Q4_K_M instead of Q5_K_XL
- Disable mlock: remove `--mlock` flag

## Scaling

### Vertical Scaling
- **GPU**: Upgrade to A100 (80GB) for larger models
- **RAM**: Increase to 128GB+ for larger context windows
- **Storage**: Use NVMe SSD for faster database queries

### Horizontal Scaling
- Deploy multiple instances behind a load balancer
- Use Redis for session management
- Separate LLM inference to dedicated GPU nodes

## Support

For deployment assistance:
- **Documentation**: [Architecture Guide](./architecture.md)
- **Issues**: [GitHub Issues](https://github.com/PowerHouse-Consulting-Group/daimones-community/issues)
- **Email**: architect@daimones.ai

---

*Last Updated: June 2026*
