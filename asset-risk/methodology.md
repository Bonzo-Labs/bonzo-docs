# Methodology

The composability of DeFi enables Bonzo Finance to interoperate with the entire Hedera ecosystem. However, it also exposes the protocol to potential financial contagion. Assets supported by the protocol affect the platform at its core — particularly assets that can be supplied as collateral — which safeguard the protocol's solvency. To ensure that an asset holds a reasonable amount of risk, Bonzo Finance's asset risk methodology framework evaluates risk based on three high-level risk factors: Hedera Token Service (HTS) Risk, Counterparty Risk, and Market Risk.

## Risk Scale&#x20;

Bonzo Finance employs a risk scale ranging from the lowest risk (A+), for the safest assets supported by the protocol (often stablecoins, like USDC), to the highest risk (D-), for volatile assets supported by the protocol (often token-based projects with minimal liquidity and high volatility). Assets exposed to high risk factors can be considered for integration; however, they will not qualify as collateral to ensure the protocol's solvency.

### Asset Risk Quantification Criterion

The asset risk quantification criterion offers a framework by which to grade every supported and potentially supported assets based on their individual risk attributes.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### Risk Assessment&#x20;

The historical data supporting the analysis is extracted from reliable sources, such as CoinGecko, TierBot, and SaucerSwap, for reliable on-chain and off-chain data. The methodology to link historical data to risk factors has been formalized based on rigid criteria for each factor and rating.

By adhering to this comprehensive risk assessment methodology, Bonzo Finance aims to ensure that the currencies integrated into the protocol contribute to a secure and stable lending and borrowing environment while minimizing exposure to various types of risks inherent in the DeFi ecosystem.

## Risk Factors

### Hedera Token Service (HTS) Risk

HTS risk evaluates the technical security and maturity of a token based on its configuration and usage metrics, offering insight into the token's market acceptance. This is critical for assessing its suitability as collateral. HTS risk includes the following factors:

**Days**: The age of the token is a crucial indicator of its stability and resilience. Older tokens have had more time to uncover and address potential vulnerabilities, and have demonstrated longevity in the market.

**Transactions**: The total number of transactions involving the token is a measure of its adoption and real-world usage. A higher number of transactions suggests a more established and actively used token, potentially indicating lower risk.

### Counterparty Risk

The counterparty risk assessment is crucial for understanding potential centralization risks and the likelihood of unilateral actions that could affect token holders. It assesses the governance and control structure of the token, focusing on the following factors:

**Holders**: The number of holders here reflects the decentralization of token ownership; a wider distribution of holders generally indicates lower counterparty risk. Additionally, a larger holder base typically indicates broader adoption and reduced concentration risk.

**Permission**: This criterion evaluates the level of control and governance decentralization. It considers the configuration of key permissions such as admin, supply, freeze, and pause functions. More decentralized governance structures with higher thresholds or no centralized control are viewed as lower risk.

### Market Risk

These market risk factors are essential for calibrating risk parameters, such as Loan-to-Value (LTV) ratios, liquidation thresholds, liquidation bonus, and usage as collateral. They provide a comprehensive view of the token's market behavior, liquidity, and stability, which are crucial for managing risk in lending and borrowing protocols.\
\
Market risk encompasses several factors related to the token's market characteristics:

**Market Cap**: The total market capitalization serves as an indicator of the token's overall market size and stability. Larger market caps generally suggest more established and less volatile tokens.

**Avg. 24 Hour Volume**: Trading volume is a key liquidity indicator. Higher volumes typically mean better liquidity, which is crucial for efficient price discovery and reduced slippage during large transactions or liquidations. The average 24 hour volume represents the availability of an asset to assess liquidity risk:

$$
E[\text{volume}]
$$

**Avg. DEX Liquidity**: This metric focuses specifically on decentralized exchange liquidity, which is critical for Bonzo Finance as it will rely on DEXs for various operations, such as liquidations. Higher DEX liquidity reduces the risk of significant price impacts during necessary token swaps.

**Normalized Volatility**: This measure of price fluctuations helps assess the token's price stability. Lower volatility is generally preferred for collateral assets as it reduces the risk of sudden value drops that could trigger liquidations. This is calculated using the standard deviation of the logarithmic returns:

$$
$\sigma\left[\ln\left(\frac{\text{close}(t+1)}{\text{close}(t)}\right)\right]$
$$

## Historical Data Matrix

The matrix below shows the figures used to quantify risks per factor. This table is based on historical data that includes the applied the calculations described above.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>Historical Data Matrix | 08/12/2024</p></figcaption></figure>

