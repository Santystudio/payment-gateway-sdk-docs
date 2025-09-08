---
Title: Error Handling
Description: How the Payment Gateway SDK manages and reports errors
---

## Error Handling Guide

Robust error handling is essential for building reliable payment systems. This guide explains how the SDK detects, reports, and helps resolve common issues during integration and runtime.

---

## 🧠 Error Categories

The SDK classifies errors into the following types:

| Type             | Description                                      | HTTP Status |
|------------------|--------------------------------------------------|-------------|
| Validation Error | Missing or invalid input parameters              | `400 Bad Request` |
| Authentication   | Invalid API key or token                         | `401 Unauthorized` |
| Authorization    | Insufficient permissions                         | `403 Forbidden` |
| Not Found        | Resource does not exist                          | `404 Not Found` |
| Server Error     | Unexpected failure on the provider’s side        | `500 Internal Server Error` |

---

## 🧪 Sample Error Response

```json
{
  "status": "error",
  "code": "AUTH_FAILED",
  "message": "Invalid API key provided",
  "timestamp": "2025-09-08T12:30:00Z"
}
try {
  const response = await sdk.createPayment(data);
} catch (error) {
  console.error("Payment failed:", error.message);
}
