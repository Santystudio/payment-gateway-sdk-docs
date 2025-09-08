---
title: Authentication
description: How to authenticate with the Payment Gateway SDK
---

# Authentication Guide

Authentication is the foundation of secure communication between your application and the payment gateway. This guide explains how to configure and use authentication methods supported by the SDK.

---

## 🔑 Supported Authentication Methods

The SDK supports multiple authentication strategies depending on the provider:

| Method         | Description                                      | Use Case                          |
|----------------|--------------------------------------------------|-----------------------------------|
| API Key        | Static key passed in request headers             | Simple server-to-server requests |
| Bearer Token   | Dynamic token used for session-based access      | OAuth flows, user sessions       |
| OAuth 2.0      | Authorization framework for delegated access     | Advanced integrations            |

> ⚠️ Always refer to your payment provider’s documentation to confirm supported methods.

---

## 🔐 Using API Keys

Most providers offer a static API key for server-side authentication.

### Example Header

## http
Authorization: ApiKey your_api_key_here

Setup in .env
API_KEY=your_api_key_here

const headers = {
  Authorization: `ApiKey ${process.env.API_KEY}`
};

Authorization: Bearer your_token_here

const headers = {
  Authorization: `Bearer ${process.env.ACCESS_TOKEN}`
};

### Testing Authentication
npm run auth:test


