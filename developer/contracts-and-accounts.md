---
description: >-
  A comprehensive overview of all deployed contracts for the Bonzo Finance
  protocol across Hedera Testnet and Mainnet environments.
---

# 📜 Contracts & Accounts

## Core Protocol Contracts

### Lending Pool Infrastructure

<table><thead><tr><th width="242">Contract Name</th><th width="269">Testnet Address</th><th>Mainnet Address</th></tr></thead><tbody><tr><td>LendingPoolAddressesProviderRegistry</td><td>0xA5B57E3d0205436Eb3bb7d0F49bf1C9E399110F8</td><td>0xE20273F10D1b85BaF56F6063cd5271C885427EC5</td></tr><tr><td>LendingPoolAddressesProvider</td><td>0x873575d4AeeBe015AcF3BB17AAa9DD248cc76D68</td><td>0x76b846DAB3646527bfb75952E1f33AfAA72B56D1</td></tr><tr><td>LendingPool</td><td>0xf67DBe9bD1B331cA379c44b5562EAa1CE831EbC2</td><td>0x236897c518996163E7b313aD21D1C9fCC7BA1afc</td></tr><tr><td>LendingPoolConfigurator</td><td>0x6Fa59558495a4D8B1701ab7924fc5a249d63cfF0</td><td>0xf41332220e51Ca8dB22De683fB0157e644e7A963</td></tr><tr><td>LendingPoolCollateralManager</td><td>0x35426e22F51165008fD594265b789C258f68D457</td><td>0x7687E1AaAD6cE335fb7d64ede7Dd7273De883698</td></tr></tbody></table>

### Oracle Contracts

| Contract Name     | Testnet Address                            | Mainnet Address                            |
| ----------------- | ------------------------------------------ | ------------------------------------------ |
| AaveOracle        | 0x9B940a1e60D652bCaf09C1d2224d1A4a544FDFb0 | 0xc0Bb4030b55093981700559a0B751DCf7Db03cBB |
| PriceOracle       | 0xF6e755380518589dE02f0F6BaA1D291C016992Cb | 0x9F1981afD19e2881A4Acb39aa144c7fBc4a6D8b3 |
| LendingRateOracle | 0xeC4a61EEb3d4015CCed52E51697347bf893931E7 | 0x2a9272C588c8b6C04757577d08285211C18232DD |

### Data Provider & Helper Contracts

| Contract Name            | Testnet Address                            | Mainnet Address                            |
| ------------------------ | ------------------------------------------ | ------------------------------------------ |
| AaveProtocolDataProvider | 0x121A2AFFA5f595175E60E01EAeF0deC43Cc3b024 | 0x78feDC4D7010E409A0c0c7aF964cc517D3dCde18 |
| WalletBalanceProvider    | 0xBB265cFA2Ccaa97260fAfd7303fCE751F3081d51 | 0xD64ffB431cF66fDEDB6f98Af07c63F49295b69e5 |
| WETHGateway              | 0x16197Ef10F26De77C9873d075f8774BdEc20A75d | 0x9a601543e9264255BebB20Cef0E7924e97127105 |

## Implementation Contracts

These are the underlying implementation contracts (proxy contracts) used by the protocol.

| Contract Name                    | Testnet Address                            | Mainnet Address                            |
| -------------------------------- | ------------------------------------------ | ------------------------------------------ |
| LendingPoolImpl                  | 0xC9beA74f6A2897c0C014Fe26e141c6518a2D2b8E | 0x5290b075d737606fccccA2f745D7337E0fCe633B |
| LendingPoolConfiguratorImpl      | 0xfa36F969AA5eFef29ADb2cf895c5B286a8eD72b1 | 0x650f70Ec874DAB7464FEAc9Ba55D07f3896721a6 |
| LendingPoolCollateralManagerImpl | 0x35426e22F51165008fD594265b789C258f68D457 | 0x7687E1AaAD6cE335fb7d64ede7Dd7273De883698 |

## Supported Mainnet Assets

### WHBAR

* Token: `0x0000000000000000000000000000000000163b5a`
* aToken: `0x6e96a607F2F5657b39bf58293d1A006f9415aF32`
* Variable Debt: `0xCD5A1FF3AD6EDd7e85ae6De3854f3915dD8c9103`

### HBARX

* Token: `0x00000000000000000000000000000000000cba44`
* aToken: `0x40EBC87627Fe4689567C47c8C9C84EDC4Cf29132`
* Variable Debt: `0xF4167Af5C303ec2aD1B96316fE013CA96Eb141B5`

### USDC

* Token: `0x000000000000000000000000000000000006f89a`
* aToken: `0xB7687538c7f4CAD022d5e97CC778d0b46457c5DB`
* Variable Debt: `0x8a90C2f80Fc266e204cb37387c69EA2ed42A3cc1`

### SAUCE

* Token: `0x00000000000000000000000000000000000b2ad5`
* aToken: `0x2bcC0a304c0bc816D501c7C647D958b9A5bc716d`
* Variable Debt: `0x736c5dbB8ADC643f04c1e13a9C25f28d3D4f0503`

### XSAUCE

* Token: `0x00000000000000000000000000000000001647e8`
* aToken: `0xEc9CEF1167b4673726B1e5f5A978150e63cDf23b`
* Variable Debt: `0x08c816eC7aC0580c802151E4efFbDa687f7Cac2a`

### KARATE

* Token: `0x000000000000000000000000000000000022d6de`
* aToken: `0x98262552C8246Ffb55E3539Ceb51838912402959`
* Variable Debt: `0xB6209F33982CE99139Ab325b13B260d32287A807`

### DOVU

* Token: `0x000000000000000000000000000000000038b3db`
* aToken: `0x89D2789481cB4CB5B6949Ff55EBA5629c5bC5B1E`
* Variable Debt: `0x9d81E1676A7e116ec725208DdeAB11929eA3F7A6`

### HST

* Token: `0x00000000000000000000000000000000000ec585`
* aToken: `0x2e63e864AAD2ce87b45d2C93bc126850DC5122c9`
* Variable Debt: `0xdc6e9E967648cd28E8BaF2EB1124ef7C9C5Bd027`

### PACK

* Token: `0x0000000000000000000000000000000000492a28`
* aToken: `0x5F98C43ce4b4765638d69B4a2407a2186A347CB9`
* Variable Debt: `0x63c7EF5398E8Fe23D95E762802F011590A7816a1`

### STEAM

* Token: `0x000000000000000000000000000000000030fb8b`
* aToken: `0x46BEf910150a3880ce6eAC60A059E70494A4805e`
* Variable Debt: `0xdFD1D43cbd700AEC5bcc151d028274412d31db70`

## Interest Rate Strategy Contracts

### Base Strategies

| Strategy Name  | Testnet Address                            | Mainnet Address                            |
| -------------- | ------------------------------------------ | ------------------------------------------ |
| Volatile One   | 0x82a278be934D9Ba2e4e46cad5d818647E2Ef0990 | 0x0eaD7dDfC2Bb172D4a899aad8E7b4d882067a001 |
| Volatile Two   | 0x58812c9430fc9C1e246E34a92a11ecea057DB049 | 0xDa47ecEC5ba98eF6a8C3c4F7EaDa3FBda6f7EED9 |
| Volatile Three | 0x5c5a27079728FCB66522760032e19cf5d94Fd823 | -                                          |

### Asset-Specific Strategies

<table><thead><tr><th width="167">Asset</th><th>Mainnet Address</th></tr></thead><tbody><tr><td>HBAR (wHBAR)</td><td>0x82C50aAfe0dc3f92e637EE05076d68180DB06d58</td></tr><tr><td>HBARX</td><td>0xA68FC75Acc8a731a1e5cc4CB717b162566d947A8</td></tr><tr><td>USDC</td><td>0x10753aD937e2f16daB73230fE5e5d8ace807C666</td></tr><tr><td>SAUCE</td><td>0xf38e204b948Db78Ca5D51cCEd7ccEe182Fe4bcA8</td></tr><tr><td>XSAUCE</td><td>0x998A60b83617F05c1Dcd4b3f5D37a2265d6a674D</td></tr><tr><td>KARATE</td><td>0x9bB33f2D511CA3089Fc5696BEe3ABee7174a556a</td></tr><tr><td>DOVU</td><td>0xC8C0c05683474a7B4c8DdaD69D0D546A841Be5D4</td></tr><tr><td>HST</td><td>0x6886E0eD3Cb5dcE6f8e50dCb692a142AE8a14775</td></tr><tr><td>PACK</td><td>0x4DF846F81135d9e63834AD4C7865F1C1983F767a</td></tr><tr><td>STEAM</td><td>0xA3E524FE431011dc6d050c32E92Acc38D2f50cB4</td></tr></tbody></table>

### HCS-20 Points

| Topic ID                                                     | Season            | Ticker ID |
| ------------------------------------------------------------ | ----------------- | --------- |
| [0.0.7159077](https://hashscan.io/mainnet/topic/0.0.7159077) | Pre-Season Points | BZPT      |
| [0.0.7159077](https://hashscan.io/mainnet/topic/0.0.7159077) | Season 1 Points   | BZ\_S1    |

## $BONZO Contracts & Accounts

Associated with the unlocking, distribution, and operations of the Bonzo Finance protocol's native $BONZO token.

### $BONZO Contracts

<table><thead><tr><th width="126.86810302734375">Allocation</th><th width="155.69091796875">Purpose</th><th width="140.041015625">Type</th><th width="182.5391845703125">Account / Contract ID</th><th width="128.62481689453125">Owner</th></tr></thead><tbody><tr><td>DAO Treasury</td><td>Treasury</td><td>Vesting Contract</td><td><a href="https://hashscan.io/mainnet/contract/0.0.8312259">0.0.8312259</a></td><td>Bonzo Foundation</td></tr><tr><td>Community</td><td>1st Edition NFT Claims</td><td>Distribution Contract</td><td><a href="https://hashscan.io/mainnet/contract/0.0.8317267">0.0.8317267</a></td><td>Bonzo Foundation</td></tr><tr><td>Community</td><td>Cybernetic NFT Claims</td><td>Distribution Contract</td><td><a href="https://hashscan.io/mainnet/contract/0.0.5725214">0.0.5725214</a><br></td><td>HeadStarter</td></tr><tr><td>Community</td><td>Pre-Season Points Claims</td><td>Distribution Contract</td><td><a href="https://hashscan.io/mainnet/contract/0.0.8317289">0.0.8317289</a></td><td>Bonzo Foundation</td></tr><tr><td>Community</td><td>Marketing Programs</td><td>Vesting Contract</td><td><a href="https://hashscan.io/mainnet/contract/0.0.8305740">0.0.8305740</a></td><td>Bonzo Foundation</td></tr><tr><td>Community</td><td>Liquidity &#x26; Staking Rewards</td><td>Vesting Contract(s)</td><td><a href="https://hashscan.io/mainnet/contract/0.0.8306863">0.0.8306863</a><br><a href="https://hashscan.io/mainnet/contract/0.0.8306542">0.0.8306542</a><br><a href="https://hashscan.io/mainnet/contract/0.0.8306744">0.0.8306744</a></td><td>Bonzo Foundation</td></tr><tr><td>Investor</td><td>Various</td><td>Vesting Contract</td><td><a href="https://hashscan.io/mainnet/contract/0.0.8329267">0.0.8329267</a></td><td>Bonzo Foundation</td></tr><tr><td>Core Development</td><td>Core Development</td><td>Vesting Contract</td><td><a href="https://hashscan.io/mainnet/contract/0.0.8305606">0.0.8305606</a></td><td>Bonzo Foundation</td></tr></tbody></table>

### $BONZO Accounts

<table><thead><tr><th width="141.40972900390625">Allocation</th><th width="165.75">Purpose</th><th width="144.0833740234375">Type</th><th width="165.9468994140625">Account / Contract ID</th><th width="120.31243896484375"></th></tr></thead><tbody><tr><td>Token Issuance Treasury</td><td>Treasury</td><td>Token Issuance Account</td><td><a href="https://hashscan.io/mainnet/account/0.0.8279084">0.0.8279084</a></td><td>Bonzo Reserve Ltd.</td></tr><tr><td>Foundation Treasury</td><td>Treasury</td><td>Holding Account</td><td><a href="https://hashscan.io/mainnet/account/0.0.8302193">0.0.8302193</a></td><td>Bonzo Foundation</td></tr><tr><td>DAO Treasury</td><td>Treasury</td><td>Holding Account</td><td><a href="https://hashscan.io/mainnet/account/0.0.8326196">0.0.8326196</a></td><td>Bonzo Foundation</td></tr><tr><td>Community</td><td>1st Edition NFT &#x26; Points Season(s)</td><td>Distribution Account</td><td><a href="https://hashscan.io/mainnet/account/0.0.8274461">0.0.8274461</a></td><td>Bonzo Foundation</td></tr><tr><td>Community</td><td>Cybernetic NFT</td><td>Distribution Account</td><td><a href="https://hashscan.io/mainnet/account/0.0.8274461">0.0.5725188</a></td><td>HeadStarter</td></tr><tr><td>Community</td><td>Marketing Programs</td><td>Operational Account</td><td><a href="https://hashscan.io/mainnet/account/0.0.7285744">0.0.7285744</a></td><td>Bonzo Foundation</td></tr><tr><td>Community</td><td>Liquidity &#x26; Staking Rewards</td><td>Operational Account(s)</td><td><a href="https://hashscan.io/mainnet/account/0.0.8326242?ph=1&#x26;ps=1&#x26;pt=1&#x26;pn=1&#x26;pc=1&#x26;pr=1&#x26;pa=1&#x26;pf=1">0.0.8326242</a><br><a href="https://hashscan.io/mainnet/account/0.0.8326207">0.0.8326207</a><br><a href="https://hashscan.io/mainnet/account/0.0.8326258">0.0.8326258</a></td><td>Bonzo Foundation</td></tr></tbody></table>
