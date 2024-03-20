# FundMe dApp

The FundMe dApp is a decentralized application developed in Solidity, designed for Ethereum-based networks. This application allows users to send ETH to the contract as a form of funding, with the minimum amount set in USD to ensure fairness regardless of cryptocurrency volatility. The dApp uses Chainlink Price Feeds for accurate conversion rates between ETH and USD.

## Features

- **Funding:** Users can fund the contract with ETH above a specified minimum threshold in USD.
- **Withdrawal:** Only the contract owner can withdraw the total balance collected.
- **Address Tracking:** Tracks and stores the amount funded by each address.
- **Owner Verification:** Restricts certain functionalities (like withdrawing funds) to the contract owner.
- **Chainlink Price Feeds:** Utilizes Chainlink's decentralized oracle network for real-time ETH to USD conversion rates.

## Requirements

- Node.js
- NPM/Yarn
- Ethereum Wallet (e.g., MetaMask)
- Foundry or Hardhat (for testing and deployment)

## Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/z0Ldev/foundry-fund-me-f23.git
cd foundry-fund-me-f23
npm install
```

or if you are using Yarn:

```bash
yarn install
```

## Setup

### Using Foundry

Initialize Foundry if you haven't already:

```bash
forge init
```

Compile the smart contracts:

```bash
forge build
```

### Using Hardhat

Initialize Hardhat in your project directory if you haven't already:

```bash
npx hardhat
```

Compile the smart contracts:

```bash
npx hardhat compile
```

## Deployment

Deploy the contract using Foundry or Hardhat. Remember to set the constructor parameter `address priceFeed` to the appropriate Chainlink Price Feed address for your network.

Example using Hardhat:

```bash
npx hardhat run scripts/deploy.js --network <network-name>
```

Replace `<network-name>` with the name of the Ethereum network you wish to deploy to (e.g., sepolia, rinkeby, mainnet).

## Interacting with the Contract

After deploying the contract, you can interact with it through Foundry scripts, Hardhat tasks, or directly through a web interface using ethers.js or web3.js. Ensure you're connected to the correct Ethereum network in your wallet.

## Testing

Test the contract using Foundry or Hardhat:

- Using Foundry:

```bash
forge test
```

- Using Hardhat:

```bash
npx hardhat test
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any bugs, features, or improvements.

## License

This project is licensed under the MIT License.
