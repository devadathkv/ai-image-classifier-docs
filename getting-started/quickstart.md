# Quick Start Guide

This guide walks you through running the AI Image Classifier locally using Docker.

---

## Prerequisites

Before starting, ensure the following tools are installed:

- Docker
- Docker Compose
- Git

---

## Clone the Repository

```bash
git clone https://github.com/example/ai-image-classifier-docs.git
cd ai-image-classifier-docs
```

---

## Start the Service

Run the following command:

```bash
docker compose up
```

The API server starts on:

```txt
http://localhost:8080
```

---

## Verify the API

Send a test request using cURL.

```bash
curl -X POST http://localhost:8080/predict \
-H "Authorization: Bearer YOUR_API_KEY" \
-H "Content-Type: application/json" \
-d '{
  "image_url": "https://example.com/dog.jpg"
}'
```

---

## Example Response

```json
{
  "prediction": "dog",
  "confidence": 0.991
}
```

---

## Next Steps

- Read the API reference documentation
- Configure GPU deployment
- Explore batch prediction APIs