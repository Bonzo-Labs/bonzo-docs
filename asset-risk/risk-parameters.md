# Risk Parameters

Each asset in the Bonzo Finance protocol has specific values related to their risk, which influences how they are supplied and borrowed. The calibration of the parameters will be conservative as the protocol launches, to ensure safety, and become more aggressive as the Bonzo Finance ecosystem matures with educated users and thriving liquidation ecosystem.

The table below shows a summary of the latest values:

<table><thead><tr><th width="136">Asset</th><th width="128">Collateral</th><th width="191">Loan-to-Value (LTV)</th><th width="210">Liquidiation Threshold*</th><th width="170">Liquidation Bonus</th><th width="148">Reserve Factor</th></tr></thead><tbody><tr><td>$HBAR</td><td>Yes</td><td>75%</td><td>89%</td><td>5%</td><td>20%</td></tr><tr><td>$HBARX</td><td>B+</td><td>75%</td><td>88%</td><td>5%</td><td>20%</td></tr><tr><td>$USDC</td><td>Yes</td><td>75%</td><td>78%</td><td>4.50%</td><td>20%</td></tr><tr><td>$SAUCE</td><td>Yes</td><td>70%</td><td>85%</td><td>8%</td><td>20%</td></tr><tr><td>$XSAUCE</td><td>Yes</td><td>70%</td><td>85%</td><td>8%</td><td>20%</td></tr><tr><td>$KARATE</td><td>No</td><td>55%</td><td>72%</td><td>12%</td><td>20%</td></tr><tr><td>$DOVU</td><td>No</td><td>55%</td><td>72%</td><td>12%</td><td>20%</td></tr></tbody></table>

_\*2-3x average normalized volatility over 1M, 3M, 6M_\
\
The table above results from the asset risk assessment relating to security, governance and the markets. Tokens with high risk exposure to single counter-parties cannot be used as collateral.

## Risk Parameter Changes

When market conditions change, risks change; Bonzo Finance is continuously monitoring the assets integrated into the protocol, which sometimes requires quickly adapting the risk parameters. The table below tacks parameter changes over time.

<table><thead><tr><th width="134">Date</th><th width="113">Asset</th><th width="194">Parameter Changed</th><th>From</th><th>To</th></tr></thead><tbody><tr><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr></tbody></table>

## Risk Parameter Analysis

The risk parameters allow to mitigate market risks of tokens supported by the protocol. Borrowing assets is guaranteed by a collateral that may be subject to volatility. Sufficient margin and incentives are needed for the position to remain collateralised in adverse market conditions. If the value of the collateral falls bellow its liquidation threshold, part of it is auctioned to liquidation bots to repay part of the position, ensuring creditors remain solvent.

### **Loan-to-Value (LTV)** <a href="#loan-to-value" id="loan-to-value"></a>

The Loan-to-Value (LTV) ratio defines the maximum amount of currency that can be borrowed with a specific collateral. It’s expressed in percentage: at LTV=75%, for every 1 HBAR worth of collateral, borrowers will be able to borrow 0.75 HBAR worth of the corresponding currency. Once a borrow is taken, the LTV evolves with market conditions.

**For each wallet the maximum LTV is calculate as the weighted average of the LTVs of the collateral assets and their value:**

$$
\text{MaxLTV} = \frac{\sum \text{Collateral}_i \text{ in HBAR} \times \text{LTV}_i}{\text{Total Collateral in HBAR}}
$$

### **Liquidation Threshold** <a href="#loan-to-value" id="loan-to-value"></a>

The liquidation threshold is the percentage at which a position is defined as undercollateralised. For example, a Liquidation Threshold of 80% means that if the value rises above 80% of the collateral, the position is undercollateralized and could be liquidated.

The delta between the Loan-To-Value (LTV) and the Liquidation Threshold is a safety cushion for borrowers.

**For each account the Liquidation Threshold is calculated as the weighted average of the Liquidation Thresholds of the collateral assets and their value:**

$$
\text{Liquidation Threshold} = \frac{\sum \text{Collateral}_i \text{ in HBAR} \times \text{Liquidation Threshold}_i}{\text{Total Collateral in HBAR}}
$$

### **Liquidation Bonus** <a href="#loan-to-value" id="loan-to-value"></a>

Bonus on the price of assets of the collateral when liquidators purchase it as part of the liquidation of a loan that has passed the liquidation threshold.

### **Health Factor** <a href="#loan-to-value" id="loan-to-value"></a>

For each wallet, these risks parameters enable the calculation of the health factor:

$$
H_f = \frac{\sum \text{Collateral}_i \text{ in HBAR} \times \text{Liquidation Threshold}_i}{\text{Total Borrows in HBAR}}
$$

When the following formula below is true, the position may be liquidated to maintain solvency as described in the diagram below.

$$
H_f < 1
$$

