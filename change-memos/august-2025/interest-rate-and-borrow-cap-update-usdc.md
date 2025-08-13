# Interest Rate & Borrow Cap Update - USDC

* **Submission Date:** August 13, 2025
* **Implementation Date:** August 13th, 2025
* **Author(s):** [Re7 Labs](https://www.re7labs.xyz/) / [Bonzo Finance Labs](https://bonzo.finance)
* **Bonzo Finance Voting Interface:** Change Memo
* **Related Memos / Discussion:** [Supply / Borrow Cap Updates - Ecosystem Assets](supply-borrow-cap-updates-ecosystem-assets.md), [Risk Parameter LTV Updates - Ecosystem Assets](risk-parameter-ltv-updates-ecosystem-assets.md)
* **Historical Interest Rates & Risk Parameters:** [Interest Rates](https://docs.bonzo.finance/bonzo-risk-framework/asset-risk/risk-parameters-per-asset) & [Parameters](https://docs.bonzo.finance/bonzo-risk-framework/liquidity-risk/actual-rates-and-parameters)

## Simple Summary

This change memo follows newly established procedures for Bonzo Finance protocol’s risk parameter updates, ensuring greater transparency and consistency. It also lays a foundation for the Bonzo Finance DAO by onboarding an independent risk steward and ecosystem contributor (Re7 Labs) to support risk analysis and authorship of change memos and DAO proposals.

This proposal adjusts the interest rate parameters and borrow caps for the USDC market in Bonzo Finance on Hedera.

## Motivation

The Bonzo Finance protocol has swiftly achieved a level of liquidity and growth that warrants refactored adjustments to its risk parameters (change memo [#1](risk-parameter-ltv-updates-ecosystem-assets.md), [#2](supply-borrow-cap-updates-ecosystem-assets.md)). The overarching motivation for these adjustments is to establish a temporary baseline, allowing the protocol to safely scale to the next attainable level and achieve maximum market efficiency for stablecoin assets (USDC).

This proposed interest rate change to the USDC market is only possible due to the parameter changes proposed in memo #1 and #2, linked above. It’s expected that baseline risk parameters will remain in place for at least 3 weeks, allowing time for comprehensive analysis by risk stewards and mitigating the need for continuous reactive / disruptive adjustments. This proposed USDC interest rate change is expected to remain intact, assuming no unforeseen risks emerge.

### Interest Rate Model Adjustment

The motivation for adjusting the USDC market’s Base Rate (minimum interest floor), Optimal Utilization (target borrowing level for balanced rates), Slope 1 (rate increase gradient before optimal point), and Slope 2 (steeper gradient after optimal point) is to achieve greater capital efficiency, less volatile APYs as utilization fluctuates, and scale the USDC market beyond its current TVL of \~$10.3M / borrow utilization of \~$4.7M.

### Borrow Cap Adjustment

Increasing the USDC Borrow Cap from 5,500,000 USDC to 10,000,000 USDC is an “in-conjunction” requirement, which removes restrictions on utilization (borrows). Lifting this restriction offers the USDC market the ability to reach its optimal utilization rate, which is required in order to realize market efficiency gains stemming from the proposed interest rate model adjustments.

## Impact & Implementation

With the proposed adjustments to the interest rate model for USDC:&#x20;

* Borrowing is expected to increase as optimal utilization rises from 52% to 85%, with more gradual rate changes due to an elongated Slope 1.
* Slope 2 reduction from 200% to 50% protects borrowers in high-demand scenarios, minimizing disruptions.
* The 2% base rate stabilizes APYs, keeping current utilization (46.2%) at parity with today's rates, reducing disruption for existing positions.

These changes will be implemented immediately after approval, with ongoing monitoring for any emerging risks.

## Specification

This Bonzo Finance Change Memo details the recommended (Rec.) adjustments to the interest rate model of the USDC market for Bonzo Finance on Hedera.

| Parameter                   | Current Value | Rec. Value |
| --------------------------- | ------------- | ---------- |
| Base Variable Interest Rate | 0%            | 2%         |
| Slope 1                     | 12%           | 13%        |
| Slope 2                     | 200%          | 50%        |
| Optimal Utilization         | 52%           | 85%        |
| Borrow Cap                  | 5,500,000     | 10,00,000  |

\
\
