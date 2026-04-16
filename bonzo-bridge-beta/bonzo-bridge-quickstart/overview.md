# Overview

### Bonzo Bridge Underlying Infrastructure

* [LayerZero](https://layerzero.network/) provides the cross-chain messaging protocol that carries instructions and verification data between source and destination chains for all Bonzo Bridge supported networks and assets.
* [Stargate](https://stargate.finance/?dstChain=hedera\&dstToken=0xCa367694CDaC8f152e33683BB36CC9d6A73F1ef2) is the issuer of the WETH LayerZero asset and acts as a supporting transfer layer, enabling things like auto-unwrapping of WETH on destination chains and taxi mode.

Hedera EVM allows bridged assets to arrive on Hedera as standard ERC-20 tokens, interoperable with [Bonzo Lend](https://app.bonzo.finance/lend), [Bonzo Vaults](https://app.bonzo.finance/vaults), [SaucerSwap](https://saucerswap.finance), and the wider Hedera DeFi ecosystem.

### Taxi Mode

Bonzo Bridge uses Stargate's [taxi mode](https://docs.stargate.finance/primitives/concepts/transport) by default. In taxi mode, each transaction is processed individually rather than batched with other users' transfers. This produces faster and more predictable delivery times, at the cost of being slightly more expensive than batched (bus) mode. Users do not need to configure this — taxi mode is applied automatically to every bridge transaction.

### Automatic Native ETH Delivery

When a user bridges WETH to a chain that uses ETH as its native currency (Ethereum, Arbitrum, Base, or Optimism), the bridge automatically unwraps WETH and delivers native ETH to the destination wallet. No additional transactions or manual unwrapping steps are required.
