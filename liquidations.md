# ⚠️ Liquidations

### Introduction&#x20;

Liquidation is a crucial mechanism in the Bonzo Finance protocol that helps maintain the health and stability of the lending and borrowing ecosystem. When a borrower's health factor drops below 1, indicating that their collateral value no longer sufficiently covers their loan value, their position becomes eligible for liquidation. This can happen when the value of the collateral decreases or the value of the borrowed debt increases relative to each other. During a liquidation, up to 50% of the borrower's debt is repaid, and the corresponding collateral value plus a liquidation fee is taken from the available collateral.

### Understanding the Liquidation Penalty&#x20;

The liquidation penalty, also known as the liquidation bonus for liquidators, varies depending on the asset used as collateral. You can find the specific liquidation fee for each asset in the risk parameters section of the Bonzo Finance documentation. This fee serves as an incentive for liquidators to participate in the liquidation process and help maintain the stability of the platform.

Liquidation Examples To better understand how liquidations work in Bonzo Finance, let's consider a couple of examples:

**Example 1**

* Alice deposits 1000 HBAR as collateral and borrows 500 HBAR worth of USDC.&#x20;
* If Alice's health factor falls below 1, her loan becomes eligible for liquidation.&#x20;
* A liquidator can repay up to 50% of her borrowed amount, which is 250 HBAR worth of USDC.&#x20;
* In return, the liquidator can claim the corresponding amount of HBAR collateral plus the liquidation bonus (e.g., 5%). In this case, the liquidator would claim 262.5 HBAR for repaying 250 HBAR worth of USDC.

**Example 2**

* Bob deposits 500 HBAR and 1000 SAUCE tokens as collateral and borrows 800 HBAR worth of USDC.&#x20;
* If Bob's health factor drops below 1, his loan becomes eligible for liquidation.&#x20;
* A liquidator can repay up to 50% of the borrowed amount, which is 400 HBAR worth of USDC. The liquidator can choose which collateral to claim based on the liquidation bonus.&#x20;
* If the liquidation bonus for SAUCE tokens (e.g., 10%) is higher than HBAR (e.g., 5%), the liquidator would opt to claim SAUCE tokens. In this case, the liquidator would claim 440 HBAR worth of SAUCE tokens for repaying 400 HBAR worth of USDC.

### Avoiding Liquidation&#x20;

To avoid liquidation, borrowers can take proactive steps to maintain a healthy collateral-to-debt ratio. This can be achieved by depositing additional collateral assets or repaying a portion of the outstanding loan. By default, loan repayments have a more significant impact on improving the health factor compared to depositing more collateral.

Borrowers should closely monitor their health factor and aim to keep it well above 1 to provide a safety buffer against market fluctuations. Tools like HAL can help users track their health factor and receive notifications when it falls below a certain threshold. Additionally, services like Defi Saver offer auto-liquidation features to help borrowers manage their positions more effectively.

It's important to be mindful of stablecoin price fluctuations due to market conditions, as they can impact the health factor. For example, if the market price of USDC deviates from its intended $1.00 peg, it can affect the collateral-to-debt ratio. More details on price oracles and their role in the liquidation process can be found in the [price discovery](https://docs.bonzo.finance) section of the Bonzo Finance documentation.

### Participating in the Liquidation Ecosystem&#x20;

Liquidations in Bonzo Finance are open to anyone, providing an opportunity for users to earn liquidation bonuses by repaying borrowers' debts and claiming their collateral. However, the liquidation process is highly competitive, with many liquidators developing custom solutions and bots to be the first to liquidate eligible loans.

If you're interested in participating in the liquidation ecosystem, you can find more information in the developers' [liquidation section of the Bonzo Finance documentation](https://docs.bonzo.finance/liquidations). This section provides technical details and guidance on how to integrate liquidation functionality into your own applications or bots.
