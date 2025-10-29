---
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Onboard wETH (LayerZero OFT) to Bonzo Lend

* **Submission Date:** October 28, 2025
* **Implementation Date:** Upon approval (est. October 30, 2025)
* **Author(s):** [Re7 Labs](https://www.re7labs.xyz/) / [Bonzo Finance Labs](https://bonzo.finance)
* **Bonzo Finance Voting Interface:** Change Memo
* **Related Memos / Discussion:** None
* **Historical Risk Parameter Updates:** [Link](https://docs.bonzo.finance/bonzo-risk-framework/asset-risk/risk-parameters-per-asset)
* **Re7 Analysis**: [Link](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRl3dkXEKv1yqGhH70g65%2Fuploads%2FOxIUnwEkuLuHbHv0cdfj%2FWETH%20Risk%20Parameters%20for%20Bonzo%20-%20Oct%2024.pdf?alt=media\&token=8cd7eb27-d18b-49ed-a2c4-e48bbf0da156)
  * _Addendum: Analysis performed prior to the addition of liquidity to the HBAR/WETH SaucerSwap v2 pool; at current liquidity depth / width, recommended supply cap is 220-230 WETH._

## Simple Summary

This memo proposes listing wETH (LayerZero OFT) on Bonzo Lend with conservative, liquidity-aware risk parameters derived from Re7’s analysis of local Hedera DEX depth and liquidation feasibility, plus alignment to industry norms (Aave/Compound) where appropriate.&#x20;

**Primary levers:**&#x20;

* Supply & Borrow Caps
* Loan-to-Value (LTV)
* Liquidation Threshold (LT)
* Liquidation Bonus (LB)
* Reserve Factor (RF)
* Close Factor (CF)
* Interest Rate Model

## Motivation

**User demand & composability:** ETH exposure is a cornerstone collateral across DeFi; adding wETH enables safer leverage, hedging, and cross-asset strategies on Hedera.

**Liquidity-constrained venue:** SaucerSwap’s [HBAR/WETH depth](https://www.saucerswap.finance/liquidity/0.0.10018365) and [USDC/WETH depth](https://app.gitbook.com/u/eMeLAVOk9dW9L8XS5kwelK8D2ua2) is meaningful but not yet comparable to mainnet venues; parameters must assume shallow local unwind paths and favor liquidation success over peak capital efficiency.

**Industry anchors:** Mature markets (e.g., Aave v3) run WETH with LTV ≈ 80%, LT ≈ 82.5–85%, LB ≈ 5%, RF ≈ 15% (varies by instance). Bonzo’s initial settings intentionally underrun these to reflect Hedera-side liquidity and bridge risk.

**Bridge/OFT considerations:** LayerZero OFT tokens add messaging & DVN assumptions; listing starts with tighter caps and explicit monitoring.

## Method (Re7)

Re7 modeled DEX price impact vs. liquidation profitability, linking caps to swaps that keep price impact below the liquidation bonus; they present conservative/realistic/capital-efficient supply-cap bands and a recommended parameter set tailored to today’s Hedera liquidity.

{% file src="../../.gitbook/assets/WETH Risk Parameters for Bonzo - Oct 24.pdf" %}

> _**Addendum**: Analysis performed prior to the addition of liquidity to the HBAR/WETH SaucerSwap v2 pool; at current liquidity depth / width, recommended supply cap is 220-230 WETH._

### Specification (Initial Listing — Phase 1)

**Asset:** `wETH (LayerZero OFT on Hedera)`

<table><thead><tr><th width="249.37890625" align="center">Parameter</th><th width="156.41796875" align="center">Recommended</th><th align="center">Rationale</th></tr></thead><tbody><tr><td align="center"><strong>Enable Borrow</strong></td><td align="center"><strong>Yes</strong></td><td align="center">Standard for blue-chip collateral; limits via caps.</td></tr><tr><td align="center"><strong>Enable Collateral</strong></td><td align="center"><strong>Yes</strong></td><td align="center">ETH-class collateral w/ conservative LTV/LT.</td></tr><tr><td align="center"><strong>Supply Cap</strong></td><td align="center"><strong>225 wETH</strong></td><td align="center">Within Re7 “realistic” 35–40 wETH band; sized to ensure profitable liquidations under local DEX depth.</td></tr><tr><td align="center"><strong>Borrow Cap</strong></td><td align="center"><strong>112 wETH</strong></td><td align="center">50% of Supply Cap to limit borrow-driven sell pressure in shallow markets.</td></tr><tr><td align="center"><strong>LTV</strong></td><td align="center"><strong>70%</strong></td><td align="center">Below Aave’s typical ~80% to reflect Hedera liquidity/bridge risk.</td></tr><tr><td align="center"><strong>Liquidation Threshold (LT)</strong></td><td align="center"><strong>75%</strong></td><td align="center">5% gap vs LTV gives reaction time and supports higher LB; wider than some mainnet settings.</td></tr><tr><td align="center"><strong>Liquidation Bonus (LB)</strong></td><td align="center"><strong>10%</strong></td><td align="center">Above mainnet norms (~5%) to ensure liquidation profitability in shallower liquidity.</td></tr><tr><td align="center"><strong>Reserve Factor (RF)</strong></td><td align="center"><strong>20%</strong></td><td align="center">Above Aave’s common 15% to accrue extra safety reserves in low-liquidity conditions.</td></tr><tr><td align="center"><strong>Close Factor (CF)</strong></td><td align="center"><strong>50%</strong></td><td align="center">Industry-standard to prevent full wipes and smooth execution.</td></tr><tr><td align="center"><strong>Interest Rate Model (Variable)</strong></td><td align="center"><p><strong>Base</strong> 0%</p><p><strong>U</strong><em><strong>opt</strong></em> 80%</p><p><strong>Slope1</strong> 3.3%</p><p><strong>Slope2</strong> 85%</p></td><td align="center">Uses well-understood WETH curves observed across Aave v3 markets (0% base; 80% kink; low Slope1 to target U<em>opt</em>; high Slope2 to protect tail liquidity).</td></tr></tbody></table>

> **Note on cap sizing:** _Analysis report was performed prior to the addition of liquidity to the HBAR/WETH SaucerSwap v2 pool; at current liquidity depth / width, recommended supply cap from Re7 is 220-230 WETH; **225 wETH** is selected to balance utility with liquidation success given a 10% LB._

## Impact & Rationale

### **Why these levels now**

* **Liquidation feasibility first:** With LT 75%, LB 10%, CF 50%, worst-case unwinds remain profitable for liquidators under modeled price impact bands, reducing bad-debt risk if markets gap.
* **Conservative vs. Aave:** Aave’s WETH often sits around LTV ≈ 80/LT ≈ 82.5 with LB ≈ 5%; Bonzo starts at 70/75/10 to account for Hedera liquidity and OFT bridge risks, then ratchets up as liquidity deepens.
* **IR curve choice:** 0% base, &#x55;_&#x6F;pt_ 80%, and modest Slope1 (3.3%) encourage healthy utilization without inducing rate spikes; Slope2 60% sharply disincentivizes >80% utilization, preserving on-chain liquidity for liquidations.

### **Bridge/OFT risk notes**

* Listing an OFT-bridged wETH introduces messaging/DVN trust assumptions; therefore, caps and RF are higher than mainnet peers, and monitoring (below) is mandated.

## Monitoring, Triggers & Next Steps

### Operational monitoring (weekly and on 10% price moves)

* **Dex Depth Check:** Track SaucerSwap WETH/HBAR active liquidity and effective swap impact bands; revisit caps if active liquidity falls materially.
* **Utilization & Rates:** If wETH utilization persistently >85% or <30% for 3+ days, consider Slope1/&#x55;_&#x6F;pt_ nudges (industry precedent).
* **Bridge/DVN Health:** Track LayerZero incident advisories and DVN composition changes; pause increases or reduce caps on adverse signals.
* **DEX liquidity deterioration:** 14-day average active WETH liquidity down >40% versus today’s baseline.
* **Volatility shock:** 24h WETH/HBAR move >20% or repeated >10% shocks over 72h (per Re7 tail analysis).
* **Bridge risk elevation:** Verified DVN/endpoint incident or materially increased trust assumptions.

### **Phase-up plan (subject to passing all guardrails for ≥2 consecutive weeks)**

* **Step 1:** Supply Cap 50 wETH, Borrow Cap 30 wETH (unchanged LTV/LT/LB/RF/CF).
* **Step 2:** If local depth materially increases (or Bonzo LP boosts are deployed), consider LTV 75%, LT 80%, LB 7.5% (approaching mainnet norms), with independent memo and stress test.

## Implementation

* Configure wETH (LayerZero OFT) with the Phase 1 parameters above.
* Announce listing + parameters in Bonzo docs / interface.
* Begin monitoring loop (weekly + on 10% price moves).
* Prepare follow-up memo for any cap increases or LTV/LT/LB adjustments post-stabilization period (≥2 weeks).

## Appendix — Parameter Sources & Industry References

* **Re7 Labs:** **WETH Risk Parameters for Bonzo Lend** (Oct 2024) — liquidity analysis, cap bands, and recommended settings.&#x20;

{% file src="../../.gitbook/assets/WETH Risk Parameters for Bonzo - Oct 24.pdf" %}

* **Aave references (comparables / norms):** parameters & governance threads on LTV/LT/LB/RF/IR curves ([1](https://governance.aave.com/t/arfc-aave-v3-deployment-on-base/13708), [2](https://aave.com/docs/resources/parameters), [3](https://aave.com/docs/developers/smart-contracts/interest-rate-strategy), [4](https://governance.aave.com/t/gauntlet-interest-rate-recommendations-for-weth-and-wmatic-on-v2-and-v3/14588))
* Close factor conventions & liquidation literature.
* LayerZero OFT / DVN risk background.
