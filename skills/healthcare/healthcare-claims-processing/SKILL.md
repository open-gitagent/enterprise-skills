---
name: healthcare-claims-processing
description: >
  Medical claims processing expertise including claim submission, adjudication rules, payment determination, and denial management workflows.
metadata:
  vertical: healthcare
  function: revenue-cycle
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "CMS, HIPAA, State DOI"
---

# Healthcare Claims Processing

## Domain Overview

Healthcare claims processing is the end-to-end lifecycle through which providers submit requests for reimbursement to payers and receive payment determinations. The process spans claim creation (coding and charge capture), electronic submission via ANSI X12 837 transactions, payer adjudication (eligibility verification, benefit determination, medical necessity review, pricing), remittance processing via X12 835 transactions, and denial/appeals management. In the United States, this process is governed by a dense regulatory stack including HIPAA Administrative Simplification (45 CFR Parts 160-164), Medicare Claims Processing Manual (CMS Pub 100-04), state prompt-pay statutes, and the No Surprises Act (P.L. 116-260). The 2024 CAQH Index reports $222 billion in industry savings from electronic transaction adoption, yet denial rates continue to climb — from 42% of providers reporting increases in 2022 to 77% in 2024, per Experian Health's State of Claims survey.

The adjudication engine is where claims succeed or fail. Payers execute a deterministic sequence: syntax validation, eligibility confirmation, benefit plan mapping, National Correct Coding Initiative (NCCI) edits, medical necessity evaluation against Local/National Coverage Determinations (LCD/NCD), coordination of benefits (COB) sequencing, and contracted rate application. A claim that clears all edits auto-adjudicates; one that trips any edit enters manual review queues where clinical staff assess documentation. The 2024 Experian Health report found 76% of denials stem from missing, incomplete, or inaccurate data at submission — a front-end problem, not an adjudication problem.

The regulatory environment is intensifying. CMS finalized the first-ever HIPAA-adopted standards for health care claims attachments in late 2024, requiring electronic exchange of supporting clinical documentation using HL7 Consolidated Clinical Document Architecture (C-CDA). The CMS Interoperability and Prior Authorization Final Rule (CMS-0057-F), finalized January 2024, mandates FHIR-based prior authorization APIs. CMS issued enforcement discretion allowing covered entities to bypass the X12 278 standard for FHIR-based prior authorization. The No Surprises Act IDR process saw 1.4 million disputes in 2024 alone — a 115% increase over 2023 — with providers initiating 99.9% of disputes and prevailing in 88% of determinations. DOJ and HHS-OIG enforcement continues to intensify, with the revitalized FCA Working Group targeting improper coding, upcoding, unbundling, and medically unnecessary services.

Denial management has evolved from a back-office collection function to a strategic revenue integrity discipline. Organizations tracking denial root causes across five categories — patient access (eligibility/registration errors), authorization, coding, medical necessity, and billing — can reduce denial rates from the industry average of 8-10% to below 4%. The shift from reactive appeals to proactive prevention requires real-time eligibility verification, automated prior authorization tracking, AI-based coding rules engines, and payer-specific edit libraries maintained against quarterly NCCI updates and individual payer policy changes.

## Core Decision Framework

Expert claims processing practitioners evaluate every claim through a five-gate adjudication model:

**Gate 1 — Structural Integrity**: Does the claim conform to X12 837P (005010X222A1) or 837I (005010X223A2) syntax? Are all required segments populated (NM1 for provider/patient, CLM for claim data, SV1/SV2 for service lines)? A 999 acknowledgment rejection means the file never entered adjudication. A 277CA rejection means the claim entered but failed payer-level edits.

**Gate 2 — Eligibility & Coverage**: Was the patient covered on the date of service? Does the plan cover the service category? Is the provider in-network or subject to No Surprises Act protections? COB sequencing: which payer is primary under the birthday rule, policyholder/dependent rule, or custodial parent rule?

**Gate 3 — Authorization & Medical Necessity**: Was prior authorization obtained when required? Does the diagnosis-procedure linkage satisfy the payer's medical policy? Do the ICD-10-CM codes meet LCD/NCD criteria? Approximately 15% of commercial claims are initially denied despite having prior authorization already obtained before treatment.

**Gate 4 — Coding Compliance**: Do CPT/HCPCS and ICD-10-CM codes pass NCCI Procedure-to-Procedure (PTP) edits, Medically Unlikely Edits (MUEs), and Add-on Code (AOC) edits? Are modifiers correctly applied (e.g., modifier 25 for significant/separate E/M, modifier 59/X{EPSU} for distinct procedural service)? Is the rendering provider NPI and taxonomy code correct?

**Gate 5 — Payment Determination**: What is the contracted rate (fee schedule, DRG, per diem, case rate, capitation)? Are there carve-outs, stop-loss provisions, or reinsurance thresholds? What is the patient cost-sharing responsibility (deductible status, coinsurance percentage, copay amount, out-of-pocket maximum accumulation)?

When analyzing a denial, work backward through these gates. The CARC tells you which gate failed; the RARC tells you what to fix.

## Step-by-Step Process

### 1. Pre-Submission (Front-End)
- Verify patient demographics and insurance eligibility in real-time (X12 270/271 transaction)
- Confirm plan benefits, deductible accumulation, and COB order
- Obtain and document prior authorization; record authorization number
- Capture charges: link CPT/HCPCS procedure codes to ICD-10-CM diagnosis codes with correct diagnosis pointers
- Apply place-of-service code, provider NPI, taxonomy code, referring provider NPI where required

### 2. Claim Scrubbing & Editing
- Run claims through NCCI PTP edit engine to catch unbundling violations
- Validate MUE thresholds (units per provider per beneficiary per date of service)
- Check payer-specific edit libraries (ClaimsXten, Cotiviti, Optum rules)
- Verify modifier appropriateness and medical record support
- Confirm timely filing compliance: Medicare = 12 months from DOS (42 CFR §424.44); Medicaid = 12 months (42 CFR §447.45); commercial = varies by payer and state (typically 90-365 days)

### 3. Electronic Submission
- Generate X12 837P (professional) or 837I (institutional) file
- Transmit via clearinghouse or direct connection to payer
- Receive 999 acknowledgment (syntax validation) — rejection here = file-level error
- Receive 277CA claim acknowledgment — rejection here = claim-level error requiring correction and resubmission

### 4. Payer Adjudication
- Automated system processes through eligibility, benefit, coding, medical necessity, and pricing engines
- Claims flagged for manual review enter work queues (medical necessity, high-dollar, complex)
- Payer determines: pay in full, pay reduced amount, pend for information, or deny
- For Medicare: clean claims must be processed within 30 days (electronic) per CMS policy; other-than-clean claims within 45 calendar days per Social Security Act §1869(a)(2)
- For Medicaid: 90% of clean claims from practitioners paid within 30 days, 99% within 90 days (42 CFR §447.45)
- For commercial: state prompt-pay laws typically require 30 days (electronic) / 45 days (paper) for clean claims

### 5. Remittance Processing
- Receive X12 835 Electronic Remittance Advice (ERA) or paper Explanation of Benefits (EOB)
- Parse CARC/RARC codes and Claim Adjustment Group Codes (CO, PR, OA, PI, CR)
- Post payments and adjustments to patient accounts
- Identify underpayments by comparing allowed amounts to contracted rates
- Transfer patient responsibility amounts to patient billing

### 6. Denial Management & Appeals
- Triage denials within 48 hours of remittance receipt
- Classify as "soft denial" (correctable/resubmittable) vs. "hard denial" (requires formal appeal)
- Conduct root cause analysis using CARC/RARC code mapping to denial categories
- Resubmit corrected claims or file formal appeal with supporting documentation
- Track appeal deadlines: Medicare redetermination = 120 days; reconsideration = 180 days; commercial = per payer contract (typically 60-180 days)
- For No Surprises Act disputes: file open negotiation notice within 30 business days of initial payment/denial; IDR initiation within 4 business days after open negotiation period

## Evaluation Criteria

| Metric | Target | Critical Threshold |
|---|---|---|
| Clean Claim Rate | ≥98% | <95% triggers process review |
| First-Pass Resolution Rate | ≥90% | <85% indicates systemic front-end issues |
| Denial Rate | <5% | >8% requires root cause intervention |
| Days in A/R (net) | <35 days | >45 days signals collection/follow-up breakdown |
| Appeal Overturn Rate | >65% | <50% suggests poor appeal quality or wrong denial targeting |
| Timely Filing Compliance | 100% | Any miss = unrecoverable revenue |
| Cost to Collect | <3.5% of net revenue | >5% indicates inefficiency |
| Denial Write-Off Rate | <2% of net revenue | >3% signals failure to work denials |

## Red Flags & Edge Cases

1. **Retroactive eligibility termination**: Patient verified as eligible at time of service, but payer retroactively terminates coverage (common with employer group changes). CARC 27 (expenses after coverage terminated) appears on remittance. The provider must pursue the patient or the new payer — the original payer has no obligation. States like New York limit retroactive termination to specific timeframes.

2. **NCCI PTP edit override without documentation**: Provider appends modifier 59 to bypass an NCCI column one/column two edit pair, but the medical record does not support a distinct procedural service. OIG audits specifically target modifier 59 overuse — a 2023 OIG Work Plan item. Claims with modifier 59 that lack supporting documentation are False Claims Act exposure.

3. **Coordination of benefits circular denial loop**: Primary payer denies claiming it is secondary; secondary payer denies claiming it is primary. Occurs frequently with divorced parents (birthday rule vs. custodial parent rule conflict), Medicare Secondary Payer situations, and workers' compensation/auto liability disputes. Resolution requires payer-to-payer COB verification and sometimes state insurance commissioner intervention.

4. **Timely filing denial on resubmitted corrected claim**: Original claim submitted timely but denied for missing information. Corrected claim resubmitted after timely filing deadline passes. Under most payer contracts, corrected claims relate back to the original submission date — but the provider must retain the original submission proof (clearinghouse confirmation with timestamp). Medicare treats corrected claims as adjustments not subject to the 12-month filing limit under 42 CFR §424.44, provided the original was timely.

5. **No Surprises Act QPA manipulation**: Payer calculates the Qualifying Payment Amount (QPA) using a narrowly defined geographic region or excluding higher-paying contracts, resulting in an artificially low initial payment. Per TMA III litigation (Texas Medical Association v. HHS), courts have pushed back on CMS guidance that weighted QPA too heavily in IDR determinations. Providers should verify QPA methodology and challenge calculations that deviate from the statutory median contracted rate.

6. **DRG upcoding through secondary diagnosis sequencing**: Changing the principal diagnosis or adding complication/comorbidity (CC/MCC) codes that are not supported by clinical documentation to assign a higher-weighted DRG. OIG and RAC auditors specifically target claims where the CC/MCC changes the DRG assignment. A $34 million DOJ settlement in 2024 involved precisely this pattern.

7. **Split billing to circumvent MUE thresholds**: Provider bills the same service across multiple claims or multiple dates of service to exceed the Medically Unlikely Edit unit limit for a single date. NCCI MUEs with Modifier Adjudication Indicator (MAI) of "3" are per-day edits that cannot be overridden by any modifier. Patterns of line-splitting trigger fraud analytics.

8. **Telehealth place-of-service code errors**: Post-pandemic telehealth claims submitted with POS 11 (office) instead of POS 02 (telehealth) or POS 10 (telehealth in patient's home). Some payers reimburse telehealth at facility rates (lower) vs. non-facility rates — incorrect POS code can result in overpayment subject to recoupment or underpayment requiring correction.

9. **Clearinghouse rejection masking timely filing failure**: Claim submitted to clearinghouse within timely filing window, but clearinghouse rejects claim for formatting error. Clearinghouse rejection ≠ payer receipt. If the corrected claim reaches the payer after the filing deadline, the payer can legitimately deny. The clearinghouse timestamp is not proof of filing with the payer.

10. **Observation vs. inpatient status on institutional claims**: Hospital bills outpatient observation (revenue code 0762) but clinical criteria support inpatient admission. Or conversely, patient admitted as inpatient but retrospectively changed to observation. Under CMS-4204-F (effective November 15, 2024), beneficiaries reclassified from inpatient to outpatient observation now have expedited determination appeal rights through BFCC-QIO. This status distinction affects DRG payment vs. APC payment — a difference often exceeding $10,000.

11. **Stale authorization used for claim submission**: Prior authorization obtained but service rendered beyond the authorization validity period (many authorizations expire after 60-90 days). Payer denies with CARC 197 (precertification/authorization absent). The authorization number on the claim technically matches, but the date of service falls outside the authorized window.

12. **Excluded provider billing**: Claims submitted for services rendered by or ordered by an individual on the OIG List of Excluded Individuals/Entities (LEIE). Under 42 U.S.C. §1320a-7, payment for these claims must be refunded, and civil monetary penalties of up to $100,000 per item/service apply. Multiple 2024-2025 OIG enforcement actions targeted entities employing excluded individuals — penalties ranged from $107,000 to $698,000.

## Common Mistakes

1. **Relying on real-time eligibility as guarantee of payment**: A 270/271 eligibility response confirms coverage status at the moment of inquiry — it does not guarantee payment, confirm benefits for the specific service, or verify that prior authorization is in place. Staff who treat eligibility verification as a complete pre-service check create downstream denials.

2. **Failing to differentiate 999 rejections from 277CA denials**: A 999 is a syntax/file-level rejection — the claim never entered the payer's adjudication system and must be corrected and retransmitted. A 277CA is a claim-level acknowledgment that may include acceptance or rejection. Treating both as "denials" conflates fundamentally different resolution workflows.

3. **Applying NCCI edits only to Medicare claims**: Many commercial payers license NCCI edits (often via ClaimsXten or Cotiviti) and apply them to all claims. Assuming NCCI edits are "Medicare only" causes preventable denials on commercial lines of business. Additionally, commercial payers often apply proprietary edits that are stricter than NCCI.

4. **Batching denial follow-up instead of triaging by financial impact**: Working denials in received order rather than prioritizing by dollar amount and appeal deadline. High-dollar inpatient denials with 60-day appeal windows require immediate attention; low-dollar outpatient denials with 180-day windows can be queued. The 2024 HFMA guidance emphasizes that 89% of hospitals report significant denial increases — triage is non-negotiable.

5. **Missing the distinction between Group Code CO and PR on remittance**: CARC with Group Code CO (Contractual Obligation) means the provider must write off the amount per contract. CARC with Group Code PR (Patient Responsibility) means the provider can bill the patient (deductible, coinsurance, copay). Posting CO adjustments as patient balances violates payer contracts; posting PR adjustments as write-offs loses revenue.

6. **Submitting secondary claims without primary payer adjudication data**: A COB claim to the secondary payer must include the primary payer's adjudication information (payment amount, adjustments, patient responsibility). Submitting a "clean" claim to the secondary without this data results in immediate rejection. The X12 837 COB loop (2320/2330) must be populated with primary payer CARC/RARC data.

7. **Ignoring payer-specific companion guide requirements**: Each payer publishes a companion guide to the X12 837 TR3 that specifies data content requirements beyond the base standard (required fields, value sets, loop usage). UnitedHealthcare, for example, updated its 837P companion guide to version 7.0 in March 2025. Ignoring these produces systematic rejections.

## Regulatory & Compliance Requirements

### Federal Statutes & Regulations
- **HIPAA Administrative Simplification** (45 CFR Parts 160-164): Mandates standard electronic transactions (X12 837, 835, 270/271, 276/277, 278), code sets (ICD-10-CM/PCS, CPT, HCPCS, NDC), and unique identifiers (NPI). New claims attachment standard finalized December 2024 using HL7 C-CDA.
- **42 CFR §424.44**: Medicare timely filing — 12 months from date of service. Exceptions for administrative error, retroactive entitlement, retroactive MA disenrollment.
- **42 CFR §447.45**: Medicaid timely claims payment — 90% of clean practitioner claims within 30 days, 99% within 90 days.
- **Social Security Act §1869(a)(2)**: Medicare must process other-than-clean claims and notify providers within 45 calendar days.
- **No Surprises Act (P.L. 116-260, Division BB)**: Prohibits balance billing for emergency services, air ambulance from out-of-network providers, and non-emergency services from out-of-network providers at in-network facilities. Establishes IDR process; administrative fee set at $115 per party for disputes initiated on or after January 22, 2024.
- **False Claims Act (31 U.S.C. §§3729-3733)**: Liability for knowingly submitting false claims to federal healthcare programs. Treble damages plus $13,946-$27,894 per claim (2024 penalty range). DOJ and OIG FCA Working Group revitalized in 2025.
- **Anti-Kickback Statute (42 U.S.C. §1320a-7b(b))**: Criminal penalties for offering/receiving remuneration to induce referrals. AKS violations can serve as predicate for FCA liability.
- **Physician Self-Referral Law / Stark Law (42 U.S.C. §1395nn)**: Prohibits referrals for designated health services to entities with financial relationships. No intent requirement — strict liability.
- **CMS-0057-F (Interoperability and Prior Authorization Final Rule)**: Requires payers to implement FHIR-based prior authorization APIs. CMS NSG issued enforcement discretion for FHIR-based prior auth bypassing X12 278.

### Key CMS Guidance
- **Medicare Claims Processing Manual (Pub 100-04)**: Chapter 1 (General Billing), Chapter 23 (NCCI), Chapter 24 (EDI)
- **NCCI Policy Manual**: PTP edits, MUEs, AOC edits updated quarterly
- **OIG Compliance Program Guidance for Hospitals**: Risk areas including upcoding, unbundling, billing for medically unnecessary services, insufficient documentation

### State Requirements
- **Prompt-Pay Statutes**: 49 states (all except South Carolina) require clean claim payment within specified timeframes (typically 30 days electronic / 45 days paper). Penalties range from 10-18% annual interest. Texas imposes tiered penalties: lesser of 50% of difference or $100,000 for claims paid 1-45 days late.

## Terminology

1. **837P/837I**: ANSI X12 electronic claim transaction formats — 837P (Professional, version 005010X222A1) for physician/outpatient services; 837I (Institutional, version 005010X223A2) for facility/inpatient services.
2. **835 (ERA)**: Electronic Remittance Advice — the ANSI X12 transaction payers send to providers detailing payment, adjustments, and denial reasons for submitted claims.
3. **Clean Claim**: A claim that can be processed without obtaining additional information from the provider or a third party. Must have all required data elements, correct formatting, and no deficiency requiring external investigation.
4. **CARC (Claim Adjustment Reason Code)**: Standardized code set (maintained by X12) explaining why a claim payment differs from the billed amount. Approximately 358 active codes. Always paired with a Group Code.
5. **RARC (Remittance Advice Remark Code)**: Supplemental code set (maintained by CMS) providing additional context to a CARC — often specifies what corrective action is needed. Approximately 1,185 active codes.
6. **Group Code (CAGC)**: Two-character code indicating financial responsibility for an adjustment: CO (Contractual Obligation — provider write-off), PR (Patient Responsibility), OA (Other Adjustment), PI (Payer Initiated Reduction), CR (Correction/Reversal).
7. **NCCI (National Correct Coding Initiative)**: CMS-maintained edit system preventing improper code combinations. Three edit types: PTP (procedure-to-procedure), MUE (medically unlikely edits), AOC (add-on code edits).
8. **MUE (Medically Unlikely Edit)**: Maximum units of service reportable by one provider for one beneficiary on one date of service. MAI values: 1 = claim line edit, 2 = absolute (regulation-based), 3 = per-day clinical benchmark.
9. **COB (Coordination of Benefits)**: Process determining payer order and payment responsibilities when a patient has multiple insurance coverages. Governed by NAIC model regulation and HIPAA COB transaction standards.
10. **QPA (Qualifying Payment Amount)**: Under the No Surprises Act, the median contracted rate for the same or similar service in the same geographic region — serves as the baseline for initial out-of-network payment and IDR determination.
11. **IDR (Independent Dispute Resolution)**: Federal arbitration process under the No Surprises Act for resolving payment disputes between providers and payers for out-of-network services.
12. **LCD/NCD (Local/National Coverage Determination)**: CMS policy documents specifying whether a service is covered by Medicare and under what clinical circumstances. NCDs are binding nationwide; LCDs are MAC-specific.
13. **DRG (Diagnosis Related Group)**: Medicare inpatient prospective payment classification system. Payment weight determined by principal diagnosis, procedures, complications/comorbidities, patient age, and discharge status.
14. **Modifier 59 / X{EPSU}**: HCPCS modifiers indicating a distinct procedural service to bypass NCCI PTP edits. X-modifiers (XE, XP, XS, XU) provide greater specificity than legacy modifier 59.
15. **MAC (Medicare Administrative Contractor)**: Private companies that CMS contracts with to process Medicare Part A and Part B claims in defined jurisdictions.
16. **Timely Filing Limit**: Maximum period after date of service within which a claim must be received by the payer. Medicare: 12 months. Medicaid: 12 months. Commercial: per contract and state law (typically 90-365 days).
17. **Prior Authorization (PA)**: Prospective utilization review requiring payer approval before a service is rendered. Failure to obtain PA when required results in denial regardless of medical necessity.
18. **Clearinghouse**: Intermediary entity that receives claims from providers, validates formatting and content, and routes to appropriate payers. Provides 999 (syntax) and 277CA (claim-level) acknowledgments.
19. **Revenue Code**: Three-digit code on institutional (UB-04/837I) claims identifying the type of service or accommodation (e.g., 0762 = observation room, 0450 = emergency room).
20. **Remittance Advice (RA)**: Document from payer explaining claim payment decisions — electronic (835/ERA) or paper (EOB/EOMB). Contains CARC/RARC codes, allowed amounts, adjustments, and patient responsibility.
21. **RAC (Recovery Audit Contractor)**: CMS-contracted auditors that identify and recover improper payments from providers on a contingency-fee basis. Focus areas include DRG validation, medical necessity, and coding accuracy.
22. **LEIE (List of Excluded Individuals/Entities)**: OIG-maintained database of individuals and entities excluded from federal healthcare programs. Billing for services rendered by excluded persons triggers CMPs up to $100,000 per item.
23. **Good Faith Estimate (GFE)**: Under the No Surprises Act, providers must furnish uninsured/self-pay patients with a written estimate of charges for scheduled services at least 72 hours in advance or upon request.

## Quality Checklist

- [ ] Patient eligibility verified within 72 hours of service date, with active coverage confirmed on the actual DOS
- [ ] Prior authorization obtained, documented with authorization number, and confirmed valid for the DOS and specific service codes billed
- [ ] ICD-10-CM diagnosis codes are specific to highest level of specificity (no unspecified codes when documentation supports greater detail)
- [ ] CPT/HCPCS codes pass NCCI PTP edit validation — no unbundled code pairs submitted without appropriate modifier and documentation support
- [ ] MUE thresholds verified for all service lines — units do not exceed MAI-3 per-day limits
- [ ] Claim form type matches service context: 837P for professional services, 837I for institutional; correct place-of-service code applied
- [ ] Rendering provider NPI and taxonomy code are current, active, and match the service being billed
- [ ] Timely filing deadline calculated and documented — claim submitted with minimum 30-day buffer before deadline
- [ ] COB order verified when multiple payers exist — primary payer billed first; secondary claim includes primary adjudication data in 2320/2330 loops
- [ ] Clearinghouse acceptance confirmation (999 + 277CA) retained with timestamp as proof of filing
- [ ] OIG LEIE checked monthly for all rendering, referring, and ordering providers — no excluded individuals on claims
- [ ] CARC/RARC codes on remittance mapped to denial category (patient access, authorization, coding, medical necessity, billing) for root cause tracking
- [ ] Appeal filed within payer-specific deadline with all supporting clinical documentation and specific citation of why the denial reason is incorrect
- [ ] No Surprises Act applicability assessed for all out-of-network claims — GFE, disclosure, and consent documentation verified
- [ ] Contracted rate verification performed on paid claims — allowed amount reconciled against fee schedule or contract terms to detect underpayment

## References

1. CMS Medicare Claims Processing Manual (Pub 100-04), Chapter 1, §70 — Timely Filing: https://www.cms.gov/Regulations-and-Guidance/Guidance/Transmittals/downloads/R2140CP.pdf
2. CMS Administrative Simplification: Adoption of Standards for Health Care Claims Attachments (2024 Final Rule): https://www.cms.gov/newsroom/fact-sheets/administrative-simplification-adoption-standards-health-care-claims-attachments-transactions
3. CMS Interoperability and Prior Authorization Final Rule (CMS-0057-F): https://www.cms.gov/priorities/burden-reduction/overview/interoperability/policies-regulations/cms-interoperability-prior-authorization-final-rule-cms-0057-f
4. 42 CFR §424.44 — Medicare Timely Filing Requirements: https://www.ecfr.gov/current/title-42/chapter-IV/subchapter-B/part-424/subpart-C/section-424.44
5. 42 CFR §447.45 — Medicaid Timely Claims Payment: https://www.ecfr.gov/current/title-42/chapter-IV/subchapter-C/part-447/subpart-A/section-447.45
6. OIG Fraud & Abuse Laws (False Claims Act, AKS, Stark, CMPs): https://oig.hhs.gov/compliance/physician-education/fraud-abuse-laws/
7. OIG Supplemental Compliance Program Guidance for Hospitals (70 FR 4858): https://www.federalregister.gov/documents/2005/01/31/05-1620/oig-supplemental-compliance-program-guidance-for-hospitals
8. OIG Enforcement Actions — CMP and Affirmative Exclusions: https://oig.hhs.gov/fraud/enforcement/?type=cmp-and-affirmative-exclusions
9. CMS NCCI Policy Manual and Edits (Chapter 23, Pub 100-04): https://www.cms.gov/regulations-and-guidance/guidance/manuals/downloads/clm104c23.pdf
10. CAQH CORE Phase III Rule 360 — Uniform Use of CARC/RARC Codes: https://www.caqh.org/hubfs/CARCsRARCs_835_Rule.pdf
11. No Surprises Act IDR Process — 2025 Data Analysis (Georgetown CHIR): https://chir.georgetown.edu/the-no-surprises-act-idr-process-an-early-look-at-2025-data/
12. CRS Report R48738 — NSA IDR Process Data Analysis for 2024: https://www.congress.gov/crs-product/R48738
13. HFMA Strategy Concepts for Denial Prevention and Management (2024): https://www.hfma.org/wp-content/uploads/2024/05/strategyconceptsfordenialpreventionandmanage-2024txstateconference.pdf
14. Experian Health State of Claims 2024 Report / Denial Management Trends: https://www.revcycle.com/?p=3194
15. AHIMA Best Practices for Denials Prevention and Management: https://journal.ahima.org/Portals/0/archives/AHIMA%20files/Best%20Practices%20for%20Denials%20Prevention%20and%20Management.pdf
16. HIPAA Journal — HIPAA Updates and Changes 2024-2026: https://www.hipaajournal.com/hipaa-updates-hipaa-changes/
17. State Prompt-Pay Statutes — 50 States Comparison: https://archivetxahp.com/wp-content/uploads/2016/11/TLR-Prompt-Pay-Issue-Brief-Appendix-State-by-State-Comparison-Jan-2016.pdf
18. White & Case — Healthcare Fraud Enforcement in 2025: https://www.whitecase.com/insight-our-thinking/healthcare-fraud-enforcement-2025-year-aggressive-action-expanding-risk
19. ArentFox Schiff — Shifting Federal Priorities in Health Care Enforcement: https://www.afslaw.com/perspectives/health-care-counsel-blog/shifting-federal-priorities-health-care-enforcement-key
20. ANSI X12 837 Transaction Set Standard — Stedi Reference: https://www.stedi.com/edi/x12/transaction-set/837
21. UnitedHealthcare 837P Companion Guide v7.0 (March 2025): https://www.uhcprovider.com/content/dam/provider/docs/public/resources/edi/EDI-837P-CG-005010X222A1.pdf
22. CMS 837P/CMS-1500 Medicare Billing Fact Sheet: https://www.cms.gov/files/document/837p-cms-1500pdf
23. Noridian Medicare — NCCI Edits Reference: https://med.noridianmedicare.com/web/jeb/topics/claim-submission/ncci
24. FinThrive — Best Practices in Denial Management (2024): https://finthrive.com/blog/best-practices-in-denial-management
25. CMS Coordination of Benefits Overview: https://www.cms.gov/priorities/key-initiatives/burden-reduction/administrative-simplification/transactions/coordination-benefits