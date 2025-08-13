# Risk Parameter LTV Updates - Ecosystem Assets

* **Submission Date:** August 13, 2025
* **Implementation Date:** August 13th, 2025
* **Author(s):** [Re7 Labs](https://www.re7labs.xyz/) / [Bonzo Finance Labs](https://bonzo.finance)
* **Bonzo Finance Voting Interface:** Change Memo
* **Related Memos / Discussion:** [Interest Rate & Borrow Cap Update - USDC](interest-rate-and-borrow-cap-update-usdc.md), [Supply / Borrow Cap Updates - Ecosystem Assets](supply-borrow-cap-updates-ecosystem-assets.md)
* **Historical Risk Parameter Updates:** [Link](https://docs.bonzo.finance/bonzo-risk-framework/asset-risk/risk-parameters-per-asset)

## Simple Summary

This change memo follows newly established procedures for Bonzo Finance protocol’s risk parameter updates, ensuring greater transparency and consistency. It also lays a foundation for the Bonzo Finance DAO by onboarding an independent risk steward and ecosystem contributor (Re7 Labs) to support risk analysis and authorship of change memos and DAO proposals.

This proposal aims to adjust the Loan-to-Value (LTV) ratios — the maximum percentage borrowable against supplied collateral — of supported ecosystem assets by:

* Increasing SAUCE, XSAUCE, and BONZO (to 40% from 30%),
* Reducing KARATE (to 20% from 25%), PACK / KBL (to 10% from 25%), and STEAM / HST (to 10% from 20%).

## Motivation

The Bonzo Finance protocol has swiftly achieved a level of liquidity and growth that warrants refined adjustments to its risk parameters. The overarching motivation is to establish a temporary baseline, allowing the protocol to safely scale and achieve maximum market efficiency for stablecoin assets like USDC.

It’s expected that baseline risk parameters will remain in place for at least 3 weeks, allowing time for comprehensive analysis by risk stewards and mitigating the need for continuous reactive / disruptive adjustments. Outcomes from that analysis will support further optimizations, which carry the protocol towards greater scalability, safety, and market efficiency.

### LTV Increases for SAUCE, XSAUCE, and BONZO

A careful assessment of secondary liquidity sources (e.g., SaucerSwap DEX) and concentrations for SAUCE, XSAUCE, and BONZO determined that their LTVs can be raised. Motivation for raising the LTV ratios of these asset markets is to maximize capital efficiency safely and without amplifying risk of other interdependent markets.

### LTV Reductions for KARATE, PACK, KBL, STEAM, and HST

A careful assessment of secondary liquidity sources (e.g., SaucerSwap DEX) and concentrations for KARATE, GRELF, DOVU, PACK, KBL, STEAM, and HST determined that the LTVs of all (besides GRELF and DOVU, which were previously lowered) must be lowered. This mitigates future liquidation risks that could result in bad debt for the protocol, while also limiting impacts on the efficiency of primary asset markets like $USDC.

Modifications to these ecosystem asset risk parameters will continue to be revisited as the supply and efficiency of secondary liquidity sources (i.e. SaucerSwap DEX / exchanges) fluctuate long-term.

### USDC Market Note

While this change memo is specific to both increases and reductions of LTV for cited ecosystem assets, it is being performed in conjunction with updating USDC market parameters, under the motivation of ensuring the USDC market operates safely with maximum capital efficiency. See [Interest Rate & Borrow Cap Update - USDC](interest-rate-and-borrow-cap-update-usdc.md).

## Impact & Implementation

* Increasing LTV for SAUCE, XSAUCE, and BONZO will enable more borrowing against these as collateral, boosting capital efficiency and safe utilization of primary assets (HBAR, HBARX, USDC) without adding undue risk.
* Reducing LTV for KARATE, PACK, KBL, STEAM, and HST poses no liquidation risks to existing positions, as Liquidation Thresholds (LTs) — the point where positions become liquidatable — remain unchanged.
* Keeping LTV for DOVU, GRELF the same poses no liquidation risks to existing positions.

These changes will be implemented immediately after approval, with ongoing monitoring for liquidity shifts.

## Specification

This Bonzo Finance Change Memo details the recommended (Rec.) adjustments to the LTV ratios of SAUCE, XSAUCE, BONZO, KARATE, PACK, KBL, STEAM, and HST markets.

Other parameters (LT: Liquidation Threshold; Liq. Bonus: Liquidation Bonus for liquidators; RF: Reserve Factor) remain unchanged. Potential Liqs. indicates no expected liquidations from these changes.

<table data-header-hidden><thead><tr><th width="96.17578125">Asset</th><th width="130.65625">Current LTV</th><th width="108.171875">Rec. LTV</th><th width="120.3359375">Current LT</th><th width="96.46484375">Rec. LT</th><th width="168.83984375">Current Liq. Bonus</th><th width="149.73046875">Rec. Liq. Bonus</th><th width="119.49609375">Current RF</th><th width="99.91796875">Rec. RF</th><th>Potential Liqs.</th></tr></thead><tbody><tr><td>SAUCE</td><td>30.00%</td><td>40.00%</td><td>68.04%</td><td>“</td><td>3.95%</td><td>“</td><td>14.60%</td><td>“</td><td>$0</td></tr><tr><td>XSAUCE</td><td>30.00%</td><td>40.00%</td><td>67.59%</td><td>“</td><td>3.95%</td><td>“</td><td>10.94%</td><td>“</td><td>$0</td></tr><tr><td>BONZO</td><td>30.00%</td><td>40.00%</td><td>59.00%</td><td>“</td><td>6.66%</td><td>“</td><td>17.25%</td><td>“</td><td>$0</td></tr><tr><td>KARATE</td><td>25.00%</td><td>20.00%</td><td>65.00%</td><td>“</td><td>3.46%</td><td>“</td><td>19.60%</td><td>“</td><td>$0</td></tr><tr><td>$GRELF</td><td>20.00%</td><td>“</td><td>59.00%</td><td>“</td><td>6.66%</td><td>“</td><td>17.25%</td><td>“</td><td>$0</td></tr><tr><td>$DOVU</td><td>20.00%</td><td>“</td><td>59.00%</td><td>“</td><td>6.66%</td><td>“</td><td>17.25%</td><td>“</td><td>$0</td></tr><tr><td>PACK</td><td>25.00%</td><td>10%</td><td>57.00%</td><td>“</td><td>6.91%</td><td>“</td><td>12.97%</td><td>“</td><td>$0</td></tr><tr><td>STEAM</td><td>20.00%</td><td>10%</td><td>57.00%</td><td>“</td><td>8.14%</td><td>“</td><td>13.88%</td><td>“</td><td>$0</td></tr><tr><td>HST</td><td>20.00%</td><td>10%</td><td>52.00%</td><td>“</td><td>6.17%</td><td>“</td><td>15.22%</td><td>“</td><td>$0</td></tr><tr><td>KBL</td><td>25.00%</td><td>10%</td><td>57.00%</td><td>“</td><td>6.66%</td><td>“</td><td>17.25%</td><td>“</td><td>$0</td></tr></tbody></table>

\


