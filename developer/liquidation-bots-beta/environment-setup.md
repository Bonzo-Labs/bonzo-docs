# Environment Setup

## Prerequisites

Before we begin, make sure you have the following:

* **Basic understanding** of Solidity, Hardhat, and JavaScript/TypeScript.
* **Node.js and npm** installed on your machine.
* [**HashPack**](https://hashpack.app) or another wallet configured for the Hedera network.
* **Hedera testnet** account credentials.

### 1. Clone the Repository

First, clone the repository containing the smart contract and script:

{% code overflow="wrap" %}
```bash
git clone https://github.com/Bonzo-Labs/bonzo-finance-contracts.git
cd bonzo-finance-contracts
```
{% endcode %}

### 2. Install Dependencies

Install the required npm packages (you may need to use the **`--legacy-peer-deps`** flag due to older versions of dependencies):

```bash
npm install --legacy-peer-deps
```

### 3. Configure Environment Variables

Create a **`.env`** file in the root directory and add your Hedera account details and other configurations:

```bash
PRIVATE_KEY=your-private-key
ACCOUNT_ID=your-account-id
PROVIDER_URL=https://testnet.hashio.io/api
LENDING_POOL_ADDRESS=0x...
DATA_PROVIDER_ADDRESS=0x...
PRICE_ORACLE_ADDRESS=0x...
LIQUIDATOR_CONTRACT_ADDRESS=0x...
```

* Replace **`your-private-key`** and **`your-account-id`** with your actual Hedera testnet account credentials.
* Replace **`0x...`** with the actual contract addresses. You can find the mainnet contract addresses [here](https://docs.bonzo.finance/hub/developer/contract-deployments).

### 4. Install Hedera SDK (if not already installed)

```bash
npm install @hashgraph/sdk
```
