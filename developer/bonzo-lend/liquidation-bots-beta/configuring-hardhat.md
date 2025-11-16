# Configuring Hardhat

The Hardhat script **`liquidate.ts`** automates the liquidation process by interacting with the deployed Liquidator contract.

### 1. Review the Script

You can find the script code [here](https://github.com/Bonzo-Labs/bonzo-finance-contracts/blob/main/scripts/liquidationFlashLoan/liquidate.ts).

#### **Key Components:**

* **Chain Data Configuration**: Contains network-specific data such as operator keys, contract addresses, and token paths.
* **Contract Setup Functions**: Functions to initialize contract instances using ABIs and addresses.
* **Liquidation Functions**: Functions that perform the liquidation using different methods (direct contract interaction, script-based).

### 2. Update Chain Data

Ensure that the **`chainData`** object in the script contains the correct addresses and keys for your environment:

```typescript
const chainData = {
  operatorId: process.env.ACCOUNT_ID,
  operatorKey: process.env.PRIVATE_KEY,
  providerUrl: process.env.PROVIDER_URL,
  liquidatorContractAddress: process.env.LIQUIDATOR_CONTRACT_ADDRESS,
  lendingPoolAddress: process.env.LENDING_POOL_ADDRESS,
  dataProviderAddress: process.env.DATA_PROVIDER_ADDRESS,
  priceOracleAddress: process.env.PRICE_ORACLE_ADDRESS,
  // Add any other required addresses and keys
};
```

### 3. Set Up Environment Variables

Ensure your **`.env`** file contains all necessary variables, as shown in the [Prerequisites](environment-setup.md) section.
