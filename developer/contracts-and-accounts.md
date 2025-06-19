---
description: >-
  A comprehensive overview of all deployed contracts for the Bonzo Finance
  protocol across Hedera Testnet and Mainnet environments.
---

# 📜 Protocol Contracts

## Core Protocol Contracts

### Lending Pool Infrastructure

<table><thead><tr><th width="242">Contract Name</th><th width="269">Testnet Address</th><th>Mainnet Address</th></tr></thead><tbody><tr><td>LendingPoolAddressesProviderRegistry</td><td><a href="https://hashscan.io/testnet/contract/0.0.4999344">0xA5B57E3d0205436Eb3bb7d0F49bf1C9E399110F8</a></td><td><a href="https://hashscan.io/mainnet/contract/0.0.7308449">0xE20273F10D1b85BaF56F6063cd5271C885427EC5</a></td></tr><tr><td>LendingPoolAddressesProvider</td><td><a href="https://hashscan.io/testnet/contract/0.0.4999346">0x873575d4AeeBe015AcF3BB17AAa9DD248cc76D68</a></td><td><a href="https://hashscan.io/mainnet/contract/0.0.7308451">0x76b846DAB3646527bfb75952E1f33AfAA72B56D1</a></td></tr><tr><td>LendingPool</td><td><a href="https://hashscan.io/testnet/contract/0.0.4999355">0xf67DBe9bD1B331cA379c44b5562EAa1CE831EbC2</a></td><td><a href="https://hashscan.io/mainnet/contract/0.0.7308459">0x236897c518996163E7b313aD21D1C9fCC7BA1afc</a></td></tr><tr><td>LendingPoolConfigurator</td><td><a href="https://hashscan.io/testnet/contract/0.0.4999359">0x6Fa59558495a4D8B1701ab7924fc5a249d63cfF0</a></td><td><a href="https://hashscan.io/mainnet/contract/0.0.7308462">0xf41332220e51Ca8dB22De683fB0157e644e7A963</a></td></tr><tr><td>LendingPoolCollateralManager</td><td><a href="https://hashscan.io/testnet/contract/0.0.4999415">0x35426e22F51165008fD594265b789C258f68D457</a></td><td><a href="https://hashscan.io/mainnet/contract/0.0.7308529">0x7687E1AaAD6cE335fb7d64ede7Dd7273De883698</a></td></tr></tbody></table>

### Oracle Contracts

| Contract Name     | Testnet Address                                                                                | Mainnet Address                                                                                |
| ----------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| AaveOracle        | [0x9B940a1e60D652bCaf09C1d2224d1A4a544FDFb0](https://hashscan.io/testnet/contract/0.0.4999377) | [0xc0Bb4030b55093981700559a0B751DCf7Db03cBB](https://hashscan.io/mainnet/contract/0.0.7308480) |
| PriceOracle       | [0xF6e755380518589dE02f0F6BaA1D291C016992Cb](https://hashscan.io/testnet/contract/0.0.4999375) | [0x9F1981afD19e2881A4Acb39aa144c7fBc4a6D8b3](https://hashscan.io/mainnet/contract/0.0.7308479) |
| LendingRateOracle | [0xeC4a61EEb3d4015CCed52E51697347bf893931E7](https://hashscan.io/testnet/contract/0.0.4999378) | [0x2a9272C588c8b6C04757577d08285211C18232DD](https://hashscan.io/mainnet/contract/0.0.7308481) |

### Data Provider & Helper Contracts

| Contract Name            | Testnet Address                                                                                | Mainnet Address                                                                                |
| ------------------------ | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| AaveProtocolDataProvider | [0x121A2AFFA5f595175E60E01EAeF0deC43Cc3b024](https://hashscan.io/testnet/contract/0.0.4999382) | [0x78feDC4D7010E409A0c0c7aF964cc517D3dCde18](https://hashscan.io/mainnet/contract/0.0.7308483) |
| WalletBalanceProvider    | [0xBB265cFA2Ccaa97260fAfd7303fCE751F3081d51](https://hashscan.io/testnet/contract/0.0.4999416) | [0xD64ffB431cF66fDEDB6f98Af07c63F49295b69e5](https://hashscan.io/mainnet/contract/0.0.7308530) |
| WETHGateway              | [0x16197Ef10F26De77C9873d075f8774BdEc20A75d](https://hashscan.io/testnet/contract/0.0.4999384) | [0x9a601543e9264255BebB20Cef0E7924e97127105](https://hashscan.io/mainnet/contract/0.0.7308485) |

## Implementation Contracts

These are the underlying implementation contracts (proxy contracts) used by the protocol.

| Contract Name                    | Testnet Address                                                                                | Mainnet Address                                                                                |
| -------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| LendingPoolImpl                  | [0xC9beA74f6A2897c0C014Fe26e141c6518a2D2b8E](https://hashscan.io/testnet/contract/0.0.4999354) | [0x5290b075d737606fccccA2f745D7337E0fCe633B](https://hashscan.io/mainnet/contract/0.0.7308458) |
| LendingPoolConfiguratorImpl      | [0xfa36F969AA5eFef29ADb2cf895c5B286a8eD72b1](https://hashscan.io/testnet/contract/0.0.4999357) | [0x650f70Ec874DAB7464FEAc9Ba55D07f3896721a6](https://hashscan.io/mainnet/contract/0.0.7308461) |
| LendingPoolCollateralManagerImpl | [0x35426e22F51165008fD594265b789C258f68D457](https://hashscan.io/testnet/account/0.0.4999415)  | [0x7687E1AaAD6cE335fb7d64ede7Dd7273De883698](https://hashscan.io/mainnet/contract/0.0.7308529) |

## Supported Mainnet Assets

### WHBAR

* Token: [`0x0000000000000000000000000000000000163b5a`](https://hashscan.io/mainnet/token/0.0.1456986)&#x20;
* aToken: [`0x6e96a607F2F5657b39bf58293d1A006f9415aF32`](https://hashscan.io/mainnet/contract/0.0.7308509)&#x20;
* Variable Debt: [`0xCD5A1FF3AD6EDd7e85ae6De3854f3915dD8c9103`](https://hashscan.io/mainnet/contract/0.0.7308511)&#x20;

### HBARX

* Token: [`0x00000000000000000000000000000000000cba44`](https://hashscan.io/mainnet/token/0.0.834116)&#x20;
* aToken: [`0x40EBC87627Fe4689567C47c8C9C84EDC4Cf29132`](https://hashscan.io/mainnet/contract/0.0.7308502)&#x20;
* Variable Debt: [`0xF4167Af5C303ec2aD1B96316fE013CA96Eb141B5`](https://hashscan.io/mainnet/contract/0.0.7308504)&#x20;

### USDC

* Token: [`0x000000000000000000000000000000000006f89a`](https://hashscan.io/mainnet/token/0.0.456858)&#x20;
* aToken: [`0xB7687538c7f4CAD022d5e97CC778d0b46457c5DB`](https://hashscan.io/mainnet/contract/0.0.7308496)&#x20;
* Variable Debt: [`0x8a90C2f80Fc266e204cb37387c69EA2ed42A3cc1`](https://hashscan.io/mainnet/contract/0.0.7308498)&#x20;

### SAUCE

* Token: [`0x00000000000000000000000000000000000b2ad5`](https://hashscan.io/mainnet/token/0.0.731861)&#x20;
* aToken: [`0x2bcC0a304c0bc816D501c7C647D958b9A5bc716d`](https://hashscan.io/mainnet/contract/0.0.7308505)&#x20;
* Variable Debt: [`0x736c5dbB8ADC643f04c1e13a9C25f28d3D4f0503`](https://hashscan.io/mainnet/contract/0.0.7308507)&#x20;

### XSAUCE

* Token: [`0x00000000000000000000000000000000001647e8`](https://hashscan.io/mainnet/token/0.0.1460200)&#x20;
* aToken: [`0xEc9CEF1167b4673726B1e5f5A978150e63cDf23b`](https://hashscan.io/mainnet/contract/0.0.7308493)&#x20;
* Variable Debt: [`0x08c816eC7aC0580c802151E4efFbDa687f7Cac2a`](https://hashscan.io/mainnet/contract/0.0.7308495)&#x20;

### KARATE

* Token: [`0x000000000000000000000000000000000022d6de`](https://hashscan.io/mainnet/token/0.0.2283230)&#x20;
* aToken: [`0x98262552C8246Ffb55E3539Ceb51838912402959`](https://hashscan.io/mainnet/contract/0.0.7308499)&#x20;
* Variable Debt: [`0xB6209F33982CE99139Ab325b13B260d32287A807`](https://hashscan.io/mainnet/contract/0.0.7308501)&#x20;

### DOVU

* Token: [`0x000000000000000000000000000000000038b3db`](https://hashscan.io/mainnet/token/0.0.3716059)&#x20;
* aToken: [`0x89D2789481cB4CB5B6949Ff55EBA5629c5bC5B1E`](https://hashscan.io/mainnet/contract/0.0.7308512)&#x20;
* Variable Debt: [`0x9d81E1676A7e116ec725208DdeAB11929eA3F7A6`](https://hashscan.io/mainnet/contract/0.0.7308514)&#x20;

### HST

* Token: [`0x00000000000000000000000000000000000ec585`](https://hashscan.io/mainnet/token/0.0.968069)&#x20;
* aToken: [`0x2e63e864AAD2ce87b45d2C93bc126850DC5122c9`](https://hashscan.io/mainnet/contract/0.0.7308515)&#x20;
* Variable Debt: [`0xdc6e9E967648cd28E8BaF2EB1124ef7C9C5Bd027`](https://hashscan.io/mainnet/contract/0.0.7308517)&#x20;

### PACK

* Token: [`0x0000000000000000000000000000000000492a28`](https://hashscan.io/mainnet/token/0.0.4794920)&#x20;
* aToken: [`0x5F98C43ce4b4765638d69B4a2407a2186A347CB9`](https://hashscan.io/mainnet/contract/0.0.7308518)&#x20;
* Variable Debt: [`0x63c7EF5398E8Fe23D95E762802F011590A7816a1`](https://hashscan.io/mainnet/contract/0.0.7308520)&#x20;

### STEAM

* Token: [`0x000000000000000000000000000000000030fb8b`](https://hashscan.io/mainnet/token/0.0.3210123)&#x20;
* aToken: [`0x46BEf910150a3880ce6eAC60A059E70494A4805e`](https://hashscan.io/mainnet/contract/0.0.7308521)&#x20;
* Variable Debt: [`0xdFD1D43cbd700AEC5bcc151d028274412d31db70`](https://hashscan.io/mainnet/contract/0.0.7308523)&#x20;

### GRELF

* Token: [`0x000000000000000000000000000000000011afa2`](https://hashscan.io/mainnet/token/0.0.1159074)&#x20;
* aToken: [`0xb8c34c9a46AEdf1decb846F942861EeE7dE78075`](https://hashscan.io/mainnet/contract/0.0.8677321)&#x20;
* Variable Debt: [`0x0E509Fc72f4b5d97494c0d45fcd1cF04d531Be44`](https://hashscan.io/mainnet/contract/0.0.8677323)&#x20;

### KBL

* Token: [`0x00000000000000000000000000000000005b665a`](https://hashscan.io/mainnet/token/0.0.5989978)
* aToken: [`0xC45A34b9D9e29fBfCAACC9193FD0CE950e63Ba81`](https://hashscan.io/mainnet/contract/0.0.9132058)
* Variable Debt: [`0x6a74429E0D761085C4D5520A14ab59874dfe1C06`](https://hashscan.io/mainnet/contract/0.0.9132060)&#x20;

### BONZO

* Token: [`0x00000000000000000000000000000000007e545e`](https://hashscan.io/mainnet/token/0.0.8279134)
* aToken: [`0xC5aa104d5e7D9baE3A69Ddd5A722b8F6B69729c9`](https://hashscan.io/mainnet/contract/0.0.9155090)
* Variable Debt: [`0x1790C9169480c5C67D8011cd0311DDE1b2DC76e0`](https://hashscan.io/mainnet/contract/0.0.9155092?pr=1\&pa=1\&ps=1\&pf=1)

## Interest Rate Strategy Contracts

### Base Strategies

| Strategy Name  | Testnet Address                                                                                | Mainnet Address                                                                                |
| -------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Volatile One   | [0x82a278be934D9Ba2e4e46cad5d818647E2Ef0990](https://hashscan.io/testnet/contract/0.0.4999387) | [0x0eaD7dDfC2Bb172D4a899aad8E7b4d882067a001](https://hashscan.io/mainnet/contract/0.0.7308488) |
| Volatile Two   | [0x58812c9430fc9C1e246E34a92a11ecea057DB049](https://hashscan.io/testnet/contract/0.0.4674857) | [0xDa47ecEC5ba98eF6a8C3c4F7EaDa3FBda6f7EED9](https://hashscan.io/mainnet/contract/0.0.7308491) |
| Volatile Three | [0x5c5a27079728FCB66522760032e19cf5d94Fd823](https://hashscan.io/testnet/contract/0.0.3666324) | -                                                                                              |

### Asset-Specific Strategies

<table><thead><tr><th width="167">Asset</th><th>Mainnet Address</th></tr></thead><tbody><tr><td>HBAR (wHBAR)</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7775843">0x82C50aAfe0dc3f92e637EE05076d68180DB06d58</a></td></tr><tr><td>HBARX</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7775845">0xA68FC75Acc8a731a1e5cc4CB717b162566d947A8</a></td></tr><tr><td>USDC</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7809070">0x10753aD937e2f16daB73230fE5e5d8ace807C666</a></td></tr><tr><td>SAUCE</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7809074">0xf38e204b948Db78Ca5D51cCEd7ccEe182Fe4bcA8</a></td></tr><tr><td>XSAUCE</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7775852">0x998A60b83617F05c1Dcd4b3f5D37a2265d6a674D</a></td></tr><tr><td>KARATE</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7809076">0x9bB33f2D511CA3089Fc5696BEe3ABee7174a556a</a></td></tr><tr><td>DOVU</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7775862">0xC8C0c05683474a7B4c8DdaD69D0D546A841Be5D4</a></td></tr><tr><td>HST</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7775868">0x6886E0eD3Cb5dcE6f8e50dCb692a142AE8a14775</a></td></tr><tr><td>PACK</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7775864">0x4DF846F81135d9e63834AD4C7865F1C1983F767a</a></td></tr><tr><td>STEAM</td><td><a href="https://hashscan.io/mainnet/contract/0.0.7775872">0xA3E524FE431011dc6d050c32E92Acc38D2f50cB4</a></td></tr></tbody></table>

### HCS-20 Points

| Topic ID                                                     | Season            | Ticker ID |
| ------------------------------------------------------------ | ----------------- | --------- |
| [0.0.7159077](https://hashscan.io/mainnet/topic/0.0.7159077) | Pre-Season Points | BZPT      |
| [0.0.7159077](https://hashscan.io/mainnet/topic/0.0.7159077) | Season 1 Points   | BZ\_S1    |
