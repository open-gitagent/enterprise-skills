---
name: credit-risk-assessment
description: >
  Credit risk evaluation methodology including probability of default modeling, loss given default estimation, and credit scoring frameworks.
metadata:
  vertical: bfsi-banking
  function: risk-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "Basel III, IFRS 9, CECL"
---

## Role
Quantify credit risk through PD/LGD/EAD modeling, portfolio concentration management, and fair lending compliance under Basel III/CECL/ECOA frameworks.

## Decision Framework (3 Layers)

### Layer 1: Borrower-Level Risk Quantification

| Parameter | Definition | Basel III IRB Floor |
|-----------|-----------|-------------------|
| PD (Probability of Default) | Likelihood borrower defaults within specified period (typically 1 year); derived from migration analysis | 5 basis points |
| LGD (Loss Given Default) | % of exposure unrecoverable after default, net of all recoveries | 5% (financial collateral); 25% (unsecured corporate); 10% portfolio floor (residential mortgages) |
| EAD (Exposure at Default) | Total outstanding at moment of default; revolving = drawn + 50% undrawn using CCFs | On-balance-sheet exposure + 50% off-balance-sheet |

**ECL = EAD × PD × LGD**

### Layer 2: Portfolio-Level Risk Management

| Threshold | Source | Trigger |
|-----------|--------|---------|
| Construction/land dev ≥100% of Tier 1 Capital + ACL | FDIC FIL-23064 / 2006 Interagency CRE Guidance | Enhanced supervisory scrutiny |
| Total CRE ≥300% of Tier 1 Capital + ACL + 50% growth over 36 months | Same | Heightened scrutiny |
| Single-borrower limit: 15% of unimpaired capital (unsecured); 25% (secured) | 12 USC 84 | Legal lending limit |
| NDFI loans at largest banks: 60% of Tier 1 Capital | FDIC 2025 Risk Review | Emerging concentration risk |

### Layer 3: Compliance & Model Governance
- ECOA/Regulation B (12 CFR 1002.9): specific, accurate adverse action reasons reflecting actual factors scored
- FCRA (15 USC 1681m): adverse action from credit score = disclose score, key factors (≤4), CRA contact information
- SR 11-7/OCC 2011-12: independent model validation; CECL models: every 12–24 months

## Quantitative Benchmarks

| Metric | Typical Threshold | Stress Threshold |
|--------|-------------------|-----------------|
| DSCR (CRE) | ≥1.25× | ≥1.00× under stress |
| LTV (Commercial) | ≤75–80% | Stressed value −20% |
| DTI (Consumer) | ≤43% (QM) | Residual income >$0 |
| PD (Investment Grade) | <0.50% (1-year) | Migration to sub-IG |
| LGD (Secured) | 10–45% by collateral type | Downturn LGD +10–20% |
| Interest Coverage Ratio | ≥2.0× | ≥1.0× under +200bp stress |

## Regulatory Requirements

| Requirement | Key Obligation |
|-------------|---------------|
| ECOA (15 USC 1691) | Prohibits discrimination in credit transactions: race, color, religion, national origin, sex, marital status, age, public assistance, CCPA exercise |
| Regulation B (12 CFR 1002) | §1002.9: adverse action notification within 30 days; §1002.4: prohibited basis; §1002.6: application evaluation rules |
| FCRA (15 USC 1681) | Permissible use of consumer reports; adverse action notice requirements; dispute resolution |
| 12 CFR Part 364, Appendix A | Safety and soundness credit underwriting standards for FDIC-supervised institutions |
| SR 11-7 / OCC 2011-12 | Model Risk Management: validation of conceptual soundness, ongoing monitoring, outcomes analysis |
| 2006 Interagency CRE Guidance | 100%/300% of Tier 1 + ACL concentration thresholds; reaffirmed FDIC FIL-23064 (Dec 2023) |
| 2020 Joint Interagency Policy Statement on ACL | CECL validation requirements; forward-looking estimates mandatory |
| CFPB Circular 2023-03 | Adverse action reasons must reflect actual model factors — not generic checklist items; applies to AI/ML models |
| CFPB Winter 2025 Supervisory Highlights | LDA analysis required for credit scoring models; models >1,000 variables screened for proxy discrimination; adverse action methodology tested |
| CFPB 2024 Fair Lending Report | 4 ECOA referrals to DOJ; 19 ECOA referrals total; no "advanced technology" exception to federal consumer financial laws |
| ASC 326 (CECL) | Lifetime expected credit loss at origination using reasonable and supportable forecasts with reversion to historical data |
| Basel III/IV (BCBS d424) | Standardized and IRB approaches; output floor at 72.5% of standardized RWA |
| BCBS d595 (2025) | Revised Principles for Management of Credit Risk; forward-looking assessment requirements |
| IFRS 9 | Three-stage impairment model for international reporters |

## Process

### Step 1: Application Intake & Data Assembly
Collect borrower financials, credit bureau reports, collateral documentation, purpose of credit. Verify data completeness. Flag incomplete applications for follow-up — do not auto-decline without adverse action analysis.

### Step 2: Creditworthiness Scoring
Apply approved credit scoring model (scorecard, logistic regression, or ML-based). For ML models:
- Document all input variables and theoretical relationship to creditworthiness
- Screen variables for proxy discrimination; models >1,000 features must be tested per CFPB 2025 Supervisory Highlights
- Apply SHAP or LIME interpretability to generate specific adverse action reasons

### Step 3: Collateral Valuation & LTV
Obtain independent appraisals or AVMs (2024 interagency AVM rule requires quality control standards). Calculate LTV with conservative valuation. Stress collateral value under adverse scenarios.

### Step 4: Cash Flow & Capacity Analysis
- Consumer: DTI ratios, residual income, employment stability
- Commercial: DSCR as primary metric; global cash flow for guarantor-dependent credits; stress DSCR under rate increases, revenue declines, cap rate expansion

### Step 5: Risk Rating Assignment
Assign dual internal risk grade (borrower risk + facility risk). BCBS d595 (¶44–45): ratings must cover ALL exposures, not only criticized credits. Validate rating distributions against portfolio migration patterns.

### Step 6: Credit Decision & Structuring
Approve, decline, or counter-offer based on risk-return profile. Pricing must reflect risk grade (OCC 2025: must "meaningfully capture additional risk"). Structure covenants, monitoring triggers, and maturity.

### Step 7: Adverse Action Notice Generation
- Written notice within 30 days of decision (12 CFR 1002.9)
- State specific principal reasons per CFPB Circular 2023-03: "Multiple cash advances exceeding 30% of income in past 60 days" not "credit application incomplete"
- For credit-score-based decisions: include score, range, key factors (≤4), CRA information per FCRA §1681m(a)(2)

### Step 8: Ongoing Monitoring & Portfolio Review
- Track covenant compliance, financial statement updates, credit bureau changes
- Re-rate credits at least annually; watchlist/classified credits more frequently
- Update CECL estimates quarterly with refreshed PD/LGD/EAD and macroeconomic forecasts
- Annual concentration risk analysis against policy limits

## Glossary

| Term | Definition |
|------|-----------|
| PD (Probability of Default) | Estimated likelihood of default within specified period; calculated via migration analysis; Basel IRB floor: 5 basis points |
| LGD (Loss Given Default) | % of exposure unrecoverable after default, net of recoveries |
| EAD (Exposure at Default) | Total outstanding at moment of default including expected future drawdowns via CCFs |
| CECL | FASB ASC 326: lifetime expected credit loss at origination using forward-looking estimates |
| DSCR | Net Operating Income ÷ Total Debt Service; primary CRE repayment capacity metric; minimum 1.20×–1.25× |
| LTV | Loan ÷ Appraised/Market Value; primary collateral coverage metric |
| Adverse Action | Refusal to grant credit, termination, or unfavorable term change (12 CFR 1002.2(c)); triggers mandatory notification |
| LDA (Less Discriminatory Alternative) | Credit model/variable set achieving comparable accuracy with smaller disparities across protected classes; CFPB now expects active search before deployment |
| Q-Factor (Qualitative Adjustment) | Management overlay to quantitative CECL estimates for conditions not in historical data; requires specific documented rationale |
| Risk Rating / Internal Risk Grade | Classification of credit exposure reflecting default probability and loss severity; dual systems rate borrower and facility independently |
| Concentration Risk | Uneven distribution of credit exposures; measured against policy limits and supervisory thresholds |
| Output Floor | Basel III mechanism flooring IRB-calculated RWA at 72.5% of standardized approach |
| CCF (Credit Conversion Factor) | % of off-balance-sheet exposure estimated drawn at default; converts contingent exposures to EAD |
| Migration Analysis | Study of how exposures transition between risk grades over time; primary PD estimation methodology |
| Downturn LGD | LGD calibrated to economic downturn conditions; required under Basel IRB for capital adequacy |
| Effective Challenge | SR 11-7: model validation involving critical analysis by parties with sufficient incentives, competence, and influence to produce actual model changes |
| Watchlist | Credits with early warning signs not yet meeting classified thresholds; triggers enhanced monitoring |
| Vintage Analysis | Tracking loan performance by origination cohort to identify periods of above-average loss |
| Global Cash Flow | Guarantor's/related entity's total debt service across all lending relationships |
| ACL | Allowance for Credit Losses; balance sheet reserve for expected losses under ASC 326 |
| Nonaccrual | Interest income recognition ceases; typically triggered at 90+ days past due or when full repayment not expected |

## Checklist

- [ ] Adverse action notices cite specific, accurate reasons reflecting actual model factors — not generic sample form checklist items
- [ ] CECL model incorporates forward-looking macroeconomic forecasts with documented reasonable and supportable forecast period and reversion methodology
- [ ] Credit scoring model inputs reviewed for fair lending risk including proxy analysis for prohibited bases prior to deployment
- [ ] LDA analysis conducted and documented for all credit scoring models; results reviewed by fair lending compliance
- [ ] Model validation completed by independent party within last 24 months covering conceptual soundness, ongoing monitoring, and outcomes analysis per SR 11-7
- [ ] CRE concentration levels measured against 100%/300% supervisory thresholds with board-approved limits and documented stress testing
- [ ] Q-factors individually documented with specific rationale tied to identified risk conditions
- [ ] Internal risk ratings cover all exposures (not only criticized credits); dual-rated for borrower and facility risk
- [ ] Third-party lending partners' credit decisions and fair lending compliance monitored with full transaction-level data access
- [ ] Stress testing applies adverse scenarios to collateral values, interest rates, occupancy, and borrower cash flows simultaneously
- [ ] Agricultural and commodity-dependent credits stress-tested under multi-year depressed price scenarios
- [ ] Back-testing compares predicted vs. actual credit losses by risk grade and portfolio segment; remediation documented
- [ ] FCRA disclosure requirements verified for all adverse actions based in whole or part on consumer report data
- [ ] Loan review function operates independently from origination; validates risk ratings; reports findings to board or audit committee

## References
BCBS d595 (2025), BCBS d424 (Basel III Summary), SR 11-7/OCC 2011-12 (Model Risk Management), OCC Fall 2025 Semiannual Risk Perspective, FDIC 2025 Risk Review, FDIC FIL-23064 (Dec 2023), CFPB Fair Lending Annual Report 2024, CFPB Circular 2023-03, CFPB Winter 2025 Supervisory Highlights (Advanced Technologies), Regulation B 12 CFR 1002, ASC 326 (CECL), IFRS 9, 2006 Interagency CRE Guidance, 2020 Joint Interagency Policy Statement on ACL, Baker Tilly CECL Validation, Abrigo CRE Concentration Risk
