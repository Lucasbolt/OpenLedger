# Openledger Automation Script

This project is an automation script designed to interact with the Openledger API and WebSocket services. It handles tasks such as generating tokens, fetching user information, claiming rewards, and maintaining WebSocket connections for multiple accounts.

## Features

- **Token Generation**: Automatically generates authentication tokens for accounts.
- **WebSocket Integration**: Establishes and maintains WebSocket connections for real-time communication.
- **Daily Rewards Claiming**: Automatically claims daily rewards for accounts.
- **User Information Fetching**: Retrieves user statistics, such as total points gained.
- **Proxy Support**: Supports HTTP and SOCKS proxies for secure and anonymous connections.
- **Error Handling & Retry Logic**: Implements retry mechanisms for failed API requests and WebSocket reconnections.

## Prerequisites

- Node.js (v16 or higher)
- NPM or Yarn
- A `wallets.txt` file containing wallet addresses (one per line).
- A `proxy.txt` file containing proxy addresses (optional, one per line).

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Lucasbolt/OpenLedger.git
    cd openledger-automation
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Create the required files:
    ```bash
    touch wallets.txt proxy.txt
    ```
    - `wallets.txt`: Add wallet addresses (one per line).
    - `proxy.txt`: Add proxy addresses (optional, one per line).

## Usage

1. Run the script:
    ```bash
    node main.js
    ```

2. The script will:
    - Read wallet and proxy information.
    - Generate tokens for each wallet.
    - Establish WebSocket connections.
    - Fetch user information and claim daily rewards.

## Configuration

- **Headers**: Modify the `headers` object in `main.js` to customize HTTP headers.
- **Intervals**: Adjust the intervals for fetching user info and claim details in the `main.js` file.

## Logging

Logs are generated for all major operations, including:
- Token generation
- WebSocket connection status
- API responses
- Errors and retries

## Error Handling

- The script retries failed API requests up to 3 times with exponential backoff.
- WebSocket connections automatically attempt to reconnect if closed unexpectedly.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Disclaimer

This script is provided as-is and is intended for educational purposes only. Use it responsibly and ensure compliance with Openledger's terms of service.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.
