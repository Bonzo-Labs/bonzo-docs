# Borrow Rate Methodology

Bonzo Finance's interest rate strategy is calibrated to manage liquidity risk and optimize utilization on the Hedera network. The borrow interest rates are derived from the Utilization Rate $$U$$.

$$U$$ is an indicator of capital availability in the pool. The interest rate model manages liquidity risk through user incentives:

* **When capital is available**: Low interest rates to encourage borrowing.
* **When capital is scarce**: High interest rates to encourage loan repayments and additional deposits.

## **Interest Rate Model**

Liquidity risk increases as $$U$$ approaches 100%. To address this, the interest rate curve is split around an optimal utilization rate $$U_{optimal}$$. Before $$U_{optimal}$$, the slope is gentle; after, it rises sharply.

The interest rate $$R_t$$ follows the model:

If $$U < U_{optimal}$$ : $$R_t = R_0 + \frac{U_t}{U_{optimal}} R_{slope1}$$

If $$U \geq U_{optimal}$$ : $$R_t = R_0 + R_{slope1} + \frac{U_t - U_{optimal}}{1 - U_{optimal}} R_{slope2}$$

In the technical implementation, the [calculateCompoundInterest](https://github.com/Bonzo-Labs/bonzo-finance-contracts/blob/660ee467156ad3078e0d61e07e347a920eb1d621/contracts/protocol/libraries/math/MathUtils.sol#L45) method relies on an approximation that mostly affects high interest rates. This is expressed as:&#x20;

$$
ActualAPY = (1 + TheoreticalAPY/secsperyear)^{secsperyear} - 1
$$

Variable interest models are derived from this formula, with parameters adjusted for each asset.

* When $$U<UoptimalU<Uoptimal$$​ the borrow interest rates increase slowly with utilization.
* When $$U≥UoptimalU≥Uoptimal​$$ the borrow interest rates increase sharply with utilization to above 50% APY if the liquidity is fully utilized.

Variable loans see their rate constantly evolving with utilization. This means they are not ideal for financial planning.

## **Model Parameters**

Bonzo Finance calibrates interest rate parameters for clusters of currencies with similar risk profiles on Hedera:

<table><thead><tr><th width="148"></th><th width="214">Optimal Utilization</th><th>Slope 1</th><th>Slope 2</th></tr></thead><tbody><tr><td><strong>Stablecoins</strong></td><td>70-90%</td><td>4% - 6%</td><td>100% - 200%</td></tr><tr><td><strong>Majors</strong></td><td>70-80% (Liquid Staking Tokens) / 60-70% (Crypto Assets)</td><td>6% - 8%</td><td>100% - 200%</td></tr><tr><td><strong>Minors</strong></td><td>≤ 55%</td><td>8% - 10%+</td><td>150% - 300%+</td></tr></tbody></table>

## **Optimization for Hedera**

Bonzo Finance optimizes its interest rate models to be competitive within the Hedera ecosystem while maintaining risk mitigation properties. This includes:

1. Adjusting $$U_{optimal}$$ for assets affected by Hedera-specific liquidity mining programs.
2. Considering unique characteristics of Hedera native tokens and their staking incentives.
3. Regular review and adjustment based on liquidity risk assessments specific to the Hedera DeFI ecosystem.

By tailoring the interest rate strategy to Hedera's unique ecosystem, Bonzo Finance aims to provide competitive rates while ensuring robust liquidity management on the network.\
