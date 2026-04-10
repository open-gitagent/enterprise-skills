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

## Role
Evaluate personal lines applications (HO/auto/umbrella) for acceptability, risk classification, and pricing under state-specific NAIC, FCRA, and McCarran-Ferguson regulatory frameworks.

## Three-Gate Decision Model

| Gate | Question | Key Factors |
|---|---|---|
| 1 — Acceptability | Within filed underwriting guidelines? | HO: construction/roof age+material/ISO PPC/CLUE history/proximity to coast+wildfire+flood/occupancy/dog breed restrictions; Auto: MVR violations 3-5yr/CLUE auto/license status/SR-22/FR-44; Umbrella: underlying limits ($300K/$500K auto, $300K+ HO), exposure count, youthful drivers |
| 2 — Classification/Tiering | Which risk segment? | Multi-variable algorithm → preferred/standard/non-standard; credit-based insurance score where state-permitted |
| 3 — Pricing | Adequate, not excessive, not unfairly discriminatory? | Filed rating plan per NAIC Model Rating Laws #1775/#1776/#1780; actuarially supported classification |

## Credit-Based Insurance Score Restrictions

| State | Auto | Homeowners |
|---|---|---|
| California, Massachusetts, Hawaii, Michigan | BANNED | CA/MA: BANNED |
| Maryland | Partial restriction | BANNED |
| Oregon, Utah, Washington, Minnesota | Partial restriction | Partial restriction |

## Evaluation Factor Weight by Line

| Factor | Homeowners | Auto | Umbrella |
|---|---|---|---|
| Prior loss history (CLUE) | High | High | High |
| Credit-based insurance score | High (where permitted) | High (where permitted) | Medium |
| Property/vehicle condition | High | Medium | N/A |
| Territory/location | High | High | Low |
| ISO Protection Class (PPC) | High | N/A | N/A |
| Roof age/material/condition | High | N/A | N/A |
| MVR violations | N/A | High | High |
| Catastrophe model score | High | Low | Low |
| Underlying limits adequacy | N/A | N/A | Critical |
| Exposure count (vehicles, properties) | N/A | N/A | High |

## Process

1. **Application Intake** — Receive ACORD 80 (homeowners), ACORD 90 (auto), ACORD 83 (umbrella); validate completeness; confirm named insured identity; OFAC SDN screening
2. **Third-Party Data Ordering** — Pull C.L.U.E. (LexisNexis); MVR (state DMV); credit-based insurance score (where permitted); replacement cost estimate (CoreLogic, Verisk); ISO PPC; catastrophe model scores (RMS/AIR/CoreLogic); flood zone determination (FEMA FIRM); wildfire/hurricane/hail risk
3. **Hazard Analysis** — Physical: roof condition via Cape Analytics/EagleView aerial imagery (66%+ owner-supplied roof ages underestimated ≥5yr per Buildfax; 20%+ understated ≥15yr), wiring type (knob-and-tube/aluminum), heating source, foundation type; Moral: fraud indicators, prior policy cancellations for misrepresentation; Morale: maintenance neglect, excessive inquiry-only CLUE hits
4. **Eligibility Screening** — Apply underwriting rules engine; check state-specific prohibited factors; CA auto: driving record/mileage/experience as three mandatory primary factors in rank order (CIC §1861.02); credit ban states: suppress CBIS modules; domestic violence protections: NAIC Model #880 §4.G prohibits basing decisions on abuse victim status
5. **Tier Assignment** — Apply approved classification plan; document contributing variables; FCRA §615(a): if credit contributed to less favorable tier, issue adverse action with 4 specific primary reasons; FL §626.9741: specific language required ("poor credit history" does not satisfy statutory requirement)
6. **Rate Application** — Apply territory/coverage/deductible/discount factors per filed rating algorithm; mandatory CA good-driver discount ≥20% for ≤1 violation point in 3 years (Prop 103); wind mitigation credits in FL/SC
7. **Coverage Determination** — Set limits/deductibles/endorsements; confirm dwelling replacement cost vs. Coverage A; umbrella: verify underlying meets required minimums; document SIR gap with insured acknowledgment where underlying falls short
8. **Documentation and Issuance** — Generate declination/non-renewal per state timing requirements (typically 30-60 days non-renewal, 10-45 days cancellation); NAIC Model #725 for auto declinations; FCRA adverse action within required timeframes; NAIC Model #670 IIPPA notice independent of FCRA notice

## Glossary

| Term | Definition |
|---|---|
| C.L.U.E. | Comprehensive Loss Underwriting Exchange (LexisNexis); ≤7 years claims history; distinguishes paid claims from inquiry-only records |
| ISO PPC | ISO Protection Class 1 (best) to 10 (worst); fire suppression capability via FSRS scoring (fire dept/water/communications/community risk) |
| CBIS | Credit-Based Insurance Score; translates credit bureau data into loss likelihood predictor; distinct from FICO lending score |
| Combined Ratio | Loss ratio + expense ratio; <100 = underwriting profit; personal auto 98.7 (2024); homeowners 105.7 (2024) |
| Adverse Action Notice | Required under FCRA §615(a)/state law for unfavorable decision based on consumer report; 4 specific reasons required |
| Tiering | Risk segmentation beyond standard classification variables using additional underwriting characteristics |
| FAIR Plan | State-mandated insurer of last resort; CA FAIR Plan exposure $650B mid-2025 (289% increase since FY2021); 7 of 12 top HO insurers limiting CA coverage |
| MVR | Motor Vehicle Report; state DMV violations, license status, endorsements/restrictions for prior 3-5 years |
| Unfair Discrimination | Treating similarly situated risks in same actuarial class differently; distinct from civil rights but intersecting via disparate impact |
| SIR | Self-Insured Retention — gap between actual underlying limits and umbrella attachment point; insured bears out-of-pocket |
| RCE | Replacement Cost Estimate; cost to rebuild dwelling at current prices; CoreLogic and Verisk are primary vendors |
| Catastrophe Model Score | Probabilistic expected loss from natural catastrophes (RMS/AIR/CoreLogic) at property-specific level |
| ACORD Forms | Form 80 (homeowners), Form 90 (auto), Form 83 (umbrella) |
| Binding Authority | Maximum risk exposure an underwriter/automated system can commit without escalation |
| Non-Renewal | Decision not to continue coverage at policy period end; state notice periods typically 30-90 days |
| Take-All-Comers (TAC) | State requirement to accept all applicants meeting minimum eligibility (Massachusetts most notable for auto) |
| Moral Hazard | Risk insured may intentionally cause/exaggerate loss due to financial incentive |
| Loss Ratio | Incurred losses / earned premium |
| Disparate Impact | Facially neutral practice disproportionately affecting protected class; addressed by CO SB21-169 and NAIC AI Bulletin |
| Residual Market | FAIR plans/assigned risk pools/JUAs providing coverage when voluntary market will not write |

## Checklist

- [ ] OFAC SDN screening completed before binding any coverage
- [ ] Credit-based insurance score not used in prohibited/restricted states (CA/MA/HI/MI auto; CA/MA/MD homeowners; partial MD/OR/UT/WA/MN)
- [ ] FCRA adverse action notice within required timeframe with 4 specific primary reasons (not generalized language) when credit contributed to unfavorable decision
- [ ] State-specific IIPPA adverse underwriting decision notice issued independently from FCRA notice (NAIC Model #670)
- [ ] Non-renewal notice complies with state timing and moratorium restrictions (CA Insurance Code §675.1: 1-year wildfire moratorium post-governor emergency declaration; FL post-claim repair restrictions)
- [ ] Umbrella underlying limits verified vs. carrier minimums; SIR gap documented with insured acknowledgment
- [ ] Roof age verified against aerial imagery (Cape Analytics/EagleView/equivalent) — not solely applicant-supplied
- [ ] Rating factors consistent with state-approved/filed plan; CA auto uses driving record/mileage/experience as primary factors in rank order (CIC §1861.02)
- [ ] No underwriting decision based solely on geographic location, property age, or lack of credit history without additional actuarial justification (NAIC Model #880 §4.B)
- [ ] AI/algorithmic underwriting models documented per NAIC AI Model Bulletin Dec 2023 governance requirements; bias testing results available for state DOI market conduct examination
- [ ] Domestic violence victim status not used as underwriting factor; claims from abuse evaluated on medical condition only (NAIC Model #880 §4.G)
- [ ] CLUE inquiry-only records distinguished from paid claims; no adverse action solely on inquiries in prohibiting states
- [ ] Replacement cost estimate validated against current construction cost indices; Coverage A set at adequate level
- [ ] All mandatory discounts applied (CA good-driver ≥20%, FL wind mitigation credits, multi-policy where filed)
- [ ] Underwriting file documentation sufficient to support acceptability/tiering/pricing under state DOI market conduct examination

## References
FCRA 15 USC §1681 §615(a)/§604(c); OFAC SDN; GLBA; McCarran-Ferguson Act 1945; NAIC Model #880/725/670/#1775/#1776/#1780; NAIC AI Model Bulletin Dec 2023 (25+ states adopted); CA Prop 103; CA Insurance Code §675.1 (wildfire moratoriums 1yr); CO SB21-169 (3 CCR 702-10 eff. Nov 2023); FL §626.9741/§626.9541; NY Insurance Circular Letter No. 7 (2024); personal auto combined ratio 98.7 (2024); homeowners combined ratio 105.7 (2024); CA FAIR Plan $650B mid-2025; NAIC Product Filing Review Handbook 2024; Buildfax roof age data; CAS; IRC; AM Best
