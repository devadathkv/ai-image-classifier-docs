# Installation Guide

This guide explains how to install and configure the AI Image Classifier environment.

---

## Requirements

| Component | Version |
|---|---|
| Python | 3.10+ |
| Docker | 24+ |
| Git | Latest version |
| RAM | Minimum 8 GB |

---

## Install Docker

Download Docker Desktop from the official Docker website.

To Verify installation:

```bash
docker --version
```

---

## Install Python

To Verify Python installation:

```bash
python --version
```

---

## Clone the Repository

```bash
git clone https://github.com/example/ai-image-classifier-docs.git
cd ai-image-classifier-docs
```

---

## Configure Environment Variables

Create a `.env` file:

```env
API_KEY=your_api_key
MODEL_VERSION=v1
```

---

## Start the Application

```bash
docker compose up
```

---

## Verify Installation

Open the following URL in a browser:

```txt
http://localhost:8080/health
```

Expected response:

```json
{
  "status": "healthy"
}
```