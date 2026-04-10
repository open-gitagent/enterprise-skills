---
name: mortgage-processing
description: >
  Residential mortgage origination and processing including application review, documentation, appraisal coordination, and closing procedures.
metadata:
  vertical: bfsi-banking
  function: lending
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "TILA-RESPA, CFPB, Fannie Mae"
---

## Role
Process residential mortgage applications from six-element TRID trigger through post-closing QC under CFPB, TRID, ATR/QM, HMDA, and fair lending requirements.

## Core Decision Framework

| Gate | Decision | Key Rule |
|---|---|---|
| Application Completeness | 6 TRID data elements received? | Name/income/SSN/property address/estimated value/loan amount; 6th element starts 3-biz-day LE clock |
| Product-Regulatory Mapping | TRID-covered? | Closed-end purchase/refi/construction = TRID; HELOC = Reg Z §1026.40; reverse mortgage = HUD-1/TIL |
| Fee Classification | Tolerance bucket? | Zero: creditor/broker/affiliate/transfer taxes/no-shop services; 10%: shopped from SPL; Unlimited: shopped off SPL/prepaid interest/property insurance/initial escrow |
| Changed Circumstance | Valid trigger to reset tolerances? | 6 triggers: changed circumstance affecting charges or eligibility, borrower-requested change, rate lock, LE expiration, delayed settlement on construction |
| Underwriting Alignment | ATR/QM status? | Safe-harbor QM: APR ≤ APOR+1.50pp; rebuttable presumption: ≤APOR+2.25pp; points-and-fees ≤3%; verify income/debt via third-party records |

## Performance Metrics

| Metric | Target | Critical Threshold |
|---|---|---|
| LE delivery timeliness | 100% within 3 biz days | <95% = corrective action |
| CD delivery timeliness | 100% ≥3 biz days pre-closing | Any miss = TRID violation |
| Fee tolerance cure rate | 0% uncured violations at closing | Any uncured = regulatory finding |
| HMDA data accuracy | >99% field-level | Error >5% key fields = exam citation |
| Adverse action notice | 100% within 30 days of completed application | Missed = Reg B violation |
| Appraisal delivery | 100% ≥3 days pre-consummation | Missed = ECOA violation |
| Intent to proceed documentation | 100% before fee collection | Undocumented = TRID violation |
| Post-closing QC defect rate | <5% sampled loans | >10% = systemic control failure |
| Application-to-close cycle | ≤45 days purchase / ≤35 days refi | >60 days = operational concern |

## Regulatory Reference Table

| Regulation | Citation | Requirement |
|---|---|---|
| TRID (LE/CD) | 12 CFR §1026.19(e)(f)(g); §1026.37; §1026.38 | Timing, content, delivery of LE and CD for closed-end mortgage loans |
| Regulation X (RESPA) | 12 CFR Part 1024 | Settlement procedures, anti-kickback §8, escrow |
| Regulation Z (TILA) | 12 CFR Part 1026 | APR disclosure, HPML, LO compensation |
| ATR/QM Rule | 12 CFR §1026.43 | Ability-to-repay; QM safe harbor/rebuttable presumption |
| Regulation B (ECOA) | 12 CFR Part 1002 | Anti-discrimination; adverse action 30 days; appraisal copy |
| Regulation C (HMDA) | 12 CFR Part 1003 | 48+ data fields annually |
| HPML Appraisal | 12 CFR §1026.35(c) | Certified appraiser; 2nd appraisal for flips within 180 days |
| AVM Quality Control | 12 CFR §1026.42 (eff. 10/1/2025) | AVM accuracy, fair lending, nondiscrimination |
| Flood Insurance | 42 USC §4012a; 12 CFR 208.25 | Mandatory for Special Flood Hazard Areas |
| FCRA | 15 USC §1681 | Permissible purpose for credit pulls; adverse action notice |
| SAFE Act/NMLS | 12 USC §5101 | LO licensing/registration |

## Process

**Phase 1 — Application Intake (Days 1-3)**
1. Receive 6 TRID data elements; timestamp receipt of 6th element
2. Pull credit report; document FCRA authorization
3. Generate LE within 3 business days of application
4. Provide SPL simultaneously with LE
5. Deliver CFPB homeownership counseling list (obtained ≤30 days prior)
6. Deliver Special Information Booklet for purchase transactions (12 CFR §1024.19(g))
7. Document borrower intent to proceed before collecting any fee beyond credit report

**Phase 2 — Documentation & Processing (Days 4-21)**
8. Collect income docs: W-2s, tax returns, pay stubs, 1099s; self-employment = 2 years tax returns
9. Collect assets: bank statements (all pages), investment accounts
10. Reconcile liabilities vs. credit report; investigate undisclosed debts
11. Order title search; review preliminary title commitment for liens/easements/encumbrances
12. Verify property insurance adequacy; flood determination (NFIP)
13. Document rate lock date/expiration; issue revised LE if lock changes disclosed terms

**Phase 3 — Appraisal & Valuation (Days 10-25)**
14. Order appraisal through compliant channel (no direct borrower-appraiser contact for HPML)
15. Verify appraiser state certification/license for jurisdiction
16. Review for USPAP compliance, comparable selection, adjustments
17. HPML: obtain 2nd independent appraisal if property sold within 180 days at materially lower price (12 CFR §1026.35(c))
18. AVM evaluations: ensure policies meet interagency final rule standards (89 FR 64,538; eff. 10/1/2025)
19. Deliver appraisal to borrower ≥3 business days before consummation (12 CFR §1026.35(c)(6))

**Phase 4 — Underwriting (Days 20-30)**
20. Submit complete file with ATR/QM analysis worksheet
21. Calculate DTI: total monthly debt obligations / gross monthly income
22. Document compensating factors if DTI exceeds institutional thresholds
23. Clear all underwriting conditions; obtain final approval with documentation
24. If denied: issue adverse action within 30 days of completed application (12 CFR §1002.9); include specific denial reasons + ECOA notice

**Phase 5 — Pre-Closing & CD (Days 25-35)**
25. Prepare CD with final loan terms, fees, cash-to-close
26. Deliver CD ≥3 business days before consummation
27. Hand-delivered: 3 calendar days; USPS first class mailed: 6 calendar days (3-day mailbox + 3-day review)
28. Verify CD-to-LE fee tolerance compliance across all 3 buckets; cure any overages before closing
29. Confirm no changes triggering new 3-day wait: APR change >1/8% (>1/4% irregular), product change, prepayment penalty addition

**Phase 6 — Closing & Post-Closing**
30. Coordinate with settlement agent; verify settlement agent provides seller's CD
31. Execute note, mortgage/deed of trust, all closing documents; fund; record mortgage with county recorder
32. Complete HMDA data: verify all 48+ fields (action taken, loan type, property type, ethnicity, race, sex, income, DTI, CLTV, rate spread)
33. Post-closing QC within 90 days: re-verify income, employment, occupancy on sample basis

## Glossary

| Term | Definition |
|---|---|
| Loan Estimate (LE) | 3-page TRID form; within 3 biz days of application; estimated terms/payments/costs (12 CFR §1026.37) |
| Closing Disclosure (CD) | 5-page TRID form; ≥3 biz days pre-consummation; final terms/costs/cash-to-close (12 CFR §1026.38) |
| Fee Tolerance | Permissible LE→CD variance: zero / 10% aggregate / unlimited buckets |
| Changed Circumstance | 6 specific triggers allowing revised LE and tolerance reset; must be contemporaneously documented |
| Consummation | Borrower becomes contractually obligated on mortgage note (not synonymous with closing in all states) |
| Application (TRID) | Receipt of 6 data elements: name/income/SSN/property address/estimated value/loan amount (12 CFR §1026.2(a)(3)(ii)) |
| Qualified Mortgage (QM) | Meets product/fees/underwriting per 12 CFR §1026.43(e); safe harbor or rebuttable presumption |
| APOR | Average Prime Offer Rate — CFPB weekly benchmark; sets QM pricing thresholds, HPML status, HMDA rate-spread |
| HPML | APR exceeds APOR by ≥1.5pp first lien / ≥3.5pp subordinate; triggers appraisal/escrow/ATR requirements |
| SPL | Service Provider List — delivery timing determines zero vs. 10%-tolerance for third-party fees |
| RESPA Section 8 | Anti-kickback; prohibits fee/kickback/thing of value for referral of settlement services |
| Adverse Action Notice | Reg B/FCRA notice for denial: specific denial reasons, ECOA notice, primary regulator contact |
| AVM | Automated Valuation Model; interagency QC standards eff. 10/1/2025 (89 FR 64,538; 12 CFR §1026.42) |
| USPAP | Uniform Standards of Professional Appraisal Practice; required for federally related transactions |
| Rate Lock | Lender commitment on rate/term; locking/extending = changed circumstance for revised LE |
| Right of Rescission | 3 biz days post-consummation for refinances on principal dwelling (12 CFR §1026.23); not purchase money |
| HMDA Reportable Data | 48+ fields: demographics, loan characteristics, property info, pricing, underwriting factors |
| Escrow Account | Holds borrower funds for taxes/insurance; HPML requires escrow ≥5 years |
| Points and Fees | Origination charges + LO compensation + certain finance charges; ≤3% of loan amount for QM |
| LO Compensation | Cannot be based on loan terms except amount; dual compensation prohibited (12 CFR §1026.36) |
| Good Faith Standard | Fee disclosed in good faith if charged ≤ disclosed within applicable tolerance threshold |

## Checklist

- [ ] All 6 TRID application data points timestamped at receipt; LE generation clock tracked
- [ ] LE delivered within 3 business days with SPL and homeownership counseling list
- [ ] Intent to proceed documented before any fee collection beyond credit report
- [ ] Every revised LE supported by contemporaneous changed circumstance documentation
- [ ] Fee tolerance analysis across all 3 buckets before CD preparation; overages identified and cured
- [ ] CD delivered ≥3 business days before consummation; delivery method and receipt evidence documented
- [ ] APR accuracy verified on final CD (within 1/8% regular; 1/4% irregular payment loans)
- [ ] ATR/QM worksheet complete: income/debt verified via third-party records; DTI or residual income documented; APR vs. APOR checked
- [ ] Appraisal through compliant channel; USPAP conformance verified; copy to borrower ≥3 days pre-closing
- [ ] Adverse action notices within 30 days for all denied/incomplete applications; specific reason codes + ECOA notice
- [ ] HMDA fields verified before annual submission (action taken, income, DTI, rate spread, ethnicity/race/sex)
- [ ] RESPA Section 8 compliance: no referral fees, kickbacks, or MSAs without bona fide services
- [ ] Flood determination obtained; flood insurance secured and escrowed where required
- [ ] Post-closing QC on sampled loans within 90 days: income re-verification, occupancy check, compliance review
- [ ] Records retained: minimum 3 years TRID / 5 years HMDA

## References
CFPB TRID; 12 CFR §1026.19(e)(f)(g)/§1026.37/§1026.38; Reg X 12 CFR Part 1024; Reg Z 12 CFR Part 1026; ATR/QM 12 CFR §1026.43; Reg B 12 CFR Part 1002; Reg C 12 CFR Part 1003; HPML 12 CFR §1026.35(c); AVM Final Rule 89 FR 64,538 (eff. 10/1/2025) 12 CFR §1026.42; FCRA 15 USC §1681; SAFE Act 12 USC §5101; Flood 42 USC §4012a; FFIEC HMDA Getting It Right 2024; CrossCheck Compliance TRID 2025; Freedom Mortgage $3.95M HMDA consent 2024; Prospect Mortgage RESPA §8 $3.5M; CFPB Fair Lending Report 2024
