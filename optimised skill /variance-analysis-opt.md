---
name: variance-analysis
description: >
  Financial variance analysis methodology including budget-to-actual comparisons, trend analysis, root cause identification, and management reporting.
metadata:
  vertical: cfo-finance
  function: fp&a
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "GAAP, IMA"
---

## Role
Decompose budget-to-actual, forecast-to-actual, and forecast-over-forecast variances into price/volume/mix drivers and convert findings into forward-looking action via the ARCTIC framework.

## Variance Triage Matrix

| Dimension | Assessment | Rule |
|---|---|---|
| 1 — Materiality Gate | Investigate if ≥10% OR ≥$X (whichever greater) | $X scale: $1K-$3K (<$2M rev); $3K-$10K ($2M-$10M); $10K-$50K+ ($10M+) |
| 2 — Controllability | Controllable / Semi-controllable / Uncontrollable | Controllable → corrective action; uncontrollable → forecast revision + hedging review |
| 3 — Persistence | One-time / Trend-forming (3 consecutive months) / Structural shift | One-time → document; trend → model to forecast; structural → budget restatement |
| 4 — Decomposition | Revenue: price × volume × mix; Cost: rate × efficiency; Overhead: spending, efficiency, production-volume | Decomposition determines which operating team owns response |

## Driver-Based Decomposition Formulas

| Effect | Formula |
|---|---|
| Price Effect | (Actual Price − Budget Price) × Actual Volume |
| Volume Effect | (Actual Volume − Budget Volume) × Budget Price |
| Mix Effect | Σ[(Actual Share_i − Budget Share_i) × Budget Price_i × Actual Total Volume] |
| Residual | Total Variance − (Price + Volume + Mix); must be within tolerance or model needs debugging |

## ARCTIC Framework (Wharton FP&A Program — Christian Wattig)

| Element | Question |
|---|---|
| Actions | What corrective or capitalizing action is recommended? |
| Risks/Opportunities | What risk does this expose? What upside exists? |
| Cause | Execution failure, planning assumption error, or external market shift? |
| Timing | Permanent run-rate change or timing difference that reverses? |
| Impact | Full-year forecast impact if trend continues? |
| Control | Is this within management's ability to influence? |

## Variance Severity Scoring

| Score | Magnitude | Persistence | Strategic Impact |
|---|---|---|---|
| 1 | <5% and below absolute threshold | One-time, reverses next period | No strategic implication |
| 2 | 5-10% or approaching absolute threshold | Two consecutive periods | Minor operational adjustment |
| 3 | 10-15% and exceeds absolute threshold | Three+ periods trending | Forecast revision required |
| 4 | 15-25% significant dollar impact | Structural shift identified | Budget restatement or reallocation |
| 5 | >25% or threatens covenant/target | Permanent model change | Board escalation, strategic pivot |

## Forecast Accuracy Metrics

| Metric | Target |
|---|---|
| MAPE (revenue) | <5% at consolidated level |
| MAPE (opex) | <8% at consolidated level |
| Forecast bias threshold | >3% for 3 consecutive periods = planning process failure |
| Variance concentration | >60% of P&L variance from <3 line items = framework working |

## Regulatory Framework

| Standard | Citation | Requirement |
|---|---|---|
| MD&A | SEC Reg S-K Item 303 | Quantify/explain material changes in revenue, expenses, cash flows; not just restatement of data |
| Revenue recognition | FASB ASC 606 | Separate recognition-timing variances (performance obligations, variable consideration) from commercial performance |
| Segment reporting | FASB ASC 280 / ASU 2023-07 | Align with CODM view; expanded segment expense disclosure |
| Management accounting | IMA Statement | Flexible budgeting, standard costing, variance decomposition best practices |
| Internal controls | COSO; SOX §404 | Variance analysis = monitoring control; threshold/rigor must detect material misstatements |
| Non-GAAP measures | SEC Reg G; Reg S-K Item 10(e) | Reconcile to nearest GAAP; GAAP equal/greater prominence |

## Process

1. **Lock Baseline** — Freeze approved budget/forecast; document version, approval date, key assumptions; maintain clear audit trail of reforecasts
2. **Collect and Validate Actuals** — Pull from ERP/GL after close; verify all material accruals/reclassifications/eliminations posted; confirm same CoA structure and consolidation rules as budget
3. **Compute Variances at Appropriate Grain** — Absolute (Actual − Budget), % ((Actual − Budget) ÷ Budget × 100), and YTD cumulative; compute at consolidated entity, BU, department, cost center, and material account lines
4. **Apply Materiality Filters** — Filter through materiality gate; adjust thresholds quarterly as business scales
5. **Decompose Material Variances** — Revenue: price/volume/mix/currency; COGS: rate/efficiency; Labor: rate/efficiency; Fixed overhead: spending/production-volume; SG&A: discretionary vs. committed, headcount vs. non-headcount
6. **Investigate Root Causes** — Apply 5 Whys or business driver tree; link financial to operational metrics (pipeline conversion, churn, yield, headcount vs. plan, vendor pricing); cross-reference with operations
7. **Classify via ARCTIC** — Apply all six ARCTIC elements per root cause
8. **Update Forecast** — Timing differences rephased; permanent changes adjust run-rate; assumption errors corrected in driver model; document every forecast change linked to trigger variance
9. **Prepare Management Reporting** — Board/Investor: 3-5 most impactful variances + waterfall bridge; C-Suite: full P&L summary + driver decomposition + forecast impact + actions; Operating leaders: account-level + operational KPIs + action owners/deadlines
10. **Close the Loop** — Track corrective actions from prior cycles; "lessons learned" log; review systematic patterns at annual budget cycle

## Glossary

| Term | Definition |
|---|---|
| ARCTIC | Actions/Risks-Opportunities/Cause/Timing/Impact/Control; Wattig (Wharton FP&A Program) structured variance commentary |
| BvA | Budget-to-Actual Variance; difference between approved budget and actual results |
| Constant-Currency Analysis | Restate actuals at budget-period FX rates to isolate operational performance from translation effects |
| Driver-Based Planning | Link financial outcomes to operational drivers (units, headcount, conversion rates, ASP) |
| Efficiency Variance | Actual input qty − standard input qty for actual output, valued at standard rate |
| Favorable Variance | Actual result that improves net income vs. budget |
| Flexible Budget | Budget adjusting variable lines to actual activity volume; isolates price/rate from volume |
| FoF | Forecast-over-Forecast; successive forecast vintage comparison; reveals how outlook is evolving |
| FvA | Forecast-to-Actual; most recent forecast vintage vs. actual; measures near-term prediction accuracy |
| MAPE | Mean Absolute Percentage Error: avg of |Forecast − Actual| / Actual across segments |
| Manager Override | Adjustment to rep/team-level forecasts; must be documented with rationale |
| Mix Variance | Variance from relative proportion shifts vs. budgeted mix; positive when mix shifts to higher-margin items |
| Price/Rate Variance | Portion attributable to actual vs. budgeted price per unit, holding quantity constant |
| Production-Volume Variance | Budgeted fixed overhead vs. allocated fixed overhead; indicates capacity utilization |
| Rolling Forecast | Extends fixed number of periods forward (typically 12-18 months); updated monthly/quarterly |
| Run-Rate Impact | Annualized effect if underlying cause persists at current monthly rate for remaining forecast period |
| Spending Variance | Actual overhead vs. budget for actual activity level; measures cost control independent of volume |
| Static Budget | Fixed budget set at period start; does not adjust for actual activity |
| Unfavorable Variance | Actual result that decreases net income vs. budget |
| Variance Bridge | Waterfall chart decomposing each driver (price/volume/mix/FX/one-time) from budget to actual |
| WMAPE | Weighted MAPE: Σ|Forecast_i − Actual_i| / ΣActual_i; weights errors by revenue magnitude |

## Checklist

- [ ] Budget baseline frozen with documented version, approval date, and key assumptions
- [ ] Actuals reconcile to audited/reviewed trial balance before variance computation
- [ ] CoA and cost center structure identical between budget and actuals (or formally restated)
- [ ] Materiality thresholds defined with absolute dollar AND percentage criteria, calibrated to entity size
- [ ] Every material revenue variance decomposed into price, volume, mix, and currency components
- [ ] Every material cost variance decomposed into rate/price and efficiency/quantity components
- [ ] Flexible budget analysis performed for all volume-sensitive cost categories
- [ ] Timing differences identified and distinguished from permanent run-rate changes
- [ ] Each variance commentary follows What → Why → So What with specific forward-looking action
- [ ] Variance bridge/waterfall reconciles: starting point + all drivers = ending point (hard tie-out)
- [ ] Intercompany eliminations verified: Σ(segment variances) + eliminations = consolidated variance
- [ ] Forecast updated to reflect variance findings with documented assumption changes
- [ ] Corrective actions from prior periods tracked with completion status and effectiveness assessment
- [ ] Report tailored: board summary, C-suite detail, and operating-leader granularity produced separately
- [ ] Constant-currency variances presented alongside reported-currency for foreign operations

## References
SEC Reg S-K Item 303 MD&A; SEC Release 33-10890 (2020 modernization); FASB ASC 606/280; ASU 2023-07; IMA Statement; COSO Internal Control Framework; SOX §404; SEC Reg G; Reg S-K Item 10(e); ARCTIC framework (Christian Wattig, Wharton FP&A Program); Abacum 2024 (61% CFOs implemented FP&A software; 221% increase); Corporate Finance Institute (BvA/FvA/FoF trio); Bennett Financials (materiality thresholds)
