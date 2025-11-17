# Vaults Explained

### What Is a Vault?

In Bonzo, a **Vault** is the main user-facing primitive: it’s where you deposit assets so that a **strategy** can put them to work on your behalf. Operationally, a Bonzo Vault:

* Accepts user deposits in a specific asset or asset pair (e.g. a DEX pair used in a [Dual Asset DEX](../vault-strategies/dual-asset-dex.md) strategy vault),
* Mints vault share tokens that represent a proportional claim on everything the strategy owns, and
* Delegates the actual yield generation (liquidity provision, fee collection, reward harvesting, compounding, range management, etc.) to one or more underlying strategies.

Instead of manually managing liquidity ranges, harvesting rewards, swapping incentives back into the underlying tokens, and re-depositing over and over — users of Bonzo Vaults simply deposit into a vault once. The vault + strategy "stack" automates those workflows and compounds at a higher frequency than most users would reasonably do themselves.

#### How Do Bonzo Vaults Earn?

Bonzo Vaults are designed so that, over time, each share represents more of the underlying position.  For example, in a [**Dual Asset DEX**](../vault-strategies/dual-asset-dex.md) strategy vault, participants earn more of the underlying token pair (e.g., more of the liquidity pool exposure the strategy is managing for its participants),

Participants don’t earn a separate “reward token” inside the vault itself — instead, fees and incentives (like DEX rewards, such as SaucerSwap LARI rewards) are harvested by the strategy, swapped as needed, and folded back into the vault’s core position, increasing the asset base backing every vault share.

#### Are Funds Locked in a Vault?

Despite the name, **Bonzo Vaults do not lock user funds**:

* Withdrawal from a vault can take place at any time — subject only to temporary "calm periods" for certain vaults, where an automated rebalancing that takes place frequently is required before participants can withdraw.
* Bonzo Finance does not take custody of any assets; funds are always self-custody and controlled by audited smart contracts; your wallet address is the owner of the vault shares that map to a proportional slice of the vault’s assets.

Vaults are designed as medium- to long-term yield tools; the benefits of compounding are often maximally realized when positions are allowed to run through multiple harvest cycles, rather than being entered and exited frequently.
