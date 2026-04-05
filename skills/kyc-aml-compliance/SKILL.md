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

# KYC AML Compliance

## Domain Overview

KYC/AML compliance in U.S. banking operates under a layered regulatory architecture rooted in the Bank Secrecy Act of 1970 (codified at 31 USC 5311-5336 and 12 USC 1829b, 1951-1960), as amended by the USA PATRIOT Act of 2001, the AML Act of 2020, and the Corporate Transparency Act. FinCEN serves as the primary administrator of BSA regulations (31 CFR Chapter X), while prudential regulators—the OCC, Federal Reserve, FDIC, and NCUA—examine institutions for compliance and bring enforcement actions. Global AML/KYC penalties reached $4.5 billion in 2024, with the TD Bank $3.1 billion settlement alone representing the largest BSA penalty in history. The enforcement environment is intensifying: federal banking agencies announced more than three dozen enforcement actions in 2024 against banks and individuals for BSA/AML/CFT failures.

A compliant BSA/AML program requires four statutory pillars plus a fifth added by the CDD Rule: (1) internal policies, procedures, and controls; (2) a designated BSA/AML compliance officer; (3) ongoing employee training; (4) independent audit/testing; and (5) risk-based customer due diligence procedures including beneficial ownership identification for legal entity customers. The AML Act of 2020 further inserted "countering the financing of terrorism" (CFT) into program requirements, mandated a government-wide AML/CFT priorities framework, and established FinCEN's beneficial ownership information (BOI) registry under the Corporate Transparency Act.

The FFIEC BSA/AML Examination Manual structures the supervisory approach around a risk-focused methodology. Examiners evaluate whether a bank's compliance program is commensurate with its risk profile across four dimensions: products/services, customers, geographic locations, and transaction volumes. Banks have flexibility in program design, but the program must demonstrably manage—not merely document—money laundering, terrorist financing, and other illicit financial activity risks. The 2025 regulatory environment reflects a dual trend: enforcement of willful violations remains aggressive (FinCEN's "first-of-its-kind data-driven enforcement operation" targeting 100+ MSBs), while regulators simultaneously ease low-value compliance burdens (FinCEN's February 2026 exceptive relief from per-account beneficial ownership re-verification under FIN-2026-R001).

Internationally, FATF's 40 Recommendations establish the global baseline. The U.S. is rated "compliant" or "largely compliant" with 31 of 40 FATF Recommendations but remains "non-compliant" on Recommendations 22, 23, and 28 (designated non-financial businesses and professions). FATF Recommendation 1 mandates the risk-based approach as the organizing principle for all AML/CFT measures, and Recommendation 10 specifies CDD requirements including beneficial ownership identification.

## Core Decision Framework

### Risk-Based Approach Decision Tree

The practitioner's mental model operates across three tiers of escalating scrutiny:

**Tier 1 — Standard Due Diligence (SDD/CDD):** Applied to all customers at onboarding. Collect CIP minimum data (name, address, DOB, TIN/SSN per 31 CFR 1020.220). Screen against OFAC SDN list, 314(a) requests, and PEP databases. Assign initial risk rating based on customer type, geography, product mix, and expected activity. For legal entity customers, identify and verify beneficial owners per 31 CFR 1010.230 (≥25% equity owners plus one individual with significant management responsibility).

**Tier 2 — Enhanced Due Diligence (EDD):** Triggered when customer risk rating exceeds the bank's defined threshold. Indicators include: foreign correspondent accounts (USA PATRIOT Act §312), private banking accounts for non-U.S. persons, PEPs, customers in FATF-identified high-risk jurisdictions, cash-intensive businesses, MSBs, marijuana-related businesses, and customers with adverse media. EDD requires deeper source-of-funds/source-of-wealth verification, senior management approval, and more frequent periodic reviews.

**Tier 3 — Suspicious Activity Escalation:** When transaction monitoring or relationship review surfaces anomalies. The decision question is not "can we explain this?" but "does the bank know, suspect, or have reason to suspect" that the transaction involves funds from illegal activity, is designed to evade BSA requirements, lacks business or lawful purpose, or involves use of the bank to facilitate criminal activity (31 CFR 1020.320(a)(2)). The $5,000 aggregation threshold applies for SAR filing; insider abuse has no dollar threshold.

### Key Decision Points

- **Open vs. decline account:** When CIP verification cannot be completed within a reasonable time, or when screening produces a confirmed OFAC match, the account must not be opened.
- **File SAR vs. document-and-monitor:** If investigation resolves the alert with a legitimate explanation consistent with the customer profile, document the rationale. If suspicion remains, file the SAR within 30 calendar days of detection (60 days if no suspect identified).
- **Continue vs. exit relationship:** SAR filing alone does not require account closure, but repeated SARs, inability to manage the risk, or law enforcement requests to maintain the account (keep-open letters) each require different treatment.
- **Apply simplified vs. standard vs. enhanced CDD:** The FATF risk-based approach requires proportionality. Over-filing SARs on low-risk customers wastes law enforcement resources; under-monitoring high-risk relationships creates enforcement exposure.

## Step-by-Step Process

### Phase 1: Customer Identification Program (CIP)
1. Collect minimum identifying information: full legal name, date of birth (individuals), address, and government-issued identification number (SSN, TIN, or passport number for non-U.S. persons).
2. Verify identity using documentary methods (unexpired government-issued photo ID) or non-documentary methods (credit bureau queries, public database checks, references from other financial institutions).
3. Screen customer name against OFAC SDN/Consolidated Lists, FinCEN 314(a) subject lists, and internal watch lists.
4. For legal entity customers, collect and verify beneficial ownership information per CDD Rule (31 CFR 1010.230): identify each individual owning ≥25% equity and one individual with significant managerial control.
5. Retain all CIP records for five years after account closure (31 CFR 1020.220(a)(3)).
6. Provide adequate notice to customers that information is being collected for identity verification purposes.

### Phase 2: Customer Due Diligence & Risk Rating
7. Develop initial customer risk profile based on: customer type (individual, entity, trust), products/services requested, geographic risk (country of origin, jurisdictions of anticipated transactions), anticipated transaction patterns, and industry/occupation.
8. Assign risk rating (e.g., low, medium, high, prohibited) using the bank's documented risk rating methodology.
9. For high-risk customers, escalate to EDD: obtain source of funds, source of wealth, purpose of account, expected transaction volume, and senior management approval.
10. Document the risk assessment rationale in the customer file.

### Phase 3: Ongoing Monitoring & Transaction Surveillance
11. Implement automated transaction monitoring calibrated to detect: structuring (deposits/withdrawals just below $10,000), rapid movement of funds (in-and-out activity), transactions inconsistent with customer profile, wire transfers to/from high-risk jurisdictions, and funnel account patterns.
12. Generate and file CTRs for currency transactions exceeding $10,000 (31 CFR 1010.311) within 15 days of the transaction. Aggregate multiple same-day transactions by/on behalf of the same person.
13. Review transaction monitoring alerts within established SLAs. Investigate alerts by comparing activity against the customer's risk profile and known business operations.
14. Update customer information and risk ratings when event-driven triggers occur (change in business nature, adverse media, law enforcement inquiry, significant transaction pattern shift).

### Phase 4: Suspicious Activity Reporting
15. When investigation confirms suspicion, prepare SAR narrative covering: who (subject identification), what (nature of suspicious activity), when (dates and timeframe), where (accounts, branches, jurisdictions), why (reason suspicion exists), and how (method of conducting activity).
16. File SAR via FinCEN's BSA E-Filing System within 30 calendar days of initial detection. If no suspect identified, additional 30 days permitted; maximum 60 days total.
17. For ongoing suspicious activity on previously reported subjects, file continuing SARs at least every 90 days.
18. Maintain SAR and supporting documentation for five years from date of filing. Never disclose SAR existence to the subject (31 CFR 1020.320(e) — "SAR confidentiality").

### Phase 5: Independent Testing & Program Governance
19. Conduct independent BSA/AML audit at least annually, covering all program pillars, transaction testing, and OFAC compliance.
20. Report audit findings to the board of directors. Track remediation of identified deficiencies.
21. BSA Officer provides periodic risk assessment updates to board and senior management, including changes to products, geographies, customer base, and regulatory environment.

## Evaluation Criteria

### Program Adequacy Assessment Matrix

| Component | Satisfactory | Needs Improvement | Deficient |
|---|---|---|---|
| **Risk Assessment** | Written, comprehensive, updated annually, covers all four risk dimensions | Exists but incomplete or stale (>18 months) | Absent or does not reflect actual risk profile |
| **CIP/CDD** | Verified 100% of accounts; BO collected for all legal entities | Verification gaps <5%; minor BO documentation deficiencies | Systematic verification failures; no BO program |
| **Transaction Monitoring** | Rules calibrated to risk; alert-to-SAR ratio documented; backlog <30 days | Some rules not risk-calibrated; backlog 30-90 days | Unmonitored transaction types; backlog >90 days; $18.3T unmonitored (TD Bank pattern) |
| **SAR Filing** | Timely, accurate, narratives address all five Ws; no late filings | Occasional late filings (<10%); narrative quality inconsistent | Systematic late/missing SARs; narratives lack specificity |
| **Training** | Annual, role-specific, covers current typologies; documented attendance | Generic training; no role differentiation | No training program or >12 months since last training |
| **Independent Testing** | Annual, independent, scope covers all BSA components | Annual but limited scope or insufficient independence | No independent testing in >18 months |
| **Board/Management Oversight** | Regular reporting, documented action on findings, adequate budget | Irregular reporting; slow remediation | No board reporting; "flat cost paradigm" despite growth |

## Red Flags & Edge Cases

1. **Structuring with precision targeting.** Customer makes multiple cash deposits of $9,500-$9,900 across different branches on the same day or consecutive days. Classic structuring pattern under 31 USC 5324, but banks often miss multi-branch patterns when branch-level monitoring lacks aggregation logic.

2. **Funnel accounts in non-operational geographies.** A customer based in one state receives dozens of cash deposits from unrelated parties in a distant state where the customer has no business presence. This was a core pattern in the TD Bank enforcement action, where employees opened accounts including for shell companies that engaged in funnel account activity in high-risk jurisdictions where TD Bank maintained no operations.

3. **Beneficial ownership opacity with layered entities.** A legal entity customer is owned by another entity registered in a jurisdiction with no public beneficial ownership registry (e.g., certain Caribbean or Pacific island nations). The 25% equity threshold under 31 CFR 1010.230 can be manipulated by creating four holding companies each owning 24.9%.

4. **Peer-to-peer payment blind spots.** Venmo, Zelle, and similar P2P transactions processed through bank accounts that lack adequate monitoring rules. FinCEN specifically cited TD Bank's failure to monitor P2P transactions, including those indicative of human trafficking patterns.

5. **Insider-facilitated laundering.** Bank employee opens accounts for shell companies in exchange for bribes, enabling millions in illicit fund flows. TD Bank's 2021 case involved an employee facilitating narcotics proceeds laundering. Insider abuse SARs have no minimum dollar threshold — any amount triggers the filing requirement.

6. **Dormant account reactivation.** Account with minimal activity for 12+ months suddenly receives large wire transfers followed by rapid disbursement. Banks that exclude dormant accounts from active monitoring miss this classic layering technique.

7. **PEP identification failure on downstream associates.** A bank identifies a foreign PEP but fails to apply EDD to the PEP's family members, close associates, or entities controlled by the PEP, violating FATF Recommendation 12 and often missing the actual laundering conduit.

8. **Trade-based money laundering through lending.** A commercial borrower provides invoices for trade finance that show over-invoicing or under-invoicing patterns (e.g., shipping goods valued at $5/unit with invoices at $50/unit). Banks focused only on credit risk miss the AML dimension of trade finance.

9. **Flat-cost compliance budget despite growth.** TD Bank enforced a "flat cost paradigm" requiring that BSA compliance spending not increase year-over-year despite significant U.S. business expansion and rising risk profiles. Regulators now explicitly scrutinize whether compliance budgets scale with institutional growth and complexity.

10. **Cryptocurrency-related banking without adequate controls.** A bank provides banking services to cryptocurrency exchanges or ATM operators without specialized monitoring rules for the velocity, volume, and cross-border nature of crypto-related transactions. Several 2024-2025 enforcement actions (KuCoin $297M, OKX $504M) involved failures at the exchange level that downstream banks should have flagged.

11. **SAR narrative deficiency — filing without substance.** A bank files SARs to "check the box" but narratives lack specificity: no transaction amounts, no behavioral context, no explanation of why activity is suspicious. FinCEN's October 2025 FAQs reiterated that SARs must contain information with "a high degree of usefulness" to law enforcement.

12. **Alert backlog normalization.** Transaction monitoring generates alerts faster than analysts can review them, and the bank treats a growing backlog as operational rather than as a compliance deficiency. The TD Bank case revealed backlogs of potentially suspicious activity that deprived law enforcement of timely intelligence.

13. **Failure to update customer information after adverse media.** A customer's name appears in public reporting about fraud, sanctions evasion, or criminal proceedings, but the bank's ongoing monitoring does not include adverse media screening, and the customer's risk rating remains unchanged.

## Common Mistakes

1. **Treating CDD as a one-time onboarding event.** The CDD Rule requires ongoing monitoring to maintain and update customer information on a risk basis. Banks that complete onboarding CDD but never refresh customer profiles fail the "ongoing" requirement of 31 CFR 1020.210(b)(5).

2. **Over-reliance on automated transaction monitoring without tuning.** Banks deploy vendor software with default rule settings and never calibrate thresholds to their specific customer base, generating either excessive false positives (analyst fatigue) or inadequate detection (missed true positives). The FFIEC Manual expects banks to demonstrate that their monitoring systems are "reasonably designed" relative to their risk profile.

3. **Conflating SAR filing with account closure.** Filing a SAR does not require closing the account, and closing an account does not eliminate the obligation to file a SAR. Some banks preemptively close accounts to avoid filing SARs, which itself constitutes a BSA violation.

4. **Applying uniform CDD to all legal entity types.** A sole-member LLC, a publicly traded corporation, and a foreign trust each require different approaches to beneficial ownership identification. The CDD Rule exempts certain entity types (publicly traded companies, regulated financial institutions, government entities) from beneficial ownership collection.

5. **BSA Officer lacks authority or direct board access.** Examiners specifically assess whether the BSA Officer has "sufficient authority and resources." A BSA Officer who reports three levels below the board, cannot independently escalate issues, or lacks dedicated staff is a structural deficiency cited in multiple 2024-2025 enforcement actions.

6. **Ignoring FinCEN 314(a) requests or treating them as optional.** Section 314(a) of the USA PATRIOT Act requires financial institutions to search their records within 14 days of receiving a FinCEN request and report positive matches. Institutions that lack a 314(a) response process face examination criticism and potential enforcement.

7. **Failing to aggregate CTR transactions across related persons.** The CTR filing obligation applies to transactions exceeding $10,000 "by, through, or to" the bank by or on behalf of the same person in a single business day. Banks that do not aggregate transactions across teller lines, branches, or related accounts under-file CTRs.

## Regulatory & Compliance Requirements

### Primary U.S. Statutory Framework
- **Bank Secrecy Act (BSA):** 31 USC 5311-5314, 5316-5336; 12 USC 1829b, 1951-1960
- **USA PATRIOT Act (2001):** Pub.L. 107-56; Section 312 (EDD for correspondent/private banking), Section 314 (information sharing), Section 326 (CIP)
- **AML Act of 2020:** Pub.L. 116-283, Division F, Sections 6001-6511
- **Corporate Transparency Act:** 31 USC 5336 (beneficial ownership reporting to FinCEN)

### Key FinCEN Regulations (31 CFR Chapter X)
- **31 CFR 1010.230:** Beneficial ownership requirements for legal entity customers (CDD Rule)
- **31 CFR 1010.310-314:** Currency Transaction Report (CTR) filing requirements ($10,000 threshold)
- **31 CFR 1020.220:** Customer Identification Program (CIP) for banks
- **31 CFR 1020.320:** Suspicious Activity Report (SAR) filing ($5,000 threshold; no threshold for insider abuse)
- **31 CFR 1010.306(a)(3):** Electronic filing requirement via BSA E-Filing System
- **31 CFR 1010.410/1020.410:** Recordkeeping for funds transfers (≥$3,000)

### Prudential Regulator Examination Authority
- **OCC:** 12 CFR 21.11 (SAR), 12 CFR 21.21 (BSA compliance program), OCC Bulletin 2024-19 (AML/CFT NPRM)
- **Federal Reserve:** 12 CFR 208.62-63, SR 25-04 (SAR FAQs)
- **FDIC:** 12 CFR 326.8 (CIP), 12 CFR 353 (SAR)
- **NCUA:** 12 CFR 748.1-748.2

### OFAC Compliance
- Executive Order 13224 (terrorism sanctions), 31 CFR Part 501 (OFAC enforcement), SDN List screening required at onboarding and on an ongoing basis

### International Standards
- **FATF Recommendations:** R.1 (risk-based approach), R.10 (CDD), R.11 (record-keeping), R.12 (PEPs), R.16 (wire transfers), R.20 (suspicious transaction reporting), R.24 (beneficial ownership transparency)
- **EU AMLR (2024):** Harmonized fines ≥€10M or 10% of turnover; establishes AMLA as central EU AML authority

### Recent Regulatory Developments (2024-2025)
- **FinCEN FIN-2024-FCT1 (June 2024):** Proposed rulemaking to modernize AML/CFT program requirements, requiring risk-based rather than rules-based approach and incorporating national AML/CFT priorities
- **FinCEN FIN-2026-R001 (February 2026):** Exceptive relief from per-account beneficial ownership re-verification; CFIs now collect BO once per customer and update on risk basis only
- **OCC Bulletin 2025-37:** Community bank minimum BSA/AML examination procedures
- **OCC Bulletin 2025-38:** Discontinuation of annual Money Laundering Risk System data collection
- **FinCEN CIP TIN Exemption (2025):** Banks may obtain TIN from third-party sources rather than directly from customers

## Terminology

1. **BSA/AML Program:** The mandatory compliance framework required under 31 USC 5318(h) comprising five pillars: internal controls, compliance officer, training, independent testing, and risk-based CDD. Not a single document but an integrated system of policies, processes, technology, and governance.

2. **Customer Identification Program (CIP):** Written procedures required under Section 326 of the USA PATRIOT Act (31 CFR 1020.220) for verifying customer identity at account opening. Minimum data: name, DOB, address, identification number.

3. **Customer Due Diligence (CDD):** The process of understanding the nature and purpose of a customer relationship and developing a customer risk profile. Codified in the 2016 CDD Rule (effective May 2018) at 31 CFR 1010.210 and 1020.210(b)(5).

4. **Enhanced Due Diligence (EDD):** Heightened scrutiny applied to high-risk customers, including deeper verification of source of funds/wealth, more frequent reviews, and senior management approval. Required by statute for foreign correspondent and private banking accounts (USA PATRIOT Act §312).

5. **Beneficial Owner:** Under 31 CFR 1010.230(d), each individual owning ≥25% equity in a legal entity customer (ownership prong) plus one individual with significant responsibility to control, manage, or direct the entity (control prong).

6. **Suspicious Activity Report (SAR):** Confidential filing to FinCEN (31 CFR 1020.320) when a transaction of $5,000+ involves funds from illegal activity, is designed to evade BSA requirements, has no business or apparent lawful purpose, or involves criminal use of the bank. Filed via BSA E-Filing; 30-day deadline from detection.

7. **Currency Transaction Report (CTR):** Mandatory FinCEN filing (31 CFR 1010.311) for cash transactions exceeding $10,000 in a single business day, aggregated across all transactions by or on behalf of the same person.

8. **Structuring (Smurfing):** Deliberately breaking transactions into amounts below reporting thresholds to evade CTR filing. A federal crime under 31 USC 5324, regardless of whether the underlying funds are legitimate.

9. **OFAC SDN List:** The Specially Designated Nationals and Blocked Persons List maintained by the Office of Foreign Assets Control. Matches require immediate blocking of assets and reporting; no transactions permitted.

10. **314(a) Request:** FinCEN request under USA PATRIOT Act §314(a) requiring financial institutions to search records for accounts or transactions of named subjects under investigation. Response required within 14 days.

11. **314(b) Voluntary Information Sharing:** USA PATRIOT Act §314(b) safe harbor permitting financial institutions to share information with each other about suspected money laundering or terrorist financing, provided they file notice with FinCEN.

12. **Politically Exposed Person (PEP):** An individual entrusted with a prominent public function (domestic or foreign). While BSA regulations primarily address "senior foreign political figures" (31 CFR 1010.605(p)), FATF Recommendation 12 extends EDD to domestic PEPs and PEP family members/close associates.

13. **Funnel Account:** An account that receives multiple cash deposits from geographically dispersed locations and then wires funds out, typically to a different jurisdiction. A primary indicator of drug trafficking proceeds laundering.

14. **Risk Rating/Customer Risk Profile:** A bank-assigned classification (e.g., low/medium/high) reflecting the customer's overall ML/TF risk based on customer type, geography, products, and activity. Must be maintained and updated per CDD Rule.

15. **Transaction Monitoring:** Automated and manual surveillance of customer transactions to detect patterns indicative of money laundering, terrorist financing, fraud, or other suspicious activity. Systems must be calibrated to the bank's specific risk profile.

16. **BSA E-Filing System:** FinCEN's electronic filing platform for CTRs, SARs, CMIRs, FBARs, and other BSA reports. Paper filing is no longer accepted for most report types.

17. **Willful Violation:** A BSA violation where the institution acted with either intentional disregard or reckless disregard of a known legal duty. Triggers enhanced civil penalties and potential criminal prosecution.

18. **National AML/CFT Priorities:** Eight priorities published by FinCEN (June 2021, updated periodically): corruption, cybercrime, domestic/international terrorist financing, fraud, transnational criminal organizations, drug trafficking, human trafficking/smuggling, and proliferation financing.

19. **Exceptive Relief (FIN-2026-R001):** FinCEN's February 2026 order relieving covered financial institutions from re-verifying beneficial ownership at every new account opening for existing legal entity customers, allowing one-time collection with risk-based updates.

20. **FFIEC BSA/AML Examination Manual:** The interagency manual providing examination procedures for federal and state examiners assessing BSA/AML compliance. Not a regulation itself but the primary reference for supervisory expectations.

21. **Independent Testing:** Annual review of the BSA/AML program conducted by a party independent of the compliance function (internal audit or external firm). Must assess program adequacy relative to the bank's risk profile and test transaction samples.

22. **Correspondent Banking:** Banking services provided by one bank (correspondent) to another bank (respondent), particularly cross-border. Subject to heightened due diligence under USA PATRIOT Act §312 for foreign correspondent accounts.

23. **Keep-Open Letter/Directive:** A law enforcement request asking a bank to maintain an account that might otherwise be closed due to suspicious activity, to assist with an ongoing investigation. The bank must continue filing SARs on the account.

## Quality Checklist

1. [ ] BSA/AML risk assessment is documented in writing, covers products/services/customers/geographies, and has been updated within the last 12 months.
2. [ ] CIP procedures collect and verify all four minimum data elements (name, DOB, address, ID number) for 100% of new individual accounts, with exceptions documented.
3. [ ] Beneficial ownership information is collected for all legal entity customers at account opening, with the ownership prong (≥25%) and control prong (one individual) both addressed per 31 CFR 1010.230.
4. [ ] Transaction monitoring system rules are calibrated to the bank's specific risk profile, not vendor defaults; tuning documentation exists showing annual review of thresholds and scenarios.
5. [ ] Alert disposition backlog does not exceed 30 days; if it exceeds 30 days, a documented remediation plan with board awareness exists.
6. [ ] SARs are filed within 30 calendar days of initial detection; no SAR exceeds the 60-day maximum deadline; insider abuse SARs are filed regardless of dollar amount.
7. [ ] CTRs are filed for all currency transactions exceeding $10,000, with proper aggregation of same-day transactions by or on behalf of the same person across all branches and channels.
8. [ ] OFAC screening occurs at account opening, for all wire transfers, and on a recurring basis against updated SDN/Consolidated lists; matches are escalated to a designated OFAC compliance contact.
9. [ ] BSA Officer has direct reporting line to the board or a board committee, has sufficient staff and budget, and the compliance budget has scaled proportionally with institutional growth.
10. [ ] Independent BSA/AML testing was completed within the last 12 months, covered all program pillars including OFAC, and findings were reported to the board with tracked remediation.
11. [ ] 314(a) response procedures are documented and tested; responses are submitted within 14 days of receipt.
12. [ ] Employee training is annual, role-specific (frontline, operations, management, board), covers current typologies and regulatory updates, and attendance is documented.
13. [ ] Customer risk ratings are updated when event-driven information is received (change in business, adverse media, law enforcement inquiry, significant transaction pattern shift).
14. [ ] SAR narratives contain the five Ws (who, what, when, where, why) plus how, with specific dollar amounts, dates, and account numbers — not boilerplate language.
15. [ ] The institution maintains a sanctions risk assessment separate from the BSA/AML risk assessment, covering OFAC programs, trade sanctions, and secondary sanctions exposure.

## References

- FinCEN, "The Bank Secrecy Act," https://www.fincen.gov/resources/statutes-and-regulations/bank-secrecy-act
- FinCEN, "CDD Final Rule," https://www.fincen.gov/resources/statutes-and-regulations/cdd-final-rule
- FinCEN, "FinCEN Assesses Record $1.3 Billion Penalty against TD Bank" (Oct 2024), https://www.fincen.gov/news/news-releases/fincen-assesses-record-13-billion-penalty-against-td-bank
- FinCEN, "Enforcement Actions," https://www.fincen.gov/news/enforcement-actions
- FinCEN Fact Sheet FIN-2024-FCT1 (June 2024), "AML/CFT Program Requirements NPRM," https://www.fincen.gov/system/files/shared/Program-NPRM-FactSheet-508.pdf
- FinCEN SAR Electronic Filing Instructions, https://www.fincen.gov/system/files/shared/FinCEN%20SAR%20ElectronicFilingInstructions-%20Stand%20Alone%20doc.pdf
- FFIEC BSA/AML Examination Manual, https://bsaaml.ffiec.gov/
- FFIEC BSA/AML Risk Assessment Procedures, https://bsaaml.ffiec.gov/manual/BSAAMLRiskAssessment/01
- FFIEC, "Appendix F – Money Laundering and Terrorist Financing Red Flags," https://bsaaml.ffiec.gov/manual/Appendices/07
- FFIEC, "Customer Identification Program," https://bsaaml.ffiec.gov/manual/AssessingComplianceWithBSARegulatoryRequirements/01
- OCC BSA/AML Bulletins and Advisories, https://www.occ.gov/topics/supervision-and-examination/bsa/bsa-aml-bulletins-fincen-advisories-related-basel/index-bsa-aml-bulletins-fincen-advisories-related-basel.html
- 31 CFR 1020.320 (SAR filing for banks), https://www.law.cornell.edu/cfr/text/31/1020.320
- 31 CFR 1010.230 (Beneficial ownership requirements), https://www.law.cornell.edu/cfr/text/31/1010.230
- 31 CFR Part 1020 (Rules for Banks), https://www.ecfr.gov/current/title-31/subtitle-B/chapter-X/part-1020
- K&L Gates, "Lessons From 2024 Anti-Money Laundering Enforcement Actions" (Feb 2025), https://www.klgates.com/Lessons-From-2024-Bank-Secrecy-Act-Anti-Money-Laundering-Enforcement-Actions-2-12-2025
- Gibson Dunn, "2025 Year-End Developments in Anti-Money Laundering," https://www.gibsondunn.com/2025-year-end-developments-in-anti-money-laundering/
- Lowenstein Sandler, "TD Bank to Pay Historic $3 Billion Over AML Compliance Violations," https://www.lowenstein.com/news-insights/publications/client-alerts/td-bank-to-pay-historic-3-billion-over-aml-compliance-violations-aml
- NETBankAudit, "Key Takeaways from Recent BSA/AML Enforcement Actions," https://www.netbankaudit.com/resources/key-takeaways-from-recent-bsa-aml-enforcement-actions
- NETBankAudit, "Key Findings from 2024 BSA/AML Audits and MIS Verification Audits," https://www.netbankaudit.com/resources/2024-bsa-aml-audits-and-mis-verification-audits
- Troutman Pepper, "FinCEN Eases Beneficial Ownership Requirements Under CDD Rule," https://www.troutman.com/insights/fincen-eases-beneficial-ownership-requirements-under-cdd-rule/
- KJK, "Navigating KYC and AML Compliance After FinCEN's Beneficial Ownership Updates," https://kjk.com/2026/02/20/navigating-kyc-and-aml-compliance-after-fincens-beneficial-ownership-updates/
- Thomson Reuters, "5 Essential Steps for KYC/AML Onboarding and Compliance," https://legal.thomsonreuters.com/blog/5-essential-steps-for-kyc-aml-onboarding-and-compliance/
- FinIntegrity, "AML/CFT and Sanctions Enforcement Actions in 2025," https://finintegrity.org/aml-cft-and-sanctions-enforcement-actions-in-2025/
- Ncontracts, "Enforcement Actions Roundup: October 2025," https://www.ncontracts.com/nsight-blog/enforcement-actions-roundup-october-2025
- FATF, "The FATF Recommendations (2012-2025)," https://www.fatf-gafi.org/en/publications/Fatfrecommendations/Fatf-recommendations.html
- FATF, "Guidance for a Risk-Based Approach: The Banking Sector," https://www.fatf-gafi.org/content/dam/fatf-gafi/guidance/Risk-Based-Approach-Banking-Sector.pdf
- Federal Reserve SAR FAQ (SR 25-04), https://www.federalreserve.gov/supervisionreg/srletters/SR2504a1.pdf
- NCUA/Joint Statement on BSA Due Diligence for PEPs, https://ncua.gov/newsroom/press-release/2020/agencies-issue-statement-bank-secrecy-act-due-diligence-requirements-customers-who-may-be-considered-peps/joint-statement
- Shuftipro, "Complete Guide to KYC Compliance Regulations in 2025," https://shuftipro.com/blog/complete-guide-to-kyc-compliance-regulations-in-2025/
- Silent Eight, "2025 Trends in AML and Financial Crime Compliance," https://www.silenteight.com/blog/2025-trends-in-aml-and-financial-crime-compliance-a-data-centric-perspective-and-deep-dive-into-transaction-monitoring
- Holland & Knight, "Recent FinCEN Actions Signal Trump Administration's Focus," https://www.hklaw.com/en/insights/publications/2026/02/recent-fincen-actions-signal-trump-administrations-focus