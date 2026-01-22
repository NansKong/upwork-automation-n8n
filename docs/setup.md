## Setup Instructions

### Prerequisites
- Docker Desktop
- n8n v2.4.4
- Apify API Key
- Replicate API Token
- Airtable Personal Access Token
- SMTP credentials for email alerts

### Docker Setup
```bash
docker run -it --rm --name n8n \
  -p 5678:5678 \
  -v ${HOME}\.n8n:/home/node/.n8n \
  n8nio/n8n

