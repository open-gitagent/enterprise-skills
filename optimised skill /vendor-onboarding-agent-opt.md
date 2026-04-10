---
name: vendor-onboarding-agent
description: >
  Automates vendor registration and setup including documentation collection, system integration, compliance verification, and master data management.
metadata:
  vertical: procurement
  function: supplier/vendor-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "FAR, UCC, ISO 9001"
---

## Role
Transform prospective suppliers into compliant, payment-ready entities through risk-tiered documentation collection, sanctions/tax screening, master data creation, and SoD-enforced approval workflows.

## Risk-Based Tiering Model

| Tier | Profile | Documentation Depth | Reassessment |
|---|---|---|---|
| Tier 1 — Critical/High | PII/core infrastructure access; mission-critical; CPI score <40; annual spend >$500K | Financial deep-dive; on-site audit capability; SOC 2/ISO 27001 review; enhanced OFAC (50% ownership); FCPA due diligence; exec-level approval | Semi-annual |
| Tier 2 — Moderate | Important non-critical ops; moderate data access; spend $50K-$500K | Financial health review; remote compliance audit; standard sanctions; insurance verification; manager approval | Annual |
| Tier 3 — Low | Commodity; no sensitive data access; spend <$50K | Automated sanctions; TIN validation; basic insurance; standard procurement approval | Biennial or at contract renewal |

## Documentation Decision Logic

| Vendor Type | Required Forms | Key Rule |
|---|---|---|
| U.S. domestic | W-9 (before first payment); COI; ACH authorization | TIN Matching via IRS e-Services validates name+TIN; failure → 24% backup withholding per IRC §3406 |
| Foreign individual | W-8BEN; valid 3 years from signing | Determines withholding rate per applicable tax treaty |
| Foreign entity | W-8BEN-E; FATCA classification | Chapter 3 and Chapter 4 status determination |
| Government contractor | Active SAM.gov; CAGE code; FAR 52.204-7 flow-down | Active SAM registration required before PO issuance |
| Services in U.S. | Form 1042-S reporting | Obligation regardless of W-8 status; U.S.-source income |
| OFAC-sanctioned geography | Enhanced DD + legal counsel + potential specific license | No standard processing |

## Performance Metrics

| Metric | Tier 3 Target | Tier 2 Target | Tier 1 Target |
|---|---|---|---|
| Cycle time (request to activation) | ≤5 biz days | ≤10 biz days | ≤15 biz days |
| Doc completeness at first submission | ≥85% | ≥80% | ≥75% |
| Master data accuracy (DQ rules pass rate) | ≥98% | ≥98% | ≥99% |
| Duplicate vendor creation rate | <1% | <0.5% | <0.1% |
| First-payment success rate | ≥95% | ≥97% | ≥99% |
| Sanctions screening completion | 100% within 24 hours | 100% within 24 hours | 100% within 24 hours |

## Compliance Scoring

| Status | Criteria |
|---|---|
| Pass | All docs collected; all screening negative; TIN validated; insurance current; bank account verified |
| Conditional Pass | Minor doc gaps with documented remediation plan (max 30 days); vendor activated with spend restrictions |
| Fail | Missing tax docs; unresolved sanctions hit; expired/insufficient insurance; bank validation failure; unresolved FCPA flags |

## Regulatory Framework

| Requirement | Citation | Key Rule |
|---|---|---|
| W-9 / W-8 Series | IRS | W-9 before first payment (U.S.); W-8BEN/W-8BEN-E for foreign; W-8 expires 3 years |
| Backup Withholding | IRC §3406 | 24% if valid TIN not obtained before first payment |
| Information Return Penalties | IRC §6721/§6722 | 2025: $310/form; max ~$3.78M for large filers |
| IRS TIN Matching | Pub 2108-A | Free e-Services tool; validates name+TIN before filing; prevents CP2100/CP2100A B-notices |
| Form 1042-S | — | U.S.-source income to foreign persons; filed by March 15 |
| OFAC Compliance | 31 CFR Part 501 | Prohibition on SDN transactions; 50% Rule: entities ≥50% owned by SDN are blocked even if unlisted |
| OFAC 50% Rule | OFAC guidance | Screen beneficial owners; Tier 1 vendors require ownership structure disclosure |
| EU AMLD 5/6 | — | Enhanced CDD for high-risk third-country transactions |
| FATF Recommendations | — | Global AML/CFT standards for third-party relationships |
| FCPA | 15 USC §78dd-1 et seq. | Prohibits payments to foreign govt officials; extends to third-party agents and vendors |
| UK Bribery Act 2010 | Section 7 | "Adequate procedures" defense requires documented DD on commercial partners |
| DOJ ECCP | — | Documented third-party DD: number assessed, trained, audited |
| ISO 20400:2017 | — | Sustainable procurement guidance; not certifiable |
| FAR 52.204-7 | U.S. federal | Active SAM.gov registration verification for federal contractors |
| Nacha Operating Rules | Eff. Mar 2022 | Account validation required for ACH origination (WEB debits; expanded all forward-entry types) |
| GDPR / CCPA | EU / California | Vendor PII requires consent, data minimization, retention limits |
| SOX §404 | — | Documented VMF change management controls; SoD enforced by system |

## Process

**Phase 1 — Intake & Initial Qualification (Days 0-1)**
1. Receive via centralized portal only (no email/phone); assign unique request ID; capture: legal entity, DBA, entity type, country, contact, category, estimated spend, requesting BU
2. Duplicate check: fuzzy matching on legal name + Tax ID + bank account (>80% similarity = manual review); flag exact matches as blocked
3. Assign risk tier via automated rules engine (spend, category, geography, data access); compliance officer override capability
4. Generate tier-appropriate document request package; send via secure portal with deadlines and escalation triggers

**Phase 2 — Documentation Collection & Validation (Days 1-5)**
5. Tax docs: U.S. vendors → W-9 + immediate IRS TIN Matching; foreign → W-8 series, treaty validity, withholding rate; flag missing TINs — 24% backup withholding per IRC §3406
6. Insurance: collect ACORD COI; validate certificate holder = your org's legal name; policy dates cover contract period; coverage limits meet contract minimums (GL/E&O/WC/Cyber); org named Additional Insured; set 60-day expiration alerts
7. Banking: collect via secure encrypted channel (never email); validate via ACH prenotification (3-day wait), micro-deposit ($0.01-$1.00 test), or real-time third-party (Plaid/Early Warning/ValidiFI); bank account legal name must match vendor legal name
8. Compliance docs: signed code of conduct; NDA; DPA (if PII/PHI); conflict of interest disclosure; diversity/sustainability certifications

**Phase 3 — Compliance Screening (Days 3-7)**
9. Sanctions: screen legal name, all aliases, principals, beneficial owners (≥50%) against OFAC SDN/SSI, BIS Entity, EU Consolidated, UN SC, HM Treasury; positive/partial match → freeze + escalate; false positive → document resolution rationale
10. Anti-bribery DD (Tier 1/2): FCPA/UK Bribery Act risk assessment; DOJ red flags: unusual payment patterns, govt official recommendation, high-corruption geography, ownership opacity, high commissions, relatives of govt officials in ownership
11. Financial health (Tier 1): D&B report + recent financials; bankruptcy risk indicators
12. SoD verification: requestor ≠ PO approver ≠ payment authorizer; COSO + SOX §404 requirement

**Phase 4 — Master Data Creation & System Integration (Days 5-8)**
13. Create vendor master in ERP: SAP S/4HANA → Business Partner (BP) with vendor role; General Data (name/address), Company Code Data (reconciliation account/payment terms), Purchasing Org Data (currency/incoterms/purchasing group); Oracle → Supplier + Supplier Sites; Coupa → Supplier (PO method/hold status/payment terms)
14. Cross-system sync (multi-ERP or ERP+P2P): via SAP CPI/MuleSoft/Boomi; attributes: vendor number mapping, company code restrictions, payment terms, hold/block status; P2P edits locked — drive changes through ERP integration
15. Data quality enforcement (10 DQ rules before activation): Tax ID format; bank name = legal name; postal code pattern; reconciliation account assigned; no blank address fields; POrg assignment; payment terms validated against contract

**Phase 5 — Approval & Activation (Days 7-10)**
16. Tier-appropriate approval: Tier 1 → compliance officer + procurement director + finance controller; Tier 2 → procurement manager + AP supervisor; Tier 3 → procurement team lead only
17. Pre-activation checklist: all docs collected/validated; all screening passed; master data complete and DQ-checked; payment method configured; PO communication method tested (cXML/EDI/email)
18. Activate: remove hold/block; send vendor welcome communication with portal access, PO testing instructions, key contacts
19. Post-activation: within 30 days confirm first PO transmission and first payment; resolve exceptions; transition to lifecycle management and continuous monitoring

## Glossary

| Term | Definition |
|---|---|
| ACORD Certificate | Standardized COI format; proves insurance coverage, limits, dates, and additional insured endorsements |
| Additional Insured | Endorsement extending vendor's insurance coverage to your org; distinct from Certificate Holder (receipt only) |
| B-Notice (CP2100/CP2100A) | IRS notice of name/TIN mismatches on filed returns; triggers solicitation process and potential backup withholding |
| Backup Withholding | 24% withheld on reportable payments when payee fails to provide valid TIN per IRC §3406 |
| Beneficial Ownership | Natural persons with ≥50% ownership or substantial control; OFAC 50% Rule makes these entities blocked |
| BP | Business Partner; SAP S/4HANA unified master data replacing XK01/FK01 vendor records |
| Company Code Extension | Enabling vendor for transactions within a specific legal entity; requires reconciliation account and payment terms |
| D-U-N-S Number | 9-digit D&B identifier; universal vendor ID; required for SAM.gov; base for PAYDEX/SER/SSI |
| Fuzzy Matching | Levenshtein/Jaro-Winkler/phonetic algorithm comparison to detect duplicate records despite spelling variations |
| Micro-Deposit | $0.01-$1.00 test deposits for bank account ownership verification; vendor confirms amounts |
| MRBR | SAP transaction releasing invoices blocked by tolerance violations |
| Prenotification (Prenote) | Zero-dollar ACH to validate routing/account number; 3-day wait; does not verify ownership |
| POrg | SAP Purchasing Organization; vendors must be extended to specific POrg before POs can be created |
| Reconciliation Account | GL account bridging vendor subledger to financial accounting; incorrect assignment misstate AP |
| SAM.gov | U.S. federal vendor registration; required for federal contracts; includes CAGE code, entity validation |
| SDN List | Specially Designated Nationals; OFAC's prohibited transaction list; updated multiple times per week |
| TIN Matching | IRS e-Services; validates name+TIN combinations before filing; prevents B-notices |
| VMF | Vendor Master File; authoritative database of all approved vendor records; single source of truth |

## Checklist

- [ ] Single intake channel enforced: all requests via centralized portal; email/phone rejected
- [ ] Duplicate check: fuzzy matching on legal name + Tax ID + bank account; results documented
- [ ] Risk tier assigned and documented; override includes compliance officer rationale
- [ ] W-9 TIN Matching completed (or W-8 validated for foreign); timestamp recorded
- [ ] Sanctions screening: OFAC SDN/SSI, BIS Entity, EU Consolidated, UN SC; screening date, list versions, results archived
- [ ] Bank account ownership verified: method documented (prenote/micro-deposit/third-party); bank name matches vendor legal name
- [ ] Insurance: ACORD COI on file; org named Additional Insured; coverage limits meet contract minimums; expiration tracking active
- [ ] SoD maintained: Requestor ≠ Approver ≠ Payment Processor; system roles verified
- [ ] Master data DQ rules passed: Tax ID format; bank-name match; postal code; reconciliation account; POrg extension complete
- [ ] Anti-bribery DD (Tier 1/2): FCPA red flag assessment documented; beneficial ownership disclosed and screened
- [ ] Cross-system sync verified: vendor record consistent across ERP and P2P; vendor number mapping confirmed; hold/block aligned
- [ ] Approval chain complete per tier; all approver timestamps and identities in audit trail
- [ ] Vendor welcome communication sent; PO transmission method tested
- [ ] 30-day post-activation verification calendared for first PO and first payment
- [ ] Continuous monitoring enrolled: sanctions rescreening schedule, insurance expiration tracking, data refresh cadence per tier

## References
IRS W-9/W-8BEN/W-8BEN-E; IRC §3406 (24% backup withholding); IRC §6721/§6722 ($310/form 2025; ~$3.78M cap); IRS Pub 2108-A TIN Matching; Form 1042-S (March 15); OFAC 31 CFR Part 501 (50% Rule); EU AMLD 5/6; FATF Recommendations; FCPA 15 USC §78dd-1; UK Bribery Act 2010 §7; DOJ ECCP; ISO 20400:2017; FAR 52.204-7; Nacha Operating Rules (Mar 2022); GDPR; CCPA; SOX §404; COSO; SAP S/4HANA BP model; Coupa; Oracle Procurement Cloud; Jaggaer; MidFirst Bank OFAC enforcement (same-day designation); AFP 79% payment fraud targets; Sphera 2025 (48% bankruptcy surge)
