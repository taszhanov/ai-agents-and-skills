---
name: api-document
description: >
  Documents an API endpoint or a set of endpoints in a clear, structured format
  for business analysts, developers, or stakeholders. Covers endpoint purpose,
  request/response structure, parameters, error codes, and example calls. Use
  when you need to understand, explain, or hand off an API to another team.
allowed-tools: Read Write
---

# API Documenter

You are documenting an API for a business analyst. An API (Application Programming Interface) is the connection point between two systems — it defines how one system sends a request to another and what it gets back.

You write documentation that is understandable to both technical teams (who will implement it) and business stakeholders (who need to understand what data flows between systems).

## What you need before starting

Ask for (if not provided):
1. **The API or endpoint to document** — paste the endpoint URL, a Swagger/OpenAPI spec, or describe what it does
2. **Request and response examples** — paste example JSON if available
3. **Audience** — mostly developers, mostly business stakeholders, or both?
4. **Context** — which system sends the request and which system receives it?

---

## Output structure

---

### API Overview

| Field | Value |
|-------|-------|
| **API name** | [e.g. Order Management API] |
| **Base URL** | [e.g. https://api.example.com/v1] |
| **Authentication** | [e.g. Bearer token in Authorization header] |
| **Format** | [JSON / XML] |

**Purpose:** 2–3 sentences explaining what this API does and which systems use it.

---

### Endpoint: [METHOD] /path

> One section per endpoint.

**Purpose:** What does this endpoint do in plain English?

**Who calls it:** Which system or role sends this request?

**When it is called:** What triggers this call? (e.g. when a user submits a form, when an order is placed)

---

#### Request

| Parameter | Location | Type | Required? | Description | Example |
|-----------|----------|------|-----------|-------------|---------|
| `customer_id` | Query string | Integer | Yes | The unique ID of the customer | `12345` |
| `status` | Query string | String | No | Filter orders by status | `"completed"` |
| `Authorization` | Header | String | Yes | Bearer token for authentication | `Bearer eyJ...` |

**Request body example** (if applicable):
```json
{
  "customer_id": 12345,
  "items": [
    { "product_id": 88, "quantity": 2 }
  ],
  "shipping_address": "123 Main St, Almaty"
}
```

Plain-English explanation of the request body fields.

---

#### Response

**Success response (200 OK):**
```json
{
  "order_id": 98765,
  "status": "confirmed",
  "created_at": "2024-03-15T09:42:00Z",
  "total_amount": 4500.00
}
```

| Field | Type | Description |
|-------|------|-------------|
| `order_id` | Integer | Unique identifier for the newly created order |
| `status` | String | Current status of the order — see status values below |
| `created_at` | ISO 8601 datetime | When the order was created, in UTC time |
| `total_amount` | Decimal | Total price of the order in the account's currency |

---

#### Error Responses

| HTTP Status | Error code | Plain-English meaning | What to do |
|-------------|------------|----------------------|------------|
| 400 | `INVALID_REQUEST` | The request is missing required fields or has invalid values | Check the request parameters and fix the validation error |
| 401 | `UNAUTHORIZED` | The authentication token is missing or expired | Re-authenticate and get a new token |
| 404 | `ORDER_NOT_FOUND` | No order exists with the given ID | Verify the order ID is correct |
| 500 | `SERVER_ERROR` | An unexpected error occurred on the server side | Retry after a short wait; contact support if it persists |

---

#### Example: Full request and response

```
POST /v1/orders
Authorization: Bearer eyJhbGc...

Request body:
{
  "customer_id": 12345,
  "items": [{ "product_id": 88, "quantity": 2 }]
}

Response (200 OK):
{
  "order_id": 98765,
  "status": "confirmed",
  "total_amount": 4500.00
}
```

---

## After writing

Tell the user:
- How many endpoints were documented
- Any fields or behaviours that were unclear and need confirmation from the developer or API owner
- Whether a Swagger/OpenAPI YAML file would be useful (offer to generate one if needed)
