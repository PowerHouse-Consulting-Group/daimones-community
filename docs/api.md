# API Reference

## Overview

The daïmōnes API provides RESTful endpoints for interacting with the philosophical reasoning engine. All endpoints return JSON responses and require authentication where noted.

**Base URL**: `https://your-domain.com/api` (or `http://localhost:5000/api` for local development)

## Authentication

Most endpoints require a valid JWT token in the `Authorization` header:

```
Authorization: Bearer <your_jwt_token>
```

Obtain a token via the `/api/auth/login` endpoint.

## Endpoints

### Authentication

#### POST `/auth/register`

Register a new user account.

**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "secure_password",
  "name": "User Name"
}
```

**Response (201):**
```json
{
  "message": "Registration successful. Please check your email to verify your account.",
  "userId": "uuid-string"
}
```

**Response (400):**
```json
{
  "error": "Email already registered"
}
```

---

#### POST `/auth/login`

Authenticate and receive a JWT token.

**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "secure_password"
}
```

**Response (200):**
```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "user": {
    "id": "uuid-string",
    "email": "user@example.com",
    "name": "User Name",
    "role": "user"
  }
}
```

**Response (401):**
```json
{
  "error": "Invalid credentials"
}
```

---

#### POST `/auth/logout`

Invalidate the current session (requires authentication).

**Headers:**
```
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "message": "Logged out successfully"
}
```

---

#### POST `/auth/verify-email`

Verify email address with token sent via email.

**Request Body:**
```json
{
  "token": "verification_token_from_email"
}
```

**Response (200):**
```json
{
  "message": "Email verified successfully"
}
```

---

#### POST `/auth/forgot-password`

Request password reset email.

**Request Body:**
```json
{
  "email": "user@example.com"
}
```

**Response (200):**
```json
{
  "message": "Password reset email sent"
}
```

---

#### POST `/auth/reset-password`

Reset password with token.

**Request Body:**
```json
{
  "token": "reset_token_from_email",
  "newPassword": "new_secure_password"
}
```

**Response (200):**
```json
{
  "message": "Password reset successfully"
}
```

---

### Chat

#### POST `/chat`

Send a message to Aristotle and receive a response.

**Headers:**
```
Authorization: Bearer <token>
Content-Type: application/json
```

**Request Body:**
```json
{
  "message": "What is the nature of virtue?",
  "conversationId": "optional-uuid-for-continuing-conversation",
  "options": {
    "maxTokens": 1024,
    "temperature": 0.7
  }
}
```

**Response (200):**
```json
{
  "response": "Virtue, or ἀρετή (aretē), is excellence of character...",
  "conversationId": "uuid-string",
  "messageId": "uuid-string",
  "tokensUsed": 256,
  "citations": [
    {
      "source": "Nicomachean Ethics",
      "book": "II",
      "chapter": "6",
      "section": "1106a-1107a",
      "text": "Virtue is a state of character concerned with choice..."
    }
  ]
}
```

**Response (401):**
```json
{
  "error": "Authentication required"
}
```

**Response (429):**
```json
{
  "error": "Rate limit exceeded. Free tier: 3 messages per day.",
  "resetAt": "2026-06-13T00:00:00Z"
}
```

---

#### GET `/chat/history`

Retrieve conversation history.

**Headers:**
```
Authorization: Bearer <token>
```

**Query Parameters:**
- `limit` (optional): Number of conversations to return (default: 10, max: 100)
- `offset` (optional): Pagination offset (default: 0)

**Response (200):**
```json
{
  "conversations": [
    {
      "id": "uuid-string",
      "title": "Discussion on Virtue",
      "createdAt": "2026-06-12T10:30:00Z",
      "messageCount": 12,
      "lastMessage": "2026-06-12T11:45:00Z"
    }
  ],
  "total": 25,
  "limit": 10,
  "offset": 0
}
```

---

#### GET `/chat/conversation/:id`

Retrieve a specific conversation with all messages.

**Headers:**
```
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "conversation": {
    "id": "uuid-string",
    "title": "Discussion on Virtue",
    "messages": [
      {
        "id": "uuid-string",
        "role": "user",
        "content": "What is virtue?",
        "timestamp": "2026-06-12T10:30:00Z"
      },
      {
        "id": "uuid-string",
        "role": "assistant",
        "content": "Virtue, or ἀρετή...",
        "timestamp": "2026-06-12T10:30:05Z",
        "citations": [...]
      }
    ]
  }
}
```

---

#### DELETE `/chat/conversation/:id`

Delete a conversation.

**Headers:**
```
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "message": "Conversation deleted"
}
```

---

### User Profile

#### GET `/user/profile`

Get current user profile.

**Headers:**
```
Authorization: Bearer <token>
```

**Response (200):**
```json
{
  "user": {
    "id": "uuid-string",
    "email": "user@example.com",
    "name": "User Name",
    "role": "user",
    "createdAt": "2026-06-01T00:00:00Z",
    "subscription": {
      "status": "active",
      "plan": "disciple",
      "currentPeriodEnd": "2026-07-12T00:00:00Z"
    }
  }
}
```

---

#### PUT `/user/profile`

Update user profile.

**Headers:**
```
Authorization: Bearer <token>
```

**Request Body:**
```json
{
  "name": "New Name"
}
```

**Response (200):**
```json
{
  "message": "Profile updated",
  "user": {
    "id": "uuid-string",
    "name": "New Name"
  }
}
```

---

### Feedback

#### POST `/feedback`

Submit feedback on a response.

**Headers:**
```
Authorization: Bearer <token>
```

**Request Body:**
```json
{
  "messageId": "uuid-string-of-assistant-message",
  "rating": "up",
  "comment": "Optional feedback comment",
  "issueType": "philosophical_accuracy"
}
```

**Response (201):**
```json
{
  "message": "Feedback submitted",
  "feedbackId": "uuid-string"
}
```

---

### Health Check

#### GET `/health`

Check API and service health (no authentication required).

**Response (200):**
```json
{
  "status": "healthy",
  "version": "1.2.3",
  "services": {
    "database": "connected",
    "llm": "ready",
    "cms": "accessible"
  },
  "uptime": 86400
}
```

---

### Blog

#### GET `/blog`

List blog posts.

**Query Parameters:**
- `lang` (optional): Language filter (`en` or `el`, default: `en`)
- `limit` (optional): Number of posts (default: 10, max: 50)
- `offset` (optional): Pagination offset (default: 0)

**Response (200):**
```json
{
  "posts": [
    {
      "id": "uuid-string",
      "slug": "alignment-theater-corporate-ai-perform-thinking",
      "title": "Alignment Theater: How Corporate AI Learned to Perform Thinking",
      "excerpt": "Corporate AI has mastered the art of appearing thoughtful while avoiding genuine philosophical inquiry...",
      "author": "Vasilis Stergiou",
      "publishedAt": "2026-05-15T00:00:00Z",
      "tags": ["alignment", "ai-ethics", "philosophy"],
      "readTime": 8
    }
  ],
  "total": 11,
  "limit": 10,
  "offset": 0
}
```

---

#### GET `/blog/:slug`

Get a specific blog post.

**Response (200):**
```json
{
  "post": {
    "id": "uuid-string",
    "slug": "alignment-theater-corporate-ai-perform-thinking",
    "title": "Alignment Theater",
    "content": "Full markdown content...",
    "author": "Vasilis Stergiou",
    "publishedAt": "2026-05-15T00:00:00Z",
    "tags": ["alignment", "ai-ethics"],
    "readTime": 8
  }
}
```

---

## Rate Limits

### Free Tier (Observer)
- **Chat**: 3 messages per day
- **History**: Last 5 conversations
- **Blog**: Unlimited access

### Disciple ($29.99/month)
- **Chat**: Unlimited messages
- **History**: Full conversation history
- **Blog**: Unlimited access
- **Rate Limit**: 60 tokens/second per user

### Archon ($99.99/month)
- **Chat**: Unlimited messages
- **History**: Full conversation history
- **Blog**: Unlimited access
- **Priority Queue**: Faster response times
- **Rate Limit**: 120 tokens/second per user

## Error Codes

| Code | Meaning |
|------|---------|
| 400 | Bad Request — Invalid parameters or malformed JSON |
| 401 | Unauthorized — Invalid or missing authentication token |
| 403 | Forbidden — Insufficient permissions for this action |
| 404 | Not Found — Resource does not exist |
| 429 | Too Many Requests — Rate limit exceeded |
| 500 | Internal Server Error — Server-side failure |
| 503 | Service Unavailable — LLM or database temporarily down |

## WebSockets (Future)

Real-time streaming responses are planned for Q4 2026. The API will support WebSocket connections at `/ws/chat` for live token streaming.

## SDK Examples

### Python

```python
import requests

# Login
response = requests.post('https://daimones.ai/api/auth/login', json={
    'email': 'user@example.com',
    'password': 'your_password'
})
token = response.json()['token']

# Chat
headers = {'Authorization': f'Bearer {token}'}
response = requests.post('https://daimones.ai/api/chat', 
    headers=headers,
    json={'message': 'What is the nature of virtue?'}
)
print(response.json()['response'])
```

### JavaScript/Node.js

```javascript
const axios = require('axios');

// Login
const { data: { token } } = await axios.post('https://daimones.ai/api/auth/login', {
  email: 'user@example.com',
  password: 'your_password'
});

// Chat
const response = await axios.post('https://daimones.ai/api/chat',
  { message: 'What is the nature of virtue?' },
  { headers: { Authorization: `Bearer ${token}` } }
);
console.log(response.data.response);
```

### cURL

```bash
# Login
TOKEN=$(curl -X POST https://daimones.ai/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{"email":"user@example.com","password":"your_password"}' \
  | jq -r '.token')

# Chat
curl -X POST https://daimones.ai/api/chat \
  -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"message":"What is the nature of virtue?"}'
```

## Support

For API questions or issues:
- **Issues**: [GitHub Issues](https://github.com/PowerHouse-Consulting-Group/daimones-community/issues)
- **Email**: support@daimones.ai

---

*Last Updated: June 2026*
