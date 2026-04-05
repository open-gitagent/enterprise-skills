---
name: claims-adjudication
description: >
  Insurance claims adjudication process including investigation, coverage analysis, liability determination, damage assessment, and settlement negotiation.
metadata:
  vertical: bfsi-insurance
  function: claims
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "NAIC, State DOI, UTPA"
---

# Claims Adjudication

## Domain Overview

Insurance claims adjudication is the structured, multi-phase process by which an insurer evaluates a claim from first notice of loss (FNOL) through final disposition — payment, denial, or litigation. The process operationalizes the insurance contract: it determines whether a reported event triggers coverage obligations, quantifies the insurer's financial exposure, and resolves the claim through payment or documented denial. Claims adjudication sits at the intersection of contract law, tort law, regulatory compliance, and actuarial science, requiring adjusters to simultaneously serve as investigators, coverage counsel proxies, negotiators, and regulatory compliance officers.

The regulatory framework governing claims adjudication in the United States is primarily state-based, anchored by the NAIC Model Unfair Claims Settlement Practices Act (Model #900), originally part of the Unfair Trade Practices Act (Model #880) and separated into a standalone act in June 1990. Model #900 identifies 14 specific prohibited "unfair" claims practices spanning misrepresentation, investigation failures, and settlement manipulation. Nearly every U.S. state has adopted some version, though critical variations exist — particularly around whether violations create a private right of action or only administrative penalties. The accompanying Model Regulations #902 (property/casualty) and #903 (life/accident/health) establish minimum operational standards for acknowledgment timelines, investigation procedures, and payment obligations.

The claims landscape is undergoing significant transformation driven by AI and automation adoption. The NAIC adopted its Model Bulletin on Use of Artificial Intelligence Systems by Insurers at the 2023 Fall National Meeting, establishing governance expectations for AI used in claims adjudication. The 2024 formation of the Third-Party Data and Models (H) Task Force signals intensifying regulatory scrutiny of algorithmic decision-making in claims. High-risk applications — including automated claim denials, AI-driven damage estimates, and predictive fraud scoring — now require documented governance programs, bias testing, and human oversight mechanisms. Carriers deploying AI in claims must demonstrate that AI Systems Programs address adverse consumer outcomes, comply with existing unfair claims practices statutes, and maintain transparency.

Bad faith litigation remains the dominant enforcement risk. Recent legislative activity reflects an evolving landscape: Florida's Section 624.1551 (December 2022) now requires an adverse adjudication confirming breach before extracontractual claims can be filed; Georgia amended its bad-faith failure-to-settle statute in 2024 to clarify time-limited demand structures; Montana's S.B. 236 (2023) imposed 60-day acceptance windows on time-limited demands; and California added Civil Procedure Code Section 999 establishing statutory frameworks for time-limited demands. Social inflation — escalating jury verdicts, litigation funding, and plaintiff-friendly legal strategies — compounds exposure for carriers that mishandle adjudication.

## Core Decision Framework

Experienced claims professionals apply a sequential, policy-centric decision framework that subordinates every judgment to the contract language and applicable law. The framework operates through five interconnected gates:

**Gate 1 — Coverage Verification ("Does coverage exist?")**
The adjuster first confirms the policy was in force at the time of loss, the reporting party is an insured or authorized claimant, and the event described falls within insuring agreement language. This requires parsing declarations pages, endorsements, and manuscript forms. Occurrence-based policies trigger on the date of loss; claims-made policies trigger on the date of claim reporting (with potential for late notice denial). The adjuster must identify all potentially applicable coverages across all policy layers, including excess and umbrella programs.

**Gate 2 — Exclusion and Condition Analysis ("Does anything negate coverage?")**
Every applicable exclusion must be evaluated against the specific facts. Exclusions are construed narrowly in most jurisdictions, and the burden of proving exclusion applicability rests on the insurer. Conditions precedent — timely notice, cooperation, submission of proof of loss — are independently evaluated. A failure of conditions may warrant denial but must be assessed against state-specific anti-forfeiture protections and prejudice requirements (many jurisdictions require the insurer to demonstrate actual prejudice from late notice).

**Gate 3 — Investigation and Liability Determination ("What happened and who is responsible?")**
Investigation scope must be proportionate to claim complexity and potential exposure. For first-party claims, the investigation confirms the event occurred as reported and quantifies the loss. For third-party liability claims, the adjuster determines the insured's legal liability using applicable negligence standards — pure comparative negligence, modified comparative negligence (50% or 51% bar), or contributory negligence depending on jurisdiction. Comparative fault percentages directly affect settlement authority calculations.

**Gate 4 — Damage Assessment and Reserve Setting ("What is this worth?")**
Damages are categorized as special (economic/quantifiable) and general (non-economic/pain and suffering). The adjuster establishes an initial case reserve reflecting the probable ultimate cost of the claim, including indemnity, allocated loss adjustment expenses (ALAE), and unallocated loss adjustment expenses (ULAE). Reserves must be updated as new information emerges and are audited for adequacy by both internal actuarial staff and external regulators during market conduct examinations.

**Gate 5 — Resolution ("How do we close this?")**
Resolution paths include voluntary settlement, structured settlement, compromise, arbitration, mediation, appraisal, litigation through verdict, or denial with documented rationale. Settlement authority is typically tiered — adjuster authority, supervisor authority, examiner committee, and executive/board authority at ascending dollar thresholds. Every denial must cite specific policy language and applicable facts per NAIC Model #900 §4(N).

## Step-by-Step Process

### Phase 1: First Notice of Loss (FNOL) and Triage
1. Receive and log FNOL with date/time stamp, claimant identification, and loss description
2. Verify policy status — confirm coverage was active on the date of loss
3. Assign claim number and route based on triage criteria: line of business, severity, complexity, and jurisdiction
4. Apply automated red-flag scoring for SIU referral indicators (frequency patterns, timing anomalies, prior claims history)
5. Acknowledge receipt to the claimant — NAIC Model #902 §5(A) requires acknowledgment within 10 working days for P&C claims; many states impose tighter deadlines (e.g., California requires 15 calendar days per 10 CCR §2695.5(e))
6. Issue reservation of rights letter if coverage questions exist — critical to preserve the insurer's defenses while investigation proceeds

### Phase 2: Coverage Analysis
7. Pull the complete policy file including all endorsements, riders, and amendments
8. Map the reported loss to specific insuring agreements — identify all potentially triggered coverages
9. Analyze each applicable exclusion against known facts
10. Evaluate conditions precedent compliance (timely notice, cooperation, proof of loss submission)
11. Research applicable state law on coverage interpretation, including any mandatory coverage provisions
12. Document coverage determination with specific policy citations; issue coverage position letter to insured

### Phase 3: Investigation
13. Assign investigation resources proportionate to complexity — staff adjuster, independent adjuster, or specialized investigator
14. Obtain recorded/written statements from insured, claimants, and witnesses
15. Collect and preserve physical evidence, photographs, police/fire reports, medical records, financial records
16. Engage necessary experts — engineers, accountants, medical professionals, accident reconstructionists, origin-and-cause investigators
17. Conduct scene inspection where warranted
18. Refer to Special Investigations Unit (SIU) if fraud indicators emerge during investigation
19. Evaluate subrogation potential — identify responsible third parties for recovery

### Phase 4: Liability Determination (Third-Party Claims)
20. Analyze applicable legal standard of care and duty owed
21. Apply jurisdiction-specific negligence framework (pure comparative, modified comparative, contributory)
22. Calculate percentage of fault allocation among all parties
23. Assess applicability of joint-and-several liability versus proportionate responsibility
24. Evaluate statutory immunities, caps, and limitations periods
25. Document liability determination with supporting evidence citations

### Phase 5: Damage Assessment
26. For property claims: obtain contractor estimates, use estimating software (Xactimate, Symbility), apply depreciation schedules, evaluate actual cash value versus replacement cost
27. For bodily injury claims: analyze medical records and bills, calculate lost wages, assess permanency/impairment ratings, evaluate general damages using jury verdict research and comparable settlement data
28. For commercial claims: assess business interruption losses, extra expense, contingent business interruption, calculate period of restoration
29. Set initial case reserve based on probable ultimate cost including ALAE
30. Review reserve adequacy at regular intervals (30/60/90-day review cycles)

### Phase 6: Settlement Negotiation and Resolution
31. Prepare settlement evaluation memo documenting coverage, liability, damages, and recommended disposition
32. Obtain settlement authority from appropriate authority level based on dollar thresholds
33. Initiate negotiation with demand analysis — evaluate claimant's demand against independent valuation
34. Present settlement offer with documented rationale
35. Explore alternative dispute resolution (ADR) where appropriate — mediation, arbitration, appraisal
36. Tender payment within 30 days of liability affirmation and damage agreement per NAIC Model #902 §6(F)
37. For denials: issue written denial citing specific policy provisions and factual basis per NAIC Model #900 §4(N)
38. Pursue subrogation recovery against responsible third parties post-settlement
39. Close file with complete documentation of all decisions, communications, and payments

## Evaluation Criteria

**Claim Handling Timeliness**
- FNOL acknowledgment: within 10 working days (NAIC standard) or state-specific requirement
- Initial contact with claimant: within 24-48 hours of assignment
- Coverage determination: within 15 business days of receiving all necessary information
- Payment after liability affirmation: within 30 days per NAIC Model #902 §6(F)
- States impose additional specific deadlines (e.g., Texas Insurance Code Chapter 542 Subchapter B: acknowledge within 15 days, accept/reject within 15 business days of all information, pay within 5 business days of notification of acceptance)

**Coverage Analysis Accuracy**
- Every denial cites specific policy language (insuring agreement, exclusion, condition)
- Applicable endorsements reviewed and applied
- State-mandated coverages confirmed (e.g., UM/UIM, PIP, medpay)
- Reservation of rights issued before coverage-questioning investigation conducted under insured's policy

**Investigation Adequacy**
- Proportionate to claim size and complexity
- All material witnesses contacted and statements documented
- Relevant expert opinions obtained for technical matters
- Evidence preservation procedures followed
- SIU referrals documented with specific indicators

**Reserve Accuracy**
- Initial reserve set within 30 days of assignment
- Reserve reflects probable ultimate cost (indemnity + ALAE)
- Regular review cadence maintained (minimum quarterly for open claims)
- Reserve-to-paid ratio within acceptable ranges by line of business

**Settlement Reasonableness**
- Settlement within range of documented claim valuation
- Authority obtained before offer extended
- Comparative verdict/settlement research documented
- No evidence of coercive settlement tactics prohibited by NAIC Model #900 §4

## Red Flags & Edge Cases

1. **Late-reported claims-made policy claims**: An insured reports a professional liability claim 60 days after policy expiration without purchasing tail coverage. The adjuster must analyze whether extended reporting period provisions exist, whether the "claim" was actually first made during the policy period (even if reported late), and whether the state's late-notice prejudice rule applies to claims-made policies — many jurisdictions treat claims-made late notice differently from occurrence policy late notice.

2. **Concurrent causation disputes**: A homeowner sustains damage from both wind (covered peril) and flood (excluded peril) during a hurricane. The adjuster must determine whether the jurisdiction follows the efficient proximate cause doctrine (coverage applies if the covered peril set the chain of events in motion) or the concurrent causation exclusion is enforceable. Post-Hurricane Katrina litigation (e.g., Leonard v. Nationwide, 499 F.3d 419, 5th Cir. 2007) established critical precedent on this issue.

3. **Stacking and anti-stacking disputes**: An insured involved in a motor vehicle accident holds multiple auto policies or a single policy with multiple vehicles. The adjuster must determine whether the jurisdiction permits stacking of UM/UIM limits and whether anti-stacking endorsements are enforceable under state law — several states (e.g., Pennsylvania, Florida) have specific stacking statutes.

4. **Time-limited settlement demands ("Holt demands" in Georgia)**: A third-party claimant sends a structured settlement demand with a short acceptance window, strict compliance terms, and conditions designed to be difficult to accept. Failure to comply precisely can expose the insured to excess judgment and the insurer to bad faith. Georgia's Pierce v. Banks (2023) held a demand was rejected because a comma was missing in the law firm name on the check.

5. **Algorithmic claim denial without human review**: An insurer uses AI to auto-deny low-severity claims based on predictive models. This violates the NAIC AI Model Bulletin's requirement for human oversight in high-risk applications and potentially constitutes failing to conduct a reasonable investigation per NAIC Model #900 §4(C).

6. **Depreciation of labor in property claims**: Some insurers depreciate labor costs when calculating actual cash value, resulting in lower initial payments. The practice has been successfully challenged in multiple class actions (e.g., Hicks v. State Farm, W.D. Ark. 2015), and several states now prohibit labor depreciation by statute or regulation.

7. **Appraisal demand timing manipulation**: A first-party property insurer delays invoking the appraisal clause until the insured has incurred significant litigation costs, then invokes appraisal to limit the scope of dispute to amount rather than coverage. Courts increasingly scrutinize waiver-by-conduct arguments in appraisal disputes.

8. **Reservation of rights letter deficiency**: An insurer investigates under a reservation of rights but fails to specifically identify the coverage defenses being reserved. Vague or boilerplate reservations may be held insufficient, estopping the insurer from asserting the coverage defense. The letter must reference specific policy provisions and factual bases.

9. **Phantom SIU referral as delay tactic**: An adjuster refers a claim to the SIU without documented fraud indicators, using the referral to suspend payment timelines. Regulators in market conduct examinations specifically audit SIU referral-to-finding ratios; ratios suggesting systemic misuse trigger enforcement action. NAIC Model #900 §4(C) prohibits using investigation as a delay tactic.

10. **Excess carrier notice failure**: A primary insurer handling a claim that may exhaust primary limits fails to provide timely notice to the excess carrier. The excess carrier may deny coverage for prejudice from late notice, leaving the insured exposed to judgment above primary limits and creating bad faith exposure for the primary insurer.

11. **Post-loss policy rescission based on material misrepresentation**: An insurer discovers a material misrepresentation on the application during claims investigation and attempts to rescind the policy ab initio rather than deny the specific claim. Rescission returns premiums but eliminates all coverage. States vary on whether the misrepresentation must be intentional or merely material, and several states (e.g., New York) limit rescission after a contestability period.

12. **Valuation disputes in total-loss auto claims**: An insurer uses comparable vehicle databases (CCC, Mitchell, Audatex) to value a total-loss vehicle but fails to include vehicles truly comparable in mileage, condition, and options. NAIC Model #902 §8 requires that valuations reflect fair market value with documented comparable vehicles from the local market area.

13. **Cross-coverage settlement manipulation**: An insurer delays settlement of a clearly liable claim under one coverage (e.g., property damage) to pressure favorable settlement under a disputed coverage (e.g., bodily injury). This is specifically prohibited by NAIC Model #900 §4(D) and has been adopted by 30+ states as a standalone prohibition.

14. **Business interruption period-of-restoration disputes**: An insurer truncates the period of restoration for a business interruption claim by asserting the insured could have resumed operations sooner. The adjuster must apply the "reasonable speed" standard and document whether delays were attributable to factors within or outside the insured's control, including supply chain disruptions and permitting delays.

## Common Mistakes

1. **Issuing denial letters that cite policy exclusions without quoting the specific language** — regulators and courts require the insurer to provide the exact policy text, not paraphrased summaries. Generic denial letters are a leading market conduct examination finding.

2. **Failing to re-investigate after receiving new information** — once an insured submits additional documentation or evidence, the prior coverage or liability determination must be re-evaluated. Treating the initial decision as final violates the duty of reasonable investigation.

3. **Setting reserves based on payment authority rather than probable ultimate cost** — adjusters sometimes anchor reserves to their own authority level rather than the claim's actual probable value, creating reserve deficiency and distorting loss development patterns visible to regulators and reinsurers.

4. **Not documenting the rationale for claim denials in the claim file contemporaneously** — post-hoc justifications created during litigation are given less weight by courts and may support inference of bad faith. Documentation must be real-time.

5. **Applying a company-wide standard for comparative negligence without considering jurisdiction-specific rules** — a 48% at-fault insured recovers fully in a pure comparative negligence state, recovers nothing in a contributory negligence state, and recovers in some but not all modified comparative states depending on the threshold.

6. **Treating the insured as an adversary in first-party claims** — the insurer owes a duty of good faith and fair dealing to its own policyholder. Applying adversarial negotiation tactics (low-balling, delay, unreasonable documentation demands) appropriate for third-party liability negotiation to first-party property claims creates bad faith exposure.

7. **Overlooking additional insureds and additional interests on endorsements** — failing to provide notice of claim or loss to lenders, landlords, or additional insureds listed on endorsements creates downstream disputes and potential E&O exposure.

8. **Using boilerplate independent medical examination (IME) vendors without vetting for bias** — courts and regulators scrutinize IME physicians who consistently support insurer positions. A pattern of using the same IME provider who uniformly finds no injury undermines the investigation's credibility.

9. **Paying claims without confirming the payee** — issuing payment to the wrong party (wrong named insured, missing mortgage clause, incorrect lienholder) creates legal complications and may not satisfy the obligation to the proper claimant.

10. **Ignoring subrogation recovery opportunities** — failing to preserve and pursue subrogation rights wastes recoverable dollars and may violate the insurer's duty to its policyholders and shareholders.

## Regulatory & Compliance Requirements

### Federal Framework
- **McCarran-Ferguson Act (15 U.S.C. §§1011-1015)**: Preserves state regulation of insurance; federal law applies only when state law does not specifically regulate the business of insurance
- **ERISA (29 U.S.C. §1001 et seq.)**: Preempts state regulation of self-funded employee benefit plans, creating parallel claims adjudication standards for ERISA-governed claims
- **NFIP (42 U.S.C. §4001 et seq.)**: Federal flood insurance claims follow FEMA-administered standards separate from state unfair claims practices acts

### NAIC Model Laws and Regulations
- **Model #900 — Unfair Claims Settlement Practices Act (1990/1997)**: Defines 14 prohibited claims practices in §4; enforcement through cease-and-desist orders and tiered penalties ($1,000/violation ordinary, $25,000/violation flagrant; aggregate caps of $100,000/$250,000 respectively); possible license revocation
- **Model #902 — Unfair Property/Casualty Claims Settlement Practices Model Regulation (1990/1997)**: Operational standards including: acknowledge claims within 10 working days (§5A); begin investigation within 10 working days (§5B); affirm/deny liability within reasonable time (§6F); tender payment within 30 days of affirmation (§6F); total-loss vehicle valuation standards (§8); replacement cost settlement standards (§9)
- **Model #903 — Unfair Life, Accident and Health Claims Settlement Practices Model Regulation (1990/1991)**: Parallel operational standards for life/health claims
- **Model #910 — Market Conduct Record Retention and Production Model Regulation**: Requires retention of claim files, correspondence, and investigation materials for examination purposes

### State-Specific Highlights
- **Texas (Ins. Code Ch. 542, Subch. B)**: The "Prompt Payment of Claims Act" — acknowledge within 15 days, accept/reject within 15 business days, pay within 5 business days; 18% annual penalty interest for violations
- **California (10 CCR §§2695.1-2695.14)**: Fair Claims Settlement Practices Regulations — among the most detailed state implementations; 15-day acknowledgment, 40-day acceptance/denial, specific documentation retention requirements
- **Florida (Fla. Stat. §627.70131)**: Property claims must be acknowledged within 14 days, payment/denial within 90 days; recent reforms (2022-2023) restrict bad faith claims and impose one-way attorney fee reforms
- **New York (Ins. Law §2601)**: Prohibits unfair claims practices; enforced through market conduct examinations by NY DFS; Circular Letter 2009-3 provides additional claims handling guidance
- **Illinois (215 ILCS 5/154.6)**: Penalty up to $250,000 per individual violation with no aggregate cap — among the most severe state penalty structures

### AI and Automation Governance
- **NAIC Model Bulletin on Use of AI Systems by Insurers (2023)**: Requires documented AI Systems Programs for claims adjudication; mandates human oversight for high-risk decisions; requires bias testing and adverse consumer outcome monitoring
- **Colorado SB 21-169**: First state to specifically regulate AI in insurance — requires testing for unfairly discriminatory outcomes; effective November 2023

## Terminology

1. **FNOL (First Notice of Loss)**: The initial report of a loss event to the insurer that triggers the claims process; the date/time of FNOL establishes the starting point for all regulatory acknowledgment and investigation timelines.

2. **Reservation of Rights (ROR)**: A written communication from an insurer to its insured acknowledging receipt of a claim while specifically preserving the insurer's right to later deny coverage based on identified policy provisions — must cite specific policy language and factual bases.

3. **Subrogation**: The insurer's legal right to pursue recovery from a third party responsible for a loss after the insurer has paid the insured's claim; must be preserved through timely action, proper documentation, and often insured cooperation.

4. **Actual Cash Value (ACV)**: The replacement cost of damaged/lost property minus depreciation; calculation methods vary by jurisdiction — broad evidence rule (majority approach) considers all relevant evidence of value, not just replacement cost minus depreciation.

5. **Replacement Cost Value (RCV)**: The cost to repair or replace damaged property with materials of like kind and quality without deduction for depreciation; typically requires the insured to actually perform the repair before the depreciation holdback is released.

6. **ALAE (Allocated Loss Adjustment Expense)**: Costs directly attributable to a specific claim — expert fees, independent adjuster fees, legal defense costs, court costs — tracked and reserved at the individual claim level.

7. **ULAE (Unallocated Loss Adjustment Expense)**: Overhead costs of the claims operation not attributable to a specific claim — staff adjuster salaries, office expenses, claims system costs — allocated actuarially across the book of business.

8. **Bad Faith**: An insurer's breach of the implied covenant of good faith and fair dealing owed to its policyholder; may be statutory (violation of unfair claims practices act), contractual (breach of policy obligations), or tortious (common law duty), with remedies varying dramatically by state.

9. **SIU (Special Investigations Unit)**: The insurer's internal unit responsible for investigating suspected fraudulent claims; referral triggers typically include specific red-flag indicators; SIU operations are subject to state fraud bureau reporting requirements.

10. **Proof of Loss**: A formal sworn statement submitted by the insured documenting the facts and amount of a claim; required by most property insurance policies within a specified timeframe (typically 60 days); late filing may or may not bar the claim depending on state prejudice requirements.

11. **Examination Under Oath (EUO)**: A formal, sworn examination of the insured conducted by the insurer's representative (typically counsel), permitted under the cooperation clause of most insurance policies; failure to submit may void coverage.

12. **Comparative Negligence**: The legal framework for allocating fault among multiple parties; pure comparative (plaintiff recovers regardless of fault percentage), modified comparative (plaintiff barred at 50% or 51% fault), or contributory negligence (plaintiff barred at any fault — DC, Maryland, Virginia, Alabama, North Carolina).

13. **Occurrence**: A single event or continuous/repeated exposure to conditions that results in bodily injury or property damage; the triggering mechanism for occurrence-based policies — date of occurrence, not date of discovery or reporting, activates coverage.

14. **Claims-Made Policy**: A policy that covers claims first made against the insured and reported to the insurer during the policy period (or extended reporting period); creates unique late-notice and tail coverage issues distinct from occurrence-based forms.

15. **Appraisal**: A contractual dispute resolution mechanism in property insurance policies for resolving disagreements over the amount of loss (not coverage) — each party selects an appraiser, the two appraisers select an umpire, and any two of three reaching agreement sets the loss amount.

16. **Loss Reserve**: The estimated liability for unpaid claims including both reported claims (case reserves) and claims incurred but not reported (IBNR); a critical component of the insurer's financial statements subject to actuarial certification and regulatory review.

17. **Duty to Defend**: In liability insurance, the insurer's obligation to provide and pay for the insured's legal defense against covered claims; triggered by allegations in the complaint that potentially fall within coverage — broader than the duty to indemnify.

18. **Estoppel and Waiver**: Legal doctrines that can prevent an insurer from asserting a coverage defense it has previously waived (intentional relinquishment) or is estopped from asserting (detrimental reliance by the insured on the insurer's conduct).

19. **Tender of Defense**: The insured's formal request to the insurer to assume the defense of a third-party claim under the liability policy; must be timely and complete — late tender may prejudice coverage.

20. **Stacking**: The practice of combining the limits of multiple insurance policies or multiple coverage units within a single policy to increase the total available coverage; permitted in some states, prohibited in others, and subject to anti-stacking endorsement enforceability.

21. **Market Conduct Examination**: A formal regulatory audit of an insurer's business practices — including claims handling — conducted by a state insurance department; findings of unfair claims practices trigger corrective action plans, fines, and potential referral for enforcement.

22. **Period of Restoration**: In business interruption insurance, the time period beginning when the physical loss occurs and ending when the property should be repaired with reasonable speed; disputes over this period are among the most contentious in commercial claims.

23. **Advance Payment**: A partial payment made by the insurer before final settlement of a claim; NAIC Model #902 §6(D) provides that advance payments should not constitute a waiver or release of any claim the insured may have.

24. **Anti-Concurrent Causation Clause (ACC)**: A policy provision excluding coverage when a covered peril and an excluded peril concurrently cause a loss; enforceability varies by jurisdiction and was heavily litigated post-Hurricane Katrina.

## Quality Checklist

1. **Coverage verification completeness**: Confirm that all policy forms, endorsements, and amendments effective on the date of loss have been reviewed and documented in the claim file — including checking for manuscript endorsements that may modify standard coverage.

2. **Regulatory timeline compliance**: Verify acknowledgment, investigation initiation, and payment timelines meet the specific requirements of the governing state — not just NAIC model standards, as state deadlines frequently differ.

3. **Denial letter specificity**: Every denial cites the exact policy provision (section, paragraph, and endorsement number) and specific factual basis; general references to "exclusions" without quoting language are insufficient.

4. **Reserve adequacy**: Confirm that case reserves reflect probable ultimate cost (indemnity + ALAE) based on current claim valuation, not adjuster authority limits or payment-to-date; document reserve rationale at each review.

5. **Investigation proportionality**: Verify that investigation scope matches claim complexity and dollar exposure — an $800 property claim does not require the same investigation depth as a $800,000 liability claim, but both require reasonable investigation.

6. **Reservation of rights timeliness**: Confirm ROR letter was issued before conducting investigation under the insured's policy when coverage questions exist; late issuance may estop coverage defenses.

7. **Subrogation preservation**: Verify that subrogation rights have been identified, documented, and preserved — including proper lien notice, evidence preservation, and timely pursuit within applicable statutes of limitation.

8. **SIU referral documentation**: Every SIU referral includes specific documented red-flag indicators justifying the referral; referrals without documented basis are audit targets during market conduct examinations.

9. **Settlement authority chain**: Confirm that settlement offers and payments have been approved at the proper authority level before being communicated to the claimant; unauthorized settlements create internal control failures.

10. **Excess/umbrella carrier notification**: For claims with exposure potentially exceeding primary limits, verify timely notice to all excess carriers and proper coordination of defense and settlement.

11. **Claimant communication log**: All communications with the insured, claimant, or their representatives are documented with date, time, participants, and substance — diary/follow-up entries maintained at appropriate intervals.

12. **Comparative negligence application**: For liability claims, confirm that fault allocation uses the correct legal standard for the applicable jurisdiction and that the analysis is documented with supporting evidence.

13. **AI/automation governance**: If any automated tools were used in claim triage, valuation, or decision-making, verify that human review occurred for coverage determinations and denials per NAIC AI Model Bulletin requirements.

14. **File documentation completeness**: The claim file must stand alone as a complete narrative — a reviewer unfamiliar with the claim should be able to understand every decision from the file documentation without oral explanation.

15. **Policyholder communication standards**: Verify that all claim status communications are clear, timely, and compliant with applicable consumer protection standards — including explanation of claim process, anticipated timelines, and insured's rights.

## References

1. NAIC Model #900 — Unfair Claims Settlement Practices Act (1997): https://content.naic.org/sites/default/files/model-law-900.pdf
2. NAIC Model #902 — Unfair Property/Casualty Claims Settlement Practices Model Regulation (1997): https://content.naic.org/sites/default/files/model-law-902.pdf
3. NAIC Model #903 — Unfair Life, Accident and Health Claims Settlement Practices Model Regulation: https://content.naic.org/sites/default/files/model-law-903.pdf
4. NAIC State Adoption Chart — UCSPA (Model #900): https://content.naic.org/sites/default/files/model-law-state-page-900.pdf
5. NAIC State Adoption Chart — Model #902: https://content.naic.org/sites/default/files/model-law-state-page-902.pdf
6. NAIC Private Rights of Action Chart (MC-55): https://content.naic.org/sites/default/files/model-law-chart-mc-55-private-rights-of-action-for-unfair-claims-settlement-practices.pdf
7. NAIC Claims Settlement Provisions Chart (MC-50): https://content.naic.org/sites/default/files/model-law-chart-mc-50-claims-settlement-provisions.pdf
8. NAIC Artificial Intelligence Topic Page and AI Model Bulletin (2023): https://content.naic.org/insurance-topics/artificial-intelligence
9. NAIC 2024 Annual Report: https://content.naic.org/sites/default/files/annual-report-2024-advancing-insurance-regulation.pdf
10. Feinman, Jay M., "The Regulation of Insurance Claim Practices," UC Irvine Law Review, Vol. 5:1319: https://uphelp.org/wp-content/uploads/2020/11/feinman_ricp.pdf
11. United Policyholders, "An Essential Protection in the Claims Process": https://sites.camden.rutgers.edu/wp-content/uploads/sites/16/2016/10/Claims3.pdf
12. Plitt, "A Roadmap for the NAIC's Unfair Claims Settlement Practices Act": https://www.insuranceexpertplitt.com/blog/2021/07/a-roadmap-for-the-naics-unfair-claims-settlement-practices-act/
13. ABA, "Liability Claims 101: A New Insurance Lawyer's Guide": https://www.americanbar.org/groups/litigation/resources/newsletters/insurance-coverage/guide-liability-insurance-claims/
14. IRMI, "The Art and Skill of Analyzing Coverage": https://www.irmi.com/articles/expert-commentary/the-art-and-skill-of-analyzing-coverage
15. IRMI, "The Claim Function and Best Practices": https://www.irmi.com/articles/expert-commentary/the-claim-function-and-best-practices
16. Dykema, "Insurance Bad Faith Report, July 2024": https://www.dykema.com/news-insights/insurance-bad-faith-report-July-2024.html
17. Dykema, "Insurance Bad Faith Report, January 2025": https://www.dykema.com/news-insights/insurance-bad-faith-report-january-2025.html
18. Hinshaw & Culbertson, "2025 Key Insurance Decisions, Trends & Developments": https://www.hinshawlaw.com/a/web/2MiqDNSbzbepmZrga9RQSj/be8Q8p/mealeys-2025-key-insurance-decisions-trends-and-developments-look-ahead-to-2026.pdf
19. Hinshaw & Culbertson, "Key Insurance Decisions 2024 and Look Ahead to 2025": https://www.hinshawlaw.com/a/web/uWGi8KYKoe2W8NUkE8nTe4/hinshaw-white-paper-key-insurance-decisions-trends-and-developments-in-2024-and-a-look-ahead-to-2025.pdf
20. National Bad Faith Survey (2025), United Policyholders/50 State Survey: https://uphelp.org/wp-content/uploads/2025/03/2025-National-Bad-Faith-Survey.pdf
21. Hunton Andrews Kurth, "Georgia Legislature Takes Another Shot at Bad Faith Claim Set-Ups": https://www.hunton.com/hunton-insurance-recovery-blog/georgia-collides-with-early-accident-settlements-legislature-takes-another-shot-at-bad-faith-claim-set-ups
22. VCA Software, "Claims Handling Best Practices: A Comprehensive Guide for 2025": https://vcasoftware.com/claims-handling-best-practices/
23. Aon, "4 Strategies to Navigate Insurance Claims Trends": https://www.aon.com/en/insights/articles/navigating-insurance-claims-trends-strategies-for-effective-claims-management
24. NAIC AI System Evaluation Tool — Industry Comments (2025): https://content.naic.org/sites/default/files/inline-files/_Comments-AI-Sys-Eval-Tool_Combined%20as%20of%202025-09-19_0.pdf
25. NAIC Third-Party Data and Models Task Force — 2024 Work Plan: https://content.naic.org/sites/default/files/2024-charges-and-work-plan-exposure-040524.pdf
26. Mercer Law Review, "Bad Faith in Modern Insurance Litigation" (2025): https://digitalcommons.law.mercer.edu/cgi/viewcontent.cgi?article=3467&context=jour_mlr
27. Industrial Commission of Arizona, "Good Faith Claims Management": https://www.azica.gov/sites/default/files/2025-08/Good%20Faith%20Claims%20Management%202024-1%20%281%29.pdf
28. NAIC Model Laws, Regulations, and Guidelines — Fall 2025: https://content.naic.org/sites/default/files/publication-model-2025-fall.pdf