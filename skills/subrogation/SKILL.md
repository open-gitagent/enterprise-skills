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

# Subrogation

## Domain Overview

Subrogation is the legal mechanism by which an insurer that has indemnified its insured for a loss "steps into the shoes" of that insured to pursue recovery from the responsible third party. The doctrine originates in equity and operates across every major insurance line — auto physical damage, general liability, property, health, and workers' compensation. In 2023 alone, Arbitration Forums, Inc. (the nation's largest intercompany arbitration provider) processed over 1.1 million arbitration disputes and nearly 2.4 million subrogation demands collectively worth over $26.4 billion. The financial impact on carrier loss ratios is material: the P&C industry has historically reported a recovery ratio (salvage and subrogation recovered as a percentage of paid losses) of approximately 5.16% industry-wide, with personal lines carriers achieving 6.73% and top-performing carriers reaching 8.81%.

Subrogation rights derive from three sources: equitable (arising by operation of law when an insurer pays a loss caused by a third party), conventional/contractual (created by express policy language granting the insurer recovery rights), and statutory (established by state or federal statute, such as PIP subrogation statutes or the Medicare Secondary Payer Act). The source of the right determines which legal doctrines govern — the made-whole doctrine, anti-subrogation rule, and ERISA preemption all hinge on whether the right is equitable, contractual, or statutory. This three-source distinction is the single most critical analytical starting point for any subrogation professional.

The regulatory landscape is intensely state-specific. Each of the 50 states has developed its own body of case law and statutory frameworks governing when and how subrogation may be exercised. The NAIC Unfair Claims Settlement Practices Act (MDL-900), adopted by nearly every state in some form, establishes minimum standards for claims investigation and settlement that directly constrain subrogation activity. Federal overlay through ERISA §502(a)(3) governs self-funded health plan subrogation, while the Medicare Secondary Payer Act (42 U.S.C. §1395y(b)) and MMSEA Section 111 reporting requirements impose mandatory obligations on all carriers settling claims involving Medicare beneficiaries. Failure to comply with Section 111 reporting exposes carriers to penalties of $1,000 per day of non-compliance per beneficiary.

NAIC Annual Statement reporting requires insurers to report salvage and subrogation in Schedule P (Parts 1-4), where recovery data appears in Column 10 as a memorandum item. Under SSAP No. 55, companies may elect to report reserves net or gross of anticipated salvage and subrogation for statutory reporting, though GAAP and tax reporting require net-of-anticipated-recovery treatment. The 2024 NAIC revision to Schedule P now requires ten years of development data for all lines, affecting how composite discount factors are calculated under IRS §846.

## Core Decision Framework

Practitioners evaluate subrogation opportunities through a five-stage decision tree:

**1. Source Identification** — Determine whether the right arises from equity, contract, or statute. Contractual subrogation provisions in policy language (conventional subrogation) are generally enforceable as written, but equitable subrogation is subject to judicial limitations. Statutory subrogation (e.g., workers' compensation, PIP) follows the specific state statute's terms.

**2. Jurisdiction-Specific Doctrine Assessment** — Three doctrines control:
- **Made-Whole Doctrine**: The majority of states require the insured to be fully compensated before the insurer may assert subrogation. States split on whether contract language can override this doctrine. Arkansas, Alabama, and West Virginia hold the doctrine applies even when contractual language says otherwise. Indiana, Ohio, and others allow clear, unambiguous policy language to displace it. Colorado codified the doctrine at C.R.S. §10-1-135 effective August 2010.
- **Anti-Subrogation Rule (ASR)**: An insurer cannot subrogate against its own insured, co-insured, or additional insured under the same policy. The ASR extends to implied co-insureds (e.g., tenants in landlord-tenant contexts under the Sutton Doctrine). Exceptions exist for intentional acts (LaSalle Nat. Bank), cross-policy scenarios (Benge), and situations where the policy explicitly excludes coverage for the loss.
- **ERISA Preemption**: For self-funded employer health plans, ERISA preempts all state laws including the made-whole doctrine. *US Airways v. McCutchen*, 133 S.Ct. 1537 (2013), held that clear plan language governs, but where the plan is silent (e.g., on attorney fee allocation), equitable common-fund principles fill the gap. *Montanile v. Board of Trustees*, 136 S.Ct. 651 (2016), further defined the limits of equitable relief available to plans.

**3. Recovery Viability Analysis** — Assess the responsible party's insurance status, policy limits, assets, and the economic viability of pursuit. For property claims under $100,000, intercompany arbitration through Arbitration Forums is mandatory when both carriers are signatories. Claims exceeding $100,000 or involving non-signatory parties require litigation.

**4. Preservation of Rights** — Identify and docket the applicable statute of limitations (ranging from 1 to 6 years depending on jurisdiction and cause of action), statute of repose (particularly for product liability and construction defect claims), and any contractual notice requirements. Conflict-of-law analysis is required whenever multiple states are involved.

**5. Medicare/Federal Compliance Check** — For any claim involving a Medicare beneficiary, verify Section 111 MMSEA reporting obligations, resolve conditional payment claims through the BCRC (Benefits Coordination & Recovery Center), and assess Medicare Set-Aside requirements for workers' compensation settlements.

## Step-by-Step Process

### Phase 1: Claim Identification & Triage
1. Review first notice of loss (FNOL) for third-party liability indicators
2. Flag claims with subrogation potential during initial adjuster investigation
3. Code claim with subrogation status indicator in claims management system
4. Determine applicable state law and whether conflict-of-law analysis is needed
5. Check whether the responsible party or its carrier is an Arbitration Forums signatory

### Phase 2: Investigation & Documentation
6. Secure evidence preservation — photographs, physical evidence, police/fire reports
7. Obtain statements from insured, witnesses, and (if possible) the responsible party
8. Engage experts as needed (origin-and-cause for fire, engineering for product defect, accident reconstruction for auto)
9. Document insured's total loss including uninsured/underinsured components for made-whole analysis
10. Verify whether any waiver of subrogation exists in underlying contracts (construction, lease)

### Phase 3: Demand & Negotiation
11. Issue subrogation demand letter to responsible party and/or their insurer
12. Include paid amounts, deductible recovery component, and supporting documentation
13. For intercompany disputes, file through Arbitration Forums E-Subro Hub within applicable deadlines
14. Negotiate liability allocation percentages and damage amounts
15. Track comparative/contributory negligence implications by jurisdiction

### Phase 4: Escalation & Resolution
16. If demand is denied or contested, evaluate arbitration vs. litigation path
17. For Arbitration Forums filings: prepare contentions, attach documentation, meet filing deadlines
18. For litigation: retain subrogation counsel, file within statute of limitations, manage discovery
19. For ERISA claims: pursue under §502(a)(3) equitable relief framework
20. Resolve and close — distribute recovered amounts (carrier reimbursement, deductible return to insured)

### Phase 5: Compliance & Reporting
21. Report recovery in Schedule P per NAIC Annual Statement Instructions
22. Complete Section 111 MMSEA reporting for Medicare beneficiary claims
23. Refund insured's deductible from recovery proceeds per state requirements
24. Update loss reserves to reflect recovery and adjust IBNR as appropriate

## Evaluation Criteria

| Metric | Benchmark | Top Performer |
|--------|-----------|--------------|
| Recovery Ratio (S&S / Net Paid Losses) | 5.16% industry-wide | 8.81%+ |
| Auto Physical Damage Recovery Ratio | 18-22% | 24%+ |
| Auto Liability Recovery Ratio | 1.0-2.0% | 2.5%+ |
| Average Days to Recovery (Physical Damage) | Within 2 years | < 12 months |
| Average Days to Recovery (Liability) | Within 9 years | < 5 years |
| Subrogation Success Rate | 60-70% | 80%+ |
| Arbitration Win Rate | 55-65% | 75%+ |
| Deductible Recovery Rate | 50-60% | 80%+ |
| Statute of Limitations Compliance | 98% | 100% |
| Section 111 Reporting Compliance | 100% required | 100% |

## Red Flags & Edge Cases

1. **Waiver of Subrogation in Construction Contract**: An insured's commercial property claim stems from contractor negligence, but the lease or construction contract contains a waiver-of-subrogation clause (common in AIA Document A201-2017, §11.3). The carrier's subrogation right is extinguished even though the insured did not inform the carrier of the waiver. Court precedent (*Ace American Insurance Co. v. American Medical Plumbing*, NJ 2019) enforced waivers covering nearly $1.2 million in damages.

2. **Same-Carrier Cross-Policy Subrogation**: The insured's homeowner carrier and the tortfeasor's auto carrier are the same company. Minnesota statute §60A.41(b) bars subrogation "for the same loss by the same company." Some states allow cross-policy subrogation; others do not. *Schmuckler v. Creurer* (Minn.) barred it; *Benge* (Ill.) allowed it.

3. **ERISA Self-Funded Plan with Ambiguous Reimbursement Language**: A self-funded employer plan seeks subrogation after an auto accident settlement, but the plan document fails to address attorney fee allocation. Under *McCutchen*, the common-fund doctrine applies by default, reducing recovery by the proportionate share of attorney fees — potentially 33-40% of the gross recovery.

4. **Medicare Beneficiary Settlement Without Section 111 Reporting**: A carrier settles a liability claim for a 67-year-old claimant without querying Medicare eligibility. CMS later issues a conditional payment recovery demand plus $1,000/day penalties under MMSEA Section 111. The carrier faces both the reimbursement obligation and cumulative daily fines.

5. **Statute of Limitations Expired Due to Conflict-of-Law Error**: A loss occurs in Florida (2-year negligence SOL, recently reduced from 4 years) but the insured resides in Ohio (4-year SOL). Subrogation counsel applies the Ohio deadline, but Florida's borrowing statute mandates applying the shorter limitation period. The claim is time-barred.

6. **Implied Co-Insured Tenant Blocks Subrogation (Sutton Doctrine)**: A landlord's property insurer attempts to subrogate against a tenant who negligently caused a fire. Under the Sutton Doctrine (applied in ~30 states), if a portion of rent payments funds the landlord's property insurance premiums, the tenant is deemed an implied co-insured, and the anti-subrogation rule bars recovery.

7. **Insured Settles Directly with Tortfeasor, Impairing Subrogation Rights**: The insured accepts a general release from the at-fault party before the carrier can pursue subrogation. The insured's duty to cooperate and protect subrogation interests was in the policy, but the carrier failed to notify the insured of its subrogation claim. Recovery against the insured for impairment may be limited.

8. **Product Liability Subrogation Barred by Statute of Repose**: A residential fire caused by a 12-year-old water heater triggers a property claim. Indiana's product liability statute of repose (IC §34-20-3-1) bars claims for products delivered more than 10 years prior. The subrogation claim against the manufacturer is extinguished regardless of the negligence evidence.

9. **Arbitration Forums Filing After Respondent Withdraws**: A carrier files an auto physical damage subrogation claim through Arbitration Forums, but the respondent carrier withdraws before hearing after asserting no coverage. Under AF rules, once withdrawn, the filing carrier may need to pursue litigation, but the arbitration filing may have consumed critical SOL time.

10. **Workers' Compensation Subrogation in No-Fault State**: A workers' compensation carrier in Michigan (no-fault auto state) attempts to subrogate against the at-fault driver's auto insurer. Michigan's no-fault statute limits recovery rights to excess economic damages above the PIP threshold. Navigating the interplay between WC subrogation and no-fault requires jurisdiction-specific expertise.

11. **Dual-Coverage Subrogation Dispute**: Two carriers insure the same loss under concurrent policies. Neither can agree on primary/excess allocation. The Special Arbitration Agreement through Arbitration Forums mandates compulsory arbitration for signatories in concurrent-coverage disputes, but the filing carrier must identify this as a Special Forum rather than standard property subrogation.

12. **Health Insurer Subrogation Against Insured's UM/UIM Recovery**: A health insurer asserts subrogation against proceeds from the insured's own uninsured/underinsured motorist claim. Several states (e.g., California, Virginia) restrict or prohibit health insurer subrogation against UM/UIM proceeds on public policy grounds.

## Common Mistakes

1. **Failing to docket statute of limitations at FNOL**: Subrogation potential is identified months later, but the SOL has run or is critically short. Best practice: docket SOL at first recognition of third-party liability, using the shortest potentially applicable limitations period.

2. **Applying home-state law without conflict-of-law analysis**: The loss occurred in a different state than the insured's residence. Most jurisdictions apply the law of the state where the injury/damage occurred (lex loci delicti), but contract-based subrogation may follow the policy's choice-of-law provision.

3. **Pursuing subrogation before insured is made whole**: In made-whole-doctrine states, premature subrogation pursuit can void the carrier's right to recovery entirely. A judicial determination may be required in some jurisdictions (e.g., Arkansas under *Riley*).

4. **Ignoring deductible recovery obligation**: Many state regulations and policy provisions require carriers to include the insured's deductible in the subrogation demand and return recovered deductible funds. Failure to pursue deductible recovery can constitute an unfair claims practice under NAIC MDL-900/902.

5. **Filing intercompany arbitration for claims exceeding $100,000**: Arbitration Forums standard jurisdiction caps at $100,000 unless all parties consent. Filing an overlimit claim wastes time and may prejudice later litigation.

6. **Not verifying waiver-of-subrogation provisions in underlying commercial contracts**: Construction, lease, and service contracts routinely contain mutual waivers. The policy file rarely contains these contracts. Proactive inquiry at FNOL prevents wasted investigation costs.

7. **Neglecting to query Medicare eligibility before settlement**: CMS enforces Section 111 reporting rigorously. Carriers must determine Medicare beneficiary status using the Coordination of Benefits Secure Website before settling any claim.

8. **Treating ERISA plan subrogation identically to insured-plan subrogation**: Self-funded ERISA plans are governed exclusively by federal law; state made-whole and common-fund doctrines apply only where plan language is silent. Insured plans remain subject to state insurance regulation per FMC Corp. v. Holliday.

## Regulatory & Compliance Requirements

### Federal Statutes & Regulations
- **ERISA §502(a)(3)** (29 U.S.C. §1132(a)(3)): Authorizes plan fiduciaries to pursue "appropriate equitable relief" for subrogation/reimbursement from self-funded plan participants. *US Airways v. McCutchen*, 133 S.Ct. 1537 (2013) is the controlling Supreme Court precedent.
- **ERISA §514(a)** (29 U.S.C. §1144(a)): Preempts state laws that "relate to" ERISA plans, including state-law made-whole doctrines for self-funded plans. *FMC Corp. v. Holliday*, 498 U.S. 52 (1990) confirmed the deemer clause protects self-funded plans from state regulation.
- **Medicare Secondary Payer Act** (42 U.S.C. §1395y(b)): Establishes Medicare's right to recover conditional payments from primary payers, including liability, no-fault, and workers' compensation insurers.
- **MMSEA Section 111** (P.L. 110-173, §111): Imposes mandatory reporting requirements on Responsible Reporting Entities (RREs). Penalties: $1,000/day per unreported beneficiary. Effective dates: GHP reporting January 1, 2009; NGHP reporting July 1, 2009.
- **IRS §832 and §846**: Govern tax treatment of discounted unpaid losses and salvage/subrogation recoverables. Rev. Proc. 2025-15 provides current-year discount factors.

### NAIC Model Laws & Regulations
- **MDL-900**: Unfair Claims Settlement Practices Act — Sections 3-4 prohibit unfair claims practices including failure to promptly investigate, failure to affirm or deny coverage within reasonable time, and misrepresenting policy provisions. Applies to subrogation-related claims handling.
- **MDL-902**: Unfair Property/Casualty Claims Settlement Practices Model Regulation — §7 establishes standards for prompt, fair, and equitable settlement. §7(A) requires acknowledgment within 21 days. Deductible recovery is an implied obligation.
- **MDL-903**: Unfair Life, Accident and Health Claims Settlement Practices Model Regulation — Parallel standards for health insurance claims affecting health subrogation practices.
- **SSAP No. 55**: Unpaid Claims, Losses, and Loss Adjustment Expenses — Governs accounting treatment of anticipated salvage and subrogation in statutory financial statements.

### State-Specific Key Statutes (Selected)
- **Colorado C.R.S. §10-1-135** (2010): Codifies made-whole doctrine for all insurance subrogation.
- **Ohio Rev. Code §2323.44**: Modifies health insurer subrogation by requiring proportionate sharing when insured cannot collect full value.
- **Florida Stat. §95.11**: Negligence SOL reduced from 4 to 2 years effective March 2023, directly impacting subrogation deadlines.
- **Minnesota Stat. §60A.41(b)**: Bars same-company subrogation "for the same loss."

## Terminology

1. **Equitable Subrogation**: Subrogation rights arising by operation of law when an insurer pays a loss caused by a third party; subject to equitable defenses including the made-whole doctrine.
2. **Conventional Subrogation**: Subrogation rights created by express language in the insurance policy contract; generally enforceable as written, though subject to state-specific limitations.
3. **Made-Whole Doctrine**: Equitable principle requiring an insured to be fully compensated for all damages before the insurer may exercise subrogation. Applied as default rule in the majority of states.
4. **Anti-Subrogation Rule (ASR)**: Legal prohibition against an insurer pursuing subrogation against its own insured, co-insured, or additional insured under the same policy. Also called the "suing your own insured" defense.
5. **Sutton Doctrine**: Extension of the ASR in landlord-tenant contexts where the tenant is deemed an implied co-insured because rent payments partially fund the landlord's property insurance premium.
6. **Intercompany Arbitration**: Binding dispute resolution between insurance carriers that are signatories to Arbitration Forums, Inc. agreements. Mandatory for auto physical damage and property subrogation claims under $100,000.
7. **Arbitration Forums, Inc. (AF)**: Not-for-profit organization (founded 1943) providing intercompany arbitration and subrogation services to over 5,400 member companies. Operates the E-Subro Hub electronic demand platform.
8. **E-Subro Hub**: Arbitration Forums' electronic platform for sending, receiving, and managing intercompany subrogation demands and escalating to arbitration.
9. **Responsible Reporting Entity (RRE)**: Under MMSEA Section 111, any insurer, self-insured entity, or TPA required to report claim information to CMS for Medicare beneficiaries.
10. **Conditional Payment**: Medicare payment made for a beneficiary's medical expenses that is subject to recovery by CMS when a primary payer (liability, no-fault, or WC insurer) is identified.
11. **BCRC (Benefits Coordination & Recovery Center)**: CMS contractor responsible for recovering conditional payments and processing Section 111 data for non-group health plans.
12. **Waiver of Subrogation**: Contractual provision in which the insured agrees to release the insurer's subrogation rights against a specified third party; common in construction contracts (AIA A201 §11.3) and commercial leases.
13. **Statute of Repose**: Absolute time limit barring claims based on the age of a product or completion of construction, regardless of when the loss occurs. Distinguished from statute of limitations, which runs from the date of loss.
14. **Salvage**: Recovery from the sale of damaged property after a claim has been paid. Reported alongside subrogation in NAIC Schedule P, Column 10.
15. **Recovery Ratio**: Salvage and subrogation recovered divided by net claims paid; the primary KPI for measuring subrogation program effectiveness.
16. **Collateral Source Rule**: Tort law doctrine preventing reduction of a plaintiff's damages based on payments received from independent sources (including insurance). Affects subrogation by protecting the insured's recovery from the tortfeasor.
17. **Common Fund Doctrine**: Equitable principle requiring a party who recovers a fund benefiting others to share the costs of recovery (typically attorney fees) proportionally. Applied as default rule in ERISA subrogation per *McCutchen*.
18. **ERISA Preemption**: Federal doctrine under 29 U.S.C. §1144(a) that supersedes state laws relating to employee benefit plans, insulating self-funded plans from state-law subrogation restrictions.
19. **Deemer Clause**: ERISA provision preventing states from treating self-funded employee benefit plans as insurance for purposes of state regulation (29 U.S.C. §1144(b)(2)(B)).
20. **Comparative Negligence Allocation**: Proportional allocation of fault in subrogation recovery; in modified comparative-fault jurisdictions, recovery may be barred if the insured's fault exceeds a threshold (typically 50% or 51%).
21. **Schedule P**: NAIC Annual Statement schedule requiring detailed development data for losses, loss adjustment expenses, and salvage/subrogation across all lines of business, reported in ten-year triangles.
22. **NASP (National Association of Subrogation Professionals)**: Industry association providing benchmarking studies, training, and best practice guidance for subrogation practitioners.
23. **Special Arbitration Agreement**: AF program for disputes where both parties have issued policies covering the same accident/occurrence and the underlying claim has been settled; mandates arbitration for contribution, indemnity, and concurrent coverage disputes.
24. **Impairment of Subrogation Rights**: Action by the insured (such as signing a general release with the tortfeasor) that prejudices the insurer's ability to pursue subrogation recovery; may void the insurer's obligation or entitle the insurer to an offset.

## Quality Checklist

1. ☐ Statute of limitations docketed at FNOL for every claim with identified third-party liability, using the shortest applicable limitations period
2. ☐ Made-whole doctrine applicability verified for the specific jurisdiction and source of subrogation right (equitable vs. contractual vs. statutory)
3. ☐ Anti-subrogation rule analysis completed, including check for co-insured, additional insured, and implied co-insured status
4. ☐ Underlying contracts (construction, lease, service agreements) reviewed for waiver-of-subrogation clauses
5. ☐ Medicare beneficiary status queried through CMS Coordination of Benefits Secure Website before any settlement
6. ☐ Section 111 MMSEA reporting completed for all claims involving Medicare beneficiaries within required quarterly filing windows
7. ☐ ERISA plan status confirmed (self-funded vs. fully insured) and plan document language reviewed for reimbursement and subrogation provisions
8. ☐ Arbitration Forums signatory status verified for both filing carrier and responding carrier; correct forum (Auto, Property, Special) selected
9. ☐ Insured's deductible included in subrogation demand and recovery proceeds allocated to deductible refund per state requirements
10. ☐ Conflict-of-law analysis documented when loss state, insured's residence state, and policy issuance state differ
11. ☐ Evidence preservation protocol followed — physical evidence, photographs, expert reports secured before spoilation risk materializes
12. ☐ Recovery reported in NAIC Schedule P Column 10; reserves adjusted net of anticipated salvage and subrogation per SSAP No. 55 election
13. ☐ Insured notified of subrogation activity and cooperating in accordance with policy cooperation clause
14. ☐ Comparative/contributory negligence assessed and factored into recovery viability and demand calculation
15. ☐ Final recovery allocated: carrier reimbursement, insured deductible return, and (if applicable) common-fund attorney fee reduction documented

## References

1. White and Williams LLP. "Fifty-State Compilation of Subrogation-Related Laws for Property Claims — Version 7" (January 2025). https://www.whiteandwilliams.com/assets/htmldocuments/Subro%20Charts%20Updated%205_10_16/Subro%20Chart%20Updates%202025/FIFTY-STATE%20COMPILATION%20OF%20SUBROGATION-RELATED%20LAWS%20FOR%20PROPERTY%20CLAIMS%20-%20Ver.%207%20-%20January%202025%20-%20Book%20Version.pdf
2. Matthiesen, Wickert & Lehrer S.C. "Anti-Subrogation Rule in All 50 States." https://www.mwl-law.com/wp-content/uploads/2018/02/ANTI-SUBROGATION-RULE-IN-ALL-50-STATES-CHART.pdf
3. Matthiesen, Wickert & Lehrer S.C. "Made Whole Doctrine in All 50 States." https://www.mwl-law.com/wp-content/uploads/2018/02/MADE-WHOLE-DOCTRINE-IN-ALL-50-STATES-CHART.pdf
4. NAIC. "Unfair Claims Settlement Practices Act (MDL-900)." https://content.naic.org/sites/default/files/model-law-900.pdf
5. NAIC. "Unfair Property/Casualty Claims Settlement Practices Model Regulation (MDL-902)." https://content.naic.org/sites/default/files/model-law-902.pdf
6. NAIC Journal of Insurance Regulation. "How's the Recovery? Salvage and Subrogation in the Property-Liability Insurance Industry" (2023). https://content.naic.org/sites/default/files/cipr-jir-2023-2.pdf
7. NAIC Journal of Insurance Regulation. "The Growth of Subrogation and the Future of Personal Injury Litigation" (Spurr). https://content.naic.org/sites/default/files/inline-files/JIR-ZA-36-06-EL.pdf
8. U.S. Department of Labor (EBSA). "Trends and Practices in Healthcare Subrogation." https://www.dol.gov/sites/dolgov/files/ebsa/researchers/analysis/health-and-welfare/trends-and-practices-in-healthcare-subrogation.pdf
9. US Airways, Inc. v. McCutchen, 569 U.S. 88 (2013). https://www.law.cornell.edu/supct/cert/11-1285
10. CMS. "NGHP User Guide — MMSEA Section 111 Reporting (v8.0, April 2025)." https://www.cms.gov/files/document/mmsea-111-april-7-2025-nghp-user-guide-version-80-chapter-i-introduction-and-overview.pdf
11. CMS. "Mandatory Insurer Reporting for Group Health Plans (GHP)." https://www.cms.gov/medicare/coordination-benefits-recovery/mandatory-insurer-reporting-group-health-plans
12. Arbitration Forums, Inc. "Rules and Reference Guide." https://home.arbfile.org/training/reference-guides/arbitration-forums,-inc-rules
13. Arbitration Forums, Inc. "Automobile Physical Damage Forum." https://home.arbfile.org/programs/auto-physical-damage
14. Rathbone Group. "The Made Whole Doctrine: Critical Knowledge in Subrogation." https://www.rathbonegroup.com/subrogation-and-the-made-whole-doctrine-critical-to-understand-hard-to-determine-impossible-to-ignore/
15. Rathbone Group. "Arbitration Forums in the Subrogation Process." https://www.rathbonegroup.com/a-look-at-arbitration-forums-in-the-subrogation-process/
16. Cozen O'Connor. "Understanding the Anti-Subrogation Doctrine." https://www.cozen.com/subrogation/resources/publications/understanding-the-anti-subrogation-doctrine-subrogation-and-recovery---articles-and-papers
17. Keis George LLP. "Further Examination of the Made Whole Doctrine." https://www.keisgeorge.com/2023/03/28/further-examination-of-the-made-whole-doctrine/
18. Praxis Risk Services. "Subrogation and Your Bottom Line." https://praxisriskservices.com/files/subropaper.pdf
19. IRS. "Rev. Proc. 2025-15 (Discount Factors for Unpaid Losses and Salvage Recoverable)." https://www.irs.gov/pub/irs-drop/rp-25-15.pdf
20. Mendes Law Firm. "Subrogation in Professional Liability Policies: The Made Whole Doctrine." https://mendes.com/news/subrogation-in-professional-liability-policies-the-made-whole-doctrine/
21. JD Supra. "Classifying Subrogation Claims Under State Insurance Liquidation Laws." https://www.jdsupra.com/legalnews/classifying-subrogation-claims-under-1612077/
22. Casualty Actuarial Society. "Salvage and Subrogation." https://www.casact.org/sites/default/files/old/clrstrans_1988_683.pdf
23. NAIC. "Model Laws, Regulations, and Guidelines — Spring 2025." https://content.naic.org/sites/default/files/publication-model-2024-spring.pdf
24. Guidewire/Arbitration Forums. "Modernize Subrogation with AF's New Guidewire Cloud Integration (2024)." https://www.guidewire.com/about/press-center/press-releases/20241212/modernize-subrogation-with-arbitration-forums-new-guidewire-cloud-integration