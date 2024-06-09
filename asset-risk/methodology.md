# Methodology

The composability of DeFi enables Bonzo Finance to connect with the rest of the Hedera ecosystem. However, it also exposes the protocol to potential financial contagion. Currencies used in the protocol affect the platform at its core, particularly those accepted as collateral, which safeguard the solvency of the protocol. To ensure that a currency holds a reasonable amount of risk, the Bonzo Finance Risk Management Team investigates three different levels.

First, the team examines Hedera Token Service configurations and counter-parties in its governance. If these risks are too high, the currencies will be disqualified for integration into the protocol or to be used as collateral. Next, the team assesses market risks, which can be managed via the protocol's parameters.

## Risk Scale&#x20;

Bonzo Finance employs a risk scale ranging from the lowest risk, A+, for the safest assets of the protocol (often stablecoins, like USDC), to the highest risk, D-. Assets exposed to high risk factors can be considered for integration. However, they will not qualify as collateral to ensure the protocol's solvency.

## Risk Factors

### Hedera Token Service Configuration Risk&#x20;

**Hedera Token Service (HTS) configuratoin risk** focuses on the technical security of a currency based on its underlying configuration. If one of the supported currencies is compromised, collaterals will be affected, threatening the solvency of the protocol. Projects must have undergone audits to be considered, yet Hedera Token Service and smart contract (managing tokens) risk is significant and cannot be fully mitigated, even with bug bounties. The Bonzo Finance team assesses maturity based on the number of days and transactions of the HTS token as a representation of use, community, and development. These proxies show how battle-tested the code is.

Given the potential for substantial losses due to key configuration and smart contract vulnerabilities, currencies with the highest risk, D+ and below, cannot be used as collateral. Currencies with a risk rating below D cannot be integrated into the protocol.

### Counter-party Risk&#x20;

**Counter-party risk** assesses qualitatively how and by whom the currency is governed. The Bonzo Finance team observes different degrees of governance decentralization that may give direct control over funds (e.g., as backing) or attack vectors to the governance architecture, which could expose control and funds. The counter-party risk is measured by the level of centralization, corresponding to the number of parties that control the protocol, as well as the number of holders and the trust in the entity, project, or processes.

Currencies with a high counter-party risk below D+ disqualify as collateral.

### Market Risk&#x20;

**Market risks** are linked to market size and fluctuations in supply and demand. These risks are particularly relevant for the protocol's assets, i.e., the collateral. If the value of the collateral decreases, it might reach the liquidation threshold and start getting liquidated. The markets then need to hold sufficient volume for these liquidations – sells which tend to lower the price of the underlying asset through slippage, affecting the value recovered.

The Bonzo Finance team looks at the average 24-hour volume representing the availability of the currency to assess liquidity risk: E\[volume].

**Volatility risk** is based on the normalized fluctuations in the currency's price and calculated as the standard deviation of the logarithmic returns: σ\[ln(close(t+1)/close(t))]. This metric is in line with industry standards used by platforms like Bitmex and Gauntlet.

These values are examined at intervals of 1 month, 3 months, and 6 months.

Cryptocurrencies can be subject to sudden volatility spikes; it is not uncommon to witness 30% changes in price within a week or a month. When this is a price increase, to protect users, it might be followed by a parameter readjustment to limit risks of new operations.

Finally, the team also considers **market capitalization**, representing the size of the market.

Market risks are used for the calibration of the model's risk parameters. Volatility helps define the required level of collateralization, known as the Loan-to-Value (LTV) ratio. Liquidity risks are contained by liquidation incentives: the liquidation threshold and bonus.

## Risk Assessment&#x20;

The historical data supporting the analysis is extracted from reliable sources and combined with on-chain data. The methodology to link historical data to risk factors has been formalized based on rigid criteria for each factor and rating.

By adhering to this comprehensive risk assessment methodology, Bonzo Finance aims to ensure that the currencies integrated into the protocol contribute to a secure and stable lending and borrowing environment while minimizing exposure to various types of risks inherent in the DeFi ecosystem.

### Historical Data Matrix

The matrix below shows the figures used to quantify risks per factor. This table is based on historical data that includes the applied the calculations described above.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>Historical Data Matrix | Last Updated 06/07/2024</p></figcaption></figure>

### Risk Quantification Criterion

The historical data is computed through our risk quantification algorithm resulting in risk ratings from the lowest risks A+ to the highest risks D- following the criteria in the table below.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Risk Quantification Criterion</p></figcaption></figure>
