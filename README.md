# Cryptomus Payment Gateway for PipraPay

[![PipraPay](https://img.shields.io/badge/Platform-PipraPay-blue.svg)](https://piprapay.com)
[![Cryptomus](https://img.shields.io/badge/Payment-Cryptomus-purple.svg)](https://cryptomus.com)
[![PHP](https://img.shields.io/badge/PHP-%3E%3D%207.4-777bb4.svg)](https://php.net)
[![License](https://img.shields.io/badge/License-AGPL%20v3-orange.svg)](LICENSE)

A professional, high-performance integration for accepting cryptocurrency payments via the **Cryptomus** API on the **PipraPay** platform. This gateway allows merchants to accept 20+ cryptocurrencies with real-time conversion and automated verification.

---

## 🌟 Key Features

*   **20+ Cryptocurrencies Supported**: Accept BTC, ETH, USDT (ERC20/TRC20/BEP20), USDC, TRX, BNB, SOL, and more.
*   **Multi-Network Support**: Seamless integration with Bitcoin, Ethereum, Tron, BSC, Polygon, Solana, and Avalanche networks.
*   **Real-Time Conversion**: Automatic conversion from crypto to your base currency (e.g., USD, BDT) using live market rates.
*   **Professional Checkout UI**: A modern, responsive checkout experience that matches the PipraPay ecosystem.
*   **Automated Webhooks**: Instant payment updates and automated transaction completion via secure callbacks.
*   **Advanced Configuration**: Support for invoice lifetime, client commissions, payment accuracy tolerance, and partial payments.
*   **Secure Signatures**: High-security MD5 + Base64 request signing to prevent tampering.

---

## 📋 Prerequisites

*   **PipraPay Core**: v1.0.0 or higher.
*   **PHP Version**: 7.4 or higher.
*   **Extensions**: `cURL`, `OpenSSL`, and `JSON` extensions must be enabled.
*   **Cryptomus Account**: A verified Merchant account at [Cryptomus.com](https://cryptomus.com).
*   **SSL Certificate**: Required for receiving secure webhook callbacks.

---

## 🚀 Installation Guide

1.  **Extract Files**: Upload the `cryptomus` folder to your PipraPay installation at:
    `pp-content/plugins/payment-gateway/cryptomus/`
2.  **Activate Plugin**: Log in to your PipraPay Admin Panel, navigate to **Plugins**, and click **Activate** on the Cryptomus gateway.
3.  **Basic Setup**: Go to **Gateway Settings** -> **Cryptomus** to begin the configuration.

---

## ⚙️ Configuration Parameters

### 🏦 Gateway Information
*   **Display Name**: The name shown to customers (e.g., "Pay with Crypto / Cryptomus").
*   **Category**: Set to **International** for global reach.
*   **Currency**: Select your default payout currency (typically USD).

### 🔑 API Credentials
You can find these in your [Cryptomus Dashboard](https://app.cryptomus.com/dashboard):
*   **Merchant UUID**: Your unique merchant identifier.
*   **Payment API Key**: Use the **Payment** key (do not use the Payout key).

### 🛠️ Advanced Options
*   **Invoice Lifetime**: Define how long (in seconds) the payment address remains valid.
*   **Allow Partial Payment**: If enabled, customers can pay in multiple transactions if the first one was insufficient.
*   **Payment Accuracy**: Set a percentage tolerance (e.g., 1%) to accept payments even if there's a minor discrepancy due to exchange rate fluctuations.

---

## 🔗 Webhook Configuration

Automated order status updates require a correctly configured Webhook URL in your Cryptomus dashboard.

**Your Webhook URL:**
`https://yourdomain.com/webhook/cryptomus/{payment_id}`

### How to set up:
1.  Log in to [Cryptomus Merchant Dashboard](https://app.cryptomus.com/settings/merchants).
2.  Select your project and go to **Settings**.
3.  Paste the Webhook URL into the **Webhook URL** field.
4.  Ensure the status is set to **Active**.

---

## 🔒 Security & Verification

This gateway implements robust security measures:
*   **Payload Signing**: Every outgoing request is signed using a cryptographic hash combining your API Key and a Base64 encoded payload.
*   **Callback Validation**: Inbound webhooks are strictly verified by regenerating the signature locally and comparing it with the `sign` header from Cryptomus.
*   **Error Logging**: Comprehensive logging for all API interactions to facilitate debugging and auditing.

---

## 📄 Support & Documentation

*   **Official Documentation**: [Cryptomus API Docs](https://doc.cryptomus.com/)
*   **Merchant Help**: [Cryptomus Support](https://t.me/cryptomussupport)
*   **iPayees Support**: [ipayees.com](https://ipayees.com)

---

Developed with ❤️ by **[iPayees Team](https://github.com/asifsofficial)** for the **PipraPay** community.