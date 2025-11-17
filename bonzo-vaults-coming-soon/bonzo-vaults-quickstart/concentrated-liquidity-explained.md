# Concentrated Liquidity Explained

The [Dual Asset DEX](../vault-strategies/dual-asset-dex.md) and [Single Asset DEX](../vault-strategies/single-asset-dex/) strategy vaults route and actively manage vault deposits in underlying [SaucerSwap](https://saucerswap.finance/) V2 (decentralized exchange) pools, called **concentrated liquidity** pools. Found below is an explanation of how concentrated liquidity pools work.

### What Is Concentrated Liquidity On Decentralized Exchanges?

Traditional automated market makers (AMMs) like **SaucerSwap v1-style pools** spread liquidity across **all prices from 0 → ∞**. Liquidity suppliers earn trading fees, but most of their capital "sits" where the market never trades.

**Concentrated Liquidity (SaucerSwap v2-Style Pools) Changes This:**

* Instead of liquidity existing everywhere, the liquidity supplier chooses a **price range** (a band) where their liquidity lives.
* Inside that band, their liquidity is “thicker,” so they earn **more fees per dollar** of capital.
* If the market price moves outside of their band, the liquidity goes **out of range** and stops earning fees.

**Concentrated Liquidity is Powerful but Introduces Two Problems for Users:**

1. The user has to **decide a range**, and keep adjusting / maintaining it manually as the price moves — if they don't, the user misses out on potential yield earnings and may experience impermanent loss.
2. Positions are represented as **NFTs**, with custom interfaces rather than simple “fungible LP tokens".

The **Dual Asset DEX** vault strategy exist to solve exactly this: let liquidity providers tap into higher yield opportunities offered by concentrated liquidity pools, while the vault strategy automatically handles range management and rebalancing.
