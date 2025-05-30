# Risk Parameters

Bonzo Finance utilizes several key risk parameters configured per asset to manage the protocol's risk exposure and ensure its stability. These parameters are carefully calibrated by Ledger Works, and are based on various risk factors to provide optimal security for lenders while maintaining flexibility for borrowers.

### **Loan-to-Value (LTV)** <a href="#loan-to-value" id="loan-to-value"></a>

The Loan-to-Value (LTV) ratio defines the maximum amount of currency that can be borrowed with a specific collateral. It’s expressed in percentage: at LTV=75%, for every 1 HBAR worth of collateral, borrowers will be able to borrow 0.75 HBAR worth of the corresponding currency.&#x20;

* **Risk Consideration**: A lower LTV indicates a more conservative lending approach, reducing the risk of under-collateralization during market volatility.\

* **Calculation:** For each connected account the maximum LTV is calculated as the weighted average of the LTVs of the collateral assets supplied and their value:

$$
\text{MaxLTV} = \frac{\sum \text{Collateral}_i \text{ in HBAR} \times \text{LTV}_i}{\text{Total Collateral in HBAR}}
$$

### **Liquidation Threshold** <a href="#loan-to-value" id="loan-to-value"></a>

The Liquidation Threshold is the point at which a loan becomes undercollateralized and eligible for liquidation. It's always set higher than the LTV to provide a buffer against market fluctuations. For more volatile assets, this buffer is typically set higher for additional protection.

* **Risk Consideration**: The gap between LTV and Liquidation Threshold acts as a safety cushion, allowing borrowers time to react to market changes before risking liquidation.
* **Calculation:** For each account the Liquidation Threshold is calculated as the weighted average of the Liquidation Thresholds of the collateral assets supplied and their value:

$$
\text{Liquidation Threshold} = \frac{\sum \text{Collateral}_i \text{ in HBAR} \times \text{Liquidation Threshold}_i}{\text{Total Collateral in HBAR}}
$$

### **Liquidation Bonus** <a href="#loan-to-value" id="loan-to-value"></a>

The Liquidation Bonus is an incentive offered to liquidators for repaying undercollateralized loans — it is viewed as a "penalty" from the perspective of the collateral supplier, as it's considered a loss on the collateral supplied. This bonus is expressed as a percentage of the collateral's value that liquidators "purchase" at a discount, as part of the liquidation process.

* **Risk Consideration**: A higher bonus incentivizes quicker liquidations, helping to maintain the protocol's solvency during market downturns. If the bonus is high per individual asset, it disincentivizes supplying the asset as collateral, as it could result in loss for the borrower.
* **Calculation**: Market Price of Asset \* (1 - Liquidation Bonus) = Discounted Price

### **Health Factor** <a href="#loan-to-value" id="loan-to-value"></a>

For each wallet, these risks parameters enable the calculation of the health factor:

$$
H_f = \frac{\sum \text{Collateral}_i \text{ in HBAR} \times \text{Liquidation Threshold}_i}{\text{Total Borrows in HBAR}}
$$

When the following formula below is true, the position may be liquidated to maintain solvency as described in the diagram below.

$$
H_f < 1
$$

<figure><img src="../.gitbook/assets/Screenshot 2024-08-07 at 4.44.16 PM.png" alt=""><figcaption><p>Risk Parameters Safeguard Solvency</p></figcaption></figure>

### Reserve Factor

The Reserve Factor is the percentage of interest payments (protocol fees) set aside as protocol reserves.  This reserve is used to sustain DAO operations and pay for protocol development; it also acts as an additional layer of security for the protocol, being employed in the case of a shortfall event, prior to any activation of the Safety Module.&#x20;

* **Risk Consideration**: A higher Reserve Factor builds a larger safety net for the protocol but may reduce yields for lenders.
* **Calculation**: Reserve Factor = (Interest Allocated to Reserves) / (Total Interest Collected) x 100%
