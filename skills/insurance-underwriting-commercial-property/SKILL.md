---
name: insurance-underwriting-commercial-property
description: >
  Commercial property insurance underwriting expertise including risk evaluation, occupancy analysis, loss history review, pricing, and regulatory compliance.
metadata:
  vertical: bfsi-insurance
  function: risk-assessment
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "NAIC, ISO, AM Best, State DOI"
---

# Insurance Underwriting Commercial Property

## Domain Overview

Commercial property underwriting evaluates the insurability and pricing of physical assets — buildings, business personal property, and the income streams they generate — against the full spectrum of perils including fire, wind, water, earthquake, and terrorism. The discipline traces its origins to post-Great Fire of London (1666) practices and still relies on the same foundational COPE framework: Construction, Occupancy, Protection, and Exposure. Modern underwriters overlay this framework with catastrophe modeling, geospatial analytics, and regulatory compliance across 50+ state jurisdictions.

The regulatory environment is state-based, not federal. Each state department of insurance enforces its own rate and form filing requirements, guided by NAIC model laws. NAIC Model #777 governs commercial rate and policy form regulation, establishing whether a state operates under prior-approval, file-and-use, use-and-file, or flex-rating systems. NAIC Model #880 (Unfair Trade Practices Act) prohibits unfair discrimination between individuals or risks of the same class and essentially the same hazard — including geographic discrimination (redlining) per NAIC MC-45. Underwriters must price risk using sound actuarial principles; geographic location alone cannot justify declination or surcharge unless supported by actual or reasonably anticipated loss experience.

ISO (now Verisk) serves as the dominant advisory organization, publishing standard coverage forms (CP 00 10, CP 00 30, CP 10 30), loss costs, and classification systems that most carriers adopt with proprietary modifications via loss cost multipliers. The NAIC's Casualty Actuarial and Statistical Task Force published a Regulatory Review of Predictive Models White Paper (adopted April 2021) establishing expectations for how regulators review predictive models within P&C rate filings, directly affecting how carriers deploy AI/ML in commercial property pricing. The NAIC Catastrophe Modeling Primer (March 2025) further codifies regulatory expectations around cat model use for flood, wildfire, hurricane, and earthquake perils.

The market has undergone significant hardening since 2020 due to escalating catastrophe losses. Verisk's 2024 Global Modeled Catastrophe Losses report identifies a $32 billion year-over-year increase in non-crop global modeled insured average annual loss (AAL), with five-year insured loss averages at $132 billion compared to $104 billion in the preceding period. Secondary perils — severe convective storms, wildfire, and inland flood — now outpace headline hurricane risk by a 2:1 ratio in frequency-driven losses. This fundamentally reshapes underwriting appetite, particularly for properties in wildfire-urban interface zones, coastal wind corridors, and FEMA Special Flood Hazard Areas.

## Core Decision Framework

### The COPE Analysis

Every commercial property risk is evaluated through four interdependent dimensions:

**Construction (C):** ISO classifies buildings into six construction classes based on fire resistivity:
- Class 1 — Frame: Exterior walls of wood or combustible materials. Highest fire hazard rating.
- Class 2 — Joisted Masonry: Masonry exterior walls with combustible floors/roof. Most common class for older commercial buildings.
- Class 3 — Noncombustible: Exterior walls, floors, and roof of metal or noncombustible materials (e.g., Butler buildings). Vulnerable to collapse at high temperatures despite being noncombustible.
- Class 4 — Masonry Noncombustible: Masonry exterior walls (≥4" thick) with noncombustible floors/roof. Common for shopping centers, warehouses, schools.
- Class 5 — Modified Fire Resistive: Fire-resistive materials with rating of ≥1 hour but <2 hours. Typical for mid-rise office buildings and condominiums.
- Class 6 — Fire Resistive: All structural elements rated ≥2 hours fire resistance. Best from underwriting standpoint. Concrete/masonry throughout.

Critical rule: If exterior load-bearing walls are combustible (including gables), the entire structure rates as Class 1 Frame, regardless of roof material. Mixed construction requires ≥66⅔% superior construction in both walls and combined floor/roof area to qualify for the higher class.

**Occupancy (O):** The use and contents of the building drive both frequency and severity expectations. A restaurant with deep-frying operations presents fundamentally different risk than a law office in an identical building. Special hazards include flammable/combustible liquids, spray-painting operations, commercial cooking, welding, cutting, and dust-producing operations (woodworking). Vacancy >60 days triggers exclusion of vandalism, sprinkler leakage, glass breakage, water damage, and theft under the standard ISO vacancy provision.

**Protection (P):** Two dimensions — public and private. Public protection is measured by ISO's Public Protection Classification (PPC), grading fire departments from 1 (exemplary) to 10 (does not meet minimum criteria). PPC evaluates: fire department response times, water supply adequacy, personnel training, equipment, and communications. Split classifications (e.g., 5/10 or 5X) reflect distance from creditable water supply — properties >1,000 feet from a hydrant receive the second (worse) classification. Private protection includes automatic sprinkler systems, fire alarms, fire walls, fire doors, and portable extinguishers. Active systems (sprinklers, alarms) provide greatest premium credit.

**Exposure (E):** External factors including adjacent building construction, distance, and occupancy; proximity to wildfire-urban interface zones; flood zone designation (FEMA SFHA vs. Zone X); seismic zone; crime rates; and proximity to coastal wind hazard. Distance <100 feet from high-hazard operations (e.g., flammable liquid storage) materially increases exposure.

### Valuation Methodology Selection

The underwriter must determine and verify the correct valuation basis, as it drives premium, coinsurance compliance, and claims outcomes:

- **Replacement Cost (RC):** Cost to repair/replace with like kind and quality at current prices, no deduction for depreciation. Most common for buildings and BPP. Not available for personal property of others, contents of residences, works of art/antiques, or stock (unless endorsed).
- **Actual Cash Value (ACV):** Replacement cost minus depreciation. Default valuation under ISO CP 00 10 when RC is not elected.
- **Functional Replacement Cost:** Cost to replace with property serving same function, using modern materials/methods. Lower than RC. Used when exact replication is impractical.
- **Agreed Value:** Predetermined value agreed by insured and insurer, suspending coinsurance penalty for the policy period. Requires a current Statement of Values. Must be renewed each policy term.

### Rate Development

Premium = Loss Cost × Loss Cost Multiplier × Modifying Factors. Seven factors determine the base rate per ISO methodology: (1) coverage form, (2) cause of loss form, (3) construction class, (4) occupancy class, (5) location/territory, (6) amount of insurance, and (7) applicable coinsurance percentage. Schedule rating credits and debits (typically ±25% to ±40% depending on state) allow underwriter judgment on premises condition, equipment maintenance, loss history, and management quality.

## Step-by-Step Process

1. **Submission Intake & Triage:** Receive ACORD 140 (Property Section) and supplemental applications. Verify completeness: building address, construction year, square footage, occupancy description, fire protection details, loss history (minimum 5 years), current Statement of Values.

2. **COPE Data Collection:** Order or verify ISO/Verisk property reports. Confirm construction class against building plans or inspection reports. Order PPC report for each location. Identify all special hazards from occupancy data.

3. **Valuation Verification:** Compare submitted values against Verisk 360Value, Marshall & Swift/Boeckh, or comparable replacement cost estimators. Flag any value discrepancy >15% — this indicates potential coinsurance exposure. Verify whether Replacement Cost or ACV is requested and appropriate.

4. **Catastrophe Exposure Assessment:** Geocode each location to latitude/longitude. Run through catastrophe models (RMS RiskLink, AIR Touchstone, CoreLogic) for wind, earthquake, flood, and wildfire. Compare modeled PML (Probable Maximum Loss) and AAL (Average Annual Loss) against portfolio aggregation limits. Check FEMA flood zone designation. Verify wildfire risk score (particularly in California, Colorado, Oregon).

5. **Loss History Analysis:** Review 5-year loss runs. Calculate loss ratio (incurred losses ÷ earned premium). Evaluate loss frequency vs. severity patterns. Attritional losses >3 per year signal occupancy or maintenance issues. Any single loss >50% of property value warrants deep-dive into cause, remediation, and building code upgrade status.

6. **Coverage Structure & Pricing:** Select appropriate coverage forms (CP 00 10, CP 00 30/32 for BI, CP 10 30 for Special Causes of Loss). Apply coinsurance percentage (80%, 90%, or 100%). Calculate premium using base rate, classification, and all applicable modifications. Determine deductible options. Apply schedule rating within filed limits. Consider Agreed Value endorsement to eliminate coinsurance risk.

7. **Terms & Conditions:** Set sub-limits for ordinance or law, flood, earthquake, equipment breakdown. Apply wind/hail percentage deductibles in coastal zones. Set terrorism coverage per TRIA requirements. Apply protective safeguards endorsement (CP 04 11) if premium credits given for sprinklers/alarms.

8. **Referral & Authority:** Compare risk against underwriting guidelines and binding authority. Risks exceeding PML thresholds, located in moratorium zones, or with adverse loss history require referral to senior underwriter or home office.

9. **Documentation & File:** Complete underwriting worksheet documenting all COPE data, pricing rationale, and declination reasons (if applicable). Maintain per NAIC Model #720 requirements — declinations and non-renewals require specific written reasons.

## Evaluation Criteria

| Factor | Weight | Superior | Acceptable | Substandard |
|--------|--------|----------|------------|-------------|
| Construction Class | 20% | Class 5-6 (fire resistive) | Class 3-4 (noncombustible) | Class 1-2 (combustible) |
| Occupancy Hazard | 20% | Office, retail (low hazard) | Light manufacturing, warehouse | Heavy manufacturing, chemical storage |
| Protection (PPC) | 15% | PPC 1-4 with sprinklers | PPC 5-7, partial sprinklers | PPC 8-10, no sprinklers |
| Catastrophe Exposure | 15% | Outside all hazard zones | Moderate zone, mitigated | High zone, unmitigated |
| Loss History (5-yr) | 15% | Loss ratio <30%, no freq. | Loss ratio 30-60% | Loss ratio >60% or >3 losses/yr |
| Valuation Adequacy | 10% | Within 5% of RC estimate | Within 15% of RC estimate | >15% variance (coinsurance risk) |
| Management Quality | 5% | Proactive maintenance, BCP | Average maintenance | Deferred maintenance, no BCP |

## Red Flags & Edge Cases

1. **Mixed Construction Misclassification:** A building with masonry walls but wood-framed gable ends exceeding 33⅓% of total exterior wall area must be downgraded to Class 1 Frame. Misclassifying as Class 2 Joisted Masonry underprices the risk by 40-60% and creates E&O exposure for the underwriter.

2. **Coinsurance Trap on Appreciating Markets:** Post-2020 construction costs have risen 30-50% in many markets. A building insured at $5M replacement cost in 2019 may now require $7.5M. With 80% coinsurance, the insured carries $5M against a required $6M — triggering a 17% penalty on every partial loss. Underwriters must verify current values at each renewal using updated cost estimators.

3. **Vacancy Beyond 60 Days:** ISO CP 00 10 includes a vacancy provision that strips coverage for vandalism, sprinkler leakage, glass breakage, water damage, and theft after 60 consecutive days. A building undergoing renovations may technically be "vacant" even with contractors present. Underwriters must confirm occupancy status and consider the CP 04 50 Vacancy Changes endorsement.

4. **Business Income Underinsurance:** The period of restoration for a major fire at a complex commercial property (e.g., custom manufacturing facility) regularly exceeds 12-18 months. Standard BI limits based on 12-month projections leave a gap when supply chain delays extend restoration to 24+ months. Post-COVID, restoration periods have increased 30-40% due to labor and material shortages.

5. **Ordinance or Law Gap:** Older buildings in jurisdictions with modern building codes face demolition-and-rebuild scenarios where code compliance costs add 25-50% above pre-loss replacement cost. Standard CP 00 10 excludes increased cost of construction due to ordinance or law. Without CP 04 05 (Ordinance or Law Coverage), the insured absorbs this gap. Underwriters should always recommend Coverages A, B, and C of this endorsement.

6. **Wildfire Score Deterioration in WUI Zones:** Properties in California, Colorado, and Oregon wildfire-urban interface areas may have acceptable wildfire scores at policy inception that deteriorate mid-term due to drought conditions, adjacent land clearing, or changes in vegetation density. Travelers' proprietary wildfire underwriting factors terrain slope, vegetation density, propensity to burn, and road access — static scoring at issuance misses dynamic risk changes.

7. **Protective Safeguards Endorsement Compliance Failure:** Endorsement CP 04 11 conditions coverage on maintaining specific protective systems (sprinklers, alarms). If an insured turns off a sprinkler system for maintenance during winter freeze and suffers a fire loss, coverage may be voided. Underwriters applying sprinkler credits must verify impairment notification procedures.

8. **TRIA Terrorism Coverage Disclosure Gap:** The Terrorism Risk Insurance Program requires insurers to make available coverage for certified acts of terrorism and disclose premium for that coverage. Failure to provide the TRIA disclosure and policyholder election form creates regulatory violations per NAIC data call requirements. Commercial properties with >$10M premium in TRIP-eligible lines must report to NAIC/Treasury via Joint Data Templates by May 15 annually.

9. **Roof Age and ACV Sub-Limitation:** ISO endorsement CP 10 36 (Limitations on Coverage for Roof Surfacing) allows carriers to value roof damage on ACV basis rather than RC. This endorsement, applied to buildings with roofs aged 15+ years, creates a significant coverage reduction. Underwriters using this endorsement should clearly communicate the impact to agents to avoid E&O claims.

10. **Flood Zone Reclassification Mid-Term:** FEMA periodically revises flood maps. A property rated as Zone X (minimal flood risk) may be reclassified to Zone AE (100-year floodplain) during the policy term. Standard commercial property forms exclude flood. If the underwriter did not recommend or require separate flood coverage at binding, the insured has an uncovered exposure.

11. **Contingent Business Income From Single-Source Supplier:** A manufacturer dependent on a single raw material supplier faces BI exposure even if its own property is undamaged. Standard BI forms cover only direct physical damage at the insured premises. Without the CP 15 08 (Business Income From Dependent Properties) endorsement, this off-premises dependency is excluded.

12. **Cannabis Occupancy in Legalized States:** Properties leased to state-legal cannabis operations create underwriting conflicts between state law and federal Schedule I classification. Many standard markets exclude cannabis occupancy entirely. Surplus lines markets may write the risk but at significantly higher rates with restrictive terms.

## Common Mistakes

- **Failing to order updated replacement cost estimates at renewal**, relying instead on trended values that compound errors year over year. A 3% annual trend applied to an initially understated value perpetuates coinsurance exposure.
- **Accepting agent-submitted construction class without verification.** Field inspections or Verisk property reports frequently reveal discrepancies — e.g., a building described as "masonry" that has combustible wood-frame additions or retrofitted aluminum siding over wood framing.
- **Ignoring the "party wall" valuation issue.** When a building shares a party wall with an adjacent structure, CP 00 10 covers the insured's ownership interest. However, the coinsurance clause applies to the full value of the wall, creating potential penalty exposure if only the ownership share is insured.
- **Underwriting BI coverage based on gross revenue rather than net income plus continuing expenses.** This systematically inflates BI limits, overcharging the insured, or conversely leaves gaps when the wrong metric was used in reverse.
- **Applying schedule rating debits without documentation.** State market conduct examiners review schedule rating files for actuarial justification. Debits applied without written rationale for the specific risk characteristic create regulatory findings and potential fines.
- **Not verifying sprinkler system adequacy for current occupancy.** A sprinkler system designed for office occupancy (Light Hazard) may be grossly inadequate if the building is converted to warehouse use (Ordinary Hazard Group 2). NFPA 13 classifications must match actual occupancy.
- **Overlooking distance-to-hydrant in split PPC classifications.** A property with PPC 4/10 rating that is >1,000 feet from a creditable hydrant gets the Class 10 rate, not Class 4. This single factor can double or triple the base rate.

## Regulatory & Compliance Requirements

### State Rate and Form Filing
- **NAIC Model #777** establishes the framework for commercial property rate and form regulation. States implement via prior-approval, file-and-use, use-and-file, or competitive rating systems. Underwriters must know their state's filing status — writing at unfiled rates creates regulatory violations.
- **California Proposition 103** requires prior approval of all P&C rates. California also requires wildfire mitigation credits per 10 CCR §2644.9 and permits catastrophe model use per 10 CCR §2644.4.5.
- **NAIC Model #720** (Property Insurance Declination, Termination and Disclosure) mandates specific written reasons for declination, cancellation, or non-renewal.

### Unfair Trade Practices
- **NAIC Model #880** Section 4(7)(4) prohibits refusing to insure, refusing to renew, canceling, or limiting coverage "solely because of the geographic location of the risk, unless such action is the result of the application of sound underwriting and actuarial principles related to actual or reasonably anticipated loss experience."
- **NAIC MC-45** chart tracks state-by-state prohibitions against redlining and geographic discrimination. Underwriters cannot use ZIP code or neighborhood demographics as proxies for risk without actuarial support.

### Market Conduct
- **Market Conduct Annual Statement (MCAS)** data collection requires P&C insurers to report complaints, claims handling metrics, and underwriting actions. State examiners review underwriting files during market conduct examinations for fair and non-discriminatory practices.
- **Predictive Model Oversight:** The NAIC Casualty Actuarial and Statistical Task Force's Regulatory Review of Predictive Models White Paper (2021) establishes that regulators may request full documentation of any predictive model used in rate-setting, including variable selection, disparate impact testing, and model governance.

### Terrorism Risk Insurance Program (TRIP)
- Federally backstopped program requiring insurers to make terrorism coverage available. Insurance groups with >$10M TRIP-eligible commercial direct earned premium must submit Joint Data Templates to NAIC/Treasury annually. Exemption applies below the $10M threshold (excluding captives and alien surplus lines).

### Catastrophe Model Use
- **NAIC Catastrophe Modeling Primer (March 2025)** provides regulatory guidance on acceptable model use for hurricane, earthquake, flood, and wildfire. Some states (Florida, Louisiana, California) have model approval processes. The Florida Commission on Hurricane Loss Projection Methodology (FCHLPM) must approve hurricane models used in rate filings.

## Terminology

- **COPE:** Construction, Occupancy, Protection, Exposure — the four-factor framework for commercial property risk evaluation.
- **ISO CP 00 10:** Building and Personal Property Coverage Form — the foundational ISO form covering direct physical loss to buildings and BPP.
- **Causes of Loss — Special Form (CP 10 30):** Open-perils (all-risk) cause of loss form providing broadest standard coverage. Covers all causes of loss not specifically excluded.
- **Coinsurance:** Contractual requirement that the insured carry coverage equal to a stated percentage (80%, 90%, 100%) of the property's value. Failure triggers proportional penalty on partial losses.
- **Agreed Value:** Optional coverage suspending the coinsurance penalty for the policy term, requiring a current Statement of Values signed by the insured and insurer.
- **Replacement Cost Value (RCV):** Cost to repair or replace damaged property with like kind and quality at current prices, without deduction for depreciation.
- **Actual Cash Value (ACV):** Replacement cost minus depreciation. The default valuation method under ISO forms unless RC is specifically endorsed.
- **PPC (Public Protection Classification):** Verisk/ISO grading system (1-10) measuring a community's fire suppression capability, based on the Fire Suppression Rating Schedule (FSRS).
- **Probable Maximum Loss (PML):** The estimated maximum loss likely to occur from a single event, considering all loss mitigation features. Inversely proportional to building size — larger buildings have lower PML as percentage of total value.
- **Average Annual Loss (AAL):** The expected value of insured losses per year across all modeled events, used for catastrophe pricing.
- **Loss Cost:** The portion of a rate that covers expected losses and loss adjustment expenses. Published by ISO as advisory; carriers apply proprietary multipliers.
- **Loss Cost Multiplier (LCM):** A carrier-specific factor applied to ISO loss costs to produce the final rate, encompassing operating expenses, profit, and contingencies.
- **Schedule Rating:** Underwriter-applied credits or debits (within state-filed limits, typically ±25-40%) based on individual risk characteristics not captured in base rating.
- **Period of Restoration:** The time frame during which Business Income coverage applies — begins at the time of direct physical loss and ends when damaged property should be repaired/replaced with reasonable speed and similar quality materials.
- **Ordinance or Law Coverage:** Endorsement (CP 04 05) covering (A) loss to undamaged portion of building required to be demolished, (B) demolition and removal costs, and (C) increased cost of construction to meet current building codes.
- **Business Income From Dependent Properties:** Endorsement CP 15 08 extending BI coverage to losses caused by damage at locations of key suppliers, customers, manufacturers, or leaders.
- **Protective Safeguards Endorsement (CP 04 11):** Conditions coverage on maintaining specified protective systems. Failure to maintain voids coverage for losses that the system would have prevented.
- **Fire Suppression Rating Schedule (FSRS):** The evaluation tool used by ISO/Verisk to assign PPC grades, analyzing fire department equipment, staffing, training, response distance, and water supply.
- **TRIA (Terrorism Risk Insurance Act):** Federal law creating a public-private system for insuring commercial property and casualty losses from certified acts of terrorism, currently reauthorized through 2027.
- **Vacancy Provision:** Standard clause in CP 00 10 reducing coverage after 60+ consecutive days of vacancy — excludes vandalism, sprinkler leakage, glass breakage, water damage, and theft; applies 15% reduction to remaining covered perils.
- **Blanket Coverage:** A single limit of insurance applying across multiple locations or categories of property, reducing coinsurance risk by pooling values.
- **Specific Rating:** Premium determination based on detailed inspection and classification of the individual risk, as opposed to class rating using standardized tables.
- **Manuscript Policy:** Custom-drafted policy language not based on ISO standard forms, used for large or complex commercial property accounts requiring tailored coverage.

## Quality Checklist

1. ☐ Construction class verified against Verisk property report or physical inspection — not solely agent-submitted data
2. ☐ Replacement cost values validated against 360Value, Marshall & Swift, or comparable estimator within prior 12 months
3. ☐ Coinsurance percentage aligned with insured's ability to maintain adequate values — Agreed Value recommended for values >$5M
4. ☐ PPC report obtained for each location with split classification evaluated (distance to hydrant confirmed)
5. ☐ Catastrophe model run completed for all perils applicable to location (wind, earthquake, flood, wildfire) with PML and AAL documented
6. ☐ Business Income adequacy worksheet completed, including Extended Period of Indemnity and Extra Expense needs assessment
7. ☐ Five-year loss history reviewed with frequency/severity analysis documented in underwriting file
8. ☐ Ordinance or Law coverage offered and insured's election documented (acceptance or written declination)
9. ☐ TRIA disclosure provided and policyholder election form executed and filed
10. ☐ Schedule rating credits/debits individually justified in writing per state filing requirements
11. ☐ Protective safeguards endorsement conditions verified — sprinkler system matches current occupancy per NFPA 13
12. ☐ Vacancy status confirmed (<60 days) with process for mid-term notification if status changes
13. ☐ All declination or non-renewal reasons documented per NAIC Model #720 requirements
14. ☐ Flood zone designation verified via current FEMA map (check for pending LOMR or map revision)
15. ☐ Wildfire risk score documented for properties in WUI zones (California, Colorado, Oregon — verify mitigation credits per state requirements)

## References

1. NAIC Model Laws, Regulations, and Guidelines — Summer 2025: https://content.naic.org/sites/default/files/publication-model-2025-summer.pdf
2. NAIC Model #777 — Property and Casualty Commercial Rate and Policy Form Model Law: https://content.naic.org/sites/default/files/model-law-777.pdf
3. NAIC Model #880 — Unfair Trade Practices Act: https://content.naic.org/sites/default/files/model-law-880.pdf
4. NAIC MC-45 — Prohibitions Against Redlining and Other Geographic Discrimination: https://content.naic.org/sites/default/files/model-law-chart-mc-45-prohibitions-against-redlining-and-other-geographic-discriminiaton.pdf
5. NAIC Annual Report 2024 — Advancing Insurance Regulation: https://content.naic.org/sites/default/files/annual-report-2024-advancing-insurance-regulation.pdf
6. NAIC Catastrophe Modeling Primer (March 2025): https://content.naic.org/sites/default/files/committees-pending-action-cat-mod-primer.pdf
7. NAIC TRIP Data Call Letter 2025: https://content.naic.org/sites/default/files/inline-files/DataCallLetter2025_final.pdf
8. ISO CP 00 10 06 07 — Building and Personal Property Coverage Form: https://www.propertyinsurancecoveragelaw.com/wp-content/uploads/2023/12/CP-00-10-10-12-Building-and-Personal-Property-Coverage-Form.pdf
9. Verisk 2024 Global Modeled Catastrophe Losses: https://www.verisk.com/4a9504/siteassets/extreme-event-solutions/2024-verisk-global-modeled-catastrophe-losses.pdf
10. Aon 2024 Climate and Catastrophe Insights Report: https://assets.aon.com/-/media/files/aon/reports/2024/climate-and-catastrophe-insights-report.pdf
11. Travelers Climate Underwriting Strategy: https://sustainability.travelers.com/drivers-of-sustained-value/climate-strategy/underwriting-strategy
12. AXA XL — Changing the Commercial Property Underwriting Dynamic: https://www.zywave.com/wp-content/uploads/sites/2/2022/04/AXA-XL-Whitepaper-Changing-the-Commercial-Property-Underwriting-Dynamic.pdf
13. WSRB — Guide to Commercial Property Risk Assessment: https://www1.wsrb.com/resources/risk-assessment-guide
14. Verisk — Ten Things a Commercial Property Underwriter Needs to Know: https://www.verisk.com/blog/ten-things-a-commercial-property-underwriter-needs-to-know/
15. Christopher J. Boggs — Understanding Commercial Property Underwriting: COPE in ALL its Glory (Big "I" Virtual University): https://www.wainsurance.org/Events/SiteAssets/Pages/YAConference/default/COPE%20Webinar.pdf
16. ISO Construction Classification Reference (Texas SORM): https://www.sorm.state.tx.us/wp-content/uploads/2017/06/Construction%20and%20Occupancy%20Classification.pdf
17. ISO's Public Protection Classification (PPC) Program: https://www.isomitigation.com/ppc/
18. California Department of Insurance — Commercial Insurance Guide: https://www.insurance.ca.gov/01-consumers/105-type/95-guides/09-comm/commercialguide.cfm
19. Insurance Valuation Problems — Coinsurance and Ordinance or Law (IIAN/Risk Education): https://www.riskeducation.org/pub/media/Dallas-MEGA/Sect-10.pdf
20. Gallagher Re — Natural Catastrophe and Climate Report 2024: https://www.ajg.com/gallagherre/-/media/files/gallagher/gallagherre/news-and-insights/2025/natural-catastrophe-and-climate-report-2025.pdf
21. NAIOP — Coinsurance: The Misunderstood Property Insurance Pitfall: https://www.naiop.org/research-and-publications/magazine/2019/summer-2019/perspectives/coinsurance-the-misunderstood-property-insurance-pitfall/
22. Adjusters International — Revisions to ISO Commercial Property Coverage Forms: https://www.adjustersinternational.com/pubs/adjusting-today/be-aware-of-recent-revisions-to-iso-commercial-property-coverage-forms/
23. Anderson Kill — Business Income Coverage: A Critical and Often Overlooked Area: https://andersonkill.com/wp-content/uploads/2023/09/PublicationID_1488_Business-Income-Coverage-a-Critical-and-Often-Overlooked-Area-of-Property-Insurance.pdf
24. Investopedia — Discrimination in Insurance Underwriting Guidelines: https://www.investopedia.com/insurance-underwriting-guidelines-discrimination-5203311
25. NAIC State Insurance Regulation White Paper: https://content.naic.org/sites/default/files/inline-files/topics_white_paper_hist_ins_reg.pdf
26. NY DFS Insurance Enforcement Actions: https://www.dfs.ny.gov/industry_guidance/enforcement_actions_Insurance
27. InsuranceXDate — Form CP 00 10 Analysis: https://www.insurancexdate.com/insurance-forms/CP/CP-00-10/
28. Centurisk — Fire Resistive Construction and ISO Classifications: https://centurisk.com/blog/hot-details-on-fire-resistive-construction-and-other-iso-classifications-rm20/