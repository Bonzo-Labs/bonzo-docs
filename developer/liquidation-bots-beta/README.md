# 💸 Liquidation Bots (Beta)

{% hint style="warning" %}
**Disclaimer:** This tutorial is for educational purposes only. Liquidations involve financial risk. All participants should ensure compliance with applicable laws and regulations in their jurisdiction before performing any liquidation activities.
{% endhint %}

In the Bonzo Protocol, liquidation occurs when a borrower's collateral value falls below a certain threshold due to changes in asset prices or accrued interest. Liquidators can repay a portion of the borrower's debt and receive a liquidation bonus on the collateral they obtain. This process helps maintain the protocol's solvency and incentivizes liquidators.&#x20;

This tutorial will demonstrate how to perform a liquidation on the Bonzo Protocol deployed on the Hedera blockchain using a custom smart contract and a Hardhat script.

#### **Core Concepts:**

* **Collateral Asset**: The asset supplied by the borrower.
* **Debt Asset**: The asset borrowed by the borrower.
* **Health Factor**: A value representing the safety of the borrower's position. A health factor below 1 indicates that the position is undercollateralized and can be liquidated.

#### **Example Code:**

* **Smart Contract**: [LiquidationContract.sol](https://github.com/Bonzo-Labs/bonzo-finance-contracts/blob/main/contracts/examples/LiquidationContract.sol)
* **Sample Scripts**: [liquidationFlashLoan scripts](https://github.com/Bonzo-Labs/bonzo-finance-contracts/tree/main/scripts/liquidationFlashLoan)

## Prerequisites

Before we begin, make sure you have the following:

* **Basic understanding** of Solidity, Hardhat, and JavaScript/TypeScript.
* **Node.js and npm** installed on your machine.
* [**HashPack**](https://hashpack.app) or another wallet configured for the Hedera network.
* **Hedera testnet** account credentials.
