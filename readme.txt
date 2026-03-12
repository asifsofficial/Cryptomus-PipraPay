=== Cryptomus Payment Gateway ===
Plugin Name: Cryptomus
Description: Accept cryptocurrency payments through Cryptomus
Version: 1.0.0
Author: iPayees
Author URI: https://ipayees.com/
License: Proprietary
Requires PHP: 7.4

== Description ==

Cryptomus payment gateway integration for accepting cryptocurrency payments. Accept Bitcoin, USDT, Ethereum, and 20+ other cryptocurrencies with automatic conversion to your preferred currency.

Features:
* Support for 20+ cryptocurrencies (BTC, ETH, USDT, USDC, BNB, TRX, etc.)
* Multiple blockchain networks (Bitcoin, Ethereum, Tron, BSC, Polygon, Solana, etc.)
* Automatic currency conversion
* Real-time payment status updates
* Secure webhook verification
* Configurable invoice lifetime
* Partial payment support
* Payment accuracy tolerance
* Client commission configuration

== Installation ==

1. Upload the plugin files to /content/plugins/payment-gateway/cryptomus/
2. Activate the plugin through the admin panel
3. Get your Merchant UUID and Payment API Key from Cryptomus dashboard
4. Configure the gateway settings with your credentials
5. Set your preferred invoice lifetime and payment options
6. Enable the gateway and start accepting crypto payments!

== Configuration ==

Required Settings:
- Merchant UUID: Your unique merchant identifier from Cryptomus
- Payment API Key: Your payment API key (different from payout API key)

Optional Settings:
- Invoice Lifetime: Time before invoice expires (30 minutes to 12 hours)
- Client Commission: Percentage of commission charged to client (0-100%)
- Allow Partial Payment: Let customers pay remaining amount if partial payment made
- Payment Accuracy: Acceptable payment inaccuracy (0-5%)
- Min/Max Amount: Set transaction limits
- Fixed/Percent Charge: Additional fees to charge

== Webhook Configuration ==

Webhook URL: https://yourdomain.com/webhook/cryptomus/{payment_id}

Configure this URL in your Cryptomus merchant dashboard to receive payment notifications.

== Supported Cryptocurrencies ==

Bitcoin (BTC), Ethereum (ETH), Tether (USDT), USD Coin (USDC), Binance Coin (BNB), 
TRON (TRX), Litecoin (LTC), Bitcoin Cash (BCH), Dogecoin (DOGE), Shiba Inu (SHIB),
Solana (SOL), Avalanche (AVAX), Polygon (MATIC/POL), Dash (DASH), Monero (XMR),
TON, and many more...

== Supported Networks ==

Bitcoin (BTC), Ethereum (ETH), Tron (TRON), Binance Smart Chain (BSC), 
Polygon, Arbitrum, Avalanche, Solana (SOL), TON, and more...

== Payment Statuses ==

- check: Payment is being checked
- process: Payment is being processed
- paid: Payment completed successfully
- paid_over: Customer paid more than required amount
- wrong_amount: Customer paid incorrect amount
- cancel: Payment was cancelled
- fail: Payment failed

== Support ==

- Cryptomus Dashboard: https://app.cryptomus.com/
- API Documentation: https://doc.cryptomus.com/
- Telegram Support: https://t.me/cryptomussupport
- iPayees Support: https://ipayees.com/

== Changelog ==

= 1.0.0 =
* Initial release
* Support for invoice payments
* Webhook integration
* Multiple cryptocurrency support
* Configurable payment options
* Real-time payment verification

== Requirements ==

* PHP 7.4 or higher
* cURL extension enabled
* SSL/HTTPS enabled for webhook callbacks
* Valid Cryptomus merchant account

== Security ==

* All API requests are signed with MD5 + Base64 encryption
* Webhook signatures are verified before processing
* SSL/TLS encryption for all communications
* Secure credential storage

== Notes ==

* Different API keys are used for payments and payouts - use Payment API Key
* Test your integration thoroughly in a test environment first
* Set appropriate min/max amounts based on cryptocurrency minimums
* Configure webhook URL in Cryptomus dashboard for automatic payment updates
* Monitor payment statuses and handle edge cases (wrong_amount, paid_over)

For more information, visit: https://cryptomus.com/

