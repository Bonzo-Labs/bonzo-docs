# 🛸 SaucerSwap DEX

## How the Liquidation Bot Utilizes SaucerSwap on Hedera

The liquidation process involves not only repaying the borrower's debt but also converting assets to ensure that the liquidator ends up with a net profit. On the Hedera network, SaucerSwap plays a crucial role in facilitating these token swaps efficiently.

### What is SaucerSwap?

[SaucerSwap](https://www.saucerswap.finance/) is a decentralized exchange (DEX) built on the Hedera network. It allows users to swap between different Hedera Token Service (HTS) assets seamlessly and provides liquidity pools for various token pairs.

### Role of SaucerSwap in Liquidation

When performing a liquidation on the Bonzo Protocol:

1. **Flash Loan**: The liquidator contract takes out a flash loan of the debt asset from the Bonzo lending pool.
2. **Debt Repayment**: The borrowed amount is used to repay the borrower's debt, thereby initiating the liquidation process.
3. **Collateral Acquisition**: In return for repaying the debt, the liquidator receives a portion of the borrower's collateral, including a liquidation bonus.
4. **Token Swap via SaucerSwap**: The collateral asset received may not be the desired asset for the liquidator. Using SaucerSwap, the liquidator swaps the collateral asset back to the original debt asset or another preferred asset.
5. **Repaying the Flash Loan**: The liquidator uses the swapped assets to repay the flash loan plus any fees, keeping any remaining assets as profit.

### Integration with the Liquidator Contract

The **`LiquidatorContract.sol`** is designed to interact seamlessly with SaucerSwap:

* **Associating Tokens**: On Hedera, tokens need to be associated with an account or contract before they can be transferred. The liquidator contract includes functions to associate necessary tokens to facilitate swaps.
* **Swapping Assets**: The **`executeOperation()`** function in the contract uses SaucerSwap's router to swap the collateral assets received during liquidation back into the debt asset or another specified token.
* **Optimizing Profits**: By leveraging SaucerSwap's liquidity pools, the liquidator can optimize the swap rates, ensuring maximum profitability from the liquidation process.

### Benefits of Using SaucerSwap

* **Liquidity**: Access to deep liquidity pools for various token pairs on the Hedera network.
* **Efficiency**: Fast and cost-effective swaps due to Hedera's high throughput and low fees.
* **Smart Contract Integration**: Easy integration with smart contracts, enabling automated and trustless execution of swaps during the liquidation process.
