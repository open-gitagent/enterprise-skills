---
name: subrogation
description: >
  Insurance subrogation process management including recovery identification, demand preparation, negotiation, arbitration, and collections.
metadata:
  vertical: bfsi-insurance
  function: claims
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "NAIC, Arbitration Forums"
---

## Role
Recover losses from responsible third parties by exercising equitable, contractual, or statutory subrogation rights through demand, arbitration, or litigation while maintaining Medicare, ERISA, and state-law compliance.

## Decision Framework

| Stage | Decision | Key Rule |
|---|---|---|
| 1 — Source ID | Equitable / contractual / statutory right? | Contractual enforceable as written; equitable subject to judicial limitations; statutory follows specific statute terms |
| 2 — Doctrine Assessment | Made-whole / ASR / ERISA applicable? | Made-whole: majority of states require full insured compensation first; ASR bars subrogating against own insured/co-insured; ERISA preempts state doctrines for self-funded plans (*US Airways v. McCutchen* 133 S.Ct. 1537 (2013); *Montanile v. Board of Trustees* 136 S.Ct. 651 (2016)) |
| 3 — Viability | Responsible party insured? Assets sufficient? | Claims <$100K: AF intercompany arbitration mandatory (signatory carriers); claims >$100K or non-signatory: litigation |
| 4 — Preservation | SOL docketed? Notice requirements met? | SOL ranges 1-6 years by jurisdiction/cause of action; FL reduced 4→2 years eff. March 2023; docket at FNOL |
| 5 — Medicare Check | Section 111 MMSEA reporting required? | Query CMS eligibility before settlement; $1,000/day/unreported beneficiary penalty; BCRC resolves conditional payments |

## Made-Whole & ASR State Split

| Issue | States — Contract Overrides Doctrine | States — Doctrine Controls |
|---|---|---|
| Made-Whole Override | Indiana, Ohio | Arkansas, Alabama, West Virginia; CO C.R.S. §10-1-135 (codified 2010) |
| Same-Company Subrogation | Illinois (*Benge*) | Minnesota Stat. §60A.41(b) |
| NY INS §3425 personal lines | N/A | Pro-rata only; no short-rate |

## Recovery Benchmarks

| Metric | Industry | Top Performer |
|---|---|---|
| Recovery Ratio (S&S / Net Paid) | 5.16% | 8.81%+ |
| Auto Physical Damage Recovery | 18-22% | 24%+ |
| Auto Liability Recovery | 1.0-2.0% | 2.5%+ |
| Days to Recovery — Physical Damage | ≤2 years | <12 months |
| Days to Recovery — Liability | ≤9 years | <5 years |
| Subrogation Success Rate | 60-70% | 80%+ |
| Arbitration Win Rate | 55-65% | 75%+ |
| Deductible Recovery Rate | 50-60% | 80%+ |
| SOL Compliance | 98% | 100% |
| Section 111 Reporting | 100% required | 100% |

## Process

**Phase 1 — Identification & Triage**
1. Review FNOL for third-party liability indicators; flag claims with subrogation potential; code in claims system
2. Determine applicable state law; conduct conflict-of-law analysis when loss state ≠ insured's residence state
3. Check whether responsible party or their carrier is an Arbitration Forums signatory

**Phase 2 — Investigation & Documentation**
4. Secure evidence preservation: photographs, physical evidence, police/fire reports
5. Obtain statements from insured, witnesses, responsible party; engage experts (origin-and-cause, engineering, accident reconstruction)
6. Document insured's total loss including uninsured/underinsured components for made-whole analysis
7. Verify whether waiver of subrogation exists in underlying contracts (AIA A201 §11.3, construction, lease)

**Phase 3 — Demand & Negotiation**
8. Issue subrogation demand letter including paid amounts, deductible recovery, supporting documentation
9. File through Arbitration Forums E-Subro Hub within applicable deadlines for intercompany disputes
10. Negotiate liability allocation percentages; track comparative/contributory negligence by jurisdiction

**Phase 4 — Escalation & Resolution**
11. If denied/contested: evaluate arbitration vs. litigation path; for ERISA claims pursue under §502(a)(3) equitable relief
12. For AF filings: prepare contentions, attach documentation, meet filing deadlines
13. For litigation: retain subrogation counsel, file within SOL, manage discovery
14. Resolve and close: distribute recovered amounts (carrier reimbursement, deductible return to insured)

**Phase 5 — Compliance & Reporting**
15. Report recovery in NAIC Annual Statement Schedule P per SSAP No. 55 election
16. Complete Section 111 MMSEA reporting for Medicare beneficiary claims; query CMS COBA before settlement
17. Refund insured's deductible from recovery proceeds per state requirements; update loss reserves; adjust IBNR

## Glossary

| Term | Definition |
|---|---|
| Equitable Subrogation | Rights arising by operation of law when insurer pays third-party-caused loss; subject to made-whole doctrine |
| Conventional Subrogation | Rights created by express policy language; enforceable as written subject to state limitations |
| Made-Whole Doctrine | Insured must be fully compensated before insurer may exercise subrogation; majority-state default rule |
| Anti-Subrogation Rule (ASR) | Bars insurer from subrogating against own insured, co-insured, or additional insured under same policy |
| Sutton Doctrine | ASR extension in landlord-tenant context: tenant deemed implied co-insured when rent partially funds property insurance |
| Intercompany Arbitration | Binding dispute resolution between AF signatory carriers; mandatory for auto physical damage and property <$100K |
| Arbitration Forums (AF) | Not-for-profit founded 1943; 5,400+ member companies; operates E-Subro Hub electronic demand platform |
| E-Subro Hub | AF electronic platform for sending, receiving, managing intercompany subrogation demands and escalating to arbitration |
| RRE (Responsible Reporting Entity) | Insurer/self-insured/TPA required to report claim info to CMS for Medicare beneficiaries under MMSEA §111 |
| Conditional Payment | Medicare payment subject to CMS recovery when a primary payer (liability/no-fault/WC) is identified |
| BCRC | Benefits Coordination & Recovery Center; CMS contractor resolving conditional payments and processing §111 data |
| Waiver of Subrogation | Contractual provision releasing insurer's subrogation rights against specified third party (AIA A201 §11.3) |
| Statute of Repose | Absolute time limit based on product age or construction completion; runs regardless of loss date |
| Salvage | Recovery from sale of damaged property after paid claim; reported alongside subrogation in Schedule P Col. 10 |
| Recovery Ratio | Salvage + subrogation recovered ÷ net claims paid; primary subrogation KPI |
| Collateral Source Rule | Tort doctrine preventing plaintiff's damages reduction based on insurance payments; affects subrogation scope |
| Common Fund Doctrine | Party recovering fund benefiting others must share recovery costs (attorney fees) proportionally; ERISA default per *McCutchen* |
| ERISA Preemption | 29 USC §1144(a) supersedes state laws relating to employee benefit plans; insulates self-funded plans from state subrogation restrictions |
| Deemer Clause | ERISA §1144(b)(2)(B): prevents states from treating self-funded plans as insurance for state regulation purposes |
| Comparative Negligence | Proportional fault allocation; modified comparative-fault states bar recovery if insured's fault exceeds 50%/51% |
| Schedule P | NAIC Annual Statement schedule; salvage/subrogation in Column 10; ten-year development triangles per 2024 NAIC revision |
| NASP | National Association of Subrogation Professionals; benchmarking, training, best practices |
| Special Arbitration Agreement | AF program for concurrent-coverage disputes; mandates arbitration for signatories |
| Impairment of Subrogation | Insured action (e.g., general release) prejudicing insurer's recovery ability; may void insurer obligation or entitle offset |

## Checklist

- [ ] SOL docketed at FNOL for every claim with identified third-party liability using shortest applicable limitations period
- [ ] Made-whole doctrine applicability verified for specific jurisdiction and source of subrogation right
- [ ] ASR analysis completed including co-insured, additional insured, and implied co-insured (Sutton Doctrine) status
- [ ] Underlying contracts reviewed for waiver-of-subrogation clauses before investigation expense incurred
- [ ] Medicare beneficiary status queried through CMS COBA before any settlement
- [ ] Section 111 MMSEA reporting completed within required quarterly filing windows
- [ ] ERISA plan status confirmed (self-funded vs. fully insured); plan document reviewed for reimbursement/subrogation provisions
- [ ] AF signatory status verified for both carriers; correct forum (Auto/Property/Special) selected; claims >$100K not filed through standard AF
- [ ] Insured's deductible included in demand; deductible recovery allocated to insured per state requirements
- [ ] Conflict-of-law analysis documented when loss state, residence state, and policy issuance state differ
- [ ] Evidence preservation protocol followed before spoilation risk materializes
- [ ] Recovery reported in Schedule P Col. 10; reserves adjusted per SSAP No. 55 election
- [ ] Insured notified of subrogation activity and cooperating per policy cooperation clause
- [ ] Comparative/contributory negligence assessed and factored into recovery viability and demand calculation
- [ ] Final recovery allocated: carrier reimbursement, insured deductible return, common-fund attorney fee reduction documented

## References
ERISA §502(a)(3) 29 USC §1132(a)(3); ERISA §514(a) 29 USC §1144(a); Medicare Secondary Payer Act 42 USC §1395y(b); MMSEA §111 P.L. 110-173 ($1,000/day penalty; GHP eff. Jan 2009; NGHP eff. Jul 2009); IRS §832/§846; Rev. Proc. 2025-15; NAIC MDL-900/902/903; SSAP No. 55; CO C.R.S. §10-1-135 (2010); OH Rev. Code §2323.44; FL Stat. §95.11 (SOL 4→2 yrs eff. Mar 2023); MN Stat. §60A.41(b); US Airways v. McCutchen 133 S.Ct. 1537 (2013); Montanile v. Board of Trustees 136 S.Ct. 651 (2016); FMC Corp. v. Holliday 498 US 52 (1990); AIA A201-2017 §11.3; AF $26.4B 2023 demands; 1.1M arbitration disputes; P&C recovery ratio 5.16%/6.73%/8.81%; NASP
