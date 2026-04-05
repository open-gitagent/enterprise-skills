---
name: personal-lines-underwriting
description: >
  Personal lines insurance underwriting covering homeowners, auto, and umbrella policies with risk selection, pricing, and coverage determination.
metadata:
  vertical: bfsi-insurance
  function: risk-assessment
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "NAIC, State DOI, FAIR Plans"
---

# Personal Lines Underwriting

## Domain Overview

Personal lines underwriting is the discipline of evaluating individual consumer insurance applications to determine acceptability, appropriate risk classification, premium adequacy, and coverage terms for homeowners (HO-2 through HO-8), personal auto (PA), and personal umbrella (PUP) policies. Unlike commercial underwriting, personal lines operates under heightened regulatory scrutiny because consumers are considered less sophisticated and more dependent on state-mandated coverage (auto liability financial responsibility laws, mortgage-required homeowners). The NAIC's Product Filing Review Handbook explicitly notes that states place "more emphasis on personal lines filings versus commercial lines filings" due to these societal considerations.

The U.S. personal lines market crossed $1 trillion in direct premiums written in 2024. Personal auto achieved a net combined ratio of 98.7 in 2024 after three consecutive years of underwriting losses, while homeowners posted a combined ratio of 105.7 — a significant improvement from 110.9 in 2023 but still unprofitable. These results reflect the critical tension underwriters face: maintaining rate adequacy while navigating state-by-state regulatory constraints on rating factors, credit score usage, territorial rating, and non-renewal authority. AM Best projects personal auto will reach 97.5 combined ratio in 2025, while homeowners remains projected to run an underwriting loss through at least 2025.

Regulatory complexity is the defining challenge. Insurance regulation under the McCarran-Ferguson Act (1945) is state-based, meaning an underwriter must comply with 50+ distinct regulatory regimes. Key regulatory dimensions include: rate filing type (prior approval vs. file-and-use vs. use-and-file), permitted rating factors (California Prop 103 mandates driving record, mileage, and experience as primary auto factors), credit-based insurance score restrictions (outright bans in CA, MA, HI, MI; partial restrictions in MD, OR, UT, WA, MN), anti-redlining protections, domestic violence victim protections, adverse action notice requirements under both FCRA and state IIPPA equivalents, and emerging AI/algorithmic governance under the NAIC Model Bulletin on AI Systems (adopted December 2023, now adopted by 25+ states).

The catastrophe exposure crisis has fundamentally reshaped homeowners underwriting. California's FAIR Plan exposure ballooned to $650 billion by mid-2025 (289% increase since FY2021), with seven of the top twelve homeowners insurers limiting coverage. State Farm stopped accepting new California homeowners applications in May 2023 and non-renewed 30,000 policies in March 2024. California Insurance Code §675.1 mandates one-year moratoriums on non-renewals in ZIP codes adjacent to wildfire perimeters following gubernatorial emergency declarations. Florida similarly restricts non-renewal during active hurricane claim repairs. Underwriters must now navigate catastrophe modeling, reinsurance cost pass-through rules, and mandatory FAIR plan participation requirements.

## Core Decision Framework

Personal lines underwriting operates on a three-gate decision model: **acceptability** (write or decline), **classification/tiering** (risk segment placement), and **pricing** (rate application within the approved rating plan). Each gate has distinct regulatory guardrails.

### Gate 1: Acceptability
The threshold question: does the risk fall within the company's filed and approved underwriting guidelines? Underwriters evaluate hazard characteristics against binding authority. Key acceptability factors by line:

- **Homeowners**: Construction type, roof age/material/condition, ISO Protection Class (1-10 scale based on FSRS scoring), prior claims history via C.L.U.E. report, property age, replacement cost estimate, proximity to coast/wildfire/flood zone, occupancy type, attractive nuisances (pools, trampolines), and dog breed restrictions where state-permitted.
- **Personal Auto**: MVR (motor vehicle report) violations in prior 3-5 years, at-fault accident history, CLUE auto claims, license status, vehicle use/garaging, SR-22/FR-44 filings, youthful driver profiles, and household driver composition.
- **Umbrella**: Underlying limits adequacy (typically $300K/$500K auto liability, $300K+ HO liability), total exposure count (vehicles, properties, watercraft, recreational vehicles), youthful driver surcharges, claims frequency, and existence of business pursuits exposures.

### Gate 2: Classification and Tiering
Accepted risks are placed into rating tiers that reflect relative expected loss. Tiering uses a multi-variable algorithm that produces a composite score. The Casualty Actuarial Society documents tiering as the insurer's method to "segment risks beyond the traditional rating variables" by using additional underwriting characteristics. Typical personal auto tiers range from "preferred" (0-1 minor violations, long tenure, high credit score where permitted) through "standard" to "non-standard" (multiple at-fault accidents, DUI/DWI, lapsed coverage). Homeowners tiers factor prior loss count, credit-based insurance score, home age, and claims-free discount eligibility.

### Gate 3: Pricing
Rates must satisfy the statutory standard: **adequate but not excessive, and not unfairly discriminatory** (NAIC Model Rating Laws #1775, #1776, #1780). This means risk classifications must be based on actuarially supportable differences in expected losses. Unfair discrimination occurs when "similarly situated risks are treated differently" — distinct from civil rights discrimination, though the two increasingly intersect through disparate impact analysis (Colorado SB21-169).

## Step-by-Step Process

1. **Application Intake** — Receive ACORD 80 (homeowners), ACORD 90 (auto), or ACORD 83 (umbrella). Validate completeness, confirm named insured identity, verify OFAC sanctions screening. Two states (take-all-comer jurisdictions for auto) prohibit declination of mandatory liability coverage requests.

2. **Third-Party Data Ordering** — Pull C.L.U.E. Property and/or Auto reports (LexisNexis), MVR from state DMV, credit-based insurance score (where state-permitted), replacement cost estimator (e.g., CoreLogic, Verisk), ISO Protection Class, and catastrophe model scores (wildfire, hurricane, hail, flood zone determination via FEMA FIRM).

3. **Hazard Analysis** — Evaluate physical, moral, and morale hazards. Physical: roof condition scores (Cape Analytics, EagleView aerial imagery show 2/3 of owner-supplied roof ages are underestimated by 5+ years per Buildfax data), wiring type (knob-and-tube, aluminum), heating source, foundation type. Moral: fraud indicators, prior policy cancellations for material misrepresentation. Morale: maintenance neglect indicators, excessive inquiry-only CLUE hits.

4. **Eligibility Screening** — Apply underwriting rules engine. Check state-specific prohibited factor restrictions. In California, auto rating must weight driving record, annual mileage, and driving experience as the three mandatory primary factors in that rank order (CIC §1861.02). In states banning credit (CA, MA, HI for auto; CA, MA, MD for homeowners), suppress credit-based scoring modules. Check domestic violence victim protections (NAIC Model #880 §4.G prohibits basing decisions on abuse victim status).

5. **Tier Assignment** — Apply approved classification plan. Document which variables contributed to tier placement. Under FCRA §615(a), if credit information contributed to a less favorable tier, issue adverse action notice with the four primary reasons from the credit report. Florida §626.9741 requires "clear and specific language" — generalized terms like "poor credit history" do not satisfy the statutory requirement.

6. **Rate Application** — Apply territory, coverage, deductible, and discount factors per the filed rating algorithm. Verify consistency with state-approved rate manual. Apply mandatory discounts (California good-driver discount ≥20% per Prop 103 for drivers with ≤1 violation point in 3 years). Apply wind mitigation credits in coastal states (Florida, South Carolina).

7. **Coverage Determination** — Set coverage limits, deductibles, and endorsements. Confirm replacement cost valuation against dwelling coverage (Coverage A). For umbrella, verify underlying limits meet or exceed required minimums and issue gap coverage or self-insured retention where underlying falls short.

8. **Documentation and Issuance** — Generate declination/non-renewal notices per state timing requirements (typically 30-60 days for non-renewal, 10-45 days for cancellation). File reasons per NAIC Model #725 for auto declinations. Issue FCRA adverse action notices within required timeframes when consumer report data influenced the decision.

## Evaluation Criteria

| Factor | Homeowners Weight | Auto Weight | Umbrella Weight |
|--------|-------------------|-------------|-----------------|
| Prior loss history (CLUE) | High | High | High |
| Credit-based insurance score | High (where permitted) | High (where permitted) | Medium |
| Property/vehicle condition | High | Medium | N/A |
| Territory/location | High | High | Low |
| Protection class (ISO PPC) | High | N/A | N/A |
| Roof age/material/condition | High | N/A | N/A |
| MVR violations | N/A | High | High |
| Occupancy/use | Medium | Medium | Low |
| Years with prior carrier | Medium | Medium | Medium |
| Underlying limits adequacy | N/A | N/A | Critical |
| Exposure count (vehicles, properties) | N/A | N/A | High |
| Catastrophe model score | High | Low | Low |

Scoring methodology: most carriers use a composite underwriting score combining these factors into a single accept/decline/refer threshold. Referred risks escalate to senior underwriter authority levels. Combined ratio by tier segment must be monitored quarterly against planned loss ratios.

## Red Flags & Edge Cases

1. **Roof age misrepresentation**: Buildfax research shows over 66% of owner-supplied roof ages are underestimated by 5+ years, and 20%+ are understated by 15+ years. Aerial imagery from Cape Analytics or EagleView reveals tarps, ponding, patching, streaking, and missing material — all indicators of undisclosed damage. Binding a homeowners policy with incorrect roof age can create coverage disputes at claim time.

2. **Credit score suppression failure**: An underwriter applies credit-based insurance scoring in a prohibited state (California, Massachusetts, Hawaii for auto; Maryland for homeowners). This triggers regulatory violations under state-specific statutes and can result in market conduct examination findings, fines, and mandatory remediation to all affected policyholders.

3. **Catastrophe moratorium violation**: Issuing a non-renewal notice for a homeowners policy in a California ZIP code subject to an active wildfire moratorium under Insurance Code §675.1. The moratorium applies for one year from the date of the Governor's emergency declaration and covers all residential property insurance — not just fire policies.

4. **FCRA adverse action notice deficiency**: Florida §626.9741 explicitly states that generalized reasons such as "poor credit history," "poor credit rating," or "poor insurance score" do not meet the statutory explanation requirement. The notice must contain the four (or fewer) primary influence factors with specific descriptions.

5. **Umbrella gap in underlying limits**: Applicant carries $100K/$300K auto liability but the umbrella requires $250K/$500K minimum underlying. If the umbrella is bound without verifying underlying limits, the insured has a self-insured retention (SIR) gap between the actual underlying limit and the umbrella attachment point — the insured bears the difference personally.

6. **Take-all-comer jurisdiction declination**: In states requiring insurers to offer auto liability to all qualified applicants (e.g., Massachusetts), declining a request for minimum liability coverage constitutes a regulatory violation unless the risk is on an OFAC sanctions list (per OFAC guidance, the insurer must refuse coverage or obtain an OFAC license).

7. **Algorithmic bias under Colorado SB21-169**: An insurer's predictive model produces disparate outcomes correlated with race, even though race is not an input variable. Colorado's 2021 law (effective November 2023 via 3 CCR 702-10) requires insurers to test big data systems — including external consumer data, algorithms, and predictive models — for unfair discrimination against protected classes and take corrective action.

8. **Domestic violence victim penalization**: Underwriter declines homeowners or auto policy based on claims history that stems from domestic violence incidents. NAIC Model #880 §4.G and state implementations (e.g., Florida §626.9541) prohibit basing decisions on abuse victim status. The insurer may consider the medical condition resulting from an incident but not whether the condition was caused by abuse.

9. **Redlining through proxy variables**: Declining or surcharging risks in a geographic area that correlates with a protected class demographic, even when using facially neutral factors like "distance to fire station" or "average home value." NAIC Model #880 §4.B(4) prohibits refusing coverage "solely because of the geographic location of the risk, unless such action is the result of the application of sound underwriting and actuarial principles related to actual or reasonably anticipated loss experience."

10. **Property age discrimination**: Declining homeowners coverage solely because the dwelling was built before a certain year. NAIC Model #880 §4.B(5) prohibits discrimination based solely on the age of the residential property. Texas TAC 21.1006 similarly bars denying coverage based on property age or value — though denial based on physical condition (wiring, plumbing, roof condition) remains permissible.

11. **Post-catastrophe rate inadequacy spiral**: In Rate Cap or Prior Approval states, persistent premium shortfalls (filed rate vs. approved rate) correlate with underwriting losses. The IRC found that Rate Cap states had the highest average direct combined ratio in 2023. Underwriters in these states face the risk of writing business at actuarially inadequate rates, contributing to insolvency risk.

12. **Lapsed coverage as sole declination factor**: Using a gap in prior insurance as the only reason to decline creates adverse selection concerns, but several states restrict this practice as potentially discriminatory against lower-income applicants who may have been unable to afford continuous coverage.

## Common Mistakes

- **Applying uniform underwriting rules across states** without accounting for state-specific prohibited factors, mandated offerings, or take-all-comer requirements. A rule that works in Texas may violate California Prop 103 or Massachusetts regulatory requirements.
- **Failing to re-pull credit at state-mandated intervals**: Washington state requires auto and homeowner insurers to re-check credit history every three years and update records accordingly. Stale credit data creates both pricing inaccuracy and regulatory exposure.
- **Conflating FCRA and state IIPPA notice requirements**: The Fair Credit Reporting Act requires adverse action notice when a consumer report contributes to a negative decision. State Insurance Information and Privacy Protection Acts (NAIC Model #670) require notice regardless of whether a consumer report was used. Compliant underwriters must issue both notices when applicable.
- **Over-reliance on aerial imagery without ground-truthing**: While remote sensing data (roof condition, pool detection, trampoline identification) improves efficiency, binding or declining based solely on aerial data without allowing the applicant to provide contradicting evidence creates E&O exposure and potential unfair practices claims.
- **Ignoring umbrella exposure aggregation**: Underwriting an umbrella policy focusing only on auto and homeowners exposures while missing watercraft over 26 feet, recreational vehicles, rental properties, or business pursuits that create uncovered underlying exposures.
- **Misclassifying occupancy type**: Rating an owner-occupied HO-3 when the property is actually tenant-occupied (requiring HO-4/DP-3), seasonal (HO-3 with vacancy provisions), or short-term rental (Airbnb/VRBO) voids critical coverage assumptions.
- **Treating inquiry-only CLUE records as claims**: CLUE reports distinguish between paid claims and inquiry-only records (policyholder called to ask about coverage but no claim was filed). Several states prohibit adverse underwriting action based solely on inquiries.

## Regulatory & Compliance Requirements

### Federal Requirements
- **Fair Credit Reporting Act (FCRA), 15 USC §1681**: Governs use of consumer reports in underwriting. §615(a) mandates adverse action notice with specific reasons when consumer report information contributes to unfavorable decision. §604(c) provides permissible purpose for insurers to obtain consumer reports for underwriting.
- **OFAC Compliance**: Insurers must screen all applicants against the Specially Designated Nationals (SDN) list. Issuing coverage to a sanctioned person without OFAC license violates federal law regardless of state take-all-comer mandates.
- **Gramm-Leach-Bliley Act (GLBA)**: Privacy of consumer financial information collected during underwriting.

### NAIC Model Laws and Bulletins
- **Model #880 — Unfair Trade Practices Act**: Prohibits unfair discrimination by race, religion, nationality, sex, marital status, geographic location (without actuarial justification), property age (as sole factor), domestic violence status, and firearm ownership (Florida implementation).
- **Model #725 — Automobile Insurance Declination, Termination, and Disclosure Act**: Requires specific reasons for auto policy declinations and non-renewals.
- **Model #670 — Insurance Information and Privacy Protection Act**: Requires adverse underwriting decision notices regardless of whether consumer report was used.
- **Model Rating Laws (#1775, #1776, #1780)**: Establish the "adequate, not excessive, not unfairly discriminatory" rate standard and prohibit risk classification based on race, creed, national origin, or religion.
- **NAIC AI Model Bulletin (December 2023)**: Requires insurers to govern AI systems used in underwriting, ensure compliance with unfair trade practices laws, implement bias testing, and maintain documentation for regulatory examination. Adopted by 25+ states as of mid-2025.

### Key State-Specific Requirements
- **California**: Prop 103 mandates prior approval rating, restricts auto factors to driving record/mileage/experience as primary factors, bans credit-based insurance scores, requires ≥20% good-driver discount. Insurance Code §675.1 imposes wildfire non-renewal moratoriums.
- **Colorado**: SB21-169 (3 CCR 702-10) requires algorithmic bias testing for external consumer data and predictive models against protected classes.
- **Florida**: §626.9741 regulates credit use with specific adverse action notice language requirements; prohibits decisions based on firearm ownership; restricts non-renewal during active claim repair periods.
- **Massachusetts/Hawaii/Michigan**: Varying credit score bans in auto and/or homeowners underwriting.
- **New York**: Insurance Circular Letter No. 7 (2024) provides AI governance guidance specific to the state's regulatory framework.

### Rate Filing Regimes
- **Prior Approval**: Insurer must obtain commissioner approval before using rates (CA, FL, NJ, NY, TX for certain lines).
- **File-and-Use**: File rates before use but may implement upon filing (many states).
- **Use-and-File**: Implement rates and file afterward within specified period.
- **Flex Rating / Rate Cap**: Caps maximum rate increase per filing period.

## Terminology

- **C.L.U.E. (Comprehensive Loss Underwriting Exchange)**: LexisNexis database containing up to 7 years of personal property and auto claims history reported by participating insurers; distinguishes paid claims from inquiry-only records.
- **ISO Protection Class (PPC)**: Classification scale from 1 (best) to 10 (worst) measuring a community's fire suppression capability using the Fire Suppression Rating Schedule; based on fire department, water supply, emergency communications, and community risk reduction. Class 10 indicates essentially no fire protection.
- **Credit-Based Insurance Score (CBIS)**: Actuarial model translating credit bureau data into a score predicting insurance loss likelihood; distinct from a FICO lending score. Restricted or banned in CA, MA, HI, MI, MD, OR, UT, and MN.
- **Combined Ratio**: Sum of loss ratio and expense ratio; the standard measure of underwriting profitability. Below 100 = underwriting profit; above 100 = underwriting loss. Personal auto posted 98.7 in 2024; homeowners posted 105.7.
- **Adverse Action Notice**: Written notice required under FCRA §615(a) and/or state law when an underwriting decision is unfavorable to the consumer based on information in a consumer report or insurance score.
- **Tiering**: The segmentation of risks into pricing tiers beyond standard classification variables, using additional underwriting characteristics to differentiate loss expectation within a rating class.
- **FAIR Plan (Fair Access to Insurance Requirements)**: State-operated or state-mandated insurer of last resort providing basic property coverage to applicants unable to obtain coverage in the voluntary market. California's FAIR Plan exposure reached $650 billion by mid-2025.
- **MVR (Motor Vehicle Report)**: State DMV record showing driving violations, license status, and endorsements/restrictions for the prior 3-5 years; primary input for auto underwriting acceptability.
- **Unfair Discrimination (Insurance Context)**: Treating similarly situated risks within the same actuarial class differently in rates, terms, or availability. Distinct from civil rights discrimination but increasingly intersecting through disparate impact analysis.
- **Self-Insured Retention (SIR)**: In umbrella policies, the gap between actual underlying coverage limits and the umbrella's required underlying limits, which the insured must pay out-of-pocket before umbrella coverage applies.
- **Replacement Cost Estimate (RCE)**: The calculated cost to rebuild a dwelling with materials of like kind and quality at current prices; used to set Coverage A (dwelling) limits. CoreLogic and Verisk are primary vendors.
- **Catastrophe Model Score**: Output from probabilistic models (RMS, AIR, CoreLogic) estimating expected loss from natural catastrophes (hurricane, wildfire, earthquake, hail, tornado) at a property-specific level.
- **ACORD Forms**: Standardized insurance application forms maintained by ACORD (Association for Cooperative Operations Research and Development): Form 80 (homeowners), Form 90 (auto), Form 83 (umbrella).
- **Binding Authority**: The maximum risk exposure an individual underwriter or automated system can commit without escalation to a higher authority level, defined by coverage amount, hazard class, and territory.
- **Non-Renewal**: Insurer's decision not to continue coverage at the end of a policy period, distinct from mid-term cancellation. Subject to state-specific notice periods (typically 30-90 days) and permissible reason restrictions.
- **Take-All-Comers (TAC)**: State requirement that an insurer writing auto liability must accept all applicants meeting minimum eligibility criteria; cannot refuse mandatory coverage. Massachusetts is the most notable TAC state.
- **Moral Hazard**: Risk that the insured may intentionally cause or exaggerate a loss due to financial incentive (e.g., property significantly over-insured relative to market value).
- **Loss Ratio**: Incurred losses divided by earned premium for a defined period. The direct measure of how much of each premium dollar is consumed by claims.
- **Disparate Impact**: A facially neutral underwriting practice or algorithm that disproportionately affects a protected class, even absent discriminatory intent. Colorado SB21-169 and the NAIC AI Model Bulletin address this in the insurance context.
- **Residual Market**: The market mechanism (FAIR plans, assigned risk pools, joint underwriting associations) that provides coverage when the voluntary market will not. States with residual markets exceeding 1% market share include MA, MD, NC, RI (auto) and CA, FL, LA, MA, MS, NC, RI, TX (homeowners).

## Quality Checklist

1. [ ] Verified OFAC sanctions screening was completed prior to binding any coverage.
2. [ ] Confirmed credit-based insurance score was not used in any state where it is prohibited or restricted (CA, MA, HI, MI, MD, OR, UT, MN).
3. [ ] FCRA adverse action notice issued within required timeframe with four specific primary reasons (not generalized language) when credit information contributed to unfavorable decision.
4. [ ] State-specific IIPPA adverse underwriting decision notice issued independently from FCRA notice where required.
5. [ ] Non-renewal notice complies with applicable state timing requirements and moratorium restrictions (check California Insurance Code §675.1 wildfire moratoriums, Florida post-claim repair restrictions).
6. [ ] Underlying limits for umbrella policy verified against carrier minimums; any gap documented as SIR with insured acknowledgment.
7. [ ] Roof age verified against aerial imagery data source (Cape Analytics, EagleView, or equivalent) — not solely reliant on applicant-supplied information.
8. [ ] Rating factors applied are consistent with the state-approved/filed rating plan; California auto rates use driving record, mileage, and experience as primary factors in rank order.
9. [ ] No underwriting decision based solely on geographic location, property age, or lack of credit history without additional actuarial justification.
10. [ ] AI/algorithmic underwriting models documented per NAIC AI Model Bulletin governance requirements; bias testing results available for regulatory examination.
11. [ ] Domestic violence victim status not used as an underwriting factor; claims arising from abuse evaluated on medical condition only.
12. [ ] CLUE report inquiry-only records distinguished from paid claims; no adverse action taken solely on inquiry records in states prohibiting such use.
13. [ ] Replacement cost estimate validated against current construction cost indices and Coverage A set at adequate level to avoid coinsurance penalty.
14. [ ] All mandatory discounts applied (California good-driver ≥20%, Florida wind mitigation credits, multi-policy discounts where filed).
15. [ ] Underwriting file documentation sufficient to support the acceptability, tiering, and pricing decision if subject to market conduct examination by state DOI.

## References

- NAIC Model #880 — Unfair Trade Practices Act: https://content.naic.org/sites/default/files/model-law-880.pdf
- NAIC Product Filing Review Handbook (2024): https://content.naic.org/sites/default/files/pfr-24.pdf
- NAIC Market Regulation Handbook 2025 Release: https://content.naic.org/sites/default/files/inline-files/2025%20Market%20Regulation%20Handbook%20What%27s%20New.pdf
- NAIC Model Bulletin: Use of Artificial Intelligence Systems by Insurers (Dec 2023): https://content.naic.org/sites/default/files/cmte-h-big-data-artificial-intelligence-wg-ai-model-bulletin.pdf.pdf
- NAIC AI Model Bulletin Adoption Map (2024-2025): https://content.naic.org/sites/default/files/cmte-h-big-data-artificial-intelligence-wg-map-ai-model-bulletin.pdf
- NAIC Use of Credit Reports/Scoring in Underwriting (MC-20, Summer 2025): https://content.naic.org/sites/default/files/model-law-chart-mc-20-use-of-credit-reports-scoring-in-underwriting.pdf
- NAIC Prohibitions Against Redlining and Geographic Discrimination (MC-45): https://content.naic.org/sites/default/files/model-law-chart-mc-45-prohibitions-against-redlining-and-other-geographic-discriminiaton.pdf
- NAIC Regulatory Resources for Consumers on Personal Lines Pricing and Underwriting: https://content.naic.org/sites/default/files/committee_related_documents/Regulator%2520Resources%2520for%2520Consumers%2520on%2520Personal%2520Lines%2520Pricing%2520and%2520Underwriting_1.pdf
- NAIC Credit-Based Insurance Scores Topic Page: https://content.naic.org/insurance-topics/credit-based-insurance-scores
- NAIC Unfair Discrimination Principles Paper (Nov 2020): https://content.naic.org/sites/default/files/call_materials/Unfair%20discrimination%20law%2C%20Nov.%2011%2C%202020.pdf
- R Street Institute — 2024 Insurance Regulation Report Card: https://www.rstreet.org/research/2024-insurance-regulation-report-card/
- IRC Report on Personal Auto Insurance State Regulation Systems: https://insuranceindustryblog.iii.org/new-irc-reportpersonal-auto-insurancestate-regulation-systems/
- Triple-I / AM Best — P&C Underwriting Profitability 2024: https://insuranceindustryblog.iii.org/pc-underwriting-profitability-prospects-for-2024-remain-firm/
- AM Best — US P/C Industry Improves Despite 2024 Underwriting Loss: https://www.insurancejournal.com/news/national/2025/02/21/812758.htm
- Triple-I — Personal Auto 2024 Underwriting Results: https://insuranceindustryblog.iii.org/personal-auto-2024-underwriting-results-best-since-pandemic/
- California CDI — Mandatory Wildfire Moratorium on Non-Renewals: https://www.insurance.ca.gov/01-consumers/140-catastrophes/MandatoryOneYearMoratoriumNonRenewals.cfm
- California Prop 103 Auto Rating Factors Study: https://www.insurance.ca.gov/0400-news/0200-studies-reports/0600-research-studies/auto-policy-studies/executive-summary.cfm
- Colorado DOI — SB21-169 Unfair Discrimination in Insurance Practices: https://doi.colorado.gov/for-consumers/sb21-169-protecting-consumers-from-unfair-discrimination-in-insurance-practices
- Florida Statutes §626.9541 — Unfair Trade Practices: https://www.leg.state.fl.us/statutes/index.cfm?App_mode=Display_Statute&URL=0600-0699/0626/Sections/0626.9541.html
- Florida Statutes §626.9741 — Use of Credit Reports/Scores: https://www.leg.state.fl.us/statutes/index.cfm?App_mode=Display_Statute&URL=0600-0699/0626/Sections/0626.9741.html
- CAS — Unfair Discrimination in Insurance: https://www.casact.org/sites/default/files/2022-07/RP1_UnfairDiscrimination_FINAL.pdf
- FORC Journal — Disparate Impact and Unfair Discrimination: https://forc.org/Public/Public/Journals/2020/Articles/Fall_2020/Vol31Ed3Article4.aspx
- Experian — States Restricting Credit-Based Insurance Scores: https://www.experian.com/blogs/ask-experian/which-states-prohibit-or-restrict-the-use-of-credit-based-insurance-scores/
- Washington State OIC — Credit Scoring Study Bills (2025): https://www.insurance.wa.gov/about-us/news/2025/state-senate-passes-restitution-credit-scoring-study-bills
- Cape Analytics — Roof Condition for Property Insurers: https://capeanalytics.com/blog/roof-condition-for-property-insurers/
- CRS — Homeowners Insurance and California Wildfires: https://www.congress.gov/crs_external_products/IN/PDF/IN12491/IN12491.2.pdf
- State Farm — California Insurance Marketplace Statement: https://newsroom.statefarm.com/state-farm-in-california-understanding-the-issues/
- PerrKnight — U.S. P&C Personal Lines Underwriting Process: https://www.perrknight.com/2011/08/23/u-s-pc-personal-lines-insurance-underwriting-process-contractual-compliance-perspectives/
- Texas DOI — Auto and Home Policy Underwriting: https://www.tdi.texas.gov/tips/auto-and-home-policy-underwriting.html
- IIAT — Underwriting and Quoting Personal Lines: https://www.iiat.org/agency-operations/insurance-laws-regulations/insurance-laws-regulations-companies-wholesalers/underwriting-and-quoting-personal-lines