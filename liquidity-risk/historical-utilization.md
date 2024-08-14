# Historical Utilization

## Introduction to Utilization Rate

Each currency reserve in Bonzo Finance is characterized by its utilization rate $$U$$:

$$
U = \frac{\text{TotalBorrows}}{\text{TotalLiquidity}}
$$

The utilization rate monitors what proportion of the reserve's total capital is borrowed at any given time.

## Balancing Risks & Benefits of Utilization

As $$U$$ approaches 100%, the available capital becomes increasingly scarce until no more liquidity is available upon $$U = 100\%$$. This situation can be problematic if depositors wish to withdraw their supplied funds, but no liquidity is available.

However, high utilization also results in higher returns for depositors. Therefore, it's essential to maximize utilization while safeguarding liquidity.

## Interest Rate Model & Optimal Utilization

The interest rate model in Bonzo Finance is calibrated around an optimal utilization rate $$Uoptimal$$ for each reserve, reflecting the unique market conditions of the Hedera network.

Bonzo Finance tracks the historical utilization rate to monitor the risk of liquidity shortages. This analysis is based on the maximum daily utilization, serving as a conservative proxy for liquidity risk. Given that Bonzo Finance is a new protocol on Hedera, the initial analysis will be limited but will grow more comprehensive over time.

As Bonzo Finance gathers more data specific to the protocol the Hedera DeFi ecosystem at large, it will provide statistics on the maximum daily utilization for various assets in Bonzo Finance markets. This data will support better understanding:

1. How often full utilization is reached for supported assets
2. Which assets tend to have higher utilization rates
3. How utilization patterns on Hedera differ from other networks

This information will be crucial for fine-tuning our interest rate models, setting appropriate risk parameters, and ensuring the overall health of the Bonzo Finance protocol within the Hedera ecosystem. After borrowing has been enabled for at least one quarter, the historical utilization analysis will be made available in the table below.

<table><thead><tr><th width="165">Statistic</th><th>% of Time</th><th data-hidden></th></tr></thead><tbody><tr><td>= 100%</td><td>-</td><td></td></tr><tr><td>>95%</td><td>-</td><td></td></tr><tr><td>>90%</td><td>-</td><td></td></tr><tr><td>>80%</td><td>-</td><td></td></tr><tr><td>>50%</td><td>-</td><td></td></tr><tr><td>&#x3C; 25%</td><td>-</td><td></td></tr><tr><td>&#x3C; 10%</td><td>-</td><td></td></tr><tr><td>&#x3C; 5%</td><td>-</td><td></td></tr></tbody></table>
