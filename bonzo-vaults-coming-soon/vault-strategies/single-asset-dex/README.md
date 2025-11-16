---
icon: coin
---

# Single Asset DEX

The Single Asset DEX vault strategy allows for single-sided liquidity deposit with a range of automated strategies that rebalance and manage impermanent loss exposure. Each strategy is pre-configured based on pair characteristics — users simply deposit and the strategy handles the rest.

### Single Asset DEX Strategy Comparison

<table data-card-size="large" data-view="cards"><thead><tr><th></th></tr></thead><tbody><tr><td><h3>Low Volatility | Ultra-Tight</h3><p>Stable pairs. Ultra-tight positioning maximizes capital efficiency. Minimal impermanent loss risk.<br></p><p><strong>Volatility</strong><br><strong>🟢</strong> Low</p><p><br><strong>Liquidity Concentration</strong><br>0.01% - 0.3% (Ultra-Tight Range)<br><br><strong>Best For</strong><br>Stablecoin Asset with Stablecoin</p><p><br><strong>Examples</strong><br><kbd>USDC</kbd>/<kbd>USDC</kbd> , <kbd>USDC</kbd>/<kbd>DAI</kbd></p></td></tr><tr><td><h3>Medium Volatility | Narrow</h3><p>LST and base asset pairs. Narrow range balances fees with low rebalancing. Conservative approach.</p><p></p><p><strong>Volatility</strong><br>🟡 🟡 Medium</p><p><br><strong>Liquidity Concentration</strong><br>0.3% - 5% (Narrow Range)<br><br><strong>Best For</strong><br>Liquid Staking Asset with Base Asset<br><br><strong>Examples</strong><br><kbd>BONZO</kbd>/<kbd>XBONZO</kbd>, <kbd>HBAR</kbd>/<kbd>HBARX</kbd></p></td></tr><tr><td><h3>High Volatility | Medium</h3><p>Volatile uncorrelated pairs. Tighter positioning for aggressive fee capture. More active management.<br><br><strong>Volatility</strong><br>🟠 🟠 🟠  High</p><p><br><strong>Liquidity Concentration</strong><br>10-30% (Medium Range)<br><br><strong>Best For</strong><br>Volatile Asset with Uncorrelated Volatile Asset<br><br><strong>Examples</strong><br><kbd>HBAR</kbd>/<kbd>SAUCE</kbd>, <kbd>HBAR</kbd>/<kbd>WETH</kbd></p></td></tr><tr><td><h3>High Volatility | Wide</h3><p>Volatile uncorrelated assets paired with a stablecoin. Wide range protects asset inventory during extreme price swings.<br><br><strong>Volatility</strong><br>🟠 🟠 🟠  High</p><p><br><strong>Liquidity Concentration</strong><br>30%+ (Wide Range)</p><p></p><p><strong>Best For</strong><br>Volatile Asset with Stablecoin<br><br><strong>Examples</strong><br><kbd>USDC</kbd>/<kbd>wETH</kbd>, <kbd>USDC</kbd>/<kbd>HBAR</kbd></p></td></tr></tbody></table>

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
