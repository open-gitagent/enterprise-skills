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

## Role
Translate clinical encounters into ICD-10-CM/PCS, CPT, and HCPCS codes to drive accurate reimbursement, DRG assignment, and compliance.

## Coding Decision Hierarchy

| Step | Action |
|---|---|
| 1 | Read entire encounter record before assigning any code |
| 2 | Identify principal diagnosis per UHDDS (condition chiefly responsible for admission); outpatient = highest specificity reason for encounter |
| 3 | Apply ICD-10-CM Official Guidelines chapter-specific rules; etiology/manifestation: underlying condition first, manifestation second (never principal DX) |
| 4 | Code to highest specificity documented; unspecified codes only when documentation genuinely lacks detail |
| 5 | Sequence secondary diagnoses: conditions requiring clinical evaluation, treatment, diagnostic procedures, extended nursing care, or increased LOS |
| 6 | Assign procedure codes: ICD-10-PCS = 7-character code across all positions; CPT = most specific code available |
| 7 | Apply modifiers only when documentation supports use (25, 59, XE/XS/XP/XU are top audit triggers) |
| 8 | Validate DRG/APC grouping; confirm coded data logically maps to expected payment group |

## E/M Selection: MDM vs. Time

| Method | Criteria |
|---|---|
| MDM | Two of three required: (1) number/complexity of problems, (2) amount/complexity of data reviewed, (3) risk of complications/morbidity/mortality |
| Total Time | All face-to-face + non-face-to-face on date of encounter: chart review, test review, ordering, documentation, care coordination |
| G2211 Add-On | Appended to 99202-99215 for longitudinal care relationships; eff. Jan 1, 2025 can accompany modifier 25 with preventive services |
| Prolonged Service 99417 | Requires ≥1 full 15-min increment above highest-level E/M minimum time; 99215 base = 40 min, so 99417 not billable until 55 min |

## Coding Accuracy Metrics

| Metric | Target | Measurement |
|---|---|---|
| Overall coding accuracy | ≥95% | Random sample ≥20 records/coder/quarter |
| Principal diagnosis accuracy | ≥98% | DRG validation audit vs. clinical record |
| CC/MCC capture rate | Within 2% of CMS benchmark | Compare to national averages by MDC |
| CPT code accuracy | ≥95% | Procedure-to-documentation matching |
| Modifier accuracy | ≥93% | Targeted modifier audit (25, 59, 76, 77) |
| Query response rate | ≥85% within 48 hrs | CDI query tracking log |
| Coding-related denial rate | <3% of total claims | CARC/RARC filtered denial analysis |
| DRG change rate on audit | <8% | Pre-bill vs. post-audit DRG comparison |

## Error Severity Classification

| Level | Definition |
|---|---|
| Critical | DRG assignment affected; overpayment (upcoding) or underpayment >$2,000 revenue impact |
| Major | CC/MCC sequencing error; missing POA; wrong modifier causing denial |
| Minor | Laterality not captured; secondary DX missing without DRG/quality impact |
| Informational | Style/convention deviation; no payment or compliance impact |

## Code Set Update Cycles

| Standard | Maintaining Organization | Update Cycle |
|---|---|---|
| ICD-10-CM | CMS/NCHS (DHHS) | Annual Oct 1 (FY2025: 252 new, 13 deleted, 36 revised) |
| ICD-10-PCS | CMS | Annual Oct 1 + April addenda |
| CPT | AMA CPT Editorial Panel | Annual Jan 1 (CPT 2025: 270 new, 112 deleted, 38 revised = 420 total) |
| HCPCS Level II | CMS | Quarterly (Jan 2026: 160 new, 101 deleted) |
| NCCI PTP Edits & MUEs | CMS | Quarterly |
| MS-DRG Definitions Manual | CMS | Annual Oct 1 |
| OIG Compliance | HHS-OIG | Seven Elements framework; updated periodically |
| AHIMA/ACDIS Queries | AHIMA/ACDIS | 2019 Update (current) |

## Process

**Inpatient Workflow**
1. Receive discharged record: discharge summary, operative reports, pathology, all provider documentation
2. Review discharge summary for PDx/secondary DX/procedures; cross-reference operative notes and progress notes for discrepancies
3. Query providers via compliant CDI queries (AHIMA/ACDIS guidelines): include clinical indicators, all clinically relevant options, "unable to determine" option; never reference financial impact
4. Assign ICD-10-CM: PDx first, then clinically significant secondary DX (CCs/MCCs); assign POA for all non-exempt codes
5. Assign ICD-10-PCS: 7-character codes via Tables — Section/Body System/Root Operation/Body Part/Approach/Device/Qualifier; B3.2: code both inspection and completed procedure for converted approach
6. Validate MS-DRG: PDx drives correct MDC; secondary DX elevates appropriate CC/MCC tier; procedures map correctly
7. Run NCCI PTP edits and MUEs; submit with bill type, discharge status

**Outpatient/Professional Workflow**
1. Review encounter: chief complaint, HPI, exam findings, assessment, plan
2. Select E/M level by MDM or total time; document selection basis
3. Assign CPT codes; check for add-on codes, bundled services, global surgical package inclusions (000/010/090 days)
4. Assign HCPCS Level II: J-codes (drugs), E-codes (DME), L-codes (orthotics); verify HCPCS-to-NDC alignment for drugs
5. Apply modifiers: 25 (separate E/M), 59/XE/XS/XP/XU (distinct procedural), 26/TC (component billing), 76/77 (repeat), anatomical (LT/RT/F1-F9)
6. Link DX codes to CPT via ICD-10-CM pointers demonstrating medical necessity
7. Validate NCCI PTP: CCMI "0" = modifiers cannot bypass; CCMI "1" = modifiers may bypass with documentation
8. Verify MUE limits; confirm units ≤ MAI threshold

## Glossary

| Term | Definition |
|---|---|
| ICD-10-CM | HIPAA-mandated diagnosis code set (all settings); 3-7 character alphanumeric; maintained by CMS/CDC-NCHS |
| ICD-10-PCS | Inpatient procedure code set only; 7-character codes from Tables across 7 axes |
| CPT | AMA-maintained code set; Category I (5-digit), Category II (tracking), Category III (emerging tech, "T" suffix) |
| HCPCS Level II | CMS alphanumeric codes (A0000-V9999); supplies/drugs/DME/ambulance/non-physician services |
| MS-DRG | Medicare Severity DRG — inpatient payment classification; PDx → MDC; secondary DX → CC/MCC tier (triad) |
| CC/MCC | Complication or Comorbidity / Major Complication or Comorbidity — secondary DX increasing resource consumption |
| POA Indicator | Present on Admission: Y/N/U/W; drives HAC payment adjustments under Deficit Reduction Act §5001(c) |
| NCCI | National Correct Coding Initiative — PTP edits (code pairs), MUEs (max units), quarterly updates |
| MUE | Medically Unlikely Edit — max units/provider/beneficiary/day; exceeding triggers automatic denial |
| Modifier 25 | Significant, separately identifiable E/M same day as procedure; standalone E/M documentation required |
| Modifier 59/X{EPSU} | Distinct procedural service; XE (separate encounter), XP (separate practitioner), XS (separate structure), XU (unusual non-overlapping); use X-modifiers when applicable |
| CDI | Clinical Documentation Improvement — concurrent record review; compliant queries to providers |
| Principal Diagnosis | Condition chiefly responsible for admission (UHDDS); determines DRG and claim adjudication |
| Root Operation (PCS) | 3rd PCS character: Excision (portion), Resection (all), Replacement (substitute), Repair, Inspection, etc. |
| Global Surgical Package | Pre/intra/post-op services bundled in surgical CPT; 000/010/090 days post-op |
| RAC | Recovery Audit Contractor — CMS post-payment auditors; MS-DRG validation RAC Topic 0001 standing approval |
| HCC | Hierarchical Condition Category — MA risk-adjustment model; maps ICD-10-CM to condition categories |
| APC | Ambulatory Payment Classification — hospital outpatient PPS; CPT/HCPCS → APC → payment rate |
| Excludes1 / Excludes2 | Excludes1 = mutually exclusive (cannot coexist); Excludes2 = not included here but may coexist |
| Query (CDI) | Compliant provider communication; clinical indicators + neutral options + "unable to determine" + no financial reference |
| Etiology/Manifestation | Sequencing rule: underlying disease (etiology) first; manifestation codes ("in diseases classified elsewhere") always second |
| PLA | Proprietary Laboratory Analyses — CPT 0001U-series; lab-specific; 37% of CPT 2025 new codes |
| Category III CPT | Temporary "T"-suffix codes for emerging technologies; data collection; may not be reimbursed; 40 new codes Jul 1, 2025 (0948T-0987T) |

## Checklist

- [ ] Principal diagnosis sequenced per UHDDS and ICD-10-CM Official Guidelines (etiology/manifestation/obstetric/injury/neoplasm rules)
- [ ] All codes at highest specificity: no unspecified when laterality/episode/trimester/type documented
- [ ] CC/MCC diagnoses clinically validated against labs/imaging/vital signs/treatment plan; not solely from CDI queries
- [ ] POA indicators assigned for all non-exempt codes: Y/N/U/W logic verified
- [ ] ICD-10-PCS root operation matches operative report language: Excision vs. Resection vs. Extraction vs. Repair; approach matches surgical access
- [ ] NCCI PTP edits cleared; no Column One/Two violations; modifiers applied only when CCMI="1" with documentation
- [ ] MUE thresholds not exceeded; units reconciled against documentation (drug doses/therapy minutes/lesion count)
- [ ] E/M level supported by MDM (two of three elements at claimed level) or time statement (total provider time documented)
- [ ] Modifiers 25 and 59 applied only with separate documentation: 25 = standalone E/M; 59 = different session/site/organ/specimen
- [ ] DRG/APC grouping validated pre-submission; no unexpected DRG shifts from secondary code changes
- [ ] Discharge status code accurate (home/SNF/rehab/LTCH/AMA/expired)
- [ ] Drug HCPCS codes match administered NDC; biosimilars coded to biosimilar-specific HCPCS (not reference biologic)
- [ ] Deleted/revised codes updated: CPT 99442/99443 deleted 2025 → replaced by 98008-98015
- [ ] CDI queries compliant: clinical indicators, neutral language, clinically relevant options including "unable to determine," no financial reference

## References
HIPAA §1173; FCA 31 USC §§3729-3733 ($13,946-$27,894/claim 2025; $2.9B DOJ recoveries 2024; Seoul Medical $62M; Independent Health $98M; Kaiser $556M Jan 2026); AKS 42 USC §1320a-7b; 42 CFR §§414.202, 424.5(a)(6), 405.929 (Two-Midnight Rule), 405.986; SSA Title XVIII §1862(a)(1)(A); Deficit Reduction Act §5001(c) (HAC POA); OIG Work Plan 2025 (RAC Topic 0001 all MS-DRGs 001-999; Two-Midnight Rule; drug HCPCS/NDC; CDT; severe malnutrition E40-E43); ICD-10-CM FY2025 Guidelines; ICD-10-PCS 2025 Guidelines; CMS NCCI Policy Manual Rev. 2/28/2025; CPT 2025 (AMA); HCPCS Jan 2026; MS-DRG Definitions Manual; AHIMA/ACDIS Query Practice Guidelines 2019; OIG Seven Elements compliance framework
