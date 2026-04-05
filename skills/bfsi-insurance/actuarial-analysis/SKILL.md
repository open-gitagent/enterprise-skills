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

# Actuarial Analysis

## Domain Overview

Actuarial analysis in insurance encompasses the quantitative evaluation of risk through loss reserving, rate making, experience rating, and predictive modeling. Each discipline operates under distinct regulatory frameworks but shares a common actuarial control cycle: data collection, assumption setting, model selection, parameter estimation, validation, and ongoing monitoring. The Actuarial Standards Board (ASB) governs practitioner conduct through Actuarial Standards of Practice (ASOPs), while the NAIC, state departments of insurance, and increasingly state-specific AI regulations (Colorado SB21-169, NY DFS Circular Letter No. 7) impose external compliance requirements on actuarial work products.

Loss reserving drives insurer financial statements — the Statement of Actuarial Opinion filed with the NAIC Annual Statement represents the single most consequential actuarial deliverable, directly affecting regulatory solvency assessments. NAIC Model Law 822 (Actuarial Opinion and Memorandum Regulation) mandates that every insurer's appointed actuary render an opinion on reserve adequacy. ASOP No. 43 (Property/Casualty Unpaid Claim Estimates) and ASOP No. 36 (Statements of Actuarial Opinion Regarding Property/Casualty Loss and Loss Adjustment Expense Reserves) govern the methodology and disclosure requirements. The NAIC's Actuarial Opinion Working Group (AOWG) publishes annual Regulatory Guidance documents — the 2024 and 2025 editions refine expectations around appointed actuary qualifications, materiality thresholds, and disclosure of data limitations.

Rate making — the process of establishing adequate, non-excessive, and non-unfairly-discriminatory rates — follows the CAS Statement of Principles Regarding Property and Casualty Insurance Ratemaking and ASOP No. 30 (Property/Casualty Rate Making). The emergence of generalized linear models (GLMs), gradient boosting machines (GBMs), and neural networks in pricing has triggered a wave of regulatory scrutiny. The NAIC's Casualty Actuarial and Statistical (C) Task Force published its Regulatory Review of Predictive Models White Paper, and the 2025 NAIC Model Review Manual provides state regulators with a standardized framework for evaluating predictive model rate filings. Colorado SB21-169 and NY DFS Circular Letter No. 7 (2024) impose specific bias testing, transparency, and governance obligations on insurers using AI/ML in underwriting and pricing.

Experience rating bridges individual risk characteristics to aggregate rate levels. The NCCI Experience Rating Plan for workers' compensation remains the most widely deployed system, using split-point credibility weighting between primary (frequency-driven) and excess (severity-driven) losses. In commercial lines beyond workers' compensation, schedule rating and loss-sensitive plans introduce actuarial judgment into individual risk modification. The interaction between predictive models and traditional experience rating creates emerging complexity — double-counting of loss experience across pricing layers remains a persistent actuarial challenge.

## Core Decision Framework

Actuarial practitioners apply a hierarchical decision framework across all four sub-disciplines:

**1. Data Sufficiency Assessment (ASOP No. 23 — Data Quality)**
Before selecting any method, evaluate whether available data meets the requirements of ASOP No. 23. Assess completeness, consistency, reasonableness, and appropriateness. For loss reserving: confirm that loss development triangles have homogeneous claim groupings and that changes in claim handling, settlement patterns, or case reserve adequacy are identified. For rate making: verify that exposure bases correctly measure risk, and that premium and loss data are on-level (adjusted for rate changes and benefit modifications).

**2. Method Selection Based on Data Maturity and Line Characteristics**
- **Short-tail, high-frequency lines** (auto physical damage, property): Chain-Ladder (paid and incurred) dominates; data matures quickly, development factors stabilize by 24-36 months.
- **Long-tail, low-frequency lines** (medical malpractice, excess casualty): Bornhuetter-Ferguson or Cape Cod methods required to anchor immature years; pure chain-ladder produces volatile and unreliable estimates for recent accident years.
- **Emerging/catastrophe-exposed lines**: Frequency-severity separation with explicit catastrophe loading (ASOP No. 38 — Catastrophe Modeling); stochastic simulation supplements deterministic point estimates.

**3. Credibility Weighting (ASOP No. 25 — Credibility Procedures)**
All actuarial estimates involve combining observed experience with prior expectations. Apply limited fluctuation (classical) or greatest accuracy (Bühlmann) credibility based on the specific application. Experience rating uses split-point credibility; rate making uses multi-level credibility across class, territory, and hazard group dimensions.

**4. Assumption Transparency and Sensitivity Testing**
Every material assumption — trend rates, loss development factors, discount rates, correlation parameters — requires documentation of the basis for selection and sensitivity testing across a reasonable range. ASOP No. 41 (Actuarial Communications) mandates disclosure of assumptions that significantly affect results.

**5. Model Governance for Predictive Analytics (ASOP No. 56 — Modeling)**
ASOP No. 56, effective October 2020, establishes requirements for model selection, input data, validation, documentation, and reliance on models developed by others. For predictive models used in pricing: perform out-of-sample validation, assess variable importance and interaction effects, conduct disparate impact testing (particularly for protected class proxies), and maintain model inventory with version control.

## Step-by-Step Process

### Loss Reserving Workflow
1. **Data Organization**: Construct loss development triangles by accident year (or report year/policy year as appropriate) with quarterly or annual evaluation dates. Separate paid losses, incurred losses, case reserves, claim counts, and ALAE/ULAE.
2. **Diagnostic Review**: Calculate link ratios (age-to-age factors) across all triangle cells. Identify outlier development periods. Plot residuals to detect systematic patterns — calendar-year effects (inflation, judicial changes), accident-year effects (underwriting changes), or development-period effects (claims handling shifts).
3. **Method Application**: Run minimum three methods — typically paid chain-ladder, incurred chain-ladder, and Bornhuetter-Ferguson on incurred. For long-tail lines, add frequency-severity, Cape Cod, and Berquist-Sherman adjustments.
4. **Selection of Ultimate Losses**: Weight methods based on data maturity by accident year. Mature years: weight toward chain-ladder. Immature years: weight toward Bornhuetter-Ferguson. Document rationale for every selection.
5. **IBNR Calculation**: IBNR = Selected Ultimate − (Paid Losses + Case Reserves). Decompose into pure IBNR (claims not yet reported), development on known claims, and reopened claims.
6. **Reasonableness Testing**: Compare implied loss ratios, claim severity trends, and frequency trends against benchmarks. Apply IRIS ratio tests (e.g., IRIS Ratio 11 — one-year reserve development to policyholders' surplus; IRIS Ratio 12 — two-year reserve development to policyholders' surplus).
7. **Actuarial Opinion Rendering**: Under NAIC Model Law 822, issue opinion as Reasonable, Qualified, Adverse, or No Opinion. Attach Actuarial Opinion Summary with risk of material adverse deviation (RMAD) analysis.

### Rate Making Workflow
1. **Data Collection and On-Leveling**: Adjust historical premiums to current rate level using parallelogram method or extension of exposures. Adjust losses for benefit-level changes and trend.
2. **Loss Development and Trending**: Project historical losses to ultimate; apply prospective loss trend (frequency × severity) to the midpoint of the future policy period.
3. **Expense Loading**: Determine fixed and variable expense provisions. Apply premium-based and loss-based expense ratios. Account for commission gradients by line and distribution channel.
4. **Profit and Contingency Loading**: Apply target combined ratio or target return on allocated surplus. Incorporate investment income offset where regulatory jurisdiction permits.
5. **Indicated Rate Change Calculation**: Use loss ratio method (indicated rate = [projected ultimate losses + LAE + fixed expenses] / [1 − variable expense ratio − profit provision] / earned premium at current rate level) or pure premium method.
6. **Classification Relativities**: Fit GLM (Tweedie or Poisson-gamma compound distribution) to determine class, territory, and rating variable relativities. Validate with holdout sample, lift curves, and Gini coefficients.
7. **Regulatory Filing**: Prepare actuarial memorandum with certification per state filing requirements. For states using NAIC CASTF Model Review Manual, include model documentation, variable justification, and disparate impact analysis.

### Experience Rating Workflow
1. **Experience Period Selection**: Typically three policy years, excluding the most recent (to allow development). Align with NCCI standard or applicable rating bureau requirements.
2. **Loss Limitation**: Apply per-claim loss limits (split point) to separate frequency signal from severity noise. NCCI's current split point is $18,500 (adjusted periodically).
3. **Expected Loss Calculation**: Multiply payroll exposure by class-specific expected loss rate to produce expected losses at both primary and excess levels.
4. **Credibility Application**: Weight actual primary losses against expected primary losses; separately weight actual excess losses against expected excess losses. Primary losses receive higher credibility (more predictive of future frequency).
5. **Experience Modification Factor**: EMF = (Actual weighted losses / Expected losses). Values >1.00 indicate worse-than-average experience; <1.00 indicates better-than-average.
6. **Review and Dispute Resolution**: Verify classification codes, payroll audits, and claim data accuracy. Experience mods are disputable; errors in underlying data are the leading cause of incorrect modifications.

### Predictive Modeling for Risk Pricing
1. **Feature Engineering**: Transform raw policyholder and claims data into model-ready features. Address multicollinearity, missing values, and categorical encoding.
2. **Model Selection**: Start with GLM as regulatory baseline (interpretable, widely accepted). Layer complexity with GAM, GBM, or random forest only where lift justifies regulatory burden.
3. **Training and Validation**: Use temporal validation (not random k-fold) to respect time-series nature of insurance data. Apply walk-forward validation for frequency and severity models separately.
4. **Fairness Testing**: Per NAIC AI Model Bulletin (April 2024) and Colorado SB21-169, test for proxy discrimination. Calculate disparate impact ratios across protected classes. Apply techniques from CAS Research Paper Series on Race and Insurance Pricing.
5. **Rate Indication Integration**: Convert model predictions to rating relativities. Ensure consistency with overall rate level indication. Avoid double-counting factors already captured in experience rating or schedule rating.
6. **Documentation and Governance**: Maintain model risk inventory per ASOP No. 56. Document model limitations, known weaknesses, and conditions under which model predictions degrade.

## Evaluation Criteria

| Criterion | Weight | Assessment Method |
|---|---|---|
| Data quality and completeness | 15% | ASOP 23 compliance checklist; triangle diagnostics |
| Method appropriateness | 20% | Alignment of selected methods with data maturity, line characteristics, and tail length |
| Assumption reasonableness | 20% | Sensitivity ranges; comparison to industry benchmarks (ISO, NCCI, A.M. Best) |
| Regulatory compliance | 15% | ASOP conformance; state filing requirements; NAIC opinion standards |
| Predictive accuracy | 15% | Out-of-sample loss ratios; Gini coefficient; lift curves; calibration plots |
| Documentation quality | 10% | ASOP 41 compliance; reproducibility; assumption transparency |
| Fairness and non-discrimination | 5% | Disparate impact testing; proxy variable analysis; regulatory acceptance |

Reserve adequacy scoring uses the NAIC IRIS framework:
- **IRIS Ratio 11** (One-Year Reserve Development / PHS): Unusual result >20%
- **IRIS Ratio 12** (Two-Year Reserve Development / PHS): Unusual result >20%
- **IRIS Ratio 13** (Estimated Current Reserve Deficiency / PHS): Unusual result >25%

## Red Flags & Edge Cases

1. **Calendar-year diagonal distortion in development triangles**: A claims department process change (e.g., new case reserving guidelines, bulk reserve adjustments, or settlement push) creates a diagonal pattern in loss triangles that chain-ladder methods propagate forward, systematically biasing IBNR. The 2024 AOWG Regulatory Guidance specifically flags this as requiring disclosure in the Actuarial Opinion Summary.

2. **Stale case reserves masking true IBNR**: When claims adjusters fail to update case reserves for several evaluation periods, incurred development factors appear artificially low. The actuary selects stable-looking factors that understate ultimate losses. Paid-to-incurred ratio analysis by development age detects this — a declining ratio signals case reserve stagnation.

3. **Bornhuetter-Ferguson anchoring to flawed a priori loss ratio**: The B-F method's stability advantage becomes a liability when the expected loss ratio is selected from an unrepresentative period (e.g., pre-pandemic data applied to post-pandemic years). Practitioners default to the prior year's selection without reassessing the environment.

4. **Trend selection bias in rate making**: Actuaries selecting trend factors that support a predetermined rate indication — cherry-picking endpoints, excluding outlier years, or switching between linear and exponential trend without justification. State regulators frequently reject filings with unsupported trend selections, as documented in Milliman's rate filing approval analysis.

5. **GLM interaction effects creating proxy discrimination**: A territory × credit score interaction in a homeowners model produces disparate impact on minority populations. The variable passes traditional actuarial fairness tests (correlation with loss) but functions as a proxy for race. Colorado SB21-169 requires quantitative testing; NY DFS Circular Letter No. 7 (2024) demands governance frameworks to detect and mitigate such effects.

6. **Experience modification data lag exploits**: In workers' compensation, the three-year experience period excluding the most recent year creates a window where large losses rolling off the experience period cause sudden mod decreases unrelated to current risk improvement. Conversely, a single catastrophic claim entering the window spikes the mod despite otherwise excellent experience.

7. **Double-counting in predictive model plus experience rating**: A predictive pricing model trained on loss data that also feeds experience rating captures the same signal twice. The policyholder gets penalized at both the class relativity level and the individual mod level. This manifests as combined ratios that are too low for experience-rated accounts and too high for non-rated accounts.

8. **Catastrophe model output treated as deterministic**: Actuaries using vendor CAT model average annual loss (AAL) in ratemaking without reflecting the full distribution. The AAL understates the capital cost of tail risk. ASOP No. 38 requires the actuary to consider the "range of possible outcomes" — a single point estimate violates this standard.

9. **ULAE ratio applied to net reserves when gross-to-net ratio is changing**: Unallocated loss adjustment expense ratios calculated on a calendar-year paid basis applied to net reserves when the cession ratio is shifting (e.g., new reinsurance treaty). The ULAE provision becomes disconnected from the actual claims handling cost structure.

10. **Loss-sensitive program reserve inadequacy**: For large deductible, retrospectively-rated, or captive programs, the ceding company books net reserves assuming full collateral adequacy. When the policyholder becomes financially impaired, the insurer bears the gross loss. Statutory Schedule P may not separately identify this credit risk embedded in reserves.

11. **Appointed actuary independence compromise**: NAIC Model Law 822 requires the appointed actuary to meet qualification standards and maintain professional independence. Pressure from management to issue a "Reasonable" opinion when the actuary's analysis indicates a range where the low end is marginally adequate — the actuary selects the low end and issues Reasonable rather than Qualified, exposing both the actuary and the company.

12. **Predictive model degradation post-deployment**: A pricing model validated at time of filing degrades as the underlying distribution shifts (portfolio mix changes, economic conditions, regulatory environment). No monitoring framework detects the drift. ASOP No. 56 Section 3.6 requires ongoing model review, but many organizations lack automated monitoring infrastructure.

13. **Credibility over-assignment to small data segments**: Applying full credibility to a class or territory with statistically insufficient exposure. The 1,082-claim threshold for full credibility (at 90% confidence, ±5% accuracy, Poisson assumption) is rarely achieved for granular segments. Over-credible segments produce volatile year-over-year rate changes that regulators flag.

## Common Mistakes

1. **Mechanical factor selection without diagnostics**: Selecting 5-year weighted average development factors for every triangle without examining whether recent development patterns differ from historical averages. Different factor selection methods (simple average, weighted average, volume-weighted, excluding high/low) exist for different diagnostic conclusions — applying one universally signals methodological laziness.

2. **Failing to reconcile methods**: Running four reserving methods, selecting results from each by accident year, but never reconciling why methods diverge. Divergence between paid and incurred chain-ladder diagnoses specific conditions (case reserve adequacy, settlement speed changes) — ignoring divergence means missing the diagnostic signal.

3. **Confusing calendar-year and accident-year trend**: Applying calendar-year loss trend to accident-year experience in ratemaking, or vice versa. Calendar-year trend reflects development pattern changes plus pure trend; accident-year trend isolates the pure trend component. Mixing these inflates or deflates indicated rate changes.

4. **Ignoring correlation in aggregate reserve distributions**: Summing independent reserve distributions across lines to get a company-wide aggregate without modeling correlation. Lines sharing the same judicial environment, economic conditions, or claims department exhibit positive correlation. The aggregate variance is larger than the sum of individual variances.

5. **Using R-squared as the primary GLM validation metric**: R-squared is inappropriate for frequency models (Poisson/negative binomial) and nearly meaningless for insurance pricing models with high inherent variance. Deviance statistics, AIC/BIC, lift curves, and double-lift analysis provide meaningful model comparison.

6. **Filing predictive model rates without plain-language variable justification**: Regulators increasingly require actuarial rationale for each rating variable — not just statistical significance, but a causal or theoretical relationship to expected loss. NAIC CASTF Model Review Manual mandates this. Filings that present only model output without explaining "why this variable predicts loss" face rejection.

7. **Not adjusting for large-loss censoring in severity trend**: Severity trends computed on losses capped at policy limits understate true severity trend when limits are inadequate. The censoring effect increases as inflation pushes more claims against limits. Use survival analysis or fit a distribution with explicit censoring.

## Regulatory & Compliance Requirements

### Actuarial Standards of Practice (ASOPs)
| ASOP | Title | Key Requirement |
|---|---|---|
| ASOP No. 12 | Risk Classification | Rating variables must be related to expected outcomes; prohibits unfair discrimination |
| ASOP No. 23 | Data Quality | Actuary must assess data completeness, reasonableness, and appropriateness before relying on it |
| ASOP No. 25 | Credibility Procedures | Establishes standards for blending observed experience with prior expectations |
| ASOP No. 30 | Property/Casualty Rate Making | Comprehensive ratemaking methodology guidance |
| ASOP No. 36 | Statements of Actuarial Opinion — P&C Loss Reserves | Requirements for the appointed actuary's opinion on reserves |
| ASOP No. 38 | Catastrophe Modeling | Standards for using catastrophe models in ratemaking and reserving |
| ASOP No. 41 | Actuarial Communications | Documentation and disclosure requirements for all actuarial work |
| ASOP No. 43 | P&C Unpaid Claim Estimates | Methodology standards for estimating unpaid claims |
| ASOP No. 56 | Modeling | Governance, validation, documentation for all actuarial models including predictive analytics |

### NAIC Requirements
- **Model Law 822** (Actuarial Opinion and Memorandum Regulation): Mandates annual statement of actuarial opinion from qualified appointed actuary. Requires Actuarial Report and Actuarial Opinion Summary. States adopt with variations.
- **NAIC IRIS Ratios Manual (2024 edition)**: Defines 13 P&C financial ratios including reserve development tests. Unusual results trigger Level 2 regulatory analysis.
- **NAIC AI Model Bulletin (April 2024)**: Requires insurers using AI/ML to maintain governance frameworks, conduct bias testing, and ensure outcomes do not unfairly discriminate. Applies to predictive models in pricing, underwriting, and claims.
- **NAIC CASTF Model Review Manual (2025)**: Standardized regulatory framework for evaluating predictive model rate filings. Covers model documentation, variable justification, validation, and disparate impact analysis.
- **AOWG Regulatory Guidance (2024, 2025)**: Annual guidance for appointed actuaries on opinion requirements, materiality, and RMAD disclosure.

### State-Specific Regulations
- **Colorado SB21-169**: Requires life insurers (effective November 2023) and property/casualty insurers (phased implementation) to test external data, algorithms, and predictive models for unfair discrimination. Mandates governance frameworks and bias testing.
- **NY DFS Circular Letter No. 7 (2024)**: Establishes expectations for insurers using AI and external consumer data sources in underwriting and pricing. Requires actuarial justification, non-discrimination testing, and consumer transparency.
- **California Bulletin 2024-7**: Revised requirements for rate application review including enhanced actuarial support documentation.

### International Standards
- **IFRS 17 (Insurance Contracts)**: Effective January 2023 for IFRS-reporting entities. Requires current-value measurement of insurance liabilities using building blocks approach (best estimate of future cash flows + risk adjustment + contractual service margin). Significantly expands actuarial analysis requirements for reserving and financial reporting.

## Terminology

- **IBNR (Incurred But Not Reported)**: Reserve component for claims that have occurred but not yet been reported to the insurer; in practice, often expanded to include development on known claims (IBNER) and pure IBNR.
- **Chain-Ladder Method**: Deterministic reserving technique projecting ultimate losses by applying age-to-age development factors to cumulative loss triangles; assumes future development follows historical patterns.
- **Bornhuetter-Ferguson (B-F) Method**: Reserving method combining an a priori expected loss ratio with actual emerged experience, producing estimates less volatile than chain-ladder for immature accident years. IBNR = Expected Ultimate × (1 − % Emerged).
- **Loss Development Factor (LDF)**: Multiplicative factor applied to losses at a given maturity to project to ultimate; also called age-to-ultimate factor or cumulative development factor.
- **On-Leveling**: Process of adjusting historical premium to the current rate level to create a consistent basis for rate indication; uses parallelogram method accounting for effective dates of rate changes.
- **Experience Modification Factor (EMF)**: Multiplicative factor applied to manual premium reflecting an individual risk's loss experience relative to its class average; values above 1.00 indicate adverse experience.
- **Split Point**: Dollar threshold in experience rating separating primary losses (below the split, reflecting frequency) from excess losses (above the split, reflecting severity); NCCI currently uses $18,500.
- **Credibility**: Actuarial measure (0 to 1) of the predictive value of a body of data; full credibility (Z=1) means the data alone is sufficient to estimate future costs within acceptable precision.
- **Bühlmann Credibility**: Greatest accuracy credibility framework minimizing expected squared error; Z = n / (n + k), where k represents the ratio of process variance to hypothetical means variance.
- **GLM (Generalized Linear Model)**: Statistical framework extending linear regression to non-normal distributions (Poisson, gamma, Tweedie); standard tool for multivariate insurance pricing.
- **Tweedie Distribution**: Compound Poisson-gamma distribution commonly used to model aggregate pure premium directly, handling the point mass at zero (no-claim) and continuous positive claims.
- **Loss Ratio Method**: Ratemaking approach where indicated rate change = (projected loss & LAE ratio + fixed expense ratio) / (1 − variable expense ratio − profit provision) − 1.
- **Pure Premium Method**: Ratemaking approach where indicated rate = (projected pure premium + fixed expense per exposure) / (1 − variable expense ratio − profit provision).
- **RMAD (Risk of Material Adverse Deviation)**: Assessment in the actuarial opinion of the likelihood that actual losses will materially exceed carried reserves; requires disclosure when risk is reasonably possible.
- **Appointed Actuary**: Actuary designated by an insurer's board of directors to render the statutory actuarial opinion; must meet NAIC qualification standards including specific continuing education requirements.
- **ULAE (Unallocated Loss Adjustment Expense)**: Claim-related expenses not directly attributable to a specific claim (e.g., claims department salaries, rent); distinguished from ALAE/DCCE which are claim-specific.
- **Tail Factor**: Development factor applied beyond the last observable maturity in a loss triangle to project to ultimate; often the most judgmental and impactful assumption in long-tail reserving.
- **Cape Cod Method**: Reserving method (also called Stanard-Bühlmann) using on-level earned premium to derive a priori loss ratio from the data itself, reducing subjectivity compared to standard B-F.
- **Berquist-Sherman Adjustment**: Technique to adjust loss development triangles for changes in claims settlement rates or case reserve adequacy levels, restoring homogeneity to the triangle.
- **Disparate Impact Testing**: Quantitative analysis assessing whether a facially neutral rating variable or pricing model produces outcomes that disproportionately affect protected classes, per NAIC and state regulatory requirements.
- **Gini Coefficient (Insurance)**: Measure of a pricing model's discriminatory power (ability to separate good risks from bad); calculated from the ordered Lorenz curve of actual versus predicted losses. Higher values indicate better risk differentiation.
- **Schedule Rating**: Subjective premium modification applied by underwriters based on characteristics not captured in manual rates (e.g., management quality, safety programs); typically ranges ±25% to ±40%.
- **Loss Cost Multiplier (LCM)**: Factor applied to advisory organization (ISO, NCCI) loss costs to produce an insurer's final rate; reflects the insurer's own expense and profit provisions.

## Quality Checklist

1. **Triangle homogeneity verified**: Confirm loss development triangles contain homogeneous data — no mixing of occurrence/claims-made policies, no merging of substantially different sub-lines, and all known discontinuities (portfolio transfers, commutations) identified and adjusted.
2. **Minimum three reserving methods applied**: At least three independent methods used, with method selection rationale documented by accident year and explicit weighting basis.
3. **ASOP No. 23 data quality assessment documented**: Written assessment of data limitations, known deficiencies, and their potential impact on results; reliance on third-party data explicitly acknowledged.
4. **Loss trend and development factor selections supported**: Each selected factor has documented basis — not simply "5-year weighted average" but why that selection period and method fits the observed data pattern.
5. **On-leveling verified with independent premium calculation**: Historical premiums brought to current rate level using documented rate change history; verified by reconstructing sample policies.
6. **Predictive model validated on out-of-time holdout**: Models used for pricing validated on temporally separated holdout (not random split), with performance metrics (Gini, lift, calibration) reported by key segments.
7. **Disparate impact analysis completed**: For any predictive model or new rating variable, disparate impact ratios calculated across available protected class dimensions; results documented with remediation plan if thresholds exceeded.
8. **ASOP No. 56 model documentation maintained**: Model inventory entry exists with version, training data description, feature list, validation results, known limitations, and conditions under which the model should not be used.
9. **Experience rating data reconciled to source**: Payroll, class codes, and claim data underlying experience modification calculations traced to audited policy records and verified claim files.
10. **Appointed actuary qualification confirmed**: Actuarial opinion signed by actuary meeting NAIC qualification standards — Fellow of CAS or FSA with relevant experience and continuing education, including specific NAIC-mandated topics.
11. **RMAD assessment explicitly addressed**: Risk of material adverse deviation evaluated and disclosed per AOWG Regulatory Guidance, with quantitative support for the assessment.
12. **Sensitivity testing documented**: Key assumptions (trend, tail factors, catastrophe loads, discount rates) varied across reasonable range with impact on indicated rate or reserve quantified.
13. **Regulatory filing requirements met**: State-specific filing requirements checked — actuarial memorandum format, required exhibits, certification language, and any predictive model supplemental filings.
14. **Calendar-year vs. accident-year basis correctly applied**: Trend analysis, development factor selection, and financial statement reconciliation use the appropriate time basis without cross-contamination.

## References

- NAIC AOWG 2024 Regulatory Guidance Document: https://content.naic.org/sites/default/files/inline-files/AOWG%20Regulatory%20Guidance%20-%202024%20Final.pdf
- NAIC AOWG 2025 Regulatory Guidance Document: https://content.naic.org/sites/default/files/inline-files/AOWG%20Regulatory%20Guidance%20-%202025%20Final.pdf
- NAIC Model Law 822 — Actuarial Opinion and Memorandum Regulation: https://content.naic.org/sites/default/files/model-law-822.pdf
- NAIC 2025 P&C Statement of Actuarial Opinion Instructions: https://content.naic.org/sites/default/files/call_materials/027_Property_2025_Actuarial_Opinion_01272025_0.pdf
- NAIC Insurance Regulatory Information System (IRIS) Ratios Manual 2024: https://content.naic.org/sites/default/files/publications-iris-manual-2024.pdf
- NAIC AI Model Bulletin (April 2024): https://content.naic.org/sites/default/files/inline-files/AI%20Model%20Bulletin%20-%20April%202024.pdf
- NAIC CASTF Model Review Manual (2025): https://content.naic.org/sites/default/files/inline-files/NAIC%20Model%20Review%20Manual__%20adopted%20by%20CASTF%2011.04.25.pdf
- NAIC CASTF Regulatory Review of Predictive Models White Paper: https://content.naic.org/sites/default/files/call_materials/CASTF%20-%20Predictive%20Model%20White%20Paper%209-09-2020.docx
- Actuarial Standards Board — Standards of Practice: http://www.actuarialstandardsboard.org/standards-of-practice/
- ASOP No. 12 — Risk Classification: http://www.actuarialstandardsboard.org/wp-content/uploads/2014/07/asop012_101.pdf
- ASOP No. 36 — Statements of Actuarial Opinion (P&C Reserves): http://www.actuarialstandardsboard.org/asops/asop-36-statements-actuarial-opinion-regarding-propertycasualty-loss-loss-adjustment-expense-reserves-proposed-revision/
- ASOP No. 43 — Property/Casualty Unpaid Claim Estimates: http://www.actuarialstandardsboard.org/asops/propertycasualty-unpaid-claim-estimates/
- ASOP No. 56 — Modeling: http://www.actuarialstandardsboard.org/wp-content/uploads/2020/01/asop056_195.pdf
- CAS Statement of Principles Regarding Property and Casualty Insurance Ratemaking: https://www.casact.org/sites/default/files/2021-05/Statement-Of-Principles-Ratemaking.pdf
- CAS Research Paper Series on Race and Insurance Pricing: https://www.casact.org/biasandinsuranceresearch
- CAS Practical Guide to Navigating Fairness in Insurance Pricing (2024): https://www.casact.org/sites/default/files/2024-08/A_Practical_Guide_to_Navigating_Fairness_in_Insurance_Pricing.pdf
- CAS Generalized Linear Models for Insurance Rating: https://www.casact.org/sites/default/files/2021-03/8_GLM.pdf
- American Academy of Actuaries — P&C Loss Reserve Law Manual (2024): https://actuary.org/wp-content/uploads/2025/03/pcmanual_24.pdf
- AAA Practice Note — Statements of Actuarial Opinion on P&C Loss Reserves (2024): https://www.actuary.org/sites/default/files/2024-12/casualty-practice-note-saopclossreserve2024.pdf
- Colorado SB21-169 — Protecting Consumers from Unfair Discrimination in Insurance: https://doi.colorado.gov/for-consumers/sb21-169-protecting-consumers-from-unfair-discrimination-in-insurance-practices
- NY DFS Circular Letter No. 7 (2024) — Use of AI in Insurance: https://www.dfs.ny.gov/industry-guidance/circular-letters/cl2024-07
- NCCI ABCs of Experience Rating: https://www.ncci.com/articles/documents/uw_abc_exp_rating.pdf
- Milliman — Understanding Rate Filing Average Days to Approval Q2 2024: https://www.milliman.com/en/insight/regulatory-insurance-intelligence-rate-filing-days-approval-q2-2024
- CAS Research Paper on IFRS 17: https://www.casact.org/sites/default/files/2025-04/CAS_Research-Paper-on-IFRS-17.pdf
- NAIC Casualty Actuarial and Statistical (C) Task Force: https://content.naic.org/committees/c/casualty-actuarial-statistical-tf
- Indiana DOI Financial Analysis Handbook — Premium Deficiency Reserves: https://www.in.gov/idoi/files/Financial-Analysis-Handbook-2023-Annual-2024-Quarterly_Part3.pdf