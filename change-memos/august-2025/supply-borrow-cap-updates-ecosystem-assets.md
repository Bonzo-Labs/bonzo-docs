# Supply / Borrow Cap Updates - Ecosystem Assets

* **Submission Date:** August 13, 2025
* **Implementation Date:** August 13th, 2025
* **Author(s):** [Re7 Labs](https://www.re7labs.xyz/) / [Bonzo Finance Labs](https://bonzo.finance)
* **Bonzo Finance Voting Interface:** Change Memo
* **Related Memos / Discussion:** [Interest Rate & Borrow Cap Update - USDC](interest-rate-and-borrow-cap-update-usdc.md), [Risk Parameter LTV Updates - Ecosystem Assets](risk-parameter-ltv-updates-ecosystem-assets.md)
* **Historical Risk Parameter Updates:** [Link](https://docs.bonzo.finance/bonzo-risk-framework/asset-risk/risk-parameters-per-asset)

## Simple Summary

This change memo follows newly established procedures for Bonzo Finance protocol’s risk parameter updates, ensuring greater transparency and consistency. It also lays a foundation for the Bonzo Finance DAO by onboarding an independent risk steward and ecosystem contributor (Re7 Labs) to support risk analysis and authorship of change memos and DAO proposals.

This proposal aims to modify the Supply Caps (maximum tokens that can be supplied as collateral) and Borrow Caps (maximum tokens that can be borrowed) of supported ecosystem assets by setting:

* Supply Caps for SAUCE, XSAUCE, and BONZO to token equivalents of $1M USD, with Borrow Caps at $250K USD.
* Supply Caps for KARATE, GRELF, and DOVU to token equivalents of $50K USD, with Borrow Caps at $10K USD.
* Supply Caps for PACK, STEAM, HST, and KBL to token equivalents of $10K USD, with Borrow Caps at $0.

Equivalent token amounts for all Supply/Borrow caps will be regularly maintained to reflect the USD values cited above, until a new change memo with updated USD figures is published.

## Motivation

The Bonzo Finance protocol has swiftly achieved a level of liquidity and growth that warrants refined adjustments to its risk parameters. The overarching motivation is to establish a temporary baseline, allowing the protocol to safely scale and achieve maximum market efficiency for stablecoin assets like USDC.

It’s expected that baseline risk parameters will remain in place for at least 3 weeks, allowing time for comprehensive analysis by risk stewards and mitigating the need for continuous reactive / disruptive adjustments. Outcomes from that analysis will support further optimizations, which carry the protocol towards greater scalability, safety, and market efficiency.

### Adjust Supply / Borrow Caps for SAUCE, XSAUCE, BONZO, KARATE, GRELF, DOVU, PACK, STEAM, HST, and KBL

These adjustments are based on assessments of secondary liquidity (e.g., on SaucerSwap DEX) and concentration risks.

The motivation for reducing the Supply / Borrow Caps of these asset markets is to limit the maximum potential impact on respective secondary liquidity sources (DEXs), in addition to mitigating the Bonzo Finance protocol’s exposure to bad debt accumulation and potential gaming:&#x20;

1. For Supply Caps, this sets maximum limits on potential liquidations that can be withstood by their respective markets, when these assets are used as collateral
2. For Borrow Caps, this sets maximum limits on potential downwards pressure that can be withstood by their respective markets, for scenarios involving the sale of these assets upon borrow

While this change memo is specific to reductions of Supply / Borrow Caps for cited ecosystem assets, it is being performed in conjunction with [LTV Updates for Ecosystem Assets](risk-parameter-ltv-updates-ecosystem-assets.md) and [Interest Rate & Borrow Cap Updates to USDC](interest-rate-and-borrow-cap-update-usdc.md) market parameters.&#x20;

The combined impact of these changes is meant to not only to support limiting maximum negative impact on supported assets, users, and the protocol itself, but also to support the protocol’s overall market structure to allow the Hedera native USDC market to operate with maximum capital efficiency.

Modifications to ecosystem asset risk parameters will continue to be revisited as the supply and efficiency of secondary liquidity sources (i.e. SaucerSwap DEX / exchanges) fluctuate long-term.

### Specification

This Bonzo Finance Change Memo details the recommended (Rec.) adjustments to the Supply/Borrow Caps for the SAUCE, XSAUCE, BONZO, KARATE, GRELF, DOVU, PACK, STEAM, HST, and KBL markets on Hedera.

| Asset  | Current Supply Cap | Rec. Supply Cap | Current Borrow Cap | Rec. Borrow Cap |
| ------ | ------------------ | --------------- | ------------------ | --------------- |
| SAUCE  | 10,000,000         | 18,138,944      | 3,000,000          | 4,534,736       |
| XSAUCE | 35,000,000         | 14,936,519      | 10,750,000         | 3,734,129       |
| BONZO  | 30,000,000         | 14,116,318      | 8,400,000          | 3,529,079       |
| KARATE | 2,000,000,000      | 385,208,012     | 803,014,392        | 77,041,602      |
| GRELF  | 949,834            | 107,642         | 450,000            | 21,528          |
| DOVU   | 102,000,000        | 19,379,844      | 230,000,000        | 3,875,968       |
| PACK   | 10,120,275         | 480,307         | 16,053,200         | 0               |
| STEAM  | 19,781,362         | 1,226,843       | 11,372,200         | 0               |
| HST    | 26,725,453         | 1,077,934       | 5,537,875          | 0               |
| KBL    | 45,450,838         | 1,161,440       | 16,000,000         | 0               |

\
