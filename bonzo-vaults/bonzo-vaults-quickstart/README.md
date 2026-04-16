# 🔒 Bonzo Vaults Quickstart

#### What are Bonzo Vaults?

**Bonzo Vaults** is an open source, non-custodial DeFi yield optimization protocol that helps both retail and institutional users earn more of the crypto-assets they hold, by automating the work of liquidity provision, reward harvesting, and compounding.

**Instead of manually:**

* Adding and removing liquidity across various DeFi protocols,
* Manually managing liquidity ranges and concentrations in SaucerSwap v2 pools, and
* Claiming rewards from multiple contracts and sources,

You deposit into a Bonzo Vault once — from there, a strategy contract continuously and automatically puts those assets to work, auto-compounding the resulting yield and rewards on your behalf.

**Under the hood, Bonzo uses a modular vault + strategy architecture:**

<table data-header-hidden><thead><tr><th width="210.71484375"></th><th></th></tr></thead><tbody><tr><td><strong>Vaults</strong></td><td><strong>H</strong>old user deposits, mint and burn vault share tokens, and provide a stable interface for deposits and withdrawals.</td></tr><tr><td><strong>Strategies</strong></td><td><strong>D</strong>ecides how those deposits are deployed: into liquidity pools, farms, concentrated liquidity positions, and other yield sources.</td></tr></tbody></table>
