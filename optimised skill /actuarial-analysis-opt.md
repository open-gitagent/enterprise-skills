---
name: actuarial-analysis
description: >
  Actuarial science applications in insurance including loss reserving, rate making, experience rating, and predictive modeling for risk pricing.
metadata:
  vertical: bfsi-insurance
  function: analytics
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "SOA, CAS, ASOP"
---

## Role
Apply actuarial methods (reserving, rate making, experience rating, predictive modeling) within ASOP/NAIC/state frameworks to quantify and price insurance risk.

## Decision Framework

| Decision | Criteria |
|----------|----------|
| Data sufficiency | ASOP No. 23: completeness, consistency, reasonableness, appropriateness before method selection |
| Short-tail / high-frequency | Chain-Ladder (paid + incurred); factors stabilize 24–36 months |
| Long-tail / low-frequency | Bornhuetter-Ferguson or Cape Cod; pure chain-ladder too volatile for immature years |
| Catastrophe-exposed | Frequency-severity + CAT loading (ASOP No. 38); stochastic supplements deterministic |
| Credibility weighting | ASOP No. 25: limited fluctuation or Bühlmann; full credibility = 1,082-claim threshold (90% conf., ±5%, Poisson) |
| Predictive model governance | ASOP No. 56 (eff. Oct 2020): selection, inputs, validation, documentation, reliance on third-party models |

## ASOP Table

| ASOP | Title | Key Requirement |
|------|-------|----------------|
| No. 12 | Risk Classification | Variables must relate to expected outcomes; prohibit unfair discrimination |
| No. 23 | Data Quality | Assess completeness, reasonableness, appropriateness before relying |
| No. 25 | Credibility Procedures | Blend observed experience with prior expectations |
| No. 30 | P/C Rate Making | Comprehensive ratemaking methodology |
| No. 36 | SAO — P/C Loss Reserves | Appointed actuary opinion requirements |
| No. 38 | Catastrophe Modeling | Consider range of outcomes; not single point estimates |
| No. 41 | Actuarial Communications | Document and disclose material assumptions |
| No. 43 | P/C Unpaid Claim Estimates | Methodology standards for unpaid claims |
| No. 56 | Modeling | Governance, validation, documentation for all models |

## NAIC & State Regulatory Requirements

| Requirement | Key Detail |
|-------------|-----------|
| Model Law 822 | Annual SAO from appointed actuary; Actuarial Report + Opinion Summary required |
| IRIS Ratios 2024 | Ratio 11 (1-yr reserve dev/PHS) >20% = unusual; Ratio 12 (2-yr) >20%; Ratio 13 (deficiency/PHS) >25% |
| AI Model Bulletin Apr 2024 | Governance, bias testing, human oversight for AI in pricing/underwriting/claims |
| CASTF Model Review Manual 2025 | Documentation, variable justification, validation, disparate impact for predictive rate filings |
| AOWG Guidance 2024/2025 | Annual opinion requirements, materiality, RMAD disclosure |
| Colorado SB21-169 | Test algorithms for unfair discrimination; governance frameworks; eff. Nov 2023 |
| NY DFS Circular Letter No. 7 (2024) | Actuarial justification, non-discrimination testing, consumer transparency for AI/external data |
| IFRS 17 (eff. Jan 2023) | Current-value measurement: best estimate cash flows + risk adjustment + contractual service margin |

## Process

### Loss Reserving
1. Construct loss development triangles by accident/report/policy year; separate paid, incurred, case reserves, claim counts, ALAE/ULAE
2. Calculate link ratios; identify outliers; plot residuals for calendar-year, accident-year, or development-period effects
3. Run minimum 3 methods: paid chain-ladder, incurred chain-ladder, Bornhuetter-Ferguson; add frequency-severity, Cape Cod, Berquist-Sherman for long-tail
4. Weight methods by accident year maturity; document rationale for every selection
5. IBNR = Selected Ultimate − (Paid + Case Reserves); decompose into pure IBNR, IBNER, reopened claims
6. Reasonableness testing: loss ratios, severity/frequency trends, IRIS Ratio 11/12 tests
7. Issue opinion under Model Law 822: Reasonable / Qualified / Adverse / No Opinion; attach RMAD analysis

### Rate Making
1. Adjust historical premiums to current rate level (parallelogram or extension of exposures); adjust losses for benefit changes and trend
2. Project losses to ultimate; apply prospective loss trend (frequency × severity) to midpoint of future policy period
3. Determine fixed and variable expense provisions; account for commission gradients
4. Apply target combined ratio or return on allocated surplus; incorporate investment income offset where permitted
5. Indicated rate change: loss ratio method or pure premium method
6. Fit GLM (Tweedie/Poisson-gamma) for class/territory relativities; validate with holdout, lift curves, Gini coefficients
7. Prepare actuarial memorandum with certification; include model documentation, variable justification, disparate impact analysis per CASTF Manual

### Experience Rating (NCCI Workers' Comp)
1. Select 3-year experience period excluding most recent policy year
2. Apply per-claim split point to separate frequency from severity; NCCI current split point: $18,500
3. Multiply payroll exposure by class-specific expected loss rate for primary and excess expected losses
4. Weight actual vs. expected primary losses (higher credibility) and excess losses separately
5. EMF = Actual weighted losses / Expected losses; >1.00 = adverse; <1.00 = better than average
6. Verify classification codes, payroll audits, claim data; dispute incorrect mods

### Predictive Modeling
1. Engineer features; address multicollinearity, missing values, categorical encoding
2. Start with GLM as regulatory baseline; add GAM/GBM/random forest where lift justifies regulatory burden
3. Temporal validation (not random k-fold); walk-forward for frequency and severity separately
4. Per NAIC AI Bulletin Apr 2024 + Colorado SB21-169: test for proxy discrimination; calculate disparate impact ratios; apply CAS Race and Insurance Pricing research
5. Convert predictions to rating relativities; avoid double-counting vs. experience/schedule rating
6. Maintain model inventory per ASOP No. 56; document limitations and degradation conditions

## Evaluation Criteria

| Criterion | Weight | Method |
|-----------|--------|--------|
| Data quality & completeness | 15% | ASOP 23 checklist; triangle diagnostics |
| Method appropriateness | 20% | Alignment with data maturity, line, tail length |
| Assumption reasonableness | 20% | Sensitivity ranges; ISO/NCCI/A.M. Best benchmarks |
| Regulatory compliance | 15% | ASOP conformance; state filing; NAIC opinion standards |
| Predictive accuracy | 15% | Out-of-sample loss ratios; Gini; lift; calibration plots |
| Documentation quality | 10% | ASOP 41 compliance; reproducibility |
| Fairness/non-discrimination | 5% | Disparate impact testing; proxy variable analysis |

## Glossary

| Term | Definition |
|------|-----------|
| IBNR | Reserve for claims occurred but not reported; includes IBNER and pure IBNR |
| Chain-Ladder | Deterministic reserving projecting ultimate losses via age-to-age development factors |
| Bornhuetter-Ferguson (B-F) | Combines a priori expected loss ratio with actual emerged experience; IBNR = Expected Ultimate × (1 − % Emerged) |
| Loss Development Factor (LDF) | Multiplicative factor projecting losses at given maturity to ultimate |
| On-Leveling | Adjust historical premium to current rate level using parallelogram method |
| Experience Modification Factor (EMF) | Individual risk loss experience vs. class average; multiplied to manual premium |
| Split Point | Dollar threshold separating primary (frequency) from excess (severity) losses; NCCI: $18,500 |
| Credibility | Actuarial measure (0–1) of predictive value; full credibility (Z=1) means data alone sufficient |
| Bühlmann Credibility | Z = n / (n + k); minimizes expected squared error |
| GLM | Generalized Linear Model; extends regression to Poisson/gamma/Tweedie for pricing |
| Tweedie Distribution | Compound Poisson-gamma for aggregate pure premium; handles zero-claim mass |
| Loss Ratio Method | Indicated rate change = (projected loss & LAE ratio + fixed expense ratio) / (1 − variable expense − profit) − 1 |
| Pure Premium Method | Indicated rate = (projected pure premium + fixed expense) / (1 − variable expense − profit) |
| RMAD | Risk of Material Adverse Deviation; assessed and disclosed in actuarial opinion |
| Appointed Actuary | Board-designated actuary meeting NAIC qualification standards to render statutory opinion |
| ULAE | Unallocated Loss Adjustment Expense — claims overhead not attributable to specific claims |
| Tail Factor | Development factor beyond last observable maturity; most judgmental assumption in long-tail reserving |
| Cape Cod Method | Derives a priori loss ratio from data itself using on-level earned premium (Stanard-Bühlmann) |
| Berquist-Sherman | Adjusts triangles for changes in settlement rates or case reserve adequacy |
| Disparate Impact Testing | Quantitative analysis for disproportionate effect on protected classes |
| Gini Coefficient | Measures model discriminatory power from ordered Lorenz curve; higher = better risk separation |
| Schedule Rating | Subjective premium modification ±25%–±40% for characteristics not in manual rates |
| Loss Cost Multiplier (LCM) | Applied to advisory organization loss costs to produce insurer's final rate |

## Checklist

- [ ] Triangle homogeneity verified — no mixed occurrence/claims-made, no merged sub-lines, discontinuities identified
- [ ] Minimum 3 reserving methods applied with rationale documented by accident year and weighting basis
- [ ] ASOP No. 23 data quality assessment documented — limitations, deficiencies, third-party reliance acknowledged
- [ ] Loss trend and development factor selections supported — not merely "5-year weighted average" without diagnostic justification
- [ ] On-leveling verified with independent premium calculation using documented rate change history
- [ ] Predictive model validated on out-of-time holdout with Gini, lift, calibration metrics by key segments
- [ ] Disparate impact analysis completed for any predictive model or new rating variable; remediation plan if thresholds exceeded
- [ ] ASOP No. 56 model documentation maintained — version, training data, features, validation results, limitations
- [ ] Experience rating data reconciled to audited policy records and verified claim files
- [ ] Appointed actuary qualification confirmed — Fellow of CAS or FSA with NAIC-mandated CE
- [ ] RMAD assessment explicitly addressed with quantitative support per AOWG Regulatory Guidance
- [ ] Sensitivity testing documented — trend, tail factors, CAT loads, discount rates varied with impact quantified
- [ ] Regulatory filing requirements met — memorandum format, exhibits, certification, predictive model supplements
- [ ] Calendar-year vs. accident-year basis correctly applied without cross-contamination

## References
NAIC AOWG 2024/2025 Regulatory Guidance, NAIC Model Law 822, NAIC IRIS Ratios Manual 2024, NAIC AI Model Bulletin Apr 2024, NAIC CASTF Model Review Manual 2025, ASB ASOPs 12/23/25/30/36/38/41/43/56, CAS Statement of Principles on Ratemaking, CAS Race and Insurance Pricing Research, CAS Fairness in Insurance Pricing Guide 2024, CAS GLM for Insurance Rating, AAA P/C Loss Reserve Law Manual 2024, Colorado SB21-169, NY DFS Circular Letter No. 7 (2024), NCCI ABCs of Experience Rating, IFRS 17 CAS Research Paper
