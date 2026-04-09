---
name: contract-review-analysis
description: >
  Commercial contract review and analysis including risk identification, clause-by-clause review, markup preparation, and negotiation recommendations.
metadata:
  vertical: legal
  function: contract-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: advanced
  regulatory-references: "UCC, Restatement of Contracts"
---

## Role
Conduct structured, multi-stage commercial contract review to identify legal and financial risks, verify regulatory compliance, and align terms with organizational objectives.

## Decision Framework (5 Layers)

| Layer | Focus |
|-------|-------|
| 1 — Context & Authority | Who is counterparty? What contract type? Whose paper? Deal value/strategic importance? Governing law? |
| 2 — Structural Integrity | Defined terms consistent? Cross-references resolve? Exhibits/schedules attached? Recitals accurate? Parties correctly identified? |
| 3 — Risk Allocation | Financial exposure (caps/waivers/LDs) + Operational risk (SLAs/acceptance) + Legal/regulatory + IP/data + Termination + Force majeure |
| 4 — Playbook Deviation | Compare each material clause to preferred/acceptable/fallback; flag severity: (a) acceptable, (b) negotiate within authority, (c) escalate, (d) deal-breaker |
| 5 — Negotiation Strategy | Per flagged deviation: specific risk created + recommended language + business rationale counterparty can understand + fallback position |

## Contract Risk Rating

| Rating | Description | Action |
|--------|-------------|--------|
| Green — Low Risk | Substantially aligns with preferred/acceptable positions; standard commercial terms | Approve with minor comments |
| Yellow — Moderate Risk | Deviations within fallback range; some non-standard but market-common terms | Negotiate specific provisions; reviewer sign-off required |
| Orange — Elevated Risk | Material deviations; unbalanced risk allocation; missing key protections; potential compliance gaps | Escalate to senior counsel; business sponsor acknowledges risk |
| Red — High Risk | Deal-breaker provisions; unlimited liability; regulatory non-compliance; fundamentally unbalanced | Reject or require fundamental restructuring; escalate to GC |

## Risk Scoring Model

| Factor | Scale | Formula |
|--------|-------|---------|
| Likelihood | 1–5 | How probable is this provision triggered? |
| Impact | 1–5 | Financial/operational/reputational consequence |
| Controllability | 1–5 | Can org mitigate operationally without contract change? |
| Priority Score | — | Likelihood × Impact × (6 − Controllability) |

>60 = immediate attention; 30–60 = negotiate; <30 = may be acceptable

## Regulatory Requirements

| Requirement | Key Obligation |
|-------------|---------------|
| UCC Article 2 §2-201 | Statute of Frauds: written agreement required for goods ≥$500 |
| UCC Article 2 §2-207 | Battle of the Forms: acceptance with additional terms forms contract; additional terms become part between merchants unless material alteration |
| UCC Article 2 §2-302 | Unconscionability |
| UCC Article 2 §2-316(2) | Warranty disclaimer of merchantability must name "merchantability" AND be conspicuous (ALL CAPS or bold) |
| UCC Article 2 §2-719 | Limitation of remedies; consequential damages limitation for personal injury from consumer goods prima facie unconscionable |
| Restatement (2d) §90 | Promissory Estoppel |
| Restatement (2d) §213 | Integrated Agreements: fully integrated agreement discharges all prior agreements |
| Restatement (2d) §356 | Liquidated damages clause fixing unreasonably large damages = unenforceable penalty |
| CISG | Applies automatically to cross-border goods sales between contracting states unless expressly excluded |
| GDPR Article 28 | Mandatory DPA for controller-processor: subject matter, duration, nature/purpose, data types, data subject categories, confidentiality, security, sub-processor controls, audit rights, deletion/return |
| CCPA/CPRA Cal. Civ. Code §1798.100 | Service provider/contractor agreements: restrict use to specified business purposes; prohibit selling/sharing; audit rights; CPPA enforcement active since Mar 2024 |
| EU Standard Contractual Clauses (Commission Implementing Decision 2021/914) | Required for EEA international data transfers; must be used unmodified; correct module required (Controller-to-Processor, etc.) |
| ABA Model Rule 1.1 (Competence) | Legal knowledge, skill, thoroughness including technology competence per Comment 8 |
| ABA Model Rule 1.3 (Diligence) | Reasonable diligence and promptness; failure to timely review = potential malpractice |
| ABA Model Rule 1.4 (Communication) | Keep clients informed of material developments |
| Dodd-Frank §§721–774 | Swap documentation for financial services |
| OCC Guidance 2023-17 | Third-Party Relationships guidance |
| HIPAA 45 CFR §164.502(e) | Business Associate Agreements |
| FAR mandatory clauses | Government contracts flow-down requirements |

## Process

### Step 1: Pre-Review Intake
- Confirm business context: deal value, relationship history, strategic importance, timeline pressure
- Identify contract type and applicable legal frameworks (UCC Art. 2, common law, CISG, specific regulations)
- Determine buy-side vs. sell-side and whose paper the draft is based on
- Gather prior versions, term sheets, LOIs, or related agreements

### Step 2: First-Pass Structural Review
- Verify all party names match legal entity names and jurisdictions of organization
- Confirm effective date mechanism (execution vs. specified date vs. last signature)
- Check defined terms: all used terms defined; consistent usage throughout
- Verify all cross-references, exhibit references, and schedule references resolve correctly
- Confirm proper signature blocks with authority representations
- Flag missing standard sections (definitions, reps, covenants, termination, general provisions)

### Step 3: Clause-by-Clause Substantive Analysis
**Scope & Deliverables**: Obligations specific and measurable? Acceptance criteria defined? Scope creep risk from "including but not limited to"?

**Payment & Financial Terms**: Payment triggers (milestones vs. calendar)? Pricing adjustment mechanisms (CPI, market rate)? Late payment interest rates and grace periods?

**Reps & Warranties**: Distinguish representations (existing fact) from warranties (future condition). Knowledge qualifiers? Survival periods?

**Indemnification**: First-party vs. third-party scope; trigger events; exclusions; notice/cooperation/control procedures; carve-out from or subject to LoL cap; mutual or unilateral?

**Limitation of Liability**: Cap structure (fixed dollar, fees-paid, hybrid, per-claim vs. aggregate)? What is capped vs. carved out (IP infringement, confidentiality breach, willful misconduct, gross negligence)? Consequential damages waiver mutual?

**Termination**: Convenience (notice period, wind-down); cause (material breach standard, cure period adequacy); insolvency; automatic expiration; post-termination obligations (data return/destruction, survival of confidentiality, transition assistance)

**IP**: Pre-existing IP, newly created IP, derivative works ownership. License scope (exclusive/non-exclusive, perpetual/term, transferable). Present-tense assignment language ("hereby assigns")?

**Data Protection**: GDPR Art. 28 DPA requirements? CCPA/CPRA service provider provisions? Correct EU SCC module (Commission Implementing Decision 2021/914)?

**Confidentiality**: Definition scope; exclusions (independently developed, publicly known, legally compelled); permitted disclosures; duration; remedies; injunctive relief specified?

**Force Majeure**: Post-pandemic events explicitly included (epidemics, government orders, supply chain)? Mitigation obligations? Long-stop termination rights? Financial inability excluded?

**Governing Law & Dispute Resolution**: Intentional and favorable governing law? Arbitral institution (AAA/JAMS/ICC), seat, arbitrators, language, provisional remedies carve-out?

### Step 4: Risk Scoring & Prioritization
Apply Likelihood × Impact × (6 − Controllability) formula per clause. Document Priority Scores.

### Step 5: Markup Preparation
- Use tracked changes — never edit without change tracking
- Accept counterparty's prior redlines before adding your own edits (one generation of changes only)
- Add explanatory comments for every substantive change explaining business rationale
- Propose alternative language — not just deletions
- Apply fallback positions where preferred position likely rejected
- Use clear version naming: `[ContractName]_v3_[YourOrg]Redline_[Date]`

### Step 6: Negotiation Recommendations Memo
- Executive summary of 3–5 material risk issues in plain language
- Prioritized list of requested changes with business impact explanation
- Recommended negotiation strategy: concede first vs. hold firm
- Deal-breaker identification with alternative structuring suggestions
- Comparison to market-standard terms where applicable

### Step 7: Final Review & Execution
- Compare final "clean" version against last redline using document comparison tool — not visual inspection
- Verify no "silent redlines" introduced by counterparty
- Confirm all exhibits, schedules, and attachments complete and correctly referenced
- Verify signature authority for all signing parties

## Glossary

| Term | Definition |
|------|-----------|
| Redline (Markup) | Contract showing proposed changes via tracked changes; only one generation visible per exchange |
| Playbook | Internal reference: preferred, acceptable, fallback positions per clause with escalation rules for deviations |
| Clause Library | Centralized repository of pre-approved contract clauses by category, risk level, industry, jurisdiction |
| Limitation of Liability (LoL) Cap | Maximum aggregate monetary exposure; fixed dollar, fees-paid, or hybrid; carve-outs exclude specified categories |
| Consequential Damages Waiver | Excludes indirect/special/incidental/consequential damages; enforceable when conspicuous and mutual |
| Indemnification | Obligation for indemnitor to compensate indemnitee for specified losses; defines what is covered (vs. LoL which caps how much) |
| Reps & Warranties | Representations = statements of existing fact; Warranties = assurances of future condition; "bring-down" confirms accuracy at closing |
| MAC/MAE | Material Adverse Change/Effect: allows termination/non-closing if circumstances change materially; Akorn v. Fresenius Kabi (Del. 2018) = Delaware standard |
| Integration Clause | Entire agreement supersedes all prior negotiations; per Restatement (2d) §213 prevents parol evidence |
| Force Majeure | Excuses non-performance from extraordinary events beyond control; exists only if expressly contracted under U.S./English common law |
| Battle of the Forms | UCC §2-207: acceptance with additional terms forms contract; additional terms between merchants become part unless materially alter |
| Survival Clause | Specifies obligations continuing after termination/expiration; absence = obligations expire at termination |
| MFN Clause | Most Favored Nation: guarantees pricing/terms at least as favorable as any other customer; antitrust risk if used by market-power party |
| Liquidated Damages | Pre-agreed remedy; enforceable when actual damages difficult to calculate and amount is reasonable forecast (Restatement §356) |
| DPA | Data Processing Agreement; mandatory per GDPR Art. 28 for controller-processor relationships |
| Change of Control | Grants termination rights or consent requirements if party undergoes M&A or majority ownership change |
| Cure Period | Window (typically 15–60 days; 5–15 for payment) to remedy material breach before termination rights exercisable |
| Fallback Position | Furthest position organization will accept before requiring senior approval or rejecting term |
| Super Cap | Secondary higher liability cap for categories carved out from general LoL (IP infringement, data breaches) |
| Order of Precedence | Establishes which document controls in conflicts (master agreement vs. SOW vs. order form); absence = courts interpret contra proferentem |

## Checklist

- [ ] Party verification: all parties identified by correct legal names, jurisdictions, authorized signatories confirmed
- [ ] Defined terms audit: every capitalized term has corresponding definition; no orphan definitions; no undefined capitalized terms
- [ ] Cross-reference verification: all internal references resolve correctly; no broken or circular references
- [ ] Liability exposure mapping: all LoL caps, carve-outs, indemnification obligations, consequential damages waivers identified and quantified; cumulative exposure calculated
- [ ] Regulatory compliance verification: GDPR Art. 28 DPA requirements met; CCPA/CPRA service provider provisions included; industry-specific mandatory clauses present (HIPAA BAA, FAR flow-downs)
- [ ] Termination rights analysis: all triggers identified (convenience, cause, insolvency, force majeure, change of control); cure periods assessed; post-termination obligations verified
- [ ] IP ownership clarity: work product ownership, pre-existing IP licensing, derivative works rights explicitly addressed
- [ ] Playbook deviation documentation: all deviations logged, risk-rated, and escalated per authority matrix
- [ ] Boilerplate clause review: integration clause doesn't exclude prior-agreed terms; assignment clause restricts transfers; governing law and dispute resolution aligned
- [ ] Force majeure: post-pandemic events addressed; mitigation obligations included; long-stop termination right exists; financial inability excluded
- [ ] Document comparison completed: final vs. last negotiated redline; no silent redlines
- [ ] Consistency check: no internal contradictions between body and exhibits/schedules; order of precedence clause included
- [ ] Warranty disclaimer conspicuousness: UCC §2-316 requirement met (ALL CAPS or bold where required)
- [ ] Data protection provisions: sub-processor controls, audit rights, breach notification timelines, data deletion/return, international transfer mechanisms addressed

## References
WorldCC Most Negotiated Terms 2024, UCC Article 2 (Cornell LII), CISG, ABA Model Rules 1.1/1.3/1.4, Nada Alnajafi Contract Redlining Etiquette, GDPR Art. 28, EU SCCs 2021 (Commission Implementing Decision 2021/914), CCPA/CPRA CPPA Regulations, ACC Indemnification/LoL Presentation 2024, Restatement (Second) of Contracts §§90/213/356, Akorn v. Fresenius Kabi (Del. 2018), VFLA Eventco v. William Morris Endeavor (Cal. Ct. App. 2024), Dodd-Frank §§721–774, OCC Guidance 2023-17, HIPAA 45 CFR §164.502(e)
