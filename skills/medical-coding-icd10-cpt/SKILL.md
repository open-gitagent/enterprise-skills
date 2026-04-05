---
name: medical-coding-icd10-cpt
description: >
  Medical coding expertise covering ICD-10-CM/PCS diagnosis coding, CPT procedure coding, HCPCS coding, and coding compliance guidelines.
metadata:
  vertical: healthcare
  function: coding
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "CMS, AMA, WHO ICD"
---

# Medical Coding ICD-10 CPT

## Domain Overview

Medical coding translates clinical encounters—diagnoses, procedures, services, and supplies—into standardized alphanumeric codes that drive reimbursement, quality reporting, and public health surveillance. The three primary code sets are ICD-10-CM (diagnosis codes for all settings), ICD-10-PCS (inpatient procedure codes), and CPT/HCPCS (outpatient procedures, professional services, supplies, and equipment). CMS and the AMA co-maintain these systems under HIPAA's Administrative Simplification mandate (§1173), making code set compliance a federal requirement, not an organizational preference.

The FY 2025 ICD-10-CM update introduced 252 new codes, 13 deletions, and 36 revisions effective October 1, 2024, including new codes for genetic susceptibility (Z15.1, Z15.2), presymptomatic Type 1 diabetes (E10.A-), and breast implant-associated anaplastic large cell lymphoma (C84.7B). The CPT 2025 code set included 420 updates—270 new codes, 112 deletions, and 38 revisions—with significant changes in AI-augmented services, remote therapeutic monitoring (98975-98978 revisions), and 16 new telehealth E/M codes (98000-98015). Category III codes for emerging technologies accounted for 30% of new CPT additions. HCPCS Level II receives quarterly updates; the January 2026 cycle added 160 new codes and 101 deletions.

Coding accuracy directly affects MS-DRG assignment for inpatient stays, where the principal diagnosis establishes the DRG and secondary diagnoses determine CC/MCC tier placement. A single misassigned CC or MCC can shift reimbursement by thousands of dollars. The DOJ recovered approximately $2.9 billion in False Claims Act civil fraud recoveries in 2024, with healthcare historically comprising 60-80% of total recoveries. Recent settlements include a $62 million resolution with Seoul Medical Group for false diagnosis codes under Medicare Advantage, a $98 million settlement with Independent Health Association for unsupported MA diagnosis codes, and a $556 million Kaiser Permanente settlement in January 2026 for similar allegations.

The OIG Work Plan for 2025 targets inpatient short-stay claims under the Two-Midnight Rule, DRG coding validation across all MS-DRGs (001-999), hospital drug billing accuracy via HCPCS/NDC alignment, and Medicare payments for clinical diagnostic laboratory tests. Recovery Audit Contractors (RACs) hold standing CMS approval to validate MS-DRG coding for all inpatient claims under topic 0001. Compliance requires alignment with the OIG's Seven Elements framework: written policies, designated compliance officer, training, communication channels, internal monitoring, enforcement through discipline, and prompt corrective action.

## Core Decision Framework

### The Coding Decision Hierarchy

Experienced coders follow a strict analytical sequence—deviating from this order introduces errors:

1. **Read the entire encounter record** before touching a code book. Premature code assignment based on partial information causes sequencing errors and missed secondary diagnoses.
2. **Identify the principal diagnosis** using the Uniform Hospital Discharge Data Set (UHDDS) definition: the condition established after study to be chiefly responsible for occasioning the admission. For outpatient, assign the reason for the encounter to the highest level of specificity.
3. **Apply the ICD-10-CM Official Guidelines** chapter-specific rules. Etiology/manifestation conventions require the underlying condition listed first, manifestation code second—manifestation codes with "in diseases classified elsewhere" in the title are never permitted as principal diagnosis.
4. **Code to the highest level of specificity** documented. Unspecified codes (e.g., J18.9 for pneumonia) are acceptable only when documentation genuinely lacks specificity—never use them as shortcuts.
5. **Sequence secondary diagnoses** based on clinical significance: conditions requiring clinical evaluation, therapeutic treatment, diagnostic procedures, extended nursing care, or increased length of stay.
6. **Assign procedure codes** matching the documented approach, body part, device, and qualifier. For ICD-10-PCS, construct codes character by character across all seven positions. For CPT, match the service to the most specific code available.
7. **Apply modifiers** only when documentation supports their use. Modifier abuse (especially 25, 59, and XE/XS/XP/XU) is a top audit trigger.
8. **Validate the DRG/APC grouping** to ensure the coded data logically maps to the expected payment group.

### Medical Decision Making vs. Time-Based E/M Selection

Since the 2021 E/M restructuring (extended through 2025), providers select office/outpatient E/M level by either MDM or total time:

- **MDM** evaluates three elements (two of three required): number/complexity of problems addressed, amount/complexity of data reviewed, and risk level of complications/morbidity/mortality
- **Total time** includes face-to-face and non-face-to-face activities on the date of encounter: chart review, test review, ordering, documentation, and care coordination
- **G2211** (complexity add-on) may be appended to 99202-99215 when the visit reflects ongoing longitudinal care relationships; effective January 1, 2025, it can accompany modifier 25 with preventive services

## Step-by-Step Process

### Inpatient Coding Workflow

1. **Receive discharged record** with complete discharge summary, operative reports, pathology, and all provider documentation
2. **Review discharge summary** for principal diagnosis, secondary diagnoses, and procedures performed; cross-reference against operative notes and progress notes for discrepancies
3. **Query providers** via compliant CDI queries (AHIMA/ACDIS guidelines) when documentation is ambiguous, conflicting, or incomplete—never lead the provider toward a specific diagnosis; always include clinical indicators and a "unable to determine" option
4. **Assign ICD-10-CM codes**: principal diagnosis first, then all clinically significant secondary diagnoses including CCs and MCCs; assign POA (Present on Admission) indicators for all non-exempt codes
5. **Assign ICD-10-PCS codes**: construct seven-character codes using Tables—Section, Body System, Root Operation, Body Part, Approach, Device, Qualifier; follow guideline B3.2 for procedures converted from one approach to another (code both the inspection and the completed procedure)
6. **Validate MS-DRG grouping**: confirm the principal diagnosis drives the correct MDC (Major Diagnostic Category), secondary diagnoses appropriately elevate to CC/MCC tier, and procedures map correctly
7. **Run NCCI edits and Medically Unlikely Edits (MUEs)** to catch bundling violations before claim submission
8. **Submit claim** with appropriate bill type, discharge status, and all supporting data elements

### Outpatient/Professional Coding Workflow

1. **Review encounter documentation** including chief complaint, HPI, exam findings, assessment, and plan
2. **Select E/M level** based on MDM or total time; document the selection basis
3. **Assign CPT codes** for all procedures and services; use the most specific code—check for add-on codes, bundled services, and global surgical package inclusions
4. **Assign HCPCS Level II codes** for supplies, drugs, DME, and services not covered by CPT (e.g., J-codes for drugs, E-codes for DME, L-codes for orthotics)
5. **Apply modifiers**: 25 (separate E/M), 59/XE/XS/XP/XU (distinct procedural service), 26 (professional component), TC (technical component), 76/77 (repeat procedures), anatomical modifiers (LT, RT, F1-F9, etc.)
6. **Link diagnosis codes** to procedure codes demonstrating medical necessity via ICD-10-CM pointers
7. **Validate against NCCI PTP edits**: check Correct Coding Modifier Indicators—CCMI "0" means modifiers cannot bypass the edit; CCMI "1" means modifiers may bypass under documented circumstances
8. **Verify MUE limits**: confirm units of service do not exceed Medically Unlikely Edit thresholds

## Evaluation Criteria

### Coding Accuracy Metrics

| Metric | Target | Measurement Method |
|--------|--------|--------------------|
| Overall coding accuracy rate | ≥95% | Random sample audit of 20+ records per coder per quarter |
| Principal diagnosis accuracy | ≥98% | DRG validation audit comparing coded PDx to clinical record |
| CC/MCC capture rate | Within 2% of benchmark | Compare facility CC/MCC rate to CMS national averages by MDC |
| CPT code accuracy | ≥95% | Procedure-to-documentation matching audit |
| Modifier accuracy | ≥93% | Targeted modifier audit (focus on 25, 59, 76, 77) |
| Query response rate | ≥85% within 48 hours | CDI query tracking log |
| Denial rate attributable to coding | <3% of total claims | RCM denial analysis filtered to coding-related CARC/RARC codes |
| DRG change rate on audit | <8% | Pre-bill vs. post-audit DRG comparison |

### Severity of Impact Classification

- **Critical**: Errors affecting DRG assignment, causing overpayment (upcoding risk) or significant underpayment (>$2,000 revenue impact)
- **Major**: Incorrect secondary diagnosis sequencing affecting CC/MCC status, missing POA indicators, wrong modifier causing claim denial
- **Minor**: Specificity issues (e.g., laterality not captured), missing secondary diagnoses that do not affect DRG or quality measures
- **Informational**: Style/convention deviations that do not affect payment or compliance

## Red Flags & Edge Cases

1. **Severe malnutrition code creep**: CMS issued a specific alert (October 2023) reminding hospitals to use severe malnutrition codes (E40-E43) correctly; RACs actively target claims where severe malnutrition upgrades a DRG without supporting clinical indicators (BMI, albumin levels, documented muscle wasting). Assigning E43 based solely on a dietitian's assessment without physician attestation and clinical evidence triggers audits.

2. **Sepsis sequencing violations**: ICD-10-CM guideline I.C.1.d requires that when sepsis meets the definition of principal diagnosis, the underlying systemic infection code (A40.-, A41.-) must be sequenced first, with the organ dysfunction code sequenced as secondary. FY 2025 added T81.49 and O86.09 to sepsis-first sequencing rules. Coding septic shock (R65.21) without the preceding sepsis code is a guideline violation.

3. **Medicare Advantage diagnosis code manipulation**: The DOJ is aggressively targeting retrospective chart reviews and physician queries designed to add diagnoses that inflate risk-adjustment factor (RAF) scores. Seoul Medical Group paid $62 million; Independent Health Association paid $98 million; Kaiser affiliates paid $556 million for these practices. Any CDI query that references financial impact or targets HCC-specific codes without clinical justification violates compliance standards.

4. **Modifier 59 overuse to bypass NCCI edits**: CMS's NCCI Policy Manual (Rev. 2/28/2025) explicitly states that modifier 59 should not be used when a more specific X-modifier (XE, XP, XS, XU) is available. Using modifier 59 solely because two codes form a PTP edit pair—without documentation of a different session, site, organ system, or specimen—constitutes improper unbundling.

5. **Two-Midnight Rule short-stay exposure**: The OIG has resumed auditing short inpatient stays (discontinued after October 2013 but reinstated in the 2025 Work Plan). Claims with length of stay under two midnights that were billed as inpatient rather than outpatient-with-observation carry high recoupment risk under 42 CFR §405.929 (post-payment review).

6. **E/M level selection without documented MDM or time**: Selecting a Level 4 or 5 E/M code (99214/99215 or 99223/99233) requires documented evidence of either the MDM elements (two of three criteria met at the claimed level) or a time statement covering total provider time. Auditors find that >20% of high-level E/M claims lack the required documentation specificity.

7. **ICD-10-PCS root operation misidentification**: Coding a procedure as "Excision" (cutting out a portion) when the documentation describes "Resection" (cutting out all of a body part) changes the PCS code and potentially the DRG. Guideline B3.4a requires biopsy procedures to be coded to the root operation Excision with the qualifier Diagnostic—confusing this with Extraction or Inspection is a recurring error.

8. **Drug HCPCS/NDC mismatch in outpatient claims**: The OIG Work Plan targets hospitals billing for drugs where the HCPCS code does not match the National Drug Code of the drug actually administered. For example, billing J9035 (bevacizumab) when a biosimilar was dispensed requires the appropriate biosimilar HCPCS code (Q5107, Q5118, etc.).

9. **POA indicator gaming on hospital-acquired conditions**: Assigning POA=Y (present on admission) to conditions that developed during the hospital stay prevents CMS from identifying Hospital-Acquired Conditions (HACs) under the HAC Reduction Program. This directly affects quality-based payment adjustments and is a compliance violation under the Deficit Reduction Act §5001(c).

10. **Telehealth code transition errors**: The 2025 CPT update deleted codes 99442 and 99443 for telephone E/M and replaced them with new synchronous audio-only codes 98008-98015. Billing deleted codes after the effective date results in automatic denials. Medicare coverage for 98000-98015 remains under review—verify payer acceptance before submission.

11. **Unbundled laboratory panel components**: Billing individual analytes separately (e.g., sodium, potassium, chloride, CO2) when a comprehensive metabolic panel (CPT 80053) was ordered and performed constitutes unbundling. NCCI MUEs and PTP edits specifically target this pattern; the OIG Work Plan monitors CDT payment trends for outliers.

12. **CC/MCC overcapture through query manipulation**: CDI queries that consistently target conditions elevating DRG tiers (e.g., acute respiratory failure, encephalopathy, severe protein-calorie malnutrition) without proportional queries for conditions that do not affect payment trigger compliance red flags. Query patterns should reflect clinical documentation gaps, not revenue optimization.

## Common Mistakes

1. **Defaulting to unspecified codes** when documentation supports specificity—coding J18.9 (pneumonia, unspecified organism) when a sputum culture result of Streptococcus pneumoniae is documented in the record and the provider acknowledged it in the treatment plan.

2. **Ignoring "Excludes1" notes** in ICD-10-CM, which indicate two conditions cannot coexist on the same claim (mutually exclusive). Excludes2 notes (meaning "not included here" but may coexist) are frequently confused with Excludes1.

3. **Applying the etiology/manifestation convention backwards**—sequencing the manifestation code (marked "Code first" or "in diseases classified elsewhere") as the principal diagnosis instead of the underlying condition.

4. **Billing G2211 with every E/M visit** regardless of whether the encounter reflects longitudinal relationship complexity. CMS designed G2211 for visits where the provider serves as the continuing focal point of care—not for episodic or first-time encounters without established relationship.

5. **Miscounting time for prolonged services**: For office/outpatient visits billed by time, 99417 (prolonged service) requires meeting the minimum time of the highest-level E/M code plus at least one full 15-minute increment. For 99215 (40-minute base), prolonged service cannot be added until 55 minutes are reached.

6. **Failing to code discontinued procedures under ICD-10-PCS**: Guideline B3.3 requires that if a procedure is discontinued before any root operation is performed, the coder assigns Inspection of the body part or anatomical region inspected—not the intended procedure code.

7. **Omitting laterality in ICD-10-CM** when the code structure provides laterality designations. For example, coding M17.11 (primary osteoarthritis, right knee) as M17.10 (unspecified knee) when the operative report clearly states "right knee."

8. **Using modifier 25 without separate documentation**: The E/M service must stand alone as a billable service with no overlapping key components with the procedure's inherent E/M. A single note saying "also evaluated for other conditions" without documented history, exam, and MDM for the separate condition does not support modifier 25.

## Regulatory & Compliance Requirements

### Federal Statutes and Regulations

| Reference | Applicability |
|-----------|---------------|
| **HIPAA §1173** (Administrative Simplification) | Mandates use of ICD-10-CM/PCS and CPT/HCPCS as standard code sets for electronic transactions |
| **False Claims Act, 31 USC §§3729-3733** | Imposes treble damages and per-claim penalties ($13,946-$27,894 per claim as of 2025) for knowingly submitting false claims, including upcoded or unbundled services |
| **Anti-Kickback Statute, 42 USC §1320a-7b** | Prohibits offering or receiving remuneration to induce referrals; diagnosis code manipulation to inflate risk-adjustment payments falls within AKS enforcement scope |
| **42 CFR §414.202** | Defines DME for HCPCS/Medicare payment purposes |
| **42 CFR §424.5(a)(6)** | Requires sufficient information to support claims |
| **42 CFR §405.986** | Governs good cause for reopening claims (relevant to RAC audits) |
| **SSA Title XVIII §1862(a)(1)(A)** | Medical necessity exclusion—services not reasonable and necessary are excluded from Medicare coverage |
| **Deficit Reduction Act §5001(c)** | Authorizes HAC nonpayment provisions, requiring accurate POA indicators |

### Coding Standards and Guidelines

| Standard | Maintaining Organization | Update Cycle |
|----------|------------------------|--------------|
| ICD-10-CM Official Guidelines | CMS/NCHS (DHHS) | Annual (Oct 1 fiscal year) |
| ICD-10-PCS Official Guidelines | CMS | Annual (Oct 1) with April addenda |
| CPT Code Set | AMA CPT Editorial Panel | Annual (Jan 1) with quarterly updates |
| HCPCS Level II | CMS | Quarterly (Jan, Apr, Jul, Oct) |
| NCCI PTP Edits & MUEs | CMS | Quarterly |
| MS-DRG Definitions Manual | CMS | Annual (Oct 1) |
| OIG Compliance Program Guidance | HHS-OIG | Updated periodically; Seven Elements framework |
| AHIMA/ACDIS Query Practice Guidelines | AHIMA/ACDIS | 2019 Update (current) |

### OIG Work Plan Active Initiatives (2025)

- **MS-DRG Coding Validation** (RAC Topic 0001): All MS-DRGs 001-999 subject to post-payment review
- **Two-Midnight Rule enforcement**: Auditing short inpatient stays for potential outpatient reclassification
- **Hospital drug billing**: Verifying HCPCS-to-NDC alignment for outpatient drug claims
- **Medicare CDT payment review**: Analyzing clinical diagnostic laboratory test payment trends for outlier identification
- **Severe malnutrition coding**: Targeted review of E40-E43 claims for clinical documentation support

## Terminology

1. **ICD-10-CM**: International Classification of Diseases, 10th Revision, Clinical Modification—the HIPAA-mandated diagnosis code set for all healthcare settings in the United States; maintained by CMS and CDC/NCHS; contains 3-7 character alphanumeric codes.

2. **ICD-10-PCS**: International Classification of Diseases, 10th Revision, Procedure Coding System—the procedure code set used exclusively for inpatient hospital reporting; 7-character alphanumeric codes constructed from Tables across Section, Body System, Root Operation, Body Part, Approach, Device, and Qualifier.

3. **CPT (Current Procedural Terminology)**: The AMA-maintained code set describing medical, surgical, and diagnostic services performed by physicians and qualified healthcare professionals; Category I (5-digit numeric), Category II (performance tracking), and Category III (emerging technology, suffixed with "T").

4. **HCPCS Level II**: CMS-maintained alphanumeric codes (A0000-V9999) for products, supplies, drugs, DME, ambulance services, and non-physician services not covered by CPT; required for Medicare and Medicaid claims.

5. **MS-DRG (Medicare Severity Diagnosis Related Group)**: The CMS payment classification grouping inpatient hospital stays into clinically coherent categories with similar resource consumption; principal diagnosis determines MDC, secondary diagnoses determine CC/MCC tier (triad: with MCC / with CC / without CC/MCC).

6. **CC/MCC (Complication or Comorbidity / Major Complication or Comorbidity)**: Secondary diagnoses that increase expected resource consumption. MCC elevates to the highest DRG tier; CC to the middle tier. CMS maintains a severity-of-illness list that defines which ICD-10-CM codes qualify.

7. **POA Indicator (Present on Admission)**: A data element reported on inpatient claims identifying whether a diagnosis was present at the time of admission (Y), not present (N), unknown (U), or clinically undetermined (W); drives HAC payment adjustments.

8. **NCCI (National Correct Coding Initiative)**: CMS program comprising PTP edits (code pairs that should not be reported together) and MUEs (maximum units of service per line per day); updated quarterly to prevent improper Part B payments.

9. **MUE (Medically Unlikely Edit)**: A CMS edit specifying the maximum units of service a provider would report under most circumstances for a single beneficiary on a single day; exceeding the MUE triggers automatic denial.

10. **Modifier 25**: CPT modifier appended to E/M codes indicating a significant, separately identifiable E/M service by the same physician on the same day as a procedure or other service; documentation must support the E/M as a standalone billable encounter.

11. **Modifier 59 / X{EPSU}**: Distinct Procedural Service modifier used to identify procedures not normally reported together but appropriate under documented circumstances; XE (separate encounter), XP (separate practitioner), XS (separate structure), XU (unusual non-overlapping service) are more specific alternatives that should be used when applicable.

12. **CDI (Clinical Documentation Improvement)**: A program staffed by CDI specialists (typically nurses or coders with clinical backgrounds) who review inpatient records concurrently to identify documentation gaps and issue compliant queries to providers for clarification.

13. **Principal Diagnosis**: The condition established after study to be chiefly responsible for occasioning the admission (inpatient) or the reason for the encounter (outpatient)—per UHDDS definition; determines DRG grouping and claim adjudication logic.

14. **Root Operation (ICD-10-PCS)**: The third character of an ICD-10-PCS code defining the objective of the procedure (e.g., Excision = cutting out/off a portion; Resection = cutting out/off all of a body part; Replacement = putting in a biological or synthetic substitute).

15. **Global Surgical Package**: The bundle of pre-operative, intra-operative, and post-operative services included in a surgical CPT code's payment; 000 (endoscopic/minor), 010 (minor with 10-day post-op), 090 (major with 90-day post-op).

16. **RAC (Recovery Audit Contractor)**: CMS-contracted entities authorized to identify and recoup Medicare overpayments and identify underpayments through post-payment claim review; MS-DRG validation (topic 0001) is a standing approved review topic.

17. **HCC (Hierarchical Condition Category)**: The risk-adjustment model used for Medicare Advantage payment; maps specific ICD-10-CM diagnosis codes to condition categories that predict future healthcare costs—subject to intense OIG and DOJ enforcement scrutiny.

18. **APC (Ambulatory Payment Classification)**: The Medicare outpatient prospective payment system grouping for hospital outpatient services; CPT/HCPCS codes map to APCs which determine payment rates.

19. **Excludes1 / Excludes2**: ICD-10-CM notation conventions. Excludes1 = "NOT CODED HERE"—the two conditions cannot occur together. Excludes2 = "NOT INCLUDED HERE"—the condition is not part of this code but may coexist and be coded additionally.

20. **Query (CDI Query)**: A compliant communication from a CDI specialist or coder to a provider seeking clarification of ambiguous, conflicting, or incomplete documentation; must include clinical indicators, avoid leading language, and never reference financial impact per AHIMA/ACDIS guidelines.

21. **Etiology/Manifestation Convention**: ICD-10-CM sequencing rule requiring the underlying disease (etiology) to be listed first, followed by the manifestation code; codes with "in diseases classified elsewhere" in their title are always sequenced second.

22. **PLA (Proprietary Laboratory Analyses)**: CPT codes (0001U-series) assigned to specific clinical laboratory tests performed by a single laboratory or manufacturer; 37% of new CPT 2025 codes were PLAs, primarily for genetic testing.

23. **Category III CPT Codes**: Temporary codes (suffixed with "T") for emerging technologies, services, and procedures; used for data collection purposes and may not be reimbursed by all payers. AMA added 40 new Category III codes (0948T-0987T) effective July 1, 2025.

## Quality Checklist

1. [ ] **Principal diagnosis sequenced correctly** per UHDDS definition and ICD-10-CM Official Guidelines Chapter-specific instructions (etiology/manifestation, obstetric, injury, and neoplasm sequencing rules verified)
2. [ ] **All codes assigned to highest specificity** supported by documentation—no unspecified codes when specificity is documented (laterality, episode of care, trimester, type)
3. [ ] **CC/MCC diagnoses clinically validated** against lab results, imaging, vital signs, treatment plan, and provider documentation—not assigned solely from CDI queries without clinical support
4. [ ] **POA indicators assigned for all non-exempt diagnosis codes** with logic verified: Y (documented or can be inferred as present), N (developed during stay), U (insufficient documentation), W (provider unable to determine)
5. [ ] **ICD-10-PCS root operation matches operative report language**—Excision vs. Resection vs. Extraction vs. Repair verified against procedure description; approach character matches documented surgical access
6. [ ] **NCCI PTP edits cleared**—no Column One/Column Two violations; modifiers applied only when CCMI="1" and documentation supports distinct service criteria
7. [ ] **MUE thresholds not exceeded** for any line item; units of service reconciled against documentation (e.g., drug doses, therapy minutes, number of lesions)
8. [ ] **E/M level supported by documented MDM or time statement**—for MDM, two of three elements met at claimed level; for time, total provider time documented and matches code threshold
9. [ ] **Modifiers 25 and 59 applied only with separate documentation**: modifier 25 requires standalone E/M documentation; modifier 59 requires evidence of different session, site, organ system, or specimen
10. [ ] **DRG/APC grouping validated** pre-submission—principal diagnosis drives correct MDC; no unexpected DRG shifts from secondary code changes
11. [ ] **Discharge status code accurate**—home, SNF, rehab, LTCH, AMA, or expired correctly assigned (affects DRG payment and transfer policy)
12. [ ] **Drug HCPCS codes match administered NDC**—biosimilars coded to biosimilar-specific HCPCS (not reference biologic code)
13. [ ] **Deleted/revised codes updated**—no submission of codes deleted in current FY/calendar year (e.g., CPT 99442/99443 deleted in 2025, replaced by 98008-98015)
14. [ ] **CDI queries are compliant**—contain clinical indicators, neutral language, clinically relevant options including "unable to determine," and no reference to financial or quality impacts

## References

1. CMS. "ICD-10-CM Official Guidelines for Coding and Reporting FY 2025." https://www.cms.gov/files/document/fy-2025-icd-10-cm-coding-guidelines.pdf
2. CMS. "ICD-10-PCS Official Guidelines for Coding and Reporting 2025." https://www.cms.gov/files/document/2025-official-icd-10-pcs-coding-guidelines.pdf
3. CMS. "Medicare NCCI Policy Manual – Chapter 1 (Rev. 2/28/2025)." https://www.cms.gov/files/document/01-chapter1-ncci-medicare-policy-manual-2025finalcleanpdf.pdf
4. CMS. "Medicare NCCI Policy Manual – Chapter 12: Supplemental Services HCPCS Level II (Rev. 1/1/2025)." https://www.cms.gov/files/document/12-chapter12-ncci-medicare-policy-manual-2025finalcleanpdf.pdf
5. CMS. "NCCI for Medicare – PTP Edits and MUE Updates." https://www.cms.gov/medicare/coding-billing/national-correct-coding-initiative-ncci-edits
6. CMS. "Medicare NCCI FAQ Library." https://www.cms.gov/medicare/coding-billing/national-correct-coding-initiative-ncci-edits/medicare-ncci-faq-library
7. CMS. "Proper Use of Modifiers 59, XE, XP, XS & XU (MLN1783722, February 2025)." https://www.cms.gov/files/document/mln1783722-proper-use-modifiers-59-xe-xp-xs-xu.pdf
8. CMS. "Evaluation and Management Services (MLN006764, November 2025)." https://www.cms.gov/files/document/mln006764-evaluation-management-services.pdf
9. CMS. "Inpatient Hospital MS-DRG Coding Validation – RAC Topic 0001." https://www.cms.gov/research-statistics-data-and-systems/monitoring-programs/medicare-ffs-compliance-programs/recovery-audit-program/approved-rac-topics-items/0001-inpatient-hospital-ms-drg-coding-validation
10. CMS. "2025 HCPCS Application Summary – Biannual 1 Non-Drug/Non-Biological Items & Services." https://www.cms.gov/files/document/2025-hcpcs-application-summary-biannual-1-2025-non-drug-non-biological-items-services.pdf
11. AMA. "AMA Releases CPT 2025 Code Set." https://www.ama-assn.org/press-center/ama-press-releases/ama-releases-cpt-2025-code-set
12. AAPC. "CMS Posts ICD-10-CM Update for FY 2025." https://www.aapc.com/blog/90927-cms-posts-icd-10-cm-update-for-fy-2025/
13. AAPC. "AMA Releases Quarterly Update to CPT 2025." https://www.aapc.com/blog/91882-ama-releases-quarterly-update-to-cpt-2025/
14. AAPC. "A Case for DRG Coding Validations." https://www.aapc.com/blog/90980-a-case-for-drg-coding-validations/
15. AAPC. "CMS Releases 2026 Update to HCPCS Level II." https://www.aapc.com/blog/93675-cms-releases-2026-update-to-hcpcs-level-ii/
16. UASI. "2025 OIG: Inpatient Documentation & Coding Issues." https://www.uasisolutions.com/inpatient-documentation-and-coding-issues
17. Healthicity. "July 2025 OIG Work Plan: 6 Compliance Areas to Watch." https://www.healthicity.com/blog/july-2025-oig-work-plan-6-compliance-areas-watch
18. White & Case. "Healthcare Fraud Enforcement in 2025: A Year of Aggressive Action." https://www.whitecase.com/insight-our-thinking/healthcare-fraud-enforcement-2025-year-aggressive-action-expanding-risk
19. White & Case. "DOJ's Record-Breaking 2025 False Claims Act Recoveries." https://www.whitecase.com/insight-alert/dojs-record-breaking-2025-false-claims-act-recoveries-and-key-healthcare-fraud
20. ABA Health Law. "Healthcare Fraud Enforcement Trends from 2024 and Issues to Watch in 2025." https://www.americanbar.org/groups/health_law/resources/esource/2025/healthcare-fraud-enforcement-trends-2024-issues-watch-2025/
21. AHIMA. "Clinical Documentation Integrity (CDI) Toolkit – Beginners' Guide." https://www.ahima.org/media/ztbfridh/cdi-toolkit-for-beginners_final.pdf
22. Sage Clinical RCM. "Driving Clinical Clarity: Best Practices for CDI Queries." https://sageclinicalrcm.com/driving-clinical-clarity-best-practices-for-high-quality-compliant-cdi-queries/