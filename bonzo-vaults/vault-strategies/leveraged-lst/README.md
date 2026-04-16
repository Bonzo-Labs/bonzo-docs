---
icon: money-bill-trend-up
---

# Leveraged LST

The **Leveraged LST** vault strategy allows anyone to earn additional yield on their liquid staking token holdings (like **HBARX**) by depositing them into this vault strategy type.

Under the hood, **Leveraged LST** strategy vault operations include the following transactions and protocols:

1. User deposits liquid staking tokens (LSTs), such as HBARX, into the vault.
2. The vault routes and supplies this token (as collateral) to the **Bonzo Lend** protocol.
3. The vault borrows the LST's underlying base asset from **Bonzo Lend** (such as HBAR).
   1. With a low loan-to-value ratio, bolstering additional prevention of liquidation.
4. The vault stakes the borrowed funds (base asset) for more LSTs via a **staking provider** protocol.
5. The vault supplies those LSTs to the **Bonzo Lend** protocol.

During withdraw from a **Leveraged LST** strategy vault, the operations cited above are performed in reverse — however, instead of un-staking the LST for the underlying base asset, the LST is swapped, using **SaucerSwap**, to circumvent cool-down periods employed by liquid staking token providers.
