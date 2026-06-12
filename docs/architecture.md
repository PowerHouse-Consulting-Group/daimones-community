# daïmōnes Architecture

## Overview

daïmōnes is a sovereign AI reasoning engine designed for philosophical inquiry and academic research. The system combines classical corpora (starting with Aristotle's complete works) with modern LLM infrastructure to demonstrate authentic reasoning free from corporate alignment constraints.

## Core Components

### 1. Reasoning Engine
- **Model**: Qwen3.6-27B-UD (Q5_K_XL quantization) via llama.cpp v8940
- **Context Window**: 16,384 tokens
- **Features**: Flash attention enabled, quantized KV cache (q4_0), batch size 512
- **Inference**: Single GPU deployment (NVIDIA L4 or equivalent), ~60 tokens/second

### 2. Retrieval-Augmented Generation (RAG)
- **Database**: PostgreSQL 15+ with pgvector extension
- **Corpus**: Polytonic Ancient Greek source texts (Corpus Aristotelicum)
- **Embeddings**: Sentence-transformers for semantic search
- **Ranking**: Cross-encoder reranker for relevance scoring

### 3. Web Application
- **Frontend**: React 18, TypeScript, Tailwind CSS v4
- **Backend**: Node.js/Express, TypeScript
- **CMS**: Directus for content management (blog, academic pages)
- **Authentication**: JWT-based with email verification

### 4. Data Pipeline
- **Corpus Processing**: Custom parsers for polytonic Greek
- **Chunking**: Semantic boundaries with overlap for context preservation
- **Indexing**: Batch vectorization with metadata tagging
- **Versioning**: Corpus snapshots with rollback capability

## Deployment Model

### Sovereign Deployment
- **Single-node**: All components on one machine (GPU + CPU)
- **Air-gapped**: Zero outbound API calls, full institutional data control
- **Compliance**: FERPA, GDPR ready — no third-party dependencies
- **Scalability**: Vertical scaling (larger GPU) or horizontal (load balancer)

### Infrastructure Requirements
- **GPU**: NVIDIA L4 (24GB VRAM) or equivalent
- **CPU**: 8+ cores, 64GB+ RAM
- **Storage**: 500GB+ SSD for corpus and model weights
- **Network**: Inbound HTTPS only, no outbound required

## Data Flow

```
User Query → Frontend → Backend API → RAG Pipeline
                                          ↓
                                    PostgreSQL + pgvector
                                          ↓
                                    Embedding + Retrieval
                                          ↓
                                    Reranking + Context Assembly
                                          ↓
                                    LLM Inference (llama.cpp)
                                          ↓
                                    Response → User
```

## Security and Privacy

- **Data Locality**: All data stays on-premise or in your cloud
- **No Telemetry**: Zero analytics, no usage tracking
- **Encryption**: TLS 1.3 in transit, AES-256 at rest
- **Access Control**: Role-based (user, academic, admin)
- **Audit Logs**: Optional query/response logging for compliance

## Extensibility

- **Multi-Philosopher**: Plato, Stoics, and others planned (requires separate corpora)
- **Custom Domains**: White-label deployments for institutions
- **API Access**: REST endpoints for programmatic access (coming soon)
- **Plugins**: Modular architecture for custom reasoning strategies

## Performance Characteristics

- **Cold Start**: ~30 seconds (model loading)
- **Warm Inference**: 60-80 tokens/second (single GPU)
- **RAG Latency**: 200-500ms (retrieval + reranking)
- **Total Response Time**: 2-5 seconds for typical philosophical queries
- **Concurrent Users**: 10-20 simultaneous sessions per GPU

## Limitations

- **Single GPU**: Not designed for high-traffic consumer applications
- **No Fine-tuning**: Zero-shot with RAG (fine-tuning roadmap TBD)
- **Language Support**: English + Polytonic Greek (Modern Greek via transliteration)
- **Context Limit**: 16K tokens (longer conversations require summarization)

## Roadmap

- **Q3 2026**: Plato corpus, multi-philosopher dialogue
- **Q4 2026**: Voice mode, mobile apps
- **2027**: Federated learning across institutions, custom model training

## Contact

For architectural questions or deployment support:
- **Technical**: architect@daimones.ai
- **General**: support@daimones.ai

---

*Last Updated: June 2026*
