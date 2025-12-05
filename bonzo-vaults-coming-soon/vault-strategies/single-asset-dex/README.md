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
