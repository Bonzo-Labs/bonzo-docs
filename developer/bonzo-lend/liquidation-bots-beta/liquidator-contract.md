# Liquidator Contract

The **`LiquidatorContract.sol`** smart contract facilitates liquidations by interacting with the Bonzo lending pool and performing token swaps via SaucerSwap.

### 1. Review the Contract

You can find the contract code [here](https://github.com/Bonzo-Labs/bonzo-finance-contracts/blob/main/contracts/examples/LiquidationContract.sol).

**Key Functions:**

* **`liquidate()`**: Initiates the flash loan and triggers the liquidation.
* **`executeOperation()`**: Called after receiving the flash-loaned amount; performs the liquidation and token swap.
* **`_associateToken()`**: Associates Hedera tokens with the contract (required on Hedera).

### 2. Compile the Contract

Compile the contract using Hardhat:

```bash
npm run compile
```

### 3. Deploy the Contract

Deploy the contract to the Hedera testnet:

```bash
npx hardhat run scripts/deploy.ts --network hedera_testnet
```

* Ensure your **`hardhat.config.ts`** is set up for the Hedera testnet.
* In **`deploy.ts`**, replace **`LendingPoolAddressesProvider_address`** and **`SaucerswapRouter_address`** with the actual contract addresses.
