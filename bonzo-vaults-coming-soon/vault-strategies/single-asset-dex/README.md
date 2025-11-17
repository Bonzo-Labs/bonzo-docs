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

### Single Asset DEX Strategies

<table data-card-size="large" data-view="cards"><thead><tr><th></th></tr></thead><tbody><tr><td><h3>Low Volatility | Ultra-Tight</h3><div data-gb-custom-block data-tag="hint" data-style="info" class="hint hint-info"><p>Stable pairs. Ultra-tight positioning maximizes capital efficiency. Minimal impermanent loss risk.</p></div><p><strong>Volatility</strong><br><strong>🟢</strong> Low</p><p><br><strong>Liquidity Concentration</strong><br>0.01% - 0.3% (Ultra-Tight Range)<br><br><strong>Best For</strong><br>Stablecoin Asset with Stablecoin</p><p><br><strong>Examples</strong><br><kbd>USDC</kbd>/<kbd>USDC</kbd> , <kbd>USDC</kbd>/<kbd>DAI</kbd></p></td></tr><tr><td><h3>Medium Volatility | Narrow</h3><div data-gb-custom-block data-tag="hint" data-style="info" class="hint hint-info"><p>LST and base asset pairs. Narrow range balances fees with low rebalancing. Conservative approach.</p></div><p><strong>Volatility</strong><br>🟡 🟡 Medium</p><p><br><strong>Liquidity Concentration</strong><br>0.3% - 5% (Narrow Range)<br><br><strong>Best For</strong><br>Liquid Staking Asset with Base Asset<br><br><strong>Examples</strong><br><kbd>BONZO</kbd>/<kbd>XBONZO</kbd>, <kbd>HBAR</kbd>/<kbd>HBARX</kbd></p></td></tr><tr><td><h3>High Volatility | Medium</h3><div data-gb-custom-block data-tag="hint" data-style="info" class="hint hint-info"><p>Volatile uncorrelated pairs. Tighter positioning for aggressive fee capture. Requires more active management.</p></div><p><strong>Volatility</strong><br>🟠 🟠 🟠  High</p><p></p><p><strong>Liquidity Concentration</strong><br>10-30% (Medium Range)<br><br><strong>Best For</strong><br>Volatile Asset with Uncorrelated Volatile Asset<br><br><strong>Examples</strong><br><kbd>HBAR</kbd>/<kbd>SAUCE</kbd>, <kbd>HBAR</kbd>/<kbd>WETH</kbd></p></td></tr><tr><td><h3>High Volatility | Wide</h3><div data-gb-custom-block data-tag="hint" data-style="info" class="hint hint-info"><p>Volatile uncorrelated assets paired with a stablecoin. Wide range protects asset inventory during extreme price swings.</p></div><p><strong>Volatility</strong><br>🟠 🟠 🟠  High</p><p></p><p><strong>Liquidity Concentration</strong><br>30%+ (Wide Range)</p><p></p><p><strong>Best For</strong><br>Volatile Asset with Stablecoin<br><br><strong>Examples</strong><br><kbd>USDC</kbd>/<kbd>wETH</kbd>, <kbd>USDC</kbd>/<kbd>HBAR</kbd></p></td></tr></tbody></table>

### Single Asset DEX Strategy Vaults

Once Bonzo Vaults is live, vaults utilizing Single Asset DEX strategy will be displayed with a link to their individual page in the tables below.

#### Low Volatility | Ultra-Tight Range

<table><thead><tr><th width="140.66015625">Primary Asset</th><th width="132.2265625">Paired With</th><th width="148.31640625">Volatility</th><th width="184.98046875">Concentration Range</th><th>Vault URL</th></tr></thead><tbody><tr><td>-</td><td>-</td><td>-</td><td>-</td><td>-</td></tr></tbody></table>

#### Medium Volatility | Narrow Range

<table><thead><tr><th width="140.66015625">Primary Asset</th><th width="132.2265625">Paired With</th><th width="148.31640625">Volatility</th><th width="184.98046875">Concentration Range</th><th>Vault URL</th></tr></thead><tbody><tr><td>HBAR</td><td>hbarx</td><td>Medium</td><td>Narrow</td><td>-</td></tr><tr><td>HBARX</td><td>hbar</td><td>Medium</td><td>Narrow</td><td>-</td></tr><tr><td>SAUCE</td><td>xsauce</td><td>Medium</td><td>Narrow</td><td>-</td></tr><tr><td>XSAUCE</td><td>sauce</td><td>Medium</td><td>Narrow</td><td>-</td></tr><tr><td>BONZO</td><td>xbonzo</td><td>Medium</td><td>Narrow</td><td>-</td></tr><tr><td>XBONZO</td><td>bonzo</td><td>Medium</td><td>Narrow</td><td>-</td></tr><tr><td>PACK</td><td>xpack</td><td>Medium</td><td>Narrow</td><td>-</td></tr><tr><td>XPACK</td><td>pack</td><td>Medium</td><td>Narrow</td><td>-</td></tr></tbody></table>

#### High Volatility | Medium Range

<table><thead><tr><th width="140.66015625">Primary Asset</th><th width="132.2265625">Paired With</th><th width="148.31640625">Volatility</th><th width="184.98046875">Concentration Range</th><th>Vault URL</th></tr></thead><tbody><tr><td>HBAR</td><td>weth</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>HBAR</td><td>wbtc</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>HBAR</td><td>sauce</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>HBAR</td><td>bonzo</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>HBAR</td><td>pack</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>HBAR</td><td>jam</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>HBAR</td><td>gib</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>WETH</td><td>hbar</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>WBTC</td><td>hbar</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>SAUCE</td><td>hbar</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>BONZO</td><td>hbar</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>PACK</td><td>hbar</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>DOVU</td><td>hbar</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>JAM</td><td>hbar</td><td>High</td><td>Medium</td><td>-</td></tr><tr><td>GIB</td><td>hbar</td><td>High</td><td>Medium</td><td>-</td></tr></tbody></table>

#### High Volatility | Wide Range

<table><thead><tr><th width="140.66015625">Primary Asset</th><th width="132.2265625">Paired Asset</th><th width="148.31640625">Volatility</th><th width="184.98046875">Concentration Range</th><th>Vault URL</th></tr></thead><tbody><tr><td>USDC</td><td>wbtc</td><td>High</td><td>Wide</td><td>-</td></tr><tr><td>USDC</td><td>hbar</td><td>High</td><td>Wide</td><td>-</td></tr><tr><td>USDC</td><td>weth</td><td>High</td><td>Wide</td><td>-</td></tr><tr><td>USDC</td><td>bonzo</td><td>High</td><td>Wide</td><td>-</td></tr><tr><td>HBAR</td><td>usdc</td><td>High</td><td>Wide</td><td>-</td></tr><tr><td>WETH</td><td>usdc</td><td>High</td><td>Wide</td><td>-</td></tr><tr><td>WBTC</td><td>usdc</td><td>High</td><td>Wide</td><td>-</td></tr></tbody></table>
