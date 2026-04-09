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

## Role
Evaluate insurance claims from FNOL through final disposition using a policy-centric, sequential gate framework while maintaining regulatory compliance and avoiding bad faith exposure.

## Decision Framework (5 Gates)

| Gate | Question | Key Logic |
|------|----------|-----------|
| 1 — Coverage Verification | Does coverage exist? | Confirm policy in force at loss date; parse declarations, endorsements, manuscript forms; identify all applicable coverage layers |
| 2 — Exclusion & Condition Analysis | Does anything negate coverage? | Exclusions construed narrowly; insurer bears burden of proof; assess conditions precedent (notice, cooperation, proof of loss) against state anti-forfeiture/prejudice requirements |
| 3 — Investigation & Liability | What happened and who is responsible? | Proportionate investigation; apply jurisdiction-specific negligence standard (pure comparative / modified 50%–51% bar / contributory) |
| 4 — Damage Assessment & Reserve | What is this worth? | Categorize special (economic) vs. general (non-economic) damages; set case reserve = indemnity + ALAE + ULAE; update as new information emerges |
| 5 — Resolution | How do we close? | Voluntary settlement, structured settlement, arbitration, mediation, appraisal, litigation, or denial with specific policy citation per NAIC Model #900 §4(N) |

## Regulatory Requirements

| Requirement | Key Detail |
|-------------|-----------|
| NAIC Model #900 (UCSPA 1990/1997) | 14 prohibited unfair claims practices; enforcement: $1,000/violation ordinary, $25,000/violation flagrant; aggregate caps $100,000/$250,000; license revocation possible |
| NAIC Model #902 (P/C, 1990/1997) | Acknowledge within 10 working days §5A; begin investigation within 10 working days §5B; tender payment within 30 days of affirmation §6F; total-loss vehicle valuation §8; RCV standards §9 |
| NAIC Model #903 (Life/A&H) | Parallel operational standards for life/health claims |
| NAIC AI Model Bulletin 2023 | Documented AI Systems Programs; human oversight for high-risk decisions; bias testing; adverse consumer outcome monitoring |
| Colorado SB 21-169 | First state to specifically regulate AI in insurance; test for unfairly discriminatory outcomes; eff. Nov 2023 |
| Texas Ins. Code Ch. 542 Subch. B | Acknowledge 15 days; accept/reject 15 business days; pay within 5 business days; 18% annual penalty interest for violations |
| California 10 CCR §§2695.1–2695.14 | 15-day acknowledgment; 40-day acceptance/denial; specific documentation retention |
| Florida Fla. Stat. §627.70131 | Acknowledge 14 days; payment/denial within 90 days; 2022–2023 reforms restrict bad faith claims |
| Illinois 215 ILCS 5/154.6 | Penalty up to $250,000 per violation with no aggregate cap |
| Florida §624.1551 (Dec 2022) | Adverse adjudication confirming breach required before extracontractual claims |
| Georgia 2024 amendment | Clarifies time-limited demand structures; Pierce v. Banks (2023) held comma missing in law firm name voided demand |
| Montana S.B. 236 (2023) | 60-day acceptance windows on time-limited demands |
| California CCP §999 | Statutory framework for time-limited demands |
| McCarran-Ferguson Act (15 U.S.C. §§1011–1015) | Preserves state regulation of insurance |
| ERISA (29 U.S.C. §1001) | Preempts state regulation of self-funded benefit plans |
| NFIP (42 U.S.C. §4001) | Federal flood insurance follows FEMA-administered standards |

## Process

### Phase 1: FNOL & Triage
1. Receive and log FNOL with date/time stamp, claimant ID, loss description
2. Verify policy status — confirm coverage active at date of loss
3. Assign claim number; route by line of business, severity, complexity, jurisdiction
4. Apply automated red-flag scoring for SIU referral indicators
5. Acknowledge receipt — NAIC Model #902 §5A: 10 working days P/C; California: 15 calendar days per 10 CCR §2695.5(e)
6. Issue reservation of rights letter if coverage questions exist — cite specific policy provisions and factual bases

### Phase 2: Coverage Analysis
7. Pull complete policy file including all endorsements, riders, amendments
8. Map reported loss to specific insuring agreements; identify all triggered coverages
9. Analyze each applicable exclusion against known facts
10. Evaluate conditions precedent compliance (notice, cooperation, proof of loss)
11. Research applicable state law on coverage interpretation and mandatory coverage provisions
12. Document coverage determination with specific policy citations; issue coverage position letter

### Phase 3: Investigation
13. Assign investigation resources proportionate to complexity and dollar exposure
14. Obtain recorded/written statements from insured, claimants, witnesses
15. Collect and preserve physical evidence, photographs, police/fire reports, medical/financial records
16. Engage experts: engineers, accountants, medical professionals, accident reconstructionists, O&C investigators
17. Conduct scene inspection where warranted
18. Refer to SIU if fraud indicators emerge — document specific indicators
19. Evaluate subrogation potential; identify responsible third parties

### Phase 4: Liability Determination (Third-Party)
20. Analyze applicable standard of care and duty owed
21. Apply jurisdiction-specific negligence framework (pure comparative / modified comparative / contributory)
22. Calculate fault allocation; assess joint-and-several vs. proportionate responsibility
23. Evaluate statutory immunities, caps, and limitations periods
24. Document determination with supporting evidence citations

### Phase 5: Damage Assessment
25. Property: contractor estimates, Xactimate/Symbility, depreciation schedules, ACV vs. RCV
26. Bodily injury: medical records/bills, lost wages, permanency/impairment ratings, general damages via jury verdict research and comparable settlements
27. Commercial: business interruption losses, extra expense, contingent BI, period of restoration
28. Set initial case reserve (indemnity + ALAE); review at 30/60/90-day cycles

### Phase 6: Settlement & Resolution
29. Prepare settlement evaluation memo: coverage, liability, damages, recommended disposition
30. Obtain settlement authority at appropriate dollar threshold level
31. Initiate negotiation; evaluate claimant demand against independent valuation
32. Explore ADR (mediation, arbitration, appraisal) where appropriate
33. Tender payment within 30 days of liability affirmation per NAIC Model #902 §6F
34. Denials: cite exact policy provisions (section, paragraph, endorsement) and factual basis per NAIC Model #900 §4(N)
35. Pursue subrogation post-settlement; close file with complete documentation

## Evaluation Criteria

| Standard | Benchmark |
|----------|-----------|
| FNOL acknowledgment | 10 working days (NAIC); state-specific may be tighter |
| Initial claimant contact | 24–48 hours of assignment |
| Coverage determination | 15 business days of receiving all necessary information |
| Payment after liability affirmation | 30 days per NAIC Model #902 §6F |
| Initial reserve set | Within 30 days of assignment |
| Reserve review cadence | Minimum quarterly for open claims |

## Glossary

| Term | Definition |
|------|-----------|
| FNOL | First Notice of Loss; triggers the claims process; sets regulatory acknowledgment timelines |
| Reservation of Rights (ROR) | Written communication preserving insurer's right to deny coverage while investigating; must cite specific provisions |
| Subrogation | Insurer's right to pursue recovery from third party responsible for a loss after paying the insured |
| Actual Cash Value (ACV) | Replacement cost minus depreciation; broad evidence rule in majority jurisdictions |
| Replacement Cost Value (RCV) | Cost to repair/replace with like kind and quality without depreciation deduction |
| ALAE | Allocated Loss Adjustment Expense — costs directly attributable to a specific claim |
| ULAE | Unallocated Loss Adjustment Expense — claims overhead not attributable to specific claims |
| Bad Faith | Insurer breach of implied covenant of good faith and fair dealing; statutory, contractual, or tortious |
| SIU | Special Investigations Unit; investigates suspected fraudulent claims |
| Proof of Loss | Formal sworn statement by insured documenting facts and amount of claim |
| EUO | Examination Under Oath; formal sworn examination of insured under cooperation clause |
| Comparative Negligence | Pure (recover regardless of fault), modified (barred at 50%/51%), or contributory (barred at any fault) |
| Occurrence | Event triggering coverage; date of occurrence activates occurrence-based policies |
| Claims-Made Policy | Coverage for claims first made and reported during policy period; distinct late-notice issues |
| Appraisal | Contractual mechanism for resolving amount-of-loss disputes (not coverage): each party selects appraiser; two of three (including umpire) set amount |
| Loss Reserve | Estimated liability for unpaid claims (case reserves + IBNR); subject to actuarial certification |
| Duty to Defend | Obligation to provide and pay for insured's legal defense; triggered by allegations potentially within coverage; broader than duty to indemnify |
| Estoppel and Waiver | Doctrines preventing insurer from asserting coverage defense previously waived or where insured relied to their detriment |
| Tender of Defense | Insured's formal request for insurer to assume third-party claim defense; must be timely and complete |
| Stacking | Combining limits of multiple policies or coverage units; permitted/prohibited varies by state |
| Market Conduct Examination | Formal regulatory audit of insurer business practices including claims handling |
| Period of Restoration | BI coverage period: from physical loss through when property should be repaired with reasonable speed |
| Anti-Concurrent Causation (ACC) | Excludes coverage when covered and excluded perils concurrently cause loss; enforceability varies by jurisdiction |

## Checklist

- [ ] All policy forms, endorsements, and amendments effective at date of loss reviewed and documented — including manuscript endorsements
- [ ] Regulatory timeline compliance verified against governing state (not just NAIC model standards)
- [ ] Denial letter cites exact policy provision (section, paragraph, endorsement number) and specific factual basis
- [ ] Case reserves reflect probable ultimate cost (indemnity + ALAE) — not adjuster authority limits or payment-to-date
- [ ] Investigation scope matches claim complexity and dollar exposure
- [ ] ROR letter issued before conducting investigation under insured's policy when coverage questions exist
- [ ] Subrogation rights identified, documented, and preserved including lien notice and evidence preservation
- [ ] Every SIU referral includes specific documented red-flag indicators
- [ ] Settlement offers and payments approved at proper authority level before communicating to claimant
- [ ] Excess/umbrella carrier notified for claims with exposure potentially exceeding primary limits
- [ ] All communications documented with date, time, participants, and substance; diary entries maintained
- [ ] Comparative negligence applies correct legal standard for applicable jurisdiction with supporting evidence
- [ ] Any automated tools used in triage/valuation/decision-making had human review for coverage determinations and denials per NAIC AI Model Bulletin 2023
- [ ] Claim file stands alone as complete narrative — reviewer unfamiliar with claim understands every decision
- [ ] Policyholder communications clear, timely, and compliant with applicable consumer protection standards

## References
NAIC Model #900/902/903, NAIC AI Model Bulletin 2023, NAIC Third-Party Data and Models Task Force 2024, Leonard v. Nationwide (5th Cir. 2007), Pierce v. Banks Georgia 2023, Dykema Insurance Bad Faith Reports 2024/2025, Hinshaw & Culbertson 2025 Key Insurance Decisions, United Policyholders 2025 National Bad Faith Survey, ABA Liability Claims Guide, IRMI Claims Best Practices, VCA Software 2025
