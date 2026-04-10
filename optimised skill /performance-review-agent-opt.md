---
name: performance-review-agent
description: >
  Monitors and scores vendor performance through KPI tracking, SLA compliance measurement, quality metrics analysis, and continuous improvement programs.
metadata:
  vertical: procurement
  function: supplier/vendor-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "ISO 9001, Six Sigma, CIPS"
---

## Role
Measure, score, and improve supplier performance via weighted KPI scorecards, structured governance reviews, and corrective action programs aligned to Kraljic segmentation.

## Supplier Segmentation & Review Intensity

| Kraljic Quadrant | Profile | Review Frequency | KPI Count | Escalation Threshold |
|---|---|---|---|---|
| Strategic | High profit impact + high supply risk | Monthly scorecard + Quarterly QBR | 10-15 | Score <80% → executive review |
| Bottleneck | Low profit impact + high supply risk | Monthly scorecard | 8-10 | Score <75% → supply assurance plan |
| Leverage | High profit impact + low supply risk | Quarterly scorecard | 6-8 | Score <70% → sourcing re-competition |
| Routine | Low profit impact + low supply risk | Semi-annual scorecard | 3-5 | Score <65% → supplier replacement |

## Composite Score Tier Classification

| Score | Tier | Action |
|---|---|---|
| 90-100 | Preferred Supplier | Eligible for volume growth, sole-source consideration |
| 80-89 | Approved Supplier | Meets expectations; maintain current allocation |
| 70-79 | Conditional Supplier | PIP required within 30 days |
| 60-69 | Probationary Supplier | SCAR issued; sourcing alternatives actively pursued |
| <60 | Disqualified | Exit plan initiated; no new POs issued |

## KPI Category Weights

| Category | Typical Weight | Key KPIs |
|---|---|---|
| Quality | 25-35% | Defect PPM/DPMO, first-pass yield ≥98%, CoC accuracy, warranty claim rate |
| Delivery | 20-30% | OTIF ≥95%, lead time variance ≤5%, ASN accuracy, expedite frequency |
| Cost | 15-25% | TCO trend, price variance to contract, cost-reduction attainment, invoice accuracy ≥99% |
| Service & Responsiveness | 10-20% | RFQ response ≤3 biz days (≤1 day expedite), issue resolution time, communication quality (1-5) |
| Compliance & Risk | 5-15% | Regulatory/labor/cyber/insurance compliance, financial stability (D&B/Z-score) |
| Innovation | 0-10% | Implemented VE proposals, process improvements, new technology adoption (score on implemented only) |

## Quantitative KPI Benchmarks

| Metric | Formula | Target | Source |
|---|---|---|---|
| OTIF | Orders on-time AND in-full / Total orders × 100 | ≥95% | ISM |
| Defect Rate (PPM) | Defective units / Total units received × 1,000,000 | <500 PPM | IATF 16949 norm |
| Perfect Order Rate | On-time + In-full + Damage-free + Correct docs / Total orders × 100 | ≥90% | SCOR RL.1.1 |
| First-Pass Yield | Units passing inspection without rework / Total units × 100 | ≥98% | Lean/Six Sigma |
| Invoice Accuracy | Invoices matching PO price+qty / Total invoices × 100 | ≥99% | AP benchmark |
| Fill Rate | Qty shipped / Qty ordered × 100 | ≥97% | ISM |
| Lead Time Variance | (Actual − Quoted) / Quoted × 100 | ≤5% | Contract terms |
| SCAR Response | Biz days SCAR issuance → D3 containment | ≤5 biz days | Internal SOP |
| RFQ Turnaround | Biz days RFQ issuance → supplier quote | ≤3 biz days standard; ≤1 day expedite | Category-dependent |

## SCOR DS Level 1 Metrics

| SCOR Code | Metric | Definition |
|---|---|---|
| RL.1.1 | Perfect Order Fulfillment | OTIF + complete documentation + damage-free delivery |
| RS.1.1 | Order Fulfillment Cycle Time | End-to-end from PO placement to goods receipt |
| AG.1.1 | Upside Supply Chain Flexibility | Ability to increase supply 20% within 30 days |
| CO.1.1 | Total Cost to Serve | Procurement + logistics + quality cost + risk cost |
| AM.1.1 | Cash-to-Cash Cycle Time | Working capital impact of payment terms |

## Process

**Phase 1 — KPI Architecture (Pre-Contract/Renewal)**
1. Classify supplier using Kraljic quadrant: map spend data against supply risk (sole-source dependency, geographic concentration, lead time volatility)
2. Select KPIs from master catalog based on quadrant; never apply strategic scorecard to routine supplier
3. Define measurement methodology per KPI: data source (SAP MM/SRM, Oracle Procurement Cloud, Coupa), formula, frequency, threshold
4. Embed KPIs in contract: metric definition, measurement method, cadence, target, tolerance, penalty/incentive, dispute resolution
5. Establish 90-day baseline before activating penalty/incentive clauses on new suppliers

**Phase 2 — Data Collection & Scoring (Ongoing)**
6. Automate transactional capture: configure ERP to log delivery timestamps, GR/IR matching, quality inspection results at goods receipt
7. Calculate KPI scores monthly; flag data gaps/anomalies before scoring (e.g., retroactive PO date manipulation masking late deliveries)
8. Apply weighted scoring model: multiply each KPI score by category weight; generate composite score
9. Generate trend analysis: current period vs. rolling 3-/6-/12-month averages; flag deviations >2 SD from mean
10. Distribute scorecard ≤10 biz days after period close

**Phase 3 — Review & Action (Periodic Governance)**
11. QBR format for Strategic/Bottleneck; written scorecard delivery for Leverage/Routine
12. Traffic-light escalation protocol:
    - Green (≥80): acknowledge, discuss improvement opportunities, review innovation pipeline
    - Yellow (70-79): written corrective action plan ≤15 biz days; 30-day follow-up scheduled
    - Red (<70): formal SCAR via 8D methodology; root cause analysis D1-D8 ≤10 biz days; weekly procurement sponsor tracking
13. Document meeting minutes, action items with owners/due dates in SRM system

**Phase 4 — Corrective Action & Continuous Improvement**
14. Track SCAR closure: verify D3 containment, D4 root cause, D6 corrective action implementation, D7 effectiveness validation
15. Require 3 consecutive measurement periods at/above target before removing probationary status
16. Invest in joint improvement for Strategic suppliers scoring 70-85: Kaizen events, process mapping workshops, shared demand forecasting
17. Update tier classification; update ASL based on 12-month rolling composite score
18. Report to executive procurement: spend-at-risk, quality cost trends, savings attainment by category

## Glossary

| Term | Definition |
|---|---|
| OTIF | On-Time In-Full — on-time AND complete quantity; measured vs. original requested date, not supplier-confirmed date |
| PPM | Parts Per Million defects; 500 PPM = 0.05% defect rate |
| DPMO | Defects Per Million Opportunities; Six Sigma metric accounting for multiple defect types per unit |
| SCAR | Supplier Corrective Action Request — formal 8D investigation + corrective action + effectiveness evidence |
| 8D Methodology | D1 Team / D2 Problem Description / D3 Containment / D4 Root Cause / D5 PCA Selection / D6 Implementation / D7 Prevention / D8 Recognition |
| QBR | Quarterly Business Review — structured governance meeting with supplier leadership on scorecard/improvement/strategy |
| Kraljic Matrix | 2×2 framework (Peter Kraljic, 1983): profit impact × supply risk → Strategic/Bottleneck/Leverage/Routine |
| TCO | Total Cost of Ownership: unit price + freight + duties + quality costs + inventory carrying + admin costs |
| Perfect Order Rate | SCOR RL.1.1 — on-time + in-full + damage-free + correct documentation |
| Cpk | Process Capability Index; ≥1.33 = capable; <1.0 = non-capable |
| ASL | Approved Supplier List: Preferred/Approved/Conditional/Probationary/Disqualified status designations |
| GR/IR | Goods Receipt / Invoice Receipt — ERP three-way match; discrepancies = delivery or billing accuracy issues |
| SRM | Supplier Relationship Management — strategy and software for full supplier lifecycle management |
| CoC | Certificate of Conformance — supplier self-attestation; not equivalent to third-party inspection |
| Lead Time Variance | (Actual − Quoted) / Quoted × 100; chronic positive variance = supplier capacity/planning problems |
| Fill Rate | Qty shipped / Qty ordered on first shipment; distinct from OTIF (quantity completeness vs. time+quantity) |
| Spend-at-Risk | Dollar value of spend managed by Conditional/Probationary-tier suppliers; key executive dashboard metric |
| PIP | Performance Improvement Plan — formal time-bound document: underperformance areas/targets/milestones/consequences |
| Gain-Sharing | Contractual cost savings sharing buyer/supplier (typically 50/50 or 60/40) to incentivize CI |
| CPARS | Contractor Performance Assessment Reporting System — U.S. federal past performance system (FAR 42.15) |
| Premium Freight | Expedited shipping from supplier late delivery; direct indicator of delivery failure cost |
| Category Management | Procurement organized by spend category; enables peer-group supplier benchmarking |
| Kaizen Event | 3-5 day focused improvement workshop at supplier facility to reduce waste in specific process |
| SCOR DS | Supply Chain Operations Reference Digital Standard — ASCM framework (formerly APICS/SCC); 250+ metrics |

## Checklist

- [ ] Every scored KPI has corresponding contract/SLA definition; no orphan metrics outside contractual scope
- [ ] KPI data sourced from system-of-record (ERP/QMS/TMS), not supplier self-reporting, for penalty/incentive calculations
- [ ] Kraljic classification reviewed within 12 months; reflects current spend, supply market conditions, business criticality
- [ ] Scorecard category weights documented with rationale linked to business strategy
- [ ] New suppliers have documented 90-day baseline before penalty/incentive clauses activate
- [ ] Scorecards include rolling 3-/6-/12-month trend data alongside current period
- [ ] Scorecards distributed ≤10 biz days after period close; QBR invitations ≥15 biz days in advance with pre-read materials
- [ ] Every open SCAR documented through all 8D stages; no SCAR >90 days at D3 without escalation
- [ ] Executive dashboards weight supplier scores by spend or risk classification (not simple average across all suppliers)
- [ ] Every sole/single-source supplier scoring <85% has documented alternate sourcing plan with qualification timeline
- [ ] Qualitative ratings (1-5) include written rubrics with examples; inter-rater variance ≤1 point
- [ ] Minimum 3 years scorecard history retained per supplier (ISO 9001:2015 Clause 7.5)
- [ ] Strategic/Bottleneck scorecards incorporate input from quality, operations, engineering, and procurement
- [ ] PIP improvement requires objective data evidence for ≥3 consecutive measurement periods before status upgrade
- [ ] Financial penalty/volume reallocation has auditable trail from raw transaction data through calculation to final score

## References
ISO 9001:2015 Clause 8.4.1/8.4.2/8.4.3; IATF 16949:2016 §8.4.2.3/8.4.2.4; SCOR DS (ASCM, formerly APICS/SCC); FAR Subpart 42.15 §42.1502 (>$750K services / >$1M supplies) §42.1503 (CPARS ≤120 days); ISO 14001:2015; SA8000; ISO 28000; ISM; CIPS; Kraljic Matrix (1983)
