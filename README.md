# 🤠 Overview

Welcome to the official documentation for Bonzo Finance — the premier lending and borrowing protocol of the Hedera network. The organizational structure of Bonzo is comprised of these four components:

* **Bonzo Finance Labs:** A Dubai-based development shop corporation is contributing to development of the Bonzo Finance protocol, along with the user interface.
* **The Bonzo Finance Protocol:** A liquidity pool-based decentralized lending protocol built on Hedera. Bonzo is powered by open source smart contracts from Aave v2 that have been adapted to Hedera's native smart contract and token services. Bonzo utilizes over-collateralized loans, flash loans, and dynamic interest rate models to facilitate permissionless lending and borrowing of crypto assets.
* **The Bonzo Interface:** An easy-to-use, web-hosted user interface that allows user interaction with the Bonzo protocol. The interface is one of many ways to interact with Bonzo.
* **The Bonzo DAO (Coming Soon):** A decentralized autonomous organization (DAO) that guides protocol development and governance through collective decision-making by its community members, enabled by the $BONZO token.

## Bonzo Finance Protocol

The [Bonzo Finance](https://www.bonzo.finance) protocol is an open source, non-custodial protocol designed to facilitate the lending and borrowing of cryptocurrencies, with a focus on HBAR, Hedera Token Service (HTS) tokens, and wrapped major assets. Bonzo prioritizes censorship resistance, security, and self-custody, enabling users to transact without reliance on trusted intermediaries that may selectively restrict access.

Bonzo Finance is based on [Aave v2](https://docs.aave.com/developers/v/2.0) and adapted to the Hedera EVM (Ethereum Virtual Machine) and native Hedera Token Service (HTS). By adapting Aave v2 to Hedera, the Bonzo Finance protocol inherits the Hedera network's high throughput, fast transaction finality, and a low, fixed, U.S. dollar-denominated fee structure. Additionally, Hedera's architecture ensures fair transaction ordering, mitigating the risk of MEV attacks commonly seen on alternative EVM-based protocols.

Bonzo Finance utilizes [Supra](bonzo-protocol/oracles/supra.md) and [Pyth](broken-reference) oracles that enable accurate and reliable price feeds for the lending and borrowing of assets, ensuring transparent and efficient operations within the protocol.
