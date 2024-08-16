# Risk Parameters per Asset

Each asset in the Bonzo Finance protocol has configurable risk parameters, which influences how they are supplied and borrowed. The calibration of the parameters will be conservative as the protocol launches, to ensure safety, and become more aggressive as the Bonzo Finance ecosystem matures with educated users, greater liquidity, and a thriving liquidation ecosystem.

The table below offers a summary of the latest risk parameters per asset:

<table><thead><tr><th width="136">Asset</th><th width="110">Collateral</th><th width="186">Loan-to-Value (LTV)</th><th width="206">Liquidation Threshold</th><th width="169">Liquidation Bonus</th><th width="148">Reserve Factor</th></tr></thead><tbody><tr><td>$HBAR</td><td>Yes</td><td>75%</td><td>80%</td><td>5%</td><td>20%</td></tr><tr><td>$HBARX</td><td>Yes</td><td>70%</td><td>75%</td><td>5%</td><td>20%</td></tr><tr><td>$USDC</td><td>Yes</td><td>75%</td><td>78%</td><td>4.5%</td><td>20%</td></tr><tr><td>$SAUCE</td><td>Yes</td><td>70%</td><td>76%</td><td>8%</td><td>20%</td></tr><tr><td>$XSAUCE</td><td>Yes</td><td>70%</td><td>76%</td><td>8%</td><td>20%</td></tr><tr><td>$KARATE</td><td>No</td><td>55%</td><td>65%</td><td>13%</td><td>20%</td></tr><tr><td>$DOVU</td><td>No</td><td>55%</td><td>65%</td><td>12%</td><td>20%</td></tr><tr><td>$PACK</td><td>No</td><td>45%</td><td>60%</td><td>12%</td><td>20%</td></tr><tr><td>$HST</td><td>No</td><td>40%</td><td>50%</td><td>12%</td><td>20%</td></tr><tr><td>$STEAM</td><td>No</td><td>45%</td><td>50%</td><td>14%</td><td>20%</td></tr></tbody></table>

The table above results from the asset risk assessment relating to security, governance and the markets. Tokens with high risk exposure to single counter-parties cannot be used as collateral.

## Risk Parameter Changes

When market conditions change, risks change; Bonzo Finance is continuously monitoring the assets integrated into the protocol, which sometimes requires quickly adapting the risk parameters. The table below tacks parameter changes over time.

<table><thead><tr><th width="134">Date</th><th width="113">Asset</th><th width="194">Parameter Changed</th><th>From</th><th>To</th></tr></thead><tbody><tr><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr></tbody></table>

## Risk Parameters Defined & Explained

The risk parameters allow to mitigate market risks of tokens supported by the protocol. Borrowing assets is guaranteed by a collateral that may be subject to volatility. Sufficient margin and incentives are needed for the position to remain collateralised in adverse market conditions. If the value of the collateral falls bellow its liquidation threshold, part of it is auctioned to liquidation bots to repay part of the position, ensuring creditors remain solvent.

### **Collateral (Yes/No)** <a href="#loan-to-value" id="loan-to-value"></a>

This .................

## Configuring Parameters via Market Risk Assessment&#x20;

The "market risk" category of the asset risk quantification criterion (found in the "[methodology](risk-score-methodology.md)" section of the documentation) has the highest impact on the configuration of risk parameters cited above.&#x20;

Market Risk includes the following components, analyzed per asset on a quarterly basis:

### **Trading Volume**

Based on the average 24 hour trading volume per asset, normalized over a period of 1M and 3M. Sufficiently traded assets ensure a smooth liquidation process.&#x20;

With low trading volume, risks can be mitigated via configuration of liquidation parameters, such as the liquidation bonus — essentially, the lower the trading volume of an asset, the higher the incentives are configured in Bonzo Finance to liquidate the asset, to account for slippage.

### **DEX Liquidity**

Similar to trading volume, average DEX liquidity normalized over 1M and 3M ensures enough liquidity in decentralized exchanges for a smooth liquidation process.&#x20;

With low average DEX liquidity, risks can be mitigated via configuration of liquidation parameters, such as the liquidation bonus — essentially, the lower the DEX liquidity, the higher the incentives are configured in Bonzo Finance to liquidate the asset, to account for slippage.

### Normalized Volatility

The average normalized volatility of an asset's price can negatively affect the collateral and its ecosystem's ability to cover liabilities. The risk of global collateral value falling below the global value of borrowed amounts can be mitigated per asset via loan-to-value (LTV) and liquidation threshold configurations. Normalized volatility also affects the liquidation process, as the margin for liquidators must allow for profit to ensure they participate in this activity.

The least volatility currencies are stablecoins, followed by majors; these assets typically have the highest LTV and the highest liquidation thresholds.

The most volatile currencies lowest LTV and the liquidations thresholds are typically set much higher, to protect users from sharp drops in price, which could quickly lead to undercollaterisation.

### Market Capitalization

Market Capitalisation (Market Cap) represents the total value of the asset's market. This is also a critical factor when it comes to liquidating collateral. The smaller the market cap, the larger the incentives for liquidating.

