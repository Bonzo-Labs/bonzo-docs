---
icon: coin
---

# Single Asset DEX

The **Single Asset DEX** vault strategy allows anyone to earn yield from **concentrated liquidity pools** on partner DEXs (like [SaucerSwap](https://saucerswap.finance/)), without having to manage ranges, NFTs, or rebalance positions themself.

Under the hood, **Single Asset DEX** strategy vaults are liquidity management contracts that takes a **single asset deposit**, creates concentrated-liquidity positions for it, and actively keeps all positions in a "productive price range".  **Single Asset DEX** vaults operate **four strategy types —** depending on the type of underlying pool assets and their volatility — each of which is described in the section below.

**How the Single Asset DEX vault strategy works:**

* Deposit a single token (which gets paired with its underlying pool asset),
* Receive fungible vault share tokens representing your share of the vault, and
* Over time, your share is backed by more of both underlying tokens as fees are earned and reinvested (auto-compounding).

The complexity and maintenance of concentrated liquidity management is entirely automated inside of the vault strategy.

{% hint style="info" %}
**Note:** Upon **deposit of a single asset** into a **Single Asset DEX** strategy vault — the strategy automatically converts _**some**_ of the single asset deposited into the asset it's paired with in the underlying pool; prior to initiating a deposit, the interface will display how much of the asset will be converted to its pair.\
\
You can track how the ratio of the two assets change over time, right from the vault interface. **Upon** **withdraw from the vault** you will receive a ratio of both tokens, which is displayed on the vault's interface prior to initiating a withdraw.
{% endhint %}

### Impermanent Loss

While Single Asset DEX and [Dual Asset DEX](./) vaults automate the complex task of liquidity provisioning, they do not eliminate the underlying economic risks of decentralized exchange (DEX) pools. Providing liquidity — even with a single asset — exposes the deposit to Impermanent Loss (IL) and market volatility.

In the context of a Single Asset vault, Impermanent Loss is best understood as the difference between the value of your vault position versus simply holding 100% of your deposited asset in a wallet.

#### **How the Single Asset DEX Strategy Mitigates Risk**

Unlike the [Dual Asset DEX](./) strategy that typically aim to maintain a neutral 50/50 split, the Single Asset DEX strategy utilizes Inventory Management logic designed to favor your deposited token.

* **Unbalanced Liquidity:** The strategy often concentrates liquidity in an "unbalanced" range that biases exposure toward the asset you deposited; this attempts to minimize "selling into strength" (selling your rising asset) compared to a standard 50/50 pool.
* **Active Boundary Management:** As prices move, the vault algorithmically adjusts its price ranges. This "active management" aims to keep your capital working and earning fees high enough to outpace the effects of divergence loss (IL).
* **Volatility Dampening:** By automating the rebalancing process, the strategy prevents the "whipsaw" effect often suffered by manual users who trade back and forth too frequently during chop.

#### **What Users Should Expect**

Despite mitigation efforts, Impermanent Loss (IL) is still possible.

* **Asset Composition Changes:** To earn yield, the vault must facilitate trades against your asset. This means if the price of your deposited asset rises significantly against its pair, the vault may gradually sell a portion of it to maintain a productive range. Conversely, if the price drops, the vault may accumulate more of the deposited asset ("buying the dip").
* **Withdrawal Ratio:** You should expect to withdraw a combination of both the deposited asset and its paired asset. The exact ratio will depend on the market conditions at the time of withdrawal.
* **Net Outcome:** The goal of the Single Asset DEX strategy is for the accumulated trading fees to exceed any impermanent loss incurred during the deposit period, resulting in a net profit in terms of the deposited asset. However, in extreme volatility where price direction is sustained and severe, the value of the vault share (in USD terms) could theoretically be lower than holding the single asset alone.
