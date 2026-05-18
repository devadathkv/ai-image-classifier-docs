# Predict Endpoint

The `/predict` endpoint performs image classification using the deployed AI model.

---

## Endpoint URL

```http
POST /predict
```

---

## Authentication

Requests require a valid API key.

```http
Authorization: Bearer YOUR_API_KEY
```

---

## Request Headers

| Header | Required | Description |
|---|---|---|
| Authorization | Yes | API authentication token |
| Content-Type | Yes | Must be `application/json` |

---

## Request Body

```json
{
  "image_url": "https://example.com/image.jpg"
}
```

---

## Request Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| image_url | string | Yes | Public URL of the image |

---

## Example Request

```bash
curl -X POST http://localhost:8080/predict \
-H "Authorization: Bearer YOUR_API_KEY" \
-H "Content-Type: application/json" \
-d '{
  "image_url": "https://example.com/cat.jpg"
}'
```

---

## Successful Response

```json
{
  "prediction": "cat",
  "confidence": 0.982
}
```

---

## Error Responses

### Unauthorized

```json
{
  "error": "Invalid API key"
}
```

### Invalid Request

```json
{
  "error": "Missing image_url parameter"
}
```

---

## Status Codes

| Code | Description |
|---|---|
| 200 | Successful prediction |
| 400 | Invalid request |
| 401 | Unauthorized |
| 500 | Internal server error |