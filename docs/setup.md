## Setup Instructions

### Prerequisites
- Docker & Docker Compose
- n8n v1.x+
- Apify API Key
- Replicate API Token
- Airtable Personal Access Token
- SMTP credentials for email alerts

### Docker Setup
```bash
docker run -it --rm \
  -p 5678:5678 \
  -e N8N_BASIC_AUTH_ACTIVE=true \
  -e N8N_BASIC_AUTH_USER=admin \
  -e N8N_BASIC_AUTH_PASSWORD=admin \
  -e TZ=Asia/Kolkata \
  n8nio/n8n
