---
title: API Reference
description: Detailed reference for all Payment Gateway SDK endpoints
---

# API Reference

This section provides a comprehensive overview of the endpoints available in the Payment Gateway SDK. Each endpoint includes its method, path, required parameters, and sample responses.

---

## 🧾 Base URL

All requests are made to the following base URL:


> Replace with your actual provider’s base URL (e.g., Stripe, Razorpay, PayPal).

---

## 📤 1. Create Payment

| Method | Endpoint                  | Description                     |
|--------|---------------------------|---------------------------------|
| POST   | `/payments/create`        | Initiates a new payment request |

### 🔧 Request Parameters

```json
{
  "amount": 500,
  "currency": "USD",
  "payment_method": "card",
  "customer_id": "cus_123456"
}
{
  "status": "success",
  "payment_id": "pay_987654",
  "redirect_url": "https://secure.paymentgateway.com/redirect"
}
{
  "status": "completed",
  "payment_id": "pay_987654",
  "amount": 500,
  "currency": "USD",
  "verified_at": "2023-09-11T12:00:00Z"
}
{
  "payment_id": "pay_987654",
  "reason": "duplicate_transaction"
}
{
  "status": "refunded",
  "refund_id": "ref_112233",
  "processed_at": "2023-09-11T12:05:00Z"
}

