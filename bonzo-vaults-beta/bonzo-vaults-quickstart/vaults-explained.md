# Vaults Explained

### What Is a Vault?

In Bonzo, a **Vault** is the main user-facing primitive: it’s where you deposit assets so that a **strategy** can put them to work on your behalf. Operationally, a Bonzo Vault:

* Accepts user deposits in a specific asset or asset pair (e.g. a DEX pair used in a [Dual Asset DEX](../vault-strategies/dual-asset-dex/) strategy vault),
* Mints vault share tokens that represent a proportional claim on everything the strategy owns, and
* Delegates the actual yield generation (liquidity provision, fee collection, reward harvesting, compounding, range management, etc.) to one or more underlying strategies.

Instead of manually managing liquidity ranges, harvesting rewards, swapping incentives back into the underlying tokens, and re-depositing over and over — users of Bonzo Vaults simply deposit into a vault once. The vault + strategy "stack" automates those workflows and compounds at a higher frequency than most users would reasonably do themselves.

#### How Do Bonzo Vaults Earn?

Bonzo Vaults are designed so that, over time, each share represents more of the underlying position. For example, in [**Dual Asset DEX**](../vault-strategies/dual-asset-dex/) and [**Single Asset DEX**](../vault-strategies/single-asset-dex/) strategy vaults, participants earn more of the underlying token pair they've deposited; for these two strategies, yield earned is maximized for depositors via three mechanisms:&#x20;

1. Active management of liquidity deposited into the vault, which is routed to SaucerSwap v2 concentrated liquidity pool(s) and actively managed / rebalanced for continuous, tight concentration (captures more trading fees).
2. Auto-compounding of those trading fees earned.
3. Harvesting [SaucerSwap LARI rewards](https://docs.saucerswap.finance/protocol/saucerswap-v2#liquidity-aligned-reward-initiative-lari), swapping (as needed) into each vault's underlying token pair, and distributing amongst vault participants.

#### Are Funds Locked in a Vault?

Despite the name, **Bonzo Vaults do not lock user funds**:

* **Withdrawals** from a vault can take place at any time; for specific vaults, there may be a 0.5% withdrawal fee configured to prevent flash loan abuse / exploitation — if a vault has a withdrawal fee configured, it will state this very clearly in the deposit interface's fee section
* **Deposits** into a vault can take place at any time — subject only to temporary "calm periods" for certain vaults, during periods of underlying asset TWAP (time-weighted average price) volatility.
* Bonzo Finance **does not custody any assets** — funds are always self-custody and controlled by audited smart contracts; wallet addresses holding a vault's liquidity pool tokens are the owner of vault shares, which map to a proportional slice of the vault’s assets.

Vaults are designed as medium to long-term yield tools. The benefits of compounding are maximally realized when positions are allowed to run through multiple harvest cycles, rather than being entered and exited frequently.
