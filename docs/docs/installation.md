---
title: Installation
description: Step-by-step guide to install and configure the Payment Gateway SDK
---

# Installation Guide

This guide walks you through setting up the Payment Gateway SDK in your local development environment. By the end, you'll have a fully functional SDK ready for authentication and API integration.

---

## 🧰 Prerequisites

Before installing the SDK, ensure the following tools are installed and properly configured:

| Tool       | Minimum Version | Check Command        |
|------------|------------------|----------------------|
| Node.js    | v16.x or higher  | `node -v`            |
| npm        | v8.x or higher   | `npm -v`             |
| Git        | Latest stable    | `git --version`      |

> ✅ Tip: Use [Node Version Manager (nvm)](https://github.com/coreybutler/nvm-windows) on Windows to manage multiple Node.js versions.

---

## 📁 Step 1: Clone the SDK Repository

Use Git to clone the SDK to your local machine:

```bash
git clone https://github.com/your-org/payment-gateway-sdk.git
cd payment-gateway-sdk

npm install
This command reads the package.json file and installs all dependencies into the node_modules folder.

⚠️ If you see errors like ERR_MODULE_NOT_FOUND, check your Node.js version and delete node_modules + package-lock.json, then retry.

API_KEY=your_api_key_here
API_SECRET=your_api_secret_here
npm run test
rm -rf node_modules package-lock.json
npm install

