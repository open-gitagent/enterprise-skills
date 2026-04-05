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

# Mortgage Processing

## Domain Overview

Residential mortgage processing is the operational backbone connecting a borrower's application to a funded loan. It spans from the moment a borrower submits the six pieces of information constituting a TRID application—name, income, Social Security number, property address, estimated property value, and loan amount sought (12 CFR §1026.2(a)(3)(ii))—through loan closing and post-closing quality control. Every step operates under a dense regulatory framework where the Consumer Financial Protection Bureau (CFPB), Office of the Comptroller of the Currency (OCC), FDIC, Federal Reserve, and state regulators impose overlapping disclosure, timing, fair lending, and underwriting requirements.

The TILA-RESPA Integrated Disclosure (TRID) rule, effective since October 2015, consolidated previously separate Truth in Lending and RESPA disclosures into the Loan Estimate (LE) and Closing Disclosure (CD). These two forms govern the entire fee disclosure lifecycle. The LE must be delivered within three business days of receiving the borrower's application. The CD must be received by the borrower at least three business days before consummation. Three specific changes—APR inaccuracy exceeding 1/8 of a percent (1/4 for irregular payment loans), loan product changes, or addition of a prepayment penalty—trigger a mandatory new three-day waiting period (12 CFR §1026.19(f)(2)(ii)). Fee tolerances are categorized into zero-tolerance, 10%-tolerance, and unlimited-tolerance buckets, with creditors responsible for curing any excess charges.

The Ability-to-Repay/Qualified Mortgage (ATR/QM) rule (12 CFR §1026.43) requires creditors to make a reasonable, good faith determination that a borrower can repay their mortgage. The revised General QM definition, effective since March 2021, replaced the rigid 43% debt-to-income cap with a price-based threshold tied to the Average Prime Offer Rate (APOR). Creditors must still consider and verify income, assets, debts, alimony, child support, and DTI ratio or residual income, and must maintain written policies and procedures documenting how these factors are weighed. Approximately 97% of current originations qualify as QMs. Fair lending compliance under ECOA (Regulation B) and the Fair Housing Act requires constant monitoring—183 institutions were cited for ECOA/Regulation B violations in 2024, and four matters were referred to the DOJ for patterns of discrimination.

The appraisal and valuation landscape shifted significantly with the interagency Automated Valuation Model (AVM) final rule (89 FR 64,538, August 2024), effective October 1, 2025. Mortgage originators using AVMs for credit decisions must now adopt policies, practices, procedures, and control systems ensuring AVMs adhere to quality control standards addressing accuracy, bias protection, and nondiscrimination. Traditional appraisals must still conform to USPAP and be performed by state-certified or licensed appraisers (12 CFR §1026.35(c)(1)(i)).

## Core Decision Framework

Experienced mortgage processors apply a layered decision framework at each stage:

**1. Application Completeness Gate**
Before any processing begins, confirm the six TRID-triggering data points are present. If five or fewer pieces exist, no Loan Estimate obligation arises—but once the sixth arrives, the three-business-day LE clock starts regardless of whether the borrower intended to formally apply. Pre-qualification with five data points does not trigger LE delivery; pre-approval with all six does.

**2. Product-Regulatory Mapping**
Map the loan product to its regulatory coverage: closed-end purchase loans, refinances, and construction loans fall under TRID. HELOCs follow Regulation Z §1026.40 separately. Reverse mortgages use legacy HUD-1 and TIL disclosures. Chattel-secured manufactured housing loans not attached to real property receive TIL but not RESPA coverage.

**3. Fee Classification and Tolerance Analysis**
Classify every fee into the correct tolerance bucket at initial LE issuance:
- **Zero tolerance**: Fees paid to the creditor, broker, or any affiliate; transfer taxes; fees for services where the consumer cannot shop
- **10% tolerance (aggregate)**: Third-party fees for services the consumer can shop for but selects a provider from the lender's Service Provider List (SPL)
- **Unlimited tolerance**: Prepaid interest, property insurance premiums, initial escrow deposits, fees for services the consumer shopped for using a provider NOT on the SPL

**4. Changed Circumstance Discipline**
A revised LE can only reset tolerances under six specific triggering events: changed circumstance affecting settlement charges, changed circumstance affecting eligibility, borrower-requested change, rate lock after initial LE, expiration of the original LE, or delayed settlement on construction loans. Each must be documented contemporaneously—the most common audit finding is failure to document the changed circumstance before issuing the revised LE.

**5. Underwriting Alignment Check**
Verify ATR/QM compliance: confirm income and debt verification using reasonably reliable third-party records, calculate DTI or assess residual income per institutional policies, and check the loan's APR against APOR thresholds. For safe-harbor QM status, APR must not exceed APOR by more than 1.50 percentage points (2.25 for rebuttable presumption).

## Step-by-Step Process

### Phase 1: Application Intake (Days 1-3)
1. Receive borrower's six data points; timestamp receipt of the sixth element
2. Pull credit report using SSN; document authorization under FCRA
3. Generate initial Loan Estimate within three business days of application receipt
4. Provide the Service Provider List (SPL) simultaneously with the LE
5. Deliver the CFPB homeownership counseling list (obtained no earlier than 30 days prior)
6. Deliver the Special Information Booklet for purchase transactions (12 CFR §1024.19(g))
7. Obtain and document borrower's "intent to proceed" before collecting any fees beyond the credit report fee

### Phase 2: Documentation & Processing (Days 4-21)
8. Collect income documentation: W-2s, tax returns, pay stubs, 1099s
9. Verify employment; document self-employment with two years of tax returns
10. Collect asset documentation: bank statements (full statements, all pages), investment accounts
11. Review liabilities against credit report; reconcile undisclosed debts
12. Order title search; review preliminary title commitment for liens, easements, encumbrances
13. Verify property insurance adequacy including flood determination (NFIP requirements)
14. If rate locks, document lock date and expiration; issue revised LE if lock changes disclosed terms

### Phase 3: Appraisal & Valuation (Days 10-25)
15. Order appraisal through compliant channel (no direct borrower-appraiser contact for HPML loans)
16. Ensure appraiser holds state certification/license for the property's jurisdiction
17. Review appraisal for USPAP compliance, adequate comparable selection, and condition/marketability adjustments
18. For higher-priced mortgage loans (HPML), obtain a second appraisal if the property was sold within 180 days at a price materially lower than current (12 CFR §1026.35(c))
19. If using AVMs for evaluations (not full appraisals), ensure institutional AVM quality control policies meet the interagency final rule standards effective October 1, 2025
20. Deliver appraisal copy to borrower promptly upon completion, or at least three business days before consummation (12 CFR §1026.35(c)(6))

### Phase 4: Underwriting Decision (Days 20-30)
21. Submit complete file to underwriting with ATR/QM analysis worksheet
22. Verify DTI calculation: total monthly debt obligations / gross monthly income
23. Document compensating factors if DTI exceeds institutional thresholds
24. Clear all underwriting conditions; obtain final approval with condition clearance documentation
25. If denied: issue adverse action notice within 30 days of completed application per Regulation B (12 CFR §1002.9), including specific denial reasons and ECOA anti-discrimination notice

### Phase 5: Pre-Closing & Closing Disclosure (Days 25-35)
26. Prepare Closing Disclosure with final loan terms, fees, and cash-to-close
27. Deliver CD to borrower at least three business days before consummation
28. If hand-delivered: three calendar days before closing. If mailed (USPS first class): six calendar days before closing (three-day mailbox presumption + three-day review)
29. Verify CD-to-LE fee tolerance compliance across all three buckets; cure any overages before closing
30. Confirm no changes triggering a new three-day waiting period (APR accuracy, product change, prepayment penalty addition)

### Phase 6: Closing & Post-Closing
31. Coordinate closing with settlement agent; verify settlement agent provides seller's CD
32. Execute note, mortgage/deed of trust, and all required closing documents
33. Fund the loan; record the mortgage with county recorder
34. Complete HMDA data entry: verify all 48+ data fields for accuracy (action taken, loan type, property type, ethnicity, race, sex, income, DTI, CLTV, rate spread, etc.)
35. Submit to post-closing QC within 90 days; re-verify income, employment, and occupancy on a sample basis

## Evaluation Criteria

| Metric | Target | Critical Threshold |
|--------|--------|--------------------|
| LE delivery timeliness | 100% within 3 business days | <95% triggers corrective action |
| CD delivery timeliness | 100% within 3 business days pre-closing | Any miss = potential TRID violation |
| Fee tolerance cure rate | 0% uncured tolerance violations at closing | Any uncured = regulatory finding |
| HMDA data accuracy | >99% field-level accuracy | Error rates >5% on key fields = exam citation |
| Adverse action notice timing | 100% within 30 days of completed application | Missed = Regulation B violation |
| Appraisal delivery to borrower | 100% ≥3 days before consummation | Missed = ECOA violation |
| Intent to proceed documentation | 100% documented before fee collection | Undocumented = TRID violation |
| Post-closing QC defect rate | <5% of sampled loans | >10% defects = systemic control failure |
| Application-to-close cycle time | ≤45 days (purchase), ≤35 days (refi) | >60 days = operational concern |

## Red Flags & Edge Cases

1. **Same-date LE and CD issuance**: Producing both the Loan Estimate and Closing Disclosure with the same issue date creates a compliance issue—the CD cannot logically precede or coincide with the LE. This persists as a top finding in TRID audits (CrossCheck Compliance, 2025).

2. **Missing SPL causing fee misclassification**: If the Service Provider List is not delivered within three business days alongside the LE, all title-related and third-party fees default to zero-tolerance classification instead of 10%-tolerance, dramatically increasing cure liability.

3. **Undocumented changed circumstances**: Processors issue revised LEs to reset fee tolerances but fail to retain contemporaneous documentation of the triggering event. Without a documented borrower request, rate lock change, or eligibility change, the revised LE does not reset tolerances—the original LE governs.

4. **HMDA data field errors on repeat**: Freedom Mortgage paid $3.95 million in 2024 for widespread HMDA data errors across multiple fields—a repeat offense following a 2019 consent order for similar violations. Systemic failures in data capture at application intake propagate errors institution-wide.

5. **Redlining through branch location patterns**: Draper and Kramer Mortgage Corporation faced ECOA/CFPA enforcement in 2025 for locating all offices in majority-white neighborhoods and avoiding marketing to majority-Black and Hispanic areas. Office placement and marketing geography generate fair lending exposure independent of individual loan decisions.

6. **RESPA Section 8 kickback schemes via MSAs**: Prospect Mortgage paid $3.5 million for funneling kickbacks through Marketing Services Agreements (MSAs) to real estate brokers in exchange for mortgage referrals. Any payment to a referral source that exceeds the fair market value of services actually rendered violates Section 8(a).

7. **Lender credit decrease without valid changed circumstance**: Once a lender credit is disclosed on the LE, it cannot decrease unless tied to a valid change in circumstance. Reducing a lender credit between LE and CD without documented justification creates a zero-tolerance violation.

8. **Construction loan TRID coverage gap**: Both construction-only and construction-permanent loans are TRID-covered if they meet general coverage requirements (Comment 17(c)(6)-2). Processors who treat construction draws as exempt from disclosure requirements create significant compliance gaps.

9. **Appraisal independence violations on HPMLs**: For higher-priced mortgage loans, creditors, loan originators, and their affiliates cannot compensate appraisers based on loan approval, or coerce appraisers to hit target values. Prior-sale flipping triggers (sale within 180 days at lower price) mandate a second independent appraisal.

10. **Borrower financial changes between approval and closing**: Lenders re-verify income and re-pull credit before funding. New credit accounts, large deposits without documentation, employment changes, or balance increases between conditional approval and closing can void approval, requiring full re-underwriting.

11. **Electronic CD delivery without E-SIGN compliance**: Delivering the Closing Disclosure electronically requires full E-SIGN Act compliance—consumer consent, ability to withdraw consent, hardware/software disclosure. Emailing a CD PDF without these safeguards does not satisfy the delivery requirement and the three-day clock does not start.

12. **Incomplete application adverse action timing trap**: If a creditor holds an incomplete application beyond 30 days without sending either a notice of incompleteness or an adverse action notice, it violates Regulation B timing requirements regardless of the application's ultimate outcome.

## Common Mistakes

1. **Collecting fees before intent to proceed**: TRID prohibits collecting any fee (beyond credit report) before the borrower documents intent to proceed after receiving the LE. Processors who collect appraisal deposits at application before LE delivery violate 12 CFR §1026.19(e)(2)(i)(A).

2. **Using inconsistent disclosure formats**: Switching between standard and alternative TRID disclosure formats within a single transaction creates a compliance violation. Choose one format at LE issuance and maintain it through the CD.

3. **Failing to provide LE on denied/withdrawn applications**: If the six TRID data points were received, an LE must be issued within three business days even if the loan is subsequently denied or withdrawn—unless the denial or withdrawal occurs within the same three-day window. Many processors skip LE generation for applications they know will not proceed.

4. **Misreporting HMDA "Not Applicable" fields**: Reporting "NA" for income when the borrower's income influenced the credit decision in any way—even as a non-dispositive factor—is an error. If a co-borrower's income was considered, it must be reported even if the primary borrower is an entity.

5. **Omitting the expiration date on initial LE**: The initial LE must include an expiration date for the estimated closing costs (10 business days is standard). Revised LEs should not carry an expiration date—including one on a revised LE is a distinct TRID error.

6. **Inadequate flood determination documentation**: Failing to obtain or retain Standard Flood Hazard Determination Forms (SFHDF) for properties in FEMA-designated flood zones, or not ensuring flood insurance is escrowed when other insurance must be escrowed, creates both regulatory and GSE salability exposure.

7. **Neglecting seller's Closing Disclosure**: Settlement agents must provide a CD to the seller, and a copy to the lender if borrower/seller information appears on separate forms. Many agents substitute HUD-1 or ALTA settlement statements, which are not acceptable CD substitutes.

8. **Overestimating fees as a tolerance buffer**: Some originators deliberately overestimate fees on the LE to build tolerance cushion, then refund the difference at closing. While technically compliant, this practice can make the lender uncompetitive and, if done systematically with no genuine good-faith basis, may draw examiner scrutiny as inconsistent with the good-faith standard.

## Regulatory & Compliance Requirements

### Federal Statutes and Implementing Regulations

| Regulation | Citation | Requirement |
|------------|----------|-------------|
| **TRID (Loan Estimate/Closing Disclosure)** | 12 CFR §1026.19(e), (f), (g); §1026.37; §1026.38 | Timing, content, and delivery of LE and CD for closed-end mortgage loans |
| **Regulation X (RESPA)** | 12 CFR Part 1024 | Settlement procedures, escrow requirements, servicing transfers, anti-kickback (§8) |
| **Regulation Z (TILA)** | 12 CFR Part 1026 | APR disclosure, right of rescission (refinances), HPML protections, loan originator compensation |
| **ATR/QM Rule** | 12 CFR §1026.43 | Ability-to-repay determination; QM safe harbor and rebuttable presumption categories |
| **Regulation B (ECOA)** | 12 CFR Part 1002 | Prohibition against credit discrimination; adverse action notice within 30 days; appraisal copy delivery |
| **Regulation C (HMDA)** | 12 CFR Part 1003 | Collection and reporting of 48+ mortgage application data fields annually |
| **HPML Appraisal Requirements** | 12 CFR §1026.35(c) | Mandatory appraisal by certified appraiser; second appraisal for recent flips |
| **AVM Quality Control Standards** | 12 CFR §1026.42 (effective 10/1/2025) | Policies ensuring AVM accuracy, fair lending compliance, and nondiscrimination |
| **Flood Insurance (NFIP)** | 42 USC §4012a; Regulation H (12 CFR 208.25) | Mandatory flood insurance for properties in Special Flood Hazard Areas |
| **FCRA** | 15 USC §1681 | Permissible purpose for credit pulls; adverse action notice when credit report data informs denial |
| **SAFE Act / NMLS** | 12 USC §5101 | Loan originator licensing/registration through NMLS |

### Key Compliance Timelines

- **Loan Estimate**: Deliver within 3 business days of application (receipt of 6th data element)
- **Closing Disclosure**: Borrower must receive ≥3 business days before consummation
- **Revised CD (material change)**: New 3-day waiting period for APR change >1/8%, product change, or prepayment penalty addition
- **Adverse Action Notice**: Within 30 days of completed application or action on incomplete application
- **Appraisal Copy to Borrower**: Promptly upon completion, or ≥3 business days before consummation
- **Homeownership Counseling List**: Within 3 business days of application
- **HMDA Annual Filing**: By March 1 for prior calendar year data
- **Right of Rescission (Refinance)**: 3 business days post-consummation; midnight of third business day

## Terminology

1. **Loan Estimate (LE)**: Three-page TRID disclosure form provided within three business days of application, itemizing estimated loan terms, projected payments, and closing costs under standardized format requirements (12 CFR §1026.37).

2. **Closing Disclosure (CD)**: Five-page TRID form replacing the HUD-1 and final TIL, delivered at least three business days before consummation, showing final loan terms, closing costs, and cash-to-close (12 CFR §1026.38).

3. **Fee Tolerance**: The permissible variance between fees disclosed on the LE and fees actually charged at closing. Three buckets: zero tolerance (no increase permitted), 10% aggregate tolerance, and unlimited tolerance.

4. **Changed Circumstance**: A specific triggering event—such as a borrower-requested change, new information, or rate lock—that permits the creditor to issue a revised LE and reset fee tolerances. Must be documented contemporaneously.

5. **Consummation**: The point at which the borrower becomes contractually obligated on the mortgage note. Not synonymous with "closing" or "settlement" in all states—some states define consummation at document signing, others at funding.

6. **Application (TRID Definition)**: Receipt of six specific data elements: borrower name, income, SSN, property address, estimated property value, and mortgage loan amount sought. Broader RESPA and Regulation B definitions differ.

7. **Qualified Mortgage (QM)**: A mortgage meeting specific product feature restrictions, points-and-fees limits, and underwriting requirements under 12 CFR §1026.43(e), affording the creditor either safe harbor or rebuttable presumption protection against ATR liability.

8. **Average Prime Offer Rate (APOR)**: Weekly survey-derived benchmark rate published by the CFPB representing prevailing rates for prime-quality mortgages. Used to determine QM pricing thresholds, HPML status, and HMDA rate-spread reporting.

9. **Higher-Priced Mortgage Loan (HPML)**: A closed-end consumer mortgage with an APR exceeding APOR by 1.5+ percentage points (first lien) or 3.5+ points (subordinate lien), triggering additional appraisal, escrow, and ability-to-repay requirements.

10. **Service Provider List (SPL)**: Written list of settlement service providers the lender allows the borrower to shop from for specific services. Delivery timing affects whether third-party fees fall into zero-tolerance or 10%-tolerance classification.

11. **RESPA Section 8**: Anti-kickback provision prohibiting any person from giving or receiving a fee, kickback, or thing of value in exchange for referral of settlement service business in connection with a federally related mortgage loan.

12. **Adverse Action Notice**: Written notification required under Regulation B (ECOA) and FCRA when a mortgage application is denied, providing specific reasons for denial, the ECOA anti-discrimination notice, and primary regulator contact information.

13. **Automated Valuation Model (AVM)**: Computerized model using public record data, statistical modeling, and comparable sales to estimate property value. Subject to new interagency quality control standards effective October 1, 2025 under 12 CFR §1026.42.

14. **USPAP (Uniform Standards of Professional Appraisal Practice)**: National standards governing real property appraisal practice, issued by the Appraisal Standards Board. Appraisals supporting federally related transactions must conform to USPAP.

15. **Rate Lock**: Commitment by the lender to hold a specific interest rate for a defined period. Locking or extending a rate can constitute a changed circumstance permitting revised LE issuance.

16. **Right of Rescission**: Three-business-day period after consummation during which a borrower may cancel a refinance transaction on their principal dwelling (12 CFR §1026.23). Does not apply to purchase money mortgages.

17. **HMDA Reportable Data**: The 48+ data fields that covered institutions must collect and report annually under Regulation C, including borrower demographics, loan characteristics, property information, pricing data, and underwriting factors.

18. **Escrow Account**: Account established by the servicer to hold borrower funds for payment of property taxes, insurance premiums, and other recurring charges. HPML rules require escrow accounts for at least five years.

19. **Points and Fees**: Specific charges that count toward QM thresholds, including origination charges, compensation to loan originators, and certain finance charges. For most loans, total points and fees cannot exceed 3% of the total loan amount for QM status.

20. **Loan Originator Compensation**: Regulation Z restricts how loan originators are paid: compensation cannot be based on loan terms or conditions (except loan amount), and dual compensation (from both consumer and creditor) is prohibited (12 CFR §1026.36).

21. **Trigger Lead**: A credit bureau product that identifies consumers who have had their credit pulled for a mortgage. Using trigger leads without permissible purpose violates FCRA; purchasing them for kickback arrangements violates RESPA Section 8.

22. **Good Faith Standard**: The TRID standard measuring disclosure accuracy—a fee is disclosed in good faith if the amount charged at closing does not exceed the amount disclosed, subject to applicable tolerance thresholds.

## Quality Checklist

- [ ] All six TRID application data points timestamped at receipt; LE generation clock tracked
- [ ] Loan Estimate delivered within three business days with SPL and homeownership counseling list
- [ ] Intent to proceed documented before any fee collection beyond credit report
- [ ] Every revised LE supported by contemporaneous changed circumstance documentation
- [ ] Fee tolerance analysis completed across all three buckets before CD preparation; overages identified and cured
- [ ] Closing Disclosure delivered ≥3 business days before consummation, with delivery method and receipt evidence documented
- [ ] APR accuracy verified on final CD (within 1/8% for regular, 1/4% for irregular payment loans)
- [ ] ATR/QM worksheet completed: income/debt verified via third-party records, DTI or residual income documented, pricing threshold checked against APOR
- [ ] Appraisal ordered through compliant channel; USPAP conformance verified; copy delivered to borrower ≥3 days pre-closing
- [ ] Adverse action notices sent within 30 days for all denied or incomplete applications, with specific reason codes and ECOA notice
- [ ] HMDA data fields verified for accuracy before annual submission (especially action taken, income, DTI, rate spread, ethnicity/race/sex)
- [ ] RESPA Section 8 compliance confirmed: no referral fees, kickbacks, or MSA arrangements lacking bona fide services
- [ ] Flood determination obtained; flood insurance secured and escrowed where required
- [ ] Post-closing QC completed on sampled loans within 90 days: income re-verification, occupancy check, compliance review
- [ ] All loan file documents retained per record retention requirements (minimum 3 years for TRID, 5 years for HMDA)

## References

1. CFPB TILA-RESPA Integrated Disclosure FAQs — https://www.consumerfinance.gov/compliance/compliance-resources/mortgage-resources/tila-respa-integrated-disclosures/tila-respa-integrated-disclosure-faqs/
2. CFPB TRID Resource Page — https://www.consumerfinance.gov/compliance/compliance-resources/mortgage-resources/tila-respa-integrated-disclosures/
3. CFPB ATR/QM Rule Resources — https://www.consumerfinance.gov/compliance/compliance-resources/mortgage-resources/ability-repay-qualified-mortgage-rule/
4. CFPB ATR/QM Small Entity Compliance Guide v3.1 — https://files.consumerfinance.gov/f/documents/cpfb_atr-qm_small-entity_compliance-guide.pdf
5. FDIC Regulation X Examination Manual — https://www.fdic.gov/consumer-compliance-examination-manual/v-3-real-estate-settlement-procedures-act-respa
6. OCC Regulation X Examination Procedures — https://www.occ.gov/news-issuances/bulletins/2015/bulletin-2015-27c.pdf
7. Federal Reserve Regulation X Procedures — https://www.federalreserve.gov/supervisionreg/caletters/ca_15-6_attach_reg_x.pdf
8. FFIEC 2024 HMDA Getting It Right Guide — https://www.ffiec.gov/sites/default/files/data/hmda/2024Guide.pdf
9. Federal Reserve Consumer Compliance Outlook: Top HMDA Violations 2024 — https://www.consumercomplianceoutlook.org/2025/first-issue/top-federal-reserve-system-compliance-violations-in-2024-home-mortgage-disclosure-act
10. CFPB Enforcement Actions Page — https://www.consumerfinance.gov/enforcement/actions/
11. Goodwin: CFPB Settles with Freedom Mortgage for $4M (HMDA) — https://www.goodwinlaw.com/en/insights/blogs/2024/06/cfpb-settles-with-nonbank-mortgage-originator-for-$4-million
12. Hudson Cook: CFPB 2024 Annual Review (Mortgage) — https://www.hudsoncook.com/article/cfpb-bites-of-the-month-2024-annual-review-mortgage-2/
13. Interagency AVM Final Rule (89 FR 64,538, August 2024) — https://www.federalregister.gov/documents/2024/08/07/2024-16197/quality-control-standards-for-automated-valuation-models
14. CFPB AVM Final Rule Fast Facts — https://files.consumerfinance.gov/f/documents/cfpb_avm-final-rule-fast-facts_2024-07.pdf
15. Mayer Brown: AVM Rule Effective October 2025 — https://www.mayerbrown.com/en/insights/publications/2025/10/mortgage-originators-and-secondary-market-participants-take-note-the-final-rule-on-automated-valuation-models-is-now-effective-and-could-apply-to-you
16. ALTA: Closing Disclosure Three-Day Rule — https://www.alta.org/blog/post/how-to-comply-with-the-closing-disclosures-three-day-rule
17. CrossCheck Compliance: TRID Common Errors 2025 — https://crosscheckcompliance.com/resources/industry-insights/trid-guidelines/
18. CrossCheck Compliance: Eight Common TRID Errors — https://crosscheckcompliance.com/resources/articles/tila-respa-trid-errors/
19. Anders CPA: TRID Tolerance Buckets — https://anderscpa.com/learn/blog/mastering-trid-tolerance-buckets-avoid-penalties-from-these-common-errors/
20. Ncontracts: Mortgage Lending Regulatory Update 2025 — https://www.ncontracts.com/nsight-blog/mortgage-lending-regulatory-update
21. Consumer Compliance Outlook: Adverse Action Notice Requirements — https://www.consumercomplianceoutlook.org/2013/second-quarter/adverse-action-notice-requirements-under-ecoa-fcra/
22. America's Credit Unions: RESPA Anti-Kickback Provisions — https://www.americascreditunions.org/blogs/compliance/respas-anti-kickback-provisions
23. Venable: CFPB RESPA Enforcement (Prospect Mortgage) — https://www.venable.com/insights/publications/2017/03/cfpb-respa-enforcement-alive-and-kickbacking
24. CFPB Fair Lending Report 2024 — https://files.consumerfinance.gov/f/documents/cfpb_fair-lending-annual-report_2025-12.pdf
25. Wipfli: Disparate Impact Enforcement Shifts 2025 — https://www.wipfli.com/insights/articles/changing-disparate-impact-enforcement-creates-new-compliance-challenges-for-lenders
26. Ncontracts: Fair Lending in 2026 — https://www.ncontracts.com/nsight-blog/fair-lending-update
27. Asurity: TRID Timing Requirements Refresher — https://www.asurity.com/blogs/trid-refresher-series-part-2-understanding-trid-timing-requirements-for-disclosures-on-mortgage-transactions/
28. CFPB Closing Disclosure Explainer — https://www.consumerfinance.gov/owning-a-home/closing-disclosure/
29. Orchestrate: TRID, HMDA, and RESPA Workflow — https://www.orchestrate.com/blog/what-trid-hmda-and-respa-mean-for-your-mortgage-workflow/
30. Texas SML: 2024 Mortgage Industry Day Rule Updates — https://www.sml.texas.gov/wp-content/uploads/2024/11/2024MID-4-New-Rule-Update-Mortgage-Industry-Day-11-04-2024.pdf