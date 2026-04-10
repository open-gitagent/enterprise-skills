---
name: qualification-scoring-agent
description: >
  Evaluates vendor capabilities and reliability through structured scoring frameworks, financial health checks, reference verification, and capability assessments.
metadata:
  vertical: procurement
  function: supplier/vendor-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "ISO 9001, CIPS, ISM"
---

## Role
Convert supplier impressions into defensible quantitative ratings via gate screening, weighted multi-criteria scoring, and reference verification to drive sourcing decisions.

## Tier-Based Qualification Depth

| Tier | Profile | Qualification Scope | Minimum Score |
|---|---|---|---|
| Tier 1 (Critical/Strategic) | Sole/single-source, custom-engineered, regulated materials | On-site audit, financial deep-dive, independent references, capability study, ESG assessment | ≥80/100; no category <70% |
| Tier 2 (Leverage/Preferred) | Multiple sources; material switching costs | Structured questionnaire, desktop financial review, supplier references, cert verification | ≥70/100 |
| Tier 3 (Routine/Transactional) | Commodity, many sources | Automated prequalification, cert check, basic financial flag | ≥60/100 |

## Gate Criteria (Pass/Fail — Stage 1)

| Gate | Requirement |
|---|---|
| Business registration | Valid licensing current |
| Certifications | ISO 9001, AS9100D, IATF 16949 (where required) — current |
| Sanctions | No presence on OFAC SDN list or equivalent |
| Debarment | No active debarment (SAM.gov; EU exclusion databases) |
| Financial viability | D&B PAYDEX ≥50 OR current ratio >1.0 |
| Insurance | Meets contract minimums |
| Enforcement | No unresolved regulatory enforcement actions ≤24 months |

## Weighted Scoring Model (Stage 2)

| Category | Typical Weight | Key Metrics |
|---|---|---|
| Quality & Technical Capability | 25–35% | Defect rates, Cpk values, certifications, technical staff |
| Financial Health | 15–25% | PAYDEX, Failure Score, current ratio, revenue trend, credit limit |
| Delivery & Operational Capacity | 15–25% | OTIF %, lead time reliability, surge capacity, utilization |
| Cost/TCO Competitiveness | 10–20% | Unit price vs. benchmark, TCO, payment terms |
| Risk & Compliance | 10–15% | Geographic risk, single-point-of-failure, regulatory history |
| ESG & Sustainability | 5–15% | EcoVadis score, carbon targets, labor practice audits |
| Innovation & Digital Maturity | 5–10% | R&D investment, EDI/API capability, collaborative planning |

## Scoring Rubric Anchors

| Score | Quality/Technical | Financial Health | Delivery/Capacity |
|---|---|---|---|
| 5 | ISO-certified, defect <0.5%, Cpk >1.67, active CI program | PAYDEX ≥80, low D&B Failure Score, current ratio >2.0, CAGR >10% | OTIF >98%, 30%+ surge capacity, <2% LT variance |
| 4 | ISO-certified, defect <1%, Cpk >1.33, CI in place | PAYDEX 70-79, mod-low risk, current ratio 1.5-2.0, stable revenue | OTIF 95-98%, 20% surge, <5% LT variance |
| 3 | ISO-certified, defect <2%, meets spec | PAYDEX 60-69, mod risk, current ratio 1.0-1.5, flat revenue | OTIF 90-95%, 10% surge, <10% LT variance |
| 2 | Cert pending/expired, defect 2-5%, reactive QA | PAYDEX 50-59, mod-high risk, current ratio 0.8-1.0, declining | OTIF 80-90%, limited surge, occasional failures |
| 1 | No QMS, defect >5%, no process controls | PAYDEX <50, high risk, current ratio <0.8, significant losses | OTIF <80%, no surge capacity, frequent failures |

## Decision Thresholds

| Score | Status | Action |
|---|---|---|
| ≥80/100; no category <70% | Qualified (Green) | Add to AVL; proceed |
| 65-79, or one category 50-69% with CAP | Conditionally Qualified (Amber) | Define corrective actions, deadlines, recheck date |
| <65; any gate failure; any category <50% | Disqualified (Red) | Notify with deficiency; one cure period for correctable items |

## Process

1. **Scope & Classification** — Map commodity/service to Kraljic quadrant; select qualification tier; assemble cross-functional team (procurement, quality/engineering, finance, legal, operations)
2. **Configure Scoring Model** — Select 5-8 weighted criteria; lock weights before any supplier data reviewed; run evaluator calibration session; document rubric anchors per score level
3. **Issue Prequalification Questionnaire (PQQ)** — Distribute: legal entity, ownership structure, certifications, 3-year financials, insurance, references, capacity data, ESG policies, cybersecurity, BCP; hard deadline, no extensions
4. **Execute Gate Screening** — OFAC SDN, SAM.gov, World Bank Debarment, EU sanctions; verify certs with issuing bodies (not supplier PDFs); pull D&B/Experian Intelliscore; one cure period for correctable gate failures
5. **Conduct Detailed Scoring** — Evaluators independently score per locked rubric; financial sub-score: PAYDEX 30%/Failure Score 20%/balance sheet ratios 30%/revenue trend 20%; flag >2-point evaluator divergence for consensus discussion
6. **Verify References & Site Visits** — Tier 1: ≥3 references (min 2 not nominated by supplier); on-site audit (production floor, quality lab, warehouse, management system docs); Tier 2: ≥2 references; reference questionnaire: volume, quality, crisis behavior, responsiveness, hidden costs, would-you-requalify
7. **Compile Qualification Decision** — Generate composite score with category breakdowns; apply thresholds; Conditionally Qualified = specific CARs + deadlines + recheck; submit per delegation of authority matrix
8. **Establish Requalification Cadence** — Tier 1: annual full requalification + quarterly scorecard; Tier 2: biennial + semi-annual check; Tier 3: triennial (triggered earlier by quality escape/delivery failure); continuous D&B/cert/sanctions alerts

## Glossary

| Term | Definition |
|---|---|
| AHP | Analytic Hierarchy Process; pairwise-comparison method for defensible weight allocation; produces consistency ratio |
| AVL | Approved Vendor List; registry of qualified suppliers authorized for purchase orders |
| Carter's 10Cs | Ray Carter (CIPS/ISM): Competency, Capacity, Commitment, Control, Cash, Cost, Consistency, Culture, Clean, Communication |
| Composite Score | Weighted sum of criterion scores × assigned weights; typically 0-100 scale |
| Cpk | Process Capability Index; ≥1.33 = capable; ≥1.67 = highly capable |
| DEA | Data Envelopment Analysis; benchmarks suppliers against each other on output-to-input ratios |
| D-U-N-S Number | 9-digit D&B identifier; required for PAYDEX, Failure Score, and SER Rating pulls |
| EcoVadis | Third-party sustainability rating (0-100): environment, labor, ethics, sustainable procurement |
| FAI | First Article Inspection; verifies first production unit meets all specs; gates qualification-to-production |
| Gate Criteria | Binary pass/fail prerequisites; failure eliminates regardless of scored strengths |
| Kraljic Matrix | 2×2: supply risk × profit impact → Strategic/Bottleneck/Leverage/Routine |
| OTIF | On-Time In-Full; measured vs. original requested date; benchmark ≥95% |
| PAYDEX | D&B dollar-weighted payment timeliness score (0-100); 80+ = prompt; <50 = high risk; requires ≥10 trade experiences for reliability |
| PQQ | Prequalification Questionnaire; primary data collection instrument for qualification scoring |
| SER Rating | Supplier Evaluation Risk; D&B metric predicting likelihood of insolvency/cessation within 12 months |
| SSI | Supplier Stability Index; D&B 90-day financial stress probability |
| TCO | Total Cost of Ownership: unit price + freight + duties + quality costs + inventory carrying + admin |
| Weighted Scoring Matrix | Criterion score × weight → summed composite; standard multi-criteria evaluation method |

## Checklist

- [ ] Gate criteria defined and applied before any scored evaluation; no gate-failed supplier received composite score
- [ ] Weights locked, documented, distributed to all evaluators before supplier data reviewed
- [ ] Evaluator calibration session conducted with documented score-level definitions per criterion
- [ ] Sanctions screening: OFAC SDN, SAM.gov, World Bank Debarment, applicable regional lists — screenshot evidence retained
- [ ] Certifications verified with issuing body or public registry (not solely supplier-provided documents)
- [ ] Financial assessment includes ≥1 external source (D&B, Experian, or equivalent) beyond supplier self-reported financials
- [ ] PAYDEX validated for ≥10 trade experiences; fewer flagged as "insufficient data" requiring additional documentation
- [ ] Reference checks include ≥1 client not nominated by supplier
- [ ] Reference interviews followed structured questionnaire: volume, quality, crisis behavior, requalification intent
- [ ] Evaluator divergences >2 points on any criterion resolved through documented consensus discussion
- [ ] Composite score spot-checked: weight × score per criterion, summed, averaged across evaluators
- [ ] Conditionally Qualified suppliers have documented corrective action plan with specific deadlines
- [ ] Requalification cadence entered in tracking system with automated reminder triggers
- [ ] Qualification package contains complete audit trail: PQQ responses, gate screening, evaluator scorecards, reference notes, financials, approval sign-offs
- [ ] Sub-tier supplier risk assessed for Tier 1 strategic suppliers; critical sub-suppliers flagged for qualification extension

## References
ISO 9001:2015 Clause 8.4; ISO 14001:2015; AS9100D; IATF 16949:2016; OFAC SDN; FCPA; UK Bribery Act 2010 §7; EU CSDDD 2024; FAR Part 9; SAM.gov; USP <1083>; FDA 21 CFR Part 820; NADCAP; GMP; D&B PAYDEX/Failure Score/SER Rating/SSI; EcoVadis; CIPS; ISM; Kraljic Matrix (1983)
