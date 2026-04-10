---
name: trade-finance
description: >
  International trade finance operations including letters of credit, documentary collections, trade guarantees, and supply chain financing.
metadata:
  vertical: bfsi-banking
  function: operations
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "UCP 600, ISP 98, Incoterms"
---

## Role
Structure, examine, and settle trade finance instruments (LC, collections, guarantees, SCF) in compliance with ICC rules, Basel capital treatment, and sanctions/AML requirements.

## Four-Question Triage

| Question | Options | Governing Rules |
|---|---|---|
| 1 — Payment mechanism? | Documentary Credit (LC) | UCP 600: bank assumes primary payment on complying presentation |
| | Documentary Collection D/P or D/A | URC 522: bank acts as agent only; no payment guarantee |
| | Demand Guarantee / SBLC | URDG 758 / ISP98: bank pays on demand asserting default |
| | Open Account + SCF | BAFT/ICC Standard Definitions: financing against approved receivables/payables |
| 2 — Risk concentration? | Issuing bank (export LC) vs. applicant (import LC); sovereign/transfer risk; commodity risk; doc fraud | Map party risk; assess country risk; verify goods vs. dual-use lists |
| 3 — Capital treatment? | Short-term self-liquidating trade LC | Basel III CCF: 20% |
| | Performance guarantees / SBLCs | CCF: 50% |
| | Financial guarantees (direct credit substitutes) | CCF: 100% |
| | Unconditionally cancellable commitments | CCF: 10% |
| 4 — Compliance triggers? | Screen at issuance, amendment, presentation, payment | OFAC SDN/SSI; EU Consolidated List; UK Sanctions; UN SC lists; EAR dual-use; TBML FATF indicators |

## Documentary Compliance Decision Logic (UCP 600)

| Step | Rule | Source |
|---|---|---|
| All required docs presented? | Data need not be identical but must not conflict | UCP 600 Art. 14(d) |
| Each doc complies on face with LC terms + ISBP 821? | Examiner checks face of documents only | UCP 600 Art. 14(a) |
| Docs consistent with each other? | ISBP 821 Preliminary Considerations | ISBP 821 |
| Within expiry + 21-day post-shipment presentation period? | Or credit-specified period, whichever earlier | UCP 600 Art. 14(c) |
| If discrepant: refuse with ALL discrepancies in single notice | Must state document disposal instructions | UCP 600 Art. 16(c) |
| Examination deadline | Maximum 5 banking days from day following presentation | UCP 600 Art. 14(b) |

## Regulatory Framework

| Rule | Publication | Key Requirement |
|---|---|---|
| UCP 600 | ICC Pub 600, 2007 | 39 articles; 175 countries; must be expressly incorporated ("Subject to UCP 600") |
| ISBP 821 | ICC Pub 821, 2023 | Granular document examination standards; supplement to UCP 600 |
| eUCP v2.1 | 2019 | Supplement for electronic document presentation |
| URC 522 | ICC Pub 522, 1995 | 26 articles governing documentary collections |
| URDG 758 | ICC Pub 758, 2010 | Demand guarantees; companion ISDGP 814; demand must include supporting statement per Art. 15(a) |
| ISP98 | ICC Pub 590 | Standby letters of credit; auto-extends expiry if issuer closed on last day (differs from UCP 600 Art. 29) |
| URBPO | ICC Pub 750E | Bank Payment Obligations |
| BSA/AML | 31 USC §5311 et seq. | CDD, SAR/CTR filing; 5-year record retention (consider 10-year IEEPA/TWEA exposure) |
| OFAC | 31 CFR Parts 500-599 | SDN List; SOL extended to 10 years via 2024 IEEPA/TWEA amendment; $48.8M penalties 2024 |
| EAR | 15 CFR Parts 730-774 | Dual-use goods export controls (BIS) |
| AML Act 2020 | Div. F NDAA FY2021 | Modernized BSA; AML/CFT Priorities |
| Basel III CRE 20 | BCBS 205, Oct 2011 | CCFs for off-balance-sheet trade finance |
| CRR III (EU) | Eff. Jan 2025 | Revised Annex I; 40% uniform CCF non-cancellable contractual commitments |
| FATF | Recommendations 1/10/20; TBML 2021 | Risk-based CDD; SAR reporting; TBML: 20-30% of global ML flows |
| Wolfsberg/ICC/BAFT | Trade Finance Principles 2019 | AML controls industry consensus |
| UNCITRAL MLETR | 2017 | Electronic transferable records; adopted Singapore 2021, Bahrain 2023, UK 2023, France 2024 |

## Process

**Phase 1 — Structuring & Issuance**
1. Applicant submits LC application: beneficiary, amount, currency, tenor, goods description, required docs, latest shipment date, expiry date/place, Incoterms, special conditions
2. Issuing bank: KYC/CDD on applicant; sanctions screen all named parties; credit assessment; facility check
3. Issue LC via SWIFT MT700 (or MT710), explicitly referencing "Subject to UCP 600"
4. Advising bank authenticates via SWIFT key exchange; advises to beneficiary without undertaking (unless confirming)

**Phase 2 — Shipment & Presentation**
5. Beneficiary assembles docs: commercial invoice, transport document (B/L/AWB/multimodal), insurance certificate (if CIF/CIP), packing list, certificate of origin, inspection certificate, credit-specified docs
6. Present within 21 calendar days of shipment (UCP 600 Art. 14(c)) and before LC expiry
7. Nominated bank examines per UCP 600 Art. 14 + ISBP 821 within maximum 5 banking days

**Phase 3 — Settlement**
8. Complying presentation: bank honours (sight), incurs DPU, or accepts/negotiates drafts per LC availability
9. Discrepant: issue refusal notice per Art. 16(c)(i)-(iii) listing ALL discrepancies; state document disposal (hold/return/act per instructions)
10. Issuing bank re-examines; reimburses nominated bank within 5 banking days; releases docs to applicant

**Phase 4 — Post-Settlement**
11. Archive per BSA 5-year minimum; 10-year OFAC exposure window per 2024 amendment
12. Update obligor exposure; release collateral/margin

**Sanctions Screening Checkpoints (Mandatory)**
- LC issuance: applicant, beneficiary, advising bank, all named parties
- Amendment: any new parties, changed ports/routes, vessel names
- Document presentation: vessel name on B/L, actual ports, any new entities
- Payment: re-screen beneficiary and intermediary banks at settlement

## Glossary

| Term | Definition |
|---|---|
| Avalisation | Bank guarantee on bill of exchange/promissory note creating independent payment obligation; common in forfaiting |
| CCF | Credit Conversion Factor; Basel % converting off-balance-sheet exposure to on-balance-sheet credit equivalent |
| Complying Presentation | Documents conforming to LC terms, UCP 600, and ISBP 821; triggers bank's absolute obligation to honour |
| D/A | Documents Against Acceptance; URC 522; docs released on acceptance of term draft |
| D/P | Documents Against Payment; docs released only upon full immediate payment |
| DPU | Deferred Payment Undertaking; bank obligation to pay at specified future date on complying presentation |
| Discrepancy | Deviation between docs and LC/UCP 600/ISBP 821 requirements |
| Forfaiting | Without-recourse purchase of receivables (avalized notes/accepted bills) removing credit and political risk from exporter |
| Negotiation | UCP 600 Art. 2; nominated bank purchases drafts/docs by advancing funds before reimbursement date |
| On-Board Notation | B/L notation confirming goods loaded on named vessel on specific date; UCP 600 Art. 20(a)(ii) |
| Payables Finance | Buyer-led SCF; suppliers sell approved receivables at discount leveraging buyer creditworthiness; BAFT Principles |
| Presentation Period | Max 21 calendar days after shipment (UCP 600 Art. 14(c)) unless LC specifies otherwise |
| Red Clause LC | LC authorizing advance payments to beneficiary before shipment; pre-shipment finance at issuing bank risk |
| Sanctions Screening | Verification of all parties/vessels/ports/goods against OFAC SDN/SSI, EU Consolidated, UK, and UN SC lists |
| Silent Confirmation | Bank adds payment undertaking without issuing bank's authorization; disputed reimbursement risk |
| SBLC | Standby LC; bank pays on demand + statement of default; may be governed by UCP 600, ISP98, or URDG 758 |
| TBML | Trade-Based Money Laundering; over/under-invoicing, phantom shipments, circular trade; FATF: 20-30% of global ML flows |
| Transferable Credit | UCP 600 Art. 38; first beneficiary may make credit available to one or more second beneficiaries |
| URDG 758 | ICC rules for demand guarantees; demand must include supporting statement per Art. 15(a) |
| Usance/Tenor | Payment period under time/acceptance LC (e.g., 90 days after sight, 180 days after B/L date) |
| Without Recourse | Finance provider assumes obligor credit risk; cannot seek repayment from seller on default |

## Checklist

- [ ] MT700 explicitly states "Subject to UCP 600, ICC Publication No. 600" and specifies availability (sight/deferred/acceptance/negotiation)
- [ ] All parties (applicant, beneficiary, advising bank, confirming bank, shipping company, vessel, ports) screened against current OFAC SDN/SSI, EU, UK, and UN sanctions lists
- [ ] Goods description permits meaningful dual-use verification; invoice mirrors LC description exactly per UCP 600 Art. 18(c)
- [ ] B/L contains valid on-board notation with vessel name and shipment date per UCP 600 Art. 20(a)(ii); routing avoids sanctioned transshipment points
- [ ] Document examination completed and any refusal issued within 5 banking days per UCP 600 Art. 14(b)
- [ ] Refusal notice lists every discrepancy in single notice with document disposal instructions per Art. 16(c)
- [ ] CIF/CIP insurance covers ≥110% of LC value in LC currency; risks per UCP 600 Art. 28(f)(ii)
- [ ] Correct Basel CCF applied: 20% self-liquidating trade LCs; 50% performance guarantees; 100% financial guarantees
- [ ] Transaction assessed against FATF TBML risk indicators: price reasonableness, goods/route logic, party coherence, doc authenticity
- [ ] Collection instruction unambiguously specifies D/P or D/A terms, charges, protest instructions, case-of-need per URC 522 Art. 4
- [ ] URDG 758 demand includes supporting statement per Art. 15(a); received before expiry
- [ ] Records archived ≥5 years; 10-year OFAC/IEEPA exposure window considered
- [ ] SCF payables finance assessed for potential reclassification from trade payables to bank debt under IFRS/US GAAP
- [ ] eUCP v2.1 electronic documents: legal enforceability of ETRs confirmed under applicable MLETR adoption status

## References
UCP 600 ICC Pub 600 (2007); ISBP 821 ICC Pub 821 (2023); eUCP v2.1; URC 522 ICC Pub 522 (1995); URDG 758 ICC Pub 758 (2010); ISP98 ICC Pub 590; URBPO ICC Pub 750E; BSA 31 USC §5311; OFAC 31 CFR Parts 500-599 (10-yr SOL 2024); EAR 15 CFR Parts 730-774; AML Act 2020; Basel III BCBS 205; CRR III (EU Jan 2025); FATF TBML Risk Indicators 2021; Wolfsberg/ICC/BAFT Trade Finance Principles 2019; UNCITRAL MLETR (UK 2023, France 2024); ICC Trade Register 2025 (<0.3% default rates); OFAC $48.8M 2024; TD Bank $3B AML
