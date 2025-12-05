---
icon: file-signature
---

# Vaults Contracts

{% hint style="success" %}
When Bonzo Vaults officially launches, all contracts deployed on the Hedera mainnet will be made available for review, with links on HashScan.
{% endhint %}

{% tabs %}
{% tab title="Bonzo Vaults Core" %}
### Bonzo Vaults Core Protocol Contracts

<details>

<summary><strong>Beefy Finance</strong> — Dual Asset DEX &#x26; Leveraged LST</summary>

### **Deployment Addresses**

<table><thead><tr><th width="199.796875">Contract Name</th><th>EVM Address</th></tr></thead><tbody><tr><td>Deployer</td><td></td></tr><tr><td>Keeper</td><td></td></tr><tr><td>Strategist</td><td></td></tr><tr><td>Bonzo Fee Recipient</td><td></td></tr><tr><td>Upgrader</td><td></td></tr><tr><td>Harvester</td><td></td></tr><tr><td>MoveTicks</td><td></td></tr></tbody></table>

### **Infrastructure Contracts**

<table><thead><tr><th width="244.453125">Contract Name</th><th>EVM Address</th></tr></thead><tbody><tr><td>vaultFactory</td><td></td></tr><tr><td>vaultV7</td><td></td></tr><tr><td>vaultV7MultiToken</td><td></td></tr><tr><td>beefySwapper</td><td></td></tr><tr><td>beefyOracle</td><td></td></tr><tr><td>keeper</td><td></td></tr><tr><td>devMultisig</td><td></td></tr><tr><td>treasuryMultisig</td><td></td></tr><tr><td>strategyOwner</td><td></td></tr><tr><td>vaultOwner</td><td></td></tr><tr><td>treasurer</td><td></td></tr><tr><td>launchpoolOwner</td><td></td></tr><tr><td>rewardPool</td><td></td></tr><tr><td>treasury</td><td></td></tr><tr><td>beefyFeeRecipient</td><td></td></tr><tr><td>multicall</td><td></td></tr><tr><td>bifiMaxiStrategy</td><td></td></tr><tr><td>voter</td><td></td></tr><tr><td>beefyFeeConfig</td><td></td></tr><tr><td>wrapperFactory</td><td></td></tr><tr><td>zap</td><td></td></tr><tr><td>zapTokenManager</td><td></td></tr><tr><td>treasurySwapper</td><td></td></tr><tr><td>clmFactory</td><td></td></tr><tr><td>clmStrategyFactory</td><td></td></tr><tr><td>clmRewardPoolFactory</td><td></td></tr><tr><td>positionMulticall</td><td></td></tr><tr><td>clmVault</td><td></td></tr><tr><td>beefyOracleChainlink</td><td></td></tr><tr><td>beefyOracleUniswapV2</td><td></td></tr><tr><td>beefyOracleUniswapV3</td><td></td></tr></tbody></table>

### Chainlink Oracles

<table><thead><tr><th width="186.171875">Contract Name</th><th>EVM Address</th></tr></thead><tbody><tr><td>Deployer</td><td></td></tr><tr><td>Keeper</td><td></td></tr><tr><td><p>BeefyOracleChainlink</p><p>(Deployed To)</p></td><td></td></tr><tr><td>BeefyOracle <br>(Owner)</td><td></td></tr><tr><td>Oracle <br>(Set For wHBAR)</td><td>Address: 0x0000000000000000000000000000000000163b5a<br>Txn: </td></tr><tr><td>Oracle <br>(Set For USDC)</td><td><p>Address: 0x000000000000000000000000000000000006f89a</p><p>Txn:</p></td></tr></tbody></table>

</details>

<details>

<summary><strong>ICHI</strong> — Single Asset DEX</summary>

### **Deployment Addresses**

<table><thead><tr><th width="195.48828125">Contract Name</th><th>EVM Contract</th></tr></thead><tbody><tr><td>ICHIVaultFactory</td><td>0x822b0bE4958ab5b4A48DA3c5f68Fc54846093618</td></tr><tr><td>ICHIVaultDeployer lib</td><td>0x4fA116f8864eE7d7cee1F5Fbb58d41b70d75A529</td></tr><tr><td>UV3Math lib</td><td>0x51aD1f2A691F0de1a28942C6d2870bBA05D1c8f7</td></tr><tr><td>Deposit Guard</td><td>0x84e653E209525f70dC1410a304dFF98fE47CfD4a</td></tr><tr><td>VaultSlippageCheckV2</td><td>0xce878019645439E64B0e375fE73DDD3d532CC819</td></tr><tr><td>Gnosis</td><td>0xC159b19C5bd0E4a0709eC13C1303Ff2Bb67F7145</td></tr><tr><td>Pool Factory</td><td>0x00000000000000000000000000000000003c3951</td></tr><tr><td>VolatilityCheck</td><td>0x1596BF18141b2Cd07BF6F7875975222C5B092064</td></tr></tbody></table>

</details>
{% endtab %}

{% tab title="Single Asset DEX" %}
### **Single Asset DEX Vaults**

<table><thead><tr><th width="158.734375">Vault Name</th><th width="267.578125">Strategy EVM Address</th><th>Vault EVM Address</th></tr></thead><tbody><tr><td><strong>JAM</strong><br><sub>(Paired with <strong>HBAR</strong>)</sub></td><td>0x7AbF45908d733a60799d1B4B04E373366770EEcC</td><td>0x26C770f89d320Da2c2341cbf410F132f44eF70CD</td></tr><tr><td><strong>HBAR</strong><br><sub>(Paired with <strong>JAM</strong>)</sub></td><td>0x1787Cd1DFAd83e85c2D4713F7032521592FA807B</td><td>0x55958da8d5aC662aa8eD45111f170C3D8e4fCB3b</td></tr><tr><td><strong>PACK</strong><br><sub>(Paired with <strong>HBAR</strong>)</sub></td><td>0x3cE3A64669d1E3ab4789235Fc3e019234C4be9B7</td><td>0xACd982eE8b869f11aa928c4760cC3C0D4f30a6d3</td></tr><tr><td><strong>HBAR</strong><br><sub>(Paired with <strong>PACK</strong>)</sub></td><td>0xC260c60b3e974F54A73c0a6F540ee5eC979fDc00</td><td>0xd1893FcFB1dbEbCCAa6813993074fEfb1569FA5F</td></tr><tr><td><strong>BONZO</strong><br><sub>(Paired with <strong>HBAR</strong>)</sub></td><td>0xC2343277CAE1090052c770dEf66Cb5911fAF4f05</td><td>0x5D1e9BCAe2c171c0C8aF697Bdd02908f280716bc</td></tr><tr><td><strong>USDC</strong><br><sub>(Paired with <strong>HBAR</strong>)</sub></td><td>0x5dAE71d8a6F980f88F6586dF1A528E53456b8C97</td><td>0x1b90B8f8ab3059cf40924338D5292FfbAEd79089</td></tr><tr><td><strong>HBAR</strong><br><sub>(Paired with <strong>USDC</strong>)</sub></td><td>0xB8021f6a7BE89DFd0F66B89CE4cae76De33A90A2</td><td>0xebaFaBBD6610304d7ae89351C5C37b8cf40c76eB</td></tr><tr><td><strong>DOVU</strong><br><sub>(Paired with <strong>HBAR</strong>)</sub></td><td>0xA1ffF8A98edb1c314cf6a64b47b842A2954304a1</td><td>0x072bC950618A4e286683886eBc01C73090BC1C8a</td></tr><tr><td><strong>HBAR</strong><br><sub>(Paired with <strong>DOVU</strong>)</sub></td><td>0xDAd5F1F4094451Ffd8DDD65dD48A99e7E277FbC9</td><td>0xEf55ABc71271dceaE4880b9000402a4b3F87D1eA</td></tr><tr><td><strong>SAUCE</strong><br><sub>(Paired with <strong>HBAR</strong>)</sub></td><td>0x5241E22Feb810C50F32Bf16a0edD4105E47Be165</td><td>0x8e253F359Ba5DDD62644b1e5DAbD3D7748fb8193</td></tr><tr><td><strong>HBAR</strong><br><sub>(Paired with SAUCE)</sub></td><td>0x9271898ceF0d44d1704245C2232D56C05150cdAf</td><td>0xc883F70804380c1a49E23A6d1DCF8e784D093a3f</td></tr><tr><td><strong>HBAR</strong><br><sub>(Paired with BONZO)</sub></td><td>0x4e1bc1184Df76e897BA5eaD761f75B01F6197726</td><td>0xd406F0C0211836dbcA3EbF3b84487137be400E57</td></tr><tr><td><strong>USDC</strong><br><sub>(Paired with <strong>wETH</strong>)</sub></td><td>0xb9A69E0261f67Da41FccBEF8511b99E2D8255806</td><td>0x0Db93Cfe4BA0b2A7C10C83FBEe81Fd2EFB871864</td></tr><tr><td><strong>wETH</strong><br><sub>(Paired with <strong>USDC</strong>)</sub></td><td>0x0084260A5f7BF324b2325487D3EF080f298057b9</td><td>0x31403d085C601F49b9644a4c9a493403FA14ABfe</td></tr><tr><td><strong>HBAR</strong><br><sub>(Paired with <strong>wBTC</strong>)</sub></td><td>0x0084260A5f7BF324b2325487D3EF080f298057b10</td><td>0x31403d085C601F49b9644a4c9a493403FA14ABfe</td></tr><tr><td><strong>wBTC</strong><br><sub>(Paired with <strong>HBAR</strong>)</sub></td><td>0x0084260A5f7BF324b2325487D3EF080f298057b11</td><td>0x31403d085C601F49b9644a4c9a493403FA14ABfe</td></tr><tr><td><strong>HBAR</strong><br><sub>(Paired with <strong>wETH</strong>)</sub></td><td>0x0084260A5f7BF324b2325487D3EF080f298057b12</td><td>0x31403d085C601F49b9644a4c9a493403FA14ABfe</td></tr><tr><td><strong>wETH</strong><br><sub>(Paired with <strong>HBAR</strong>)</sub></td><td>0x0084260A5f7BF324b2325487D3EF080f298057b13</td><td>0x31403d085C601F49b9644a4c9a493403FA14ABfe</td></tr><tr><td><strong>USDC</strong><br><sub>(Paired with <strong>wBTC</strong>)</sub></td><td>0x0084260A5f7BF324b2325487D3EF080f298057b14</td><td>0x31403d085C601F49b9644a4c9a493403FA14ABfe</td></tr><tr><td><strong>wBTC</strong><br><sub>(Paired with <strong>USDC</strong>)</sub></td><td>0x0084260A5f7BF324b2325487D3EF080f298057b15</td><td>0x31403d085C601F49b9644a4c9a493403FA14ABfe</td></tr></tbody></table>
{% endtab %}

{% tab title="Dual Asset DEX" %}
### **Dual Asset DEX Vaults**

<details>

<summary>USDC-HBAR</summary>



<table><thead><tr><th width="226.73828125">Contract Name</th><th>EVM Address</th></tr></thead><tbody><tr><td>strategyProxy</td><td></td></tr><tr><td>strategyImplementation</td><td></td></tr><tr><td>proxyAdmin</td><td></td></tr><tr><td>vault</td><td></td></tr><tr><td>clmLibrary</td><td></td></tr><tr><td>lariLibrary</td><td></td></tr><tr><td>pool</td><td>0xc5b707348da504e9be1bd4e21525459830e7b11d</td></tr><tr><td>token0</td><td>0x000000000000000000000000000000000006f89a</td></tr><tr><td>token1</td><td>0x0000000000000000000000000000000000163b5a</td></tr><tr><td>positionWidth</td><td></td></tr><tr><td>maxTickDeviation</td><td></td></tr><tr><td>twapInterval</td><td>300</td></tr><tr><td>rewardTokens</td><td>0x0000000000000000000000000000000000163b5a<br>0x00000000000000000000000000000000000b2ad5<br>0x0000000000000000000000000000000000492a28</td></tr><tr><td>deployer</td><td></td></tr><tr><td>deploymentTime</td><td></td></tr><tr><td>chainType</td><td>mainnet</td></tr><tr><td>isUpgradeable</td><td>True</td></tr><tr><td>managedBy</td><td>hardhat-upgrades</td></tr></tbody></table>

</details>

<details>

<summary>USDC-SAUCE</summary>



<table><thead><tr><th width="226.73828125">Contract Name</th><th>EVM Address</th></tr></thead><tbody><tr><td>strategyProxy</td><td></td></tr><tr><td>strategyImplementation</td><td></td></tr><tr><td>proxyAdmin</td><td></td></tr><tr><td>vault</td><td></td></tr><tr><td>clmLibrary</td><td></td></tr><tr><td>lariLibrary</td><td></td></tr><tr><td>pool</td><td>0x36acdfe1cbf9098bdb7a3c62b8eaa1016c111e31</td></tr><tr><td>token0</td><td>0x000000000000000000000000000000000006f89a</td></tr><tr><td>token1</td><td>0x00000000000000000000000000000000000b2ad5</td></tr><tr><td>positionWidth</td><td></td></tr><tr><td>maxTickDeviation</td><td></td></tr><tr><td>twapInterval</td><td>300</td></tr><tr><td>rewardTokens</td><td>0x0000000000000000000000000000000000163b5a<br>0x00000000000000000000000000000000000b2ad5<br>0x0000000000000000000000000000000000492a28</td></tr><tr><td>deployer</td><td></td></tr><tr><td>deploymentTime</td><td></td></tr><tr><td>chainType</td><td>mainnet</td></tr><tr><td>isUpgradeable</td><td>True</td></tr><tr><td>managedBy</td><td>hardhat-upgrades</td></tr></tbody></table>

</details>

<details>

<summary>BONZO-XBONZO</summary>



<table><thead><tr><th width="226.73828125">Contract Name</th><th>EVM Address</th></tr></thead><tbody><tr><td>strategyProxy</td><td></td></tr><tr><td>strategyImplementation</td><td></td></tr><tr><td>proxyAdmin</td><td></td></tr><tr><td>vault</td><td></td></tr><tr><td>clmLibrary</td><td></td></tr><tr><td>lariLibrary</td><td></td></tr><tr><td>pool</td><td>0xf6cc94f16bc141115fcb9b587297aecfa14f4eb6</td></tr><tr><td>token0</td><td>0x00000000000000000000000000000000007e545e</td></tr><tr><td>token1</td><td>0x0000000000000000000000000000000000818e2d</td></tr><tr><td>positionWidth</td><td></td></tr><tr><td>maxTickDeviation</td><td></td></tr><tr><td>twapInterval</td><td>300</td></tr><tr><td>rewardTokens</td><td>0x0000000000000000000000000000000000163b5a<br>0x00000000000000000000000000000000000b2ad5<br>0x0000000000000000000000000000000000492a28</td></tr><tr><td>deployer</td><td></td></tr><tr><td>deploymentTime</td><td></td></tr><tr><td>chainType</td><td>mainnet</td></tr><tr><td>isUpgradeable</td><td>True</td></tr><tr><td>managedBy</td><td>hardhat-upgrades</td></tr></tbody></table>

</details>

<details>

<summary>SAUCE-XSAUCE</summary>



<table><thead><tr><th width="226.73828125">Contract Name</th><th>EVM Address</th></tr></thead><tbody><tr><td>strategyProxy</td><td></td></tr><tr><td>strategyImplementation</td><td></td></tr><tr><td>proxyAdmin</td><td></td></tr><tr><td>vault</td><td></td></tr><tr><td>clmLibrary</td><td></td></tr><tr><td>lariLibrary</td><td></td></tr><tr><td>pool</td><td>0xcfeffaae43f176f91602d75ec1d0637e273c973b</td></tr><tr><td>token0</td><td>0x00000000000000000000000000000000000b2ad5</td></tr><tr><td>token1</td><td>0x00000000000000000000000000000000001647e8</td></tr><tr><td>positionWidth</td><td></td></tr><tr><td>maxTickDeviation</td><td></td></tr><tr><td>twapInterval</td><td>300</td></tr><tr><td>rewardTokens</td><td>0x0000000000000000000000000000000000163b5a<br>0x00000000000000000000000000000000000b2ad5<br>0x0000000000000000000000000000000000492a28</td></tr><tr><td>deployer</td><td></td></tr><tr><td>deploymentTime</td><td></td></tr><tr><td>chainType</td><td>mainnet</td></tr><tr><td>isUpgradeable</td><td>True</td></tr><tr><td>managedBy</td><td>hardhat-upgrades</td></tr></tbody></table>

</details>
{% endtab %}

{% tab title="Leveraged LST" %}
### **Leveraged Liquid Staking Token (LST) Vaults**

<details>

<summary><strong>HBARX</strong></summary>



<table><thead><tr><th width="192.1796875">Contract Name</th><th>EVM Address</th></tr></thead><tbody><tr><td>strategyProxy</td><td></td></tr><tr><td>strategyImplementation</td><td></td></tr><tr><td>proxyAdmin</td><td></td></tr><tr><td>vault</td><td></td></tr><tr><td>want</td><td>0x00000000000000000000000000000000000cba44</td></tr><tr><td>borrowToken</td><td>0x0000000000000000000000000000000000163b5a</td></tr><tr><td>aToken</td><td>0x40EBC87627Fe4689567C47c8C9C84EDC4Cf29132</td></tr><tr><td>debtToken</td><td>0xCD5A1FF3AD6EDd7e85ae6De3854f3915dD8c9103</td></tr><tr><td>lendingPool</td><td>0x236897c518996163E7b313aD21D1C9fCC7BA1afc</td></tr><tr><td>rewardsController</td><td>0x0f3950d2fCbf62a2D79880E4fc251E4CB6625FBC</td></tr><tr><td>stakingContract</td><td>0x0000000000000000000000000000000000158d97</td></tr><tr><td>unirouter</td><td>0x00000000000000000000000000000000003c437a</td></tr><tr><td>whbarGateway</td><td>0xa7e46f496b088A8f8ee35B74D7E58d6Ce648Ae64</td></tr><tr><td>maxBorrowable</td><td>3000</td></tr><tr><td>slippageTolerance</td><td>50</td></tr><tr><td>isRewardsAvailable</td><td>false</td></tr><tr><td>isBonzoDeployer</td><td>false</td></tr><tr><td>vaultName</td><td>HBARX LST VAULT</td></tr><tr><td>vaultSymbol</td><td>bvHBARX-LEV-BONZO</td></tr><tr><td>deployer</td><td></td></tr><tr><td>deploymentTime</td><td></td></tr><tr><td>chainType</td><td>mainnet</td></tr><tr><td>isUpgradeable</td><td>true</td></tr><tr><td>managedBy</td><td>hardhat-upgrades</td></tr></tbody></table>

</details>
{% endtab %}
{% endtabs %}
