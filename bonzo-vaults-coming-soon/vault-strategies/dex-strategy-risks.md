---
icon: triangle-exclamation
---

# DEX Strategy Risks

When using a **Dual Asset DEX** or **Single Asset DEX** vault, you accept the following non-exhaustive set of risks:

#### **1. Price & Market Risk**

* If both tokens go down in USD terms, the value of your position (and your vault shares) also goes down.
* If one token crashes or gets exploited, your share of the pool may end up heavily skewed toward that failing asset.
* High volatility can increase both earned fees and impermanent loss; outcomes are not guaranteed to be positive.

#### **2. Impermanent Loss Risk**

* Large relative price moves between the two tokens (e.g., Token A 2–3x vs. Token B or vice versa) can lead to significant IL.
* Even with active management, you may withdraw more of the underperforming token and less of the outperforming token than you initially contributed, after all rebalances.
* If you exit after a big divergence without a price “reversion,” the IL is realized and may outweigh fees and rewards.

#### **3. Range Management & Strategy Risk**

* The **Dual Asset DEX** strategy relies on on-chain logic (e.g., `moveTicks()` functions) being called regularly to keep positions in a healthy band. If these calls are delayed, fail, or become uneconomical, positions can sit out of range and stop earning fees.
* The chosen parameters  — how wide ranges are, how often to rebalance, how the main vs. alt positions are configured --  are strategy choices, not guarantees. Different choices would produce different results; past performance of a given configuration does not guarantee future outcomes.
* During rebalances, harvests, and LARI reward function calls, there may be slippage and trading costs that reduce net returns.

#### **4. LARI & Incentive Token Risk**

* Vaults which offer LARI (SaucerSwap liquidity incentives) or other reward token mechanims carry their own market and liquidity risk. If reward token prices fall, the additional yield from incentives shrinks.
* For **Dual Asset DEX** vault strategies with LARI incentives, they will typically swap LARI rewards into the underlying pool tokens; this adds DEX execution risk (slippage, price impact) each time rewards are harvested and converted.

#### **5. Smart Contract & Protocol Risk**

By using the vault, you are trusting multiple smart contract systems:

* The vault contracts themselves,
* The underlying SaucerSwap v2 concentrated liquidity pools, and
* Any related reward or integrations contracts involved in the strategy.

Even with audits and testing, smart contracts can contain bugs, vulnerabilities, or unexpected behaviors that may lead to loss of funds.

Other protocol-level risks include:

* Issues or exploits in the underlying blockchain or network,
* Governance changes or upgrades to partner protocols,
* Oracle or price-manipulation attacks on the pools where the strategy is deployed.

#### **6. Liquidity, Slippage & Timing Risk**

* Large deposits or withdrawals relative to vault size can experience **slippage** as the strategy rebalances and repositions liquidity.
* Entering or exiting during periods of extreme volatility or low liquidity can lead to worse execution and a less favorable mix of tokens upon withdrawal.
* Vault share prices move with underlying pool conditions; the value of shares can be higher or lower at any given moment depending on market behavior.
