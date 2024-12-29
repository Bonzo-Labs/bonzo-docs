# Dashboard Metrics Explained

The Bonzo Finance dashboard provides users with essential information about their lending and borrowing positions. Here's an overview of these metrics:&#x20;

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p>Bonzo Finance Dashboard</p></figcaption></figure>

<table><thead><tr><th width="249">Terminology</th><th>Description</th></tr></thead><tbody><tr><td><strong>Loan Health Indicator Bar</strong></td><td>This bar represents the overall health of all current positions combined. It visually displays a user's current loan-to-value (LTV) ratio (white), relative to their maximum LTV (yellow) and liquidation LTV (red).</td></tr><tr><td><strong>Borrow Power</strong></td><td>This figure represents the maximum amount a user can borrow based on their supplied collateral. It fluctuates with market conditions and the value of supplied collateral.</td></tr><tr><td><strong>Net APY</strong></td><td>This percentage shows a user's net earnings or costs from using the platform. It combines the interest earned from lending assets with the interest paid for borrowing assets. A positive number means a user is earning more interest than they are paying.</td></tr><tr><td><strong>Health Factor</strong></td><td>A crucial metric for borrowers, the Health Factor indicates how close your position is to being liquidated. The higher this number, the safer your position. If it approaches 1, you're at risk of liquidation.</td></tr><tr><td><strong>Loan-to-Value (LTV)</strong></td><td>This percentage indicates how much value a user has borrowed, relative to the value supplied as collateral. For example, if a user has supplied $1,000 worth of assets as collateral and borrowed $500, their LTV would be 50%.</td></tr><tr><td><strong>Liquidation LTV</strong></td><td>This is the maximum LTV a user's position(s) can reach before being susceptible for liquidation. If a user's current LTV reaches this threshold, their collateral may be liquidated to repay their loan.</td></tr></tbody></table>

### **Understanding and Utilization of Metrics:**

* Users should regularly monitor their **Health Factor**. If it's decreasing, users should consider repaying some of their loan(s) or supplying more assets as collateral.
* Use **Borrow Power** wisely — just because a user can borrow more, doesn't always mean they should.
* Users should aim to keep **loan-to-value (LTV)** comfortably below the **Liquidation LTV** to maintain a safe position to prevent liquidations.
* **Net APY** is an aggregate APY that combines all supply & borrow position APYs to determine an aggregate APY. A positive Net APY means that a user is earning more than they're paying in interest.
  * _Net APY does not factor in supplemental liquidity incentives (APYs with a ✨ next to them) or the usage of borrowed funds across other DeFi platforms outside of Bonzo Finance._
