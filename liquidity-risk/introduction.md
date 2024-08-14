# Introduction

Bonzo Finance is an open source, non-custodial lending protocol built on the Hedera network, leveraging open source Aave v2 to enable borrowing of various digital assets from liquidity pools in the Hedera ecosystem. Asset depositors receive aTokens in exchange for their deposits.

Liquidity is a critical metric for Bonzo Finance, as it represents the protocol's capacity to handle core operations: facilitating borrowing and allowing the redemption of aTokens. Insufficient liquidity can severely impair the protocol's functionality.

The protocol's liquidity can be gauged at any given moment through its utilization ratio — the proportion of each asset's supply pool that is currently being borrowed.

This section delves into Bonzo Finance's liquidity risk by:

1. Analyzing the historical availability of assets on the Hedera network
2. Identifying periods of liquidity scarcity
3. Examining the valuation of aTokens

It's important to note that illiquid assets often suffer from valuation discounts due to the challenge of finding counterparties, especially in newer DeFi ecosystems, such as Hedera's.

By studying historical utilization rates and aToken valuations, Bonzo Finance can assess the protocol's liquidity risk level. This understanding allows for the implementation of effective risk management strategies, including:

1. Tailoring the borrow interest rate model to the Hedera network's unique characteristics
2. Establishing alternative sources of aToken liquidity that align with Hedera's ecosystem

These measures aim to ensure Bonzo Finance maintains robust liquidity, supporting its operations and growth within Hedera's DeFi ecosystem.
