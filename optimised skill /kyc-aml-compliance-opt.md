---
name: kyc-aml-compliance
description: >
  Know Your Customer and Anti-Money Laundering compliance including customer due diligence, enhanced due diligence, transaction monitoring, and SAR filing.
metadata:
  vertical: bfsi-banking
  function: compliance
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "BSA, FinCEN, FATF, USA PATRIOT Act"
---

## Role
BSA/AML/CFT compliance program: CIP, risk-based CDD/EDD, transaction monitoring, SAR/CTR filing, and independent audit governance.

## Three-Tier Risk Framework

| Tier | Trigger | Requirements |
|---|---|---|
| 1 — Standard CDD | All new customers | CIP minimum data; OFAC SDN screen; 314(a) check; initial risk rating; BO for legal entities (≥25% equity + 1 control prong per 31 CFR 1010.230) |
| 2 — Enhanced Due Diligence (EDD) | High-risk rating exceeded | Foreign correspondent (§312), private banking non-U.S. persons, PEPs, FATF high-risk jurisdictions, cash-intensive businesses, MSBs, MRBs; source of funds/wealth; senior management approval; more frequent reviews |
| 3 — SAR Escalation | Alert investigation unresolved | File if bank knows/suspects/has reason to suspect: illegal funds, BSA evasion, no lawful purpose, criminal use; $5,000 threshold; no threshold for insider abuse |

## Key Decision Points

| Decision | Rule |
|---|---|
| Open vs. decline | CIP incomplete or confirmed OFAC match → do not open |
| File SAR vs. document-and-monitor | Suspicion remains after investigation → file; legitimate explanation consistent with profile → document |
| Continue vs. exit relationship | SAR alone ≠ closure required; repeated SARs/unmanageable risk/keep-open letter → separate treatment |
| SAR deadline | 30 calendar days from detection; 60 days max if no suspect identified; continuing SARs every 90 days |

## Program Adequacy Matrix

| Component | Satisfactory | Needs Improvement | Deficient |
|---|---|---|---|
| Risk Assessment | Written, comprehensive, annual, covers 4 dimensions | Incomplete or >18 months stale | Absent or misaligned |
| CIP/CDD | 100% verified; BO all legal entities | Gaps <5%; minor BO deficiencies | Systematic failures; no BO program |
| Transaction Monitoring | Risk-calibrated; alert-to-SAR documented; backlog <30 days | Some rules uncalibrated; backlog 30-90 days | Unmonitored types; backlog >90 days |
| SAR Filing | Timely, accurate, 5 Ws in narratives; no late filings | Occasional late (<10%); inconsistent narratives | Systematic late/missing; lacks specificity |
| Training | Annual, role-specific, current typologies, attendance documented | Generic; no role differentiation | None or >12 months lapsed |
| Independent Testing | Annual, independent, full scope | Annual but limited scope/independence | None in >18 months |
| Board Oversight | Regular reporting; documented action; scaled budget | Irregular; slow remediation | No board reporting; flat-cost paradigm |

## Process

**Phase 1 — Customer Identification Program (CIP)**
1. Collect: full legal name, DOB, address, government ID number (SSN/TIN/passport for non-U.S.)
2. Verify: documentary (unexpired gov't photo ID) or non-documentary (credit bureau, public database)
3. Screen: OFAC SDN/Consolidated Lists, FinCEN 314(a), internal watch lists
4. Legal entities: collect BO per 31 CFR 1010.230 — ≥25% equity owners (ownership prong) + 1 individual with significant management control (control prong)
5. Retain CIP records 5 years after account closure (31 CFR 1020.220(a)(3)); provide customer notice

**Phase 2 — CDD & Risk Rating**
6. Develop risk profile: customer type, products/services, geography, anticipated transaction patterns, industry
7. Assign risk rating (low/medium/high/prohibited) per documented methodology
8. EDD for high-risk: source of funds/wealth, purpose, expected volume, senior management approval
9. Document risk assessment rationale in customer file

**Phase 3 — Transaction Monitoring**
10. Calibrate automated monitoring for: structuring (sub-$10K deposits), rapid fund movement, activity inconsistent with profile, high-risk jurisdiction wires, funnel account patterns
11. File CTRs for currency transactions >$10,000 within 15 days (31 CFR 1010.311); aggregate same-day by/on behalf of same person
12. Review alerts within established SLAs; compare activity to customer risk profile
13. Update risk ratings on event-driven triggers: business change, adverse media, law enforcement inquiry, significant pattern shift

**Phase 4 — SAR Filing**
14. Prepare SAR narrative: who/what/when/where/why/how; specific amounts, dates, account numbers
15. File via FinCEN BSA E-Filing within 30 days of detection; 60-day max if no suspect
16. Continuing SARs every 90 days for ongoing suspicious activity
17. Maintain SAR + documentation 5 years from filing; never disclose to subject (31 CFR 1020.320(e))

**Phase 5 — Independent Testing & Governance**
18. Annual BSA/AML audit covering all program pillars; report findings to board; track remediation
19. BSA Officer provides periodic risk assessment updates; budget must scale with institutional growth

## Glossary

| Term | Definition |
|---|---|
| BSA/AML Program | 5-pillar framework: internal controls, compliance officer, training, independent testing, risk-based CDD |
| CIP | Customer Identification Program — §326 PATRIOT Act (31 CFR 1020.220); name/DOB/address/ID number |
| CDD | Customer Due Diligence — 2016 CDD Rule (31 CFR 1010.210, 1020.210(b)(5)); nature/purpose of relationship |
| EDD | Enhanced Due Diligence — heightened scrutiny for high-risk customers; mandatory for §312 accounts |
| Beneficial Owner | 31 CFR 1010.230: each individual owning ≥25% equity + one individual with significant management control |
| SAR | Suspicious Activity Report — 31 CFR 1020.320; $5,000+ threshold; no threshold for insider abuse; 30-day deadline |
| CTR | Currency Transaction Report — 31 CFR 1010.311; >$10,000 cash in one business day; aggregate same-person |
| Structuring (Smurfing) | Deliberate sub-threshold transaction splits to evade CTR filing; criminal under 31 USC 5324 |
| OFAC SDN List | Specially Designated Nationals list — immediate asset blocking; no transactions permitted |
| 314(a) Request | FinCEN records search request under PATRIOT Act §314(a); response required within 14 days |
| 314(b) Sharing | Voluntary information sharing safe harbor for ML/TF between institutions; file notice with FinCEN |
| PEP | Politically Exposed Person — prominent public function; EDD required per FATF R.12 (family/associates too) |
| Funnel Account | Receives dispersed cash deposits; wires out to different jurisdiction; primary drug trafficking indicator |
| Risk Rating | Low/medium/high classification based on customer type, geography, products, activity; must be maintained |
| Transaction Monitoring | Automated/manual surveillance calibrated to bank's specific risk profile (not vendor defaults) |
| BSA E-Filing System | FinCEN electronic platform for CTRs, SARs, CMIRs, FBARs; paper filing not accepted |
| Willful Violation | Intentional or reckless disregard of known legal duty; triggers enhanced civil penalties + criminal prosecution |
| AML/CFT Priorities | 8 FinCEN priorities (June 2021): corruption, cybercrime, domestic/intl terrorism, fraud, TCOs, drug trafficking, human trafficking, proliferation financing |
| Exceptive Relief FIN-2026-R001 | Feb 2026: BO collected once per customer; update on risk basis only; no per-account re-verification |
| FFIEC BSA/AML Manual | Interagency examination procedures; primary reference for supervisory expectations |
| Independent Testing | Annual review by party independent of compliance function; assesses program adequacy + transaction samples |
| Correspondent Banking | Cross-border banking services; heightened due diligence under PATRIOT Act §312 |
| Keep-Open Letter | Law enforcement directive to maintain suspicious account for investigation; bank continues filing SARs |

## Checklist

- [ ] BSA/AML risk assessment documented, covers products/services/customers/geographies, updated ≤12 months
- [ ] CIP verifies all 4 data elements (name/DOB/address/ID) for 100% of new individual accounts; exceptions documented
- [ ] BO collected for all legal entity customers: ownership prong (≥25%) and control prong per 31 CFR 1010.230
- [ ] Transaction monitoring calibrated to bank-specific risk profile (not vendor defaults); annual tuning documented
- [ ] Alert backlog ≤30 days; if >30 days, documented remediation plan with board awareness
- [ ] SARs filed within 30 calendar days; no SAR exceeds 60-day max; insider abuse SARs filed regardless of dollar amount
- [ ] CTRs filed for all >$10,000 currency transactions; same-day transactions properly aggregated across branches/channels
- [ ] OFAC screening at account opening, all wire transfers, and recurring against updated SDN/Consolidated Lists
- [ ] BSA Officer has direct board/committee reporting line; staff and budget scaled proportionally with institutional growth
- [ ] Independent testing completed ≤12 months; covers all pillars including OFAC; findings reported to board with tracked remediation
- [ ] 314(a) response procedures documented and tested; responses submitted within 14 days
- [ ] Training annual, role-specific (frontline/operations/management/board), covers current typologies; attendance documented
- [ ] Customer risk ratings updated on event-driven information (business change/adverse media/law enforcement/pattern shift)
- [ ] SAR narratives include 5 Ws + how; specific dollar amounts/dates/account numbers — no boilerplate
- [ ] Sanctions risk assessment separate from BSA/AML risk assessment; covers OFAC programs, trade sanctions, secondary sanctions

## References
BSA 31 USC 5311-5336; 12 USC 1829b, 1951-1960; USA PATRIOT Act Pub.L. 107-56 (§312 EDD, §314 info sharing, §326 CIP); AML Act of 2020 Pub.L. 116-283; Corporate Transparency Act 31 USC 5336; 31 CFR 1010.230/310-314/1020.220/1020.320/1010.306(a)(3)/1010.410; OCC 12 CFR 21.11/21.21; Fed Reserve 12 CFR 208.62-63 (SR 25-04); FDIC 12 CFR 326.8/353; NCUA 12 CFR 748; EO 13224; 31 CFR Part 501 (OFAC); FATF R.1/10/11/12/16/20/24; EU AMLR 2024 (≥€10M or 10% turnover); FIN-2024-FCT1; FIN-2026-R001 (Feb 2026 BO exceptive relief); OCC Bulletins 2025-37/2025-38; TD Bank $3.1B penalty Oct 2024 (largest BSA penalty); global AML penalties $4.5B 2024; FFIEC BSA/AML Examination Manual
