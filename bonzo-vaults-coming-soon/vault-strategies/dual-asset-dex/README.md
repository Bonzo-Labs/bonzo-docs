---
icon: coins
---

# Dual Asset DEX

The **Dual Asset DEX** vault strategy allows anyone to earn yield from **concentrated liquidity pools** on partner DEXs (like [SaucerSwap](https://saucerswap.finance/)), without having to manage ranges, NFTs, or rebalance positions themself.

Under the hood, **Dual Asset DEX** strategy vaults are liquidity management contracts that takes user deposits, creates concentrated-liquidity positions for them, and actively keeps those positions in a "productive price range".

**How the Dual Asset DEX vault strategy works:**

* Deposit a pair of tokens,
* Receive fungible vault share tokens representing your share of the vault, and
* Over time, your share is backed by more of the underlying tokens as fees are earned and reinvested (auto-compounding).

The complexity and maintenance of concentrated liquidity management is entirely automated inside of the vault strategy.

### The Dual Asset DEX Vault Strategy Explained

The **Dual Asset DEX vault strategy** has one job: **keep as close to 100% of the liquidity deployed in range and earning fees for users**. That includes all deposits, the trading fees currently building up in the pool, and all past fees that have already been compounded back into the position.

Whenever a user deposits or withdraws — or a scheduled "harvest" function runs — the vault strategy **withdraws liquidity from the pool and rebalances** the concentrated-liquidity position. First, it pulls all liquidity out of the underlying DEX pool and collects any accrued fees, so it is temporarily holding all of both tokens. From there, it creates two positions in the pool:

* A M**ain Position**, where it uses a roughly 50/50 mix of the pair and deploys it into a symmetric price range around the current market price. This is the “core” concentrated liquidity position that earns most of the trading fees while the price stays in that band.
* An **Alt Position**, built from any leftover of the token that has become "overweight" as prices moved. Instead of selling those extra "overweight" tokens to rebalance the pool, the strategy intentionally parks it in a narrower, single-sided band that hugs one side of the main position. This keeps the excess token deployed and fee-earning, instead of idle or immediately sold / deposited into the 50/50 range.

<div align="center" data-with-frame="true"><figure><img src="../../../.gitbook/assets/Screenshot 2025-11-14 at 3.01.11 AM.png" alt="" width="375"><figcaption><p>Main Position &#x26; Alt Position | SaucerSwap V2 Pool Visualization</p></figcaption></figure></div>

Over time, market prices move — if the vault never adjusted, the positions would drift out of range, stop earning, and leave the liquidity supplier overexposed to the weaker token. To avoid that, the strategy periodically checks the current pool price, chooses a fresh range around it, and **rebuilds the same main + alt structure around the new price**. In Bonzo Vaults, this is done through an on-chain `moveTicks()` style function that is called automatically every so often to keep things in a healthy band and resist short-term price manipulation.

The net effect is that all liquidity in the vault is **continuously repositioned around the market price**, with a balanced core and a single-sided band for any excess, so almost all of the liquidity stays active and earning fees — without the strategy constantly selling tokens just to rebalance, which is where many users who manage liquidity themselves in a SaucerSwap v2 pool end up experiencing significant impermanent loss.

### Yield Earnings: DEX Trading Fees & LARI Rewards

Liquidity that's been deposited by the vault into an underlying SaucerSwap v2 concentrated liquidity pool generates fees for every trade. In addition, if an underlying pool offers LARI token incentives, vault participants will receive these, as well.

#### Trading Fees

The **Dual Asset DEX** vault strategy is designed to periodically pull trading fees out of the pool and compound them back into participant positions:

1. The vault claims trading fees that have accrued to the main + alt positions,
2. Returns everything into the vault strategy (rather than leaving earned fees idle in the contract), and
3. Reinvests the value back into the main and alt ranges (compounding)

#### LARI Rewards

The **Dual Asset DEX** vault strategy was also designed to support SaucerSwap v2 liquidity pools which have [LARI rewards](https://docs.saucerswap.finance/get-started/faq#what-is-lari) enabled; rewards from LARI are earned by the vault as they're emitted from SaucerSwap and shared amongst vault participations proportional to their share of ownership:

1. LARI rewards emitted by SaucerSwap to pool participants and send to the vault contract
2. A "LARI" function is called, similar to calling the vault's "harvest" function
3. The vault swaps all rewards received for the underlying pool tokens on SaucerSwap
4. The vault rebalances / deposits tokens received from the swap into the underlying pool
5. Participants utilizing the vault see an increase in yield proportional to their share

### Vault Share Tokens

When you deposit assets into a Dual Asset DEX vault, you get back a **vault share token**. That token is **not** a fixed claim on a fixed amount of Token A and Token B (not 1:1). Instead, it represents a proportional slice of everything the strategy owns:

* The current main + alt positions in the pool,
* All fees and rewards harvested and folded back into the vault's liquidity position(s).

As the strategy continues to **harvest trading fees**, **collect incentives**, and **rebuilding positions** around the market price — each vault share gradually becomes worth more of the underlying token pair over time. That’s the compounding effect: the number of shares you hold stays the same, but the assets backing each share increase as the vault does its job.

**When you’re ready to exit, you simply withdraw from the vault:**

* Your vault shares are burned,
* And the vault sends you your slice of the current position in Token A and Token B — including any imbalance that’s built up from price moves and concentrated liquidity behavior.

Day-to-day you do not have to think about fee claims, reward contracts, or compounding logic — you just need to know that your Dual Asset DEX vault token is a growing claim on the strategy’s assets.

### Impermanent Loss

Providing concentrated liquidity in any DEX pool – including through a Dual Asset DEX or [Single Asset DEX](../single-asset-dex/) vault – exposes you to market risk and impermanent loss (IL). The vault automates range management and compounding, but it cannot remove the underlying economic risk of being a liquidity provider.

The **Dual Asset DEX** strategy is **designed to keep liquidity in range and fee-earning as much as possible**, and to avoid unnecessary token selling when rebalancing. This helps in a few ways:

* By staying in range, the position can continuously earn trading fees, which may offset some or all of the impermanent loss over time.
* The “Alt Position” parks any “overweight” token in a single-sided band instead of instantly selling it back into a 50/50 mix, which reduces constant churn and slippage compared to manual rebalancing.
* Auto-compounding fees and rewards means the vault is always trying to grow the asset base backing each vault share.

However, impermanent loss is still possible when utilizing a **Dual Asset DEX** strategy vault.  Impermanent loss is the difference between the value of your tokens if you had simply held them in your wallet, versus the value of your share of the liquidity pool when you withdraw.

When prices move, the pool’s AMM math gradually rebalances you into more of the weaker token and less of the stronger token. If the relative price between the two tokens has changed a lot by the time you exit, your position may be worth less (in USD terms) than simply holding the original tokens, even after including fees and rewards.
