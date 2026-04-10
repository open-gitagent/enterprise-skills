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

## Role
End-to-end medical claims lifecycle: submission → adjudication → remittance → denial management.

## Five-Gate Adjudication Framework

| Gate | Focus | Key Checks |
|---|---|---|
| 1 — Structural | X12 syntax | 837P (005010X222A1) / 837I (005010X223A2); 999=file-reject; 277CA=claim-level |
| 2 — Eligibility | Coverage, COB | Birthday/policyholder/custodial rule; NSA in-network protections |
| 3 — Auth/Necessity | PA, LCD/NCD | ICD-10-CM meets LCD/NCD criteria; ~15% denied despite prior auth |
| 4 — Coding | NCCI edits | PTP/MUE/AOC edits; modifiers 25, 59/X{EPSU}; provider NPI/taxonomy |
| 5 — Payment | Contracted rate | Fee schedule/DRG/per diem/capitation; deductible; OOP max |

**CARC identifies gate failure; RARC specifies corrective action.**

## KPI Benchmarks

| Metric | Target | Alert Threshold |
|---|---|---|
| Clean Claim Rate | ≥98% | <95% triggers process review |
| First-Pass Resolution | ≥90% | <85% = systemic front-end issue |
| Denial Rate | <5% | >8% = root cause intervention |
| Net Days A/R | <35 | >45 |
| Appeal Overturn Rate | >65% | <50% |
| Timely Filing Compliance | 100% | Any miss = unrecoverable |
| Cost to Collect | <3.5% net revenue | >5% |
| Denial Write-Off Rate | <2% net revenue | >3% |

## Process

1. **Pre-Submission** — X12 270/271 real-time eligibility; confirm benefits/deductible/COB; obtain and document PA (auth number); CPT/HCPCS → ICD-10-CM linkage; apply POS code, NPI, taxonomy code
2. **Scrubbing** — NCCI PTP edits; MUE thresholds; ClaimsXten/Cotiviti/Optum payer libraries; modifier appropriateness; timely filing: Medicare 12 mo (42 CFR §424.44), Medicaid 12 mo (42 CFR §447.45), commercial 90-365 days
3. **Submission** — Generate 837P/837I; transmit via clearinghouse; receive 999 (syntax) + 277CA (claim-level acknowledgment)
4. **Adjudication** — Medicare: clean ≤30 days electronic, other-than-clean ≤45 days (SSA §1869(a)(2)); Medicaid: 90%/30d, 99%/90d (42 CFR §447.45); commercial: 30d/45d per state prompt-pay statutes
5. **Remittance** — Parse X12 835 ERA; CARC/RARC/Group Code (CO=write-off, PR=patient resp, OA, PI, CR); post payments; reconcile allowed amounts vs. contracted rates; transfer patient responsibility
6. **Denial Management** — Triage ≤48 hrs; soft vs. hard denial classification; root cause via CARC/RARC mapping; Medicare redetermination 120d, reconsideration 180d; NSA: open negotiation 30 biz days, IDR initiation 4 biz days after

## Glossary

| Term | Definition |
|---|---|
| 837P/837I | ANSI X12 claim: professional (005010X222A1) / institutional (005010X223A2) |
| 835/ERA | Electronic Remittance Advice — payer payment, adjustment, and denial detail |
| Clean Claim | Complete, correctly formatted claim processable without additional info |
| CARC | Claim Adjustment Reason Code (~358 active) — always paired with Group Code |
| RARC | Remittance Advice Remark Code (~1,185 active) — specifies corrective action |
| Group Code (CAGC) | CO=contractual write-off; PR=patient responsibility; OA; PI; CR |
| NCCI | CMS edit system: PTP (code pairs), MUE (max units), AOC (add-on codes); quarterly updates |
| MUE | Medically Unlikely Edit — max units/provider/beneficiary/day; MAI 1/2/3 |
| COB | Coordination of Benefits — payer ordering per NAIC model regulation and HIPAA |
| QPA | Qualifying Payment Amount — NSA median contracted rate; IDR determination baseline |
| IDR | Independent Dispute Resolution — federal NSA arbitration; $115/party (effective Jan 22, 2024) |
| LCD/NCD | Local/National Coverage Determination — CMS Medicare coverage criteria |
| DRG | Diagnosis Related Group — inpatient payment; PDx + procedures + CC/MCC tier |
| Modifier 59/X{EPSU} | Distinct procedural service; XE/XP/XS/XU preferred over legacy 59 |
| MAC | Medicare Administrative Contractor — processes Part A/B claims by jurisdiction |
| Timely Filing Limit | Medicare: 12 mo; Medicaid: 12 mo; commercial: 90-365 days per contract/state |
| Prior Authorization | Prospective payer approval; denial if absent regardless of medical necessity |
| Clearinghouse | Intermediary — 999 (syntax) and 277CA (claim-level) acknowledgments |
| Revenue Code | 3-digit institutional code (0762=observation, 0450=ER) |
| RAC | Recovery Audit Contractor — CMS contingency-fee auditors; improper payments |
| LEIE | OIG exclusion list — CMPs up to $100K/item for excluded provider billing |
| GFE | Good Faith Estimate — uninsured/self-pay patients ≥72 hrs before scheduled service |

## Checklist

- [ ] Eligibility verified ≤72 hrs; active coverage confirmed on actual DOS
- [ ] PA obtained, auth number documented, valid for DOS and specific service codes billed
- [ ] ICD-10-CM at highest specificity; no unspecified codes when documentation supports detail
- [ ] CPT/HCPCS pass NCCI PTP; no unbundled pairs without modifier + documentation support
- [ ] MUE thresholds checked; units do not exceed MAI-3 per-day limits for all service lines
- [ ] Claim form: 837P=professional, 837I=institutional; correct POS code applied
- [ ] Rendering NPI and taxonomy code current and active, matching service billed
- [ ] Timely filing deadline documented; claim submitted with ≥30-day buffer before deadline
- [ ] COB verified; primary billed first; secondary includes primary adjudication data (2320/2330 loops)
- [ ] 999 + 277CA confirmation retained with timestamp as proof of payer filing
- [ ] LEIE checked monthly for all rendering, referring, and ordering providers
- [ ] CARC/RARC mapped to denial category (access/auth/coding/necessity/billing) for root cause tracking
- [ ] Appeal filed within payer-specific deadline with clinical documentation and specific denial rebuttal
- [ ] NSA applicability assessed; GFE, disclosure, and consent documentation verified
- [ ] Paid claim reconciled against contracted rates; underpayments identified and pursued

## References
HIPAA 45 CFR Parts 160-164; CMS Pub 100-04; No Surprises Act P.L. 116-260 (IDR $115/party Jan 22, 2024); FCA 31 USC §§3729-3733 ($13,946-$27,894/claim 2025); AKS 42 USC §1320a-7b; Stark Law 42 USC §1395nn; CMS-0057-F; 42 CFR §424.44; 42 CFR §447.45; SSA §1869(a)(2); LEIE CMPs $100K; CMS-4204-F (eff. Nov 15, 2024); NCCI Policy Manual; CAQH CORE; HFMA; AHIMA; Experian Health State of Claims 2024
