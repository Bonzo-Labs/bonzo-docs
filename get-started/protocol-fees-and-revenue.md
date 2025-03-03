# 💸 Protocol Fees & Revenue

As a decentralized lending and borrowing protocol, Bonzo Finance is committed to creating a robust and economically sustainable ecosystem that benefits all stakeholders. The protocol’s fee structure is designed to ensure the long-term viability of the protocol while providing attractive opportunities for target user personas.

## Protocol Fees

At the core of Bonzo Finance's fee model are four distinct fee types that work together to ensure platform sustainability, incentivize optimal behavior, and protect all participants. These carefully calibrated fees maintain the protocol's financial health, compensate liquidity providers fairly, and create the right market dynamics for long-term growth while distributing value across the ecosystem.

### **Borrowing Rate**

The Borrowing Rate is a dynamic (variable) and annualized interest rate (APY) that borrowers pay when taking loans from the protocol. Unlike fees that primarily benefit the protocol, borrowing rates primarily flow to suppliers (lenders) who provide the liquidity being borrowed, with only a portion (the [Reserve Factor](protocol-fees-and-revenue.md#reserve-factor)) going to the protocol itself. The most up-to-date interest rate models per asset are found in the [Risk Framework](https://docs.bonzo.finance/bonzo-risk-framework/liquidity-risk/actual-rates-and-parameters) documentation.

* **Purpose**: To compensate suppliers for providing liquidity and to regulate market demand for borrowing based on supply and utilization
* **Mechanism**: Dynamic rates that increase as utilization increases, incentivizing repayments during high utilization and encouraging borrowing during low utilization
* **Calculation**: Uses a two-slope model based on utilization:
  * When utilization < optimal: Rate = Base + (Utilization/Optimal) × Slope1
  * When utilization ≥ optimal: Rate = Base + Slope1 + ((Utilization-Optimal)/(1-Optimal)) × Slope2
* **Beneficiaries**: Primarily suppliers (lenders) of the asset, with a portion (Reserve Factor) going to the protocol treasury

### **Reserve Factor**

The Reserve Factor Fee is a percentage of interest paid by borrowers that is allocated to the protocol's reserves and set on a per-asset basis. These reserves act as a safety buffer for the platform, creating a financial cushion that protects lenders from potential losses during market volatility or unexpected events. The most up-to-date Reserve Factor fee(s) per asset are found in the [Risk Framework](https://docs.bonzo.finance/bonzo-risk-framework/asset-risk/risk-parameters-per-asset) documentation.

* **Purpose**: To build a protocol safety reserve that serves as the first line of defense against shortfall events
* **Mechanism**: A fixed percentage of all interest payments made by borrowers is automatically directed to the protocol treasury
* **Beneficiary**: The protocol treasury, which can be used by the Bonzo Finance DAO for various purposes, including but not limited to providing rewards to Safety Module participants

### **Liquidation Bonus**

The Liquidation Bonus (sometimes referred to as Liquidation Fee from the borrower's perspective) is applied when a borrower's collateral is liquidated due to their position falling below the required collateralization ratio. This fee is a percentage of the liquidated collateral and is paid to the liquidator as an incentive for maintaining the health of the platform. The most up-to-date Liquidation Bonus fee(s) per asset are found in the [Risk Framework](https://docs.bonzo.finance/bonzo-risk-framework/asset-risk/risk-parameters-per-asset) documentation.&#x20;

* **Purpose**: To incentivize third-party liquidators to repay at-risk loans and maintain the solvency of the protocol.
* **Mechanism**: When a position becomes undercollateralized, liquidators can repay a portion of the debt and receive the equivalent value plus a bonus in collateral assets.

### **Flash Loans**

Flash Loans are uncollateralized loans that must be borrowed and repaid within a single blockchain transaction. The Flash Loan Fee is a fixed percentage charged on the borrowed amount for using this service.

* **Purpose**: To generate revenue from users leveraging Flash Loans for arbitrage, liquidations, and other financial operations.
* **Mechanism**: A fixed percentage (0.09%) of the total borrowed amount is charged when a Flash Loan is executed.
* **Current Value**: 0.09% of the Flash Loan volume.
* **Beneficiary**: The majority of the fee (excluding the asset's Reserve Factor) is distributed to liquidity providers of the respective asset.
