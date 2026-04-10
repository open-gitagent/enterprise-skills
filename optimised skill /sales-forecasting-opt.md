---
name: sales-forecasting
description: >
  Sales forecast methodology including pipeline-weighted, historical trending, bottoms-up modeling, and forecast accuracy measurement.
metadata:
  vertical: sales
  function: analytics
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "SEC, SOX"
---

## Role
Synthesize pipeline data, historical performance, and rep intelligence into structured revenue projections driving hiring, capacity planning, inventory, marketing, and board guidance.

## Methodology Selection Matrix

| Method | When to Apply | Limitation |
|---|---|---|
| Pipeline-Weighted | CRM has ≥4 quarters of stage-level conversion data; 50+ active opportunities | Requires clean CRM data; recalibrate stage probabilities quarterly with actuals (never vendor defaults) |
| Historical Trending | Mature, renewals-heavy businesses with predictable buying cycles | Cannot model net-new product lines, market disruptions, or GTM motion changes |
| Bottoms-Up | Rep-level accountability required; clearly defined territories | Requires strong forecast category discipline (Commit/Best Case/Pipeline enforced uniformly) |
| Top-Down | Sanity check only; never primary | Cannot substitute for pipeline evidence; exposes gap between field capacity and corporate targets |

## Hybrid Model Decision Logic

| Layer | Method | Function |
|---|---|---|
| Primary engine | Pipeline-weighted | Drives weekly forecast calls |
| Calibration | Historical trending | Flags anomalies; Q3 historically 15% below Q2? |
| Accountability | Bottoms-up rollup | Each manager owns their number |
| Reality check | Top-down allocation | Prevents organizational delusion |

When methods diverge >15%, conduct root-cause analysis before submitting forecast.

## Forecast Accuracy Grading (Forrester/SiriusDecisions)

| Grade | Variance | Assessment |
|---|---|---|
| Excellent | ≤±5% | Top-decile; only 20% of orgs achieve (Xactly 2024) |
| Good | >±5% to ≤±10% | Operationally reliable; supports board guidance |
| Acceptable | >±10% to ≤±15% | Common mid-market; process improvements needed |
| Poor | >±15% | Systemic failure; stage definitions, data hygiene, or methodology broken |

Segment variance targets: Enterprise B2B ±10%; Mid-market ±15-20%; SMB ±20-30%.

## Pipeline Health Indicators

| Metric | Benchmark |
|---|---|
| Coverage ratio | 3×-5× enterprise; 2.5×-4× mid-market; 2×-3× SMB |
| Commit conversion rate | ≥85% of Commit should close within forecast period |
| Best Case conversion | 33%-50% of Best Case closes within period |
| Slip rate | ≤15% of Commit deals push to next quarter |
| Deal aging | <10% of pipeline stuck beyond 1.5× median stage duration |

## Process

**Phase 1 — Foundation (Weeks 1-2 of Quarter)**
1. **Audit CRM data quality** — Verify mandatory fields (amount, close date, stage, next step, forecast category) on 95%+ of opportunities; remediate past-dated close dates
2. **Recalibrate stage probabilities** — Pull prior-quarter conversion rates by stage; replace vendor defaults with actuals (e.g., if Proposal converts at 35% but set at 50%, adjust immediately)
3. **Set pipeline coverage targets** — Quota ÷ Historical Win Rate = required pipeline; enterprise B2B 3×-5×; mid-market 2.5×-4×; SMB 2×-3×
4. **Collect Day One forecasts** — Each rep submits Commit/Best Case/Pipeline; record immutable snapshot per Forrester accuracy methodology

**Phase 2 — Weekly Execution**
5. **Run weekly forecast calls** — Inspect Commit deals first: verify mutual close plan, confirmed timeline, known approvals, scheduled next milestone; question any Commit without identified Economic Buyer
6. **Apply MEDDPICC deal inspection** — Enterprise deals $100K+: Metrics, Economic Buyer, Decision Criteria, Decision Process, Paper Process, Identify Pain, Champion, Competition; missing elements = risk signals
7. **Calculate weighted pipeline** — Sum (Deal Value × Stage Probability) across all opportunities; compare against quota gap (Quota minus Closed-Won to date)
8. **Track deal velocity** — Deals exceeding 1.5× median stage duration require intervention or reclassification

**Phase 3 — Forecast Submission**
9. **Build range forecast** — Floor=Commit sum; Target=Commit + 50% Best Case; Ceiling=Commit + Best Case; Total Pipeline for coverage visibility
10. **Apply manager adjustments** — Document every override with rationale
11. **Cross-validate against historical trending** — Variance >20% requires written explanation
12. **Submit to Finance/CFO** — Include pipeline coverage ratio, weighted pipeline, category breakdown, risk commentary

**Phase 4 — Post-Period Measurement**
13. **Calculate accuracy metrics** — Point-in-time: 1 − |Forecast − Actual| / Actual; MAPE across segments; WMAPE for multi-segment orgs; bias detection: persistent positive = sandbagging, persistent negative = happy ears
14. **Conduct forecast retrospective** — Identify slipped/pulled-in/changed deals; map causes to process failures (poor qualification, optimistic staging, missing stakeholders)

## Glossary

| Term | Definition |
|---|---|
| Pipeline-Weighted Forecast | Sum of (Deal Value × Stage-Based Win Probability) across all active opportunities |
| Commit | ≥90% confidence deals with mutual close plan, confirmed timeline, known approval chain, scheduled next milestone |
| Best Case | Fully qualified deals with close plan but unresolved risk; 33-50% expected to close within period |
| Pipeline | Early-stage/uncertain deals; ~25% expected to close within quarter |
| Day One Forecast | First forecast at period start; immutable baseline for accuracy measurement per Forrester |
| MAPE | Mean Absolute Percentage Error: average of |Forecast − Actual| / Actual across segments |
| WMAPE | Weighted MAPE: Σ|Forecast_i − Actual_i| / ΣActual_i; weights errors by revenue magnitude |
| Pipeline Coverage Ratio | Total open pipeline ÷ remaining quota; enterprise benchmark 3×-5× |
| Forecast Coverage | Weighted pipeline (probability-adjusted) ÷ quota; more realistic than raw coverage |
| Slip Rate | % of Commit deals failing to close within forecast period; pushed to next quarter |
| Sandbagging | Systematic under-forecasting by withholding deals or suppressing to Best Case/Pipeline; inflates beat rates |
| Happy Ears | Over-forecasting by promoting deals to Commit based on verbal signals without confirming process/budget/procurement |
| Stage Velocity | Average days per pipeline stage; anomalies signal stalled deals or process breakdowns |
| Deal Aging | Time elapsed in current stage; >1.5× median = elevated risk |
| Economic Buyer (EB) | Individual with discretionary budget authority to approve; distinct from Champion |
| Champion | Internal advocate with power/influence who actively sells on your behalf; must have EB access and personal win |
| Paper Process | Procurement/legal/admin steps between verbal agreement and signed contract; includes security review, PO |
| Bottoms-Up Forecast | Aggregated individual rep forecasts rolled through management layers to company total |
| Top-Down Forecast | TAM × expected market share decomposed into regional/rep targets; sanity check only |
| Rolling Forecast | Continuously updated projection adding new forward period as each period closes |
| Forecast Bias | Systematic over/under-forecasting; positive = sandbagging; negative = happy ears |
| Manager Override | Adjustment applied by manager to rep-level forecasts based on experience or deal-level intelligence |
| Close Plan | Documented mutual agreement on steps, owners, and timeline to complete transaction |
| Quota Gap | Quota target minus Closed-Won to date; drives urgency and pipeline generation requirements |

## Checklist

- [ ] Stage probabilities recalibrated using actual prior-quarter conversion data, not vendor defaults
- [ ] Day One forecast snapshot recorded and immutable for accuracy measurement
- [ ] Every Commit-category deal has confirmed Economic Buyer, mutual close plan, and initiated paper process
- [ ] Pipeline coverage ratio within acceptable range per segment (3×-5× enterprise; 2.5×-4× mid-market)
- [ ] Forecast submitted as a range (Commit floor / Target / Best Case ceiling), not a single number
- [ ] Accuracy measured by segment (region, BU, revenue type) — not just aggregate
- [ ] Deal aging alerts configured — opportunities exceeding 1.5× median stage duration flagged
- [ ] Manager overrides documented with written rationale for every adjustment >5% of team total
- [ ] Forecast-to-revenue mapping validated with Finance — bookings reconciled to ASC 606 recognition schedule
- [ ] Close date distribution analyzed — <20% of pipeline carrying quarter-end date without procurement justification
- [ ] Bias tracking active — individual rep over/under-forecast trends monitored across ≥3 periods
- [ ] Weekly forecast call cadence maintained with standardized Commit inspection protocol
- [ ] Historical trending cross-validation performed — current forecast vs. same-quarter prior year ± growth rate
- [ ] Partner/channel pipeline separated and weighted at segment-specific conversion rates (typically 40-60% of direct)
- [ ] Currency impact isolated for international forecast rollups — FX variance excluded from sales execution accuracy

## References
Xactly 2024 Sales Forecasting Benchmark Report; Forrester/SiriusDecisions Forecast Accuracy Framework; MEDDPICC (PTC 1996); ASC 606 / IFRS 15; PSLRA Safe Harbor 15 USC §78u-5; SEC Reg S-K Item 10(b); SOX §302/§906; Salesforce Forecast Categories; Salesforce Einstein; Clari; Gong; Deloitte 2024 (ML improves accuracy ≤30%); Gartner ($12.9M poor data quality cost)
