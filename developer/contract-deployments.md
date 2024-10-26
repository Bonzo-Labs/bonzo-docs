---
description: >-
  A comprehensive overview of all deployed contracts for the Bonzo Finance
  protocol across Hedera Testnet and Mainnet environments.
---

# 📜 Contract Deployments

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

<table><thead><tr><th width="130">Asset</th><th>Testnet Address</th><th>Mainnet Address</th></tr></thead><tbody><tr><td>SAUCE</td><td>0xd1AfE10418B06729Dd01C0B6166E436E276a0018</td><td>0x9e472c982e1D482A04F4851410F70DF5D038D0DC</td></tr><tr><td>USDC</td><td>0x6966Fe23C576f741621d894F1c5e2dfEb8da4abA</td><td>0x2b8d1b9EC23D518e0541Ed3dD3E95a5F8B7Ac55b</td></tr><tr><td>HBARX</td><td>0x96Cd2b01Dd091f91C0245A12B9345607C8256FeE</td><td>0x8d9f6dC943bb43496E0C9a75C1D89Dc17Cf5F23A</td></tr><tr><td>HBAR</td><td>0x6dE7E16877c30cA25302C6693b764c844E663Af9</td><td>0x428F8b2143b0e8df135D1154F0A2F6e14f66Aa11</td></tr><tr><td>XSAUCE</td><td>-</td><td>-</td></tr><tr><td>KARATE</td><td>-</td><td>-</td></tr><tr><td>DOVU</td><td>-</td><td>-</td></tr><tr><td>HST</td><td>-</td><td>-</td></tr><tr><td>PACK</td><td>-</td><td>-</td></tr><tr><td>STEAM</td><td>-</td><td>-</td></tr></tbody></table>
