---
name: lead-qualification
description: >
  Lead qualification frameworks including BANT, MEDDIC, and CHAMP methodologies for identifying and prioritizing sales-ready opportunities.
metadata:
  vertical: sales
  function: pipeline
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "FTC, CAN-SPAM, TCPA"
---

## Role
Filter and prioritize prospects using BANT/MEDDIC/CHAMP/MEDDPICC to identify sales-ready opportunities and maintain trustworthy pipeline.

## Framework Selection Matrix

| Sales Context | Framework | Deal Size | Cycle | Stakeholders |
|---|---|---|---|---|
| Transactional/high-velocity | BANT | <$25K | <30 days | 1-3 |
| Mid-market/consultative | CHAMP | $25K-$100K | 1-3 months | 3-6 |
| Enterprise/complex | MEDDIC | $50K-$500K | 3-9 months | 5-10 |
| Enterprise + procurement | MEDDPICC | $100K+ | 6-12 months | 5-15+ |
| Hybrid (two-tier) | BANT → MEDDIC | Variable | Variable | Variable |

## BANT Scoring (Quick Qualification)

| Criterion | Confirmed (2 pts) | Partial (1 pt) | Unknown/Absent (0 pts) |
|---|---|---|---|
| Budget | Allocated; amount discussed | General awareness; "need to find budget" | No budget; "none this year" |
| Authority | DM identified and engaged | Influencer engaged; DM not met | No purchasing authority |
| Need | Specific use case + business impact | General interest; "exploring" | No clear need |
| Timeline | Active project with target date | "Sometime this quarter" | "Just looking" |

**Threshold: 5/8 = advance. <4 = nurture or disqualify.**

## MEDDPICC Scoring (Complex Deal Inspection)

| Element | Score 3 | Score 2 | Score 1 | Score 0 |
|---|---|---|---|---|
| Metrics | Quantified ROI/KPI agreed | General business goals | Vague value prop | Not discussed |
| Economic Buyer | Identified, met, engaged, supportive | Identified and met | Identified, no access | Unknown |
| Decision Criteria | Documented, weighted in your favor | Known, neutral | Partial understanding | Unknown |
| Decision Process | Full process mapped + timeline | Key steps known | High-level | Black box |
| Paper Process | Legal/procurement documented | General awareness | Know it exists | Not explored |
| Identify Pain | Pain quantified in $ impact | Clearly articulated | Acknowledged generally | Not surfaced |
| Champion | Advocate who has taken action | Supportive + influence | Friendly, no action | None |
| Competition | Mapped; differentiation clear | Know competitors | Suspect competition | No visibility |

**Max: 24. Pipeline threshold: 15+ (63%). Commit forecast: 17+ (71%).**

## CHAMP Scoring (Consultative)
Score each 1-5: Challenges (specificity/urgency), Authority (DM access + buying committee), Money (budget available or createable), Prioritization (rank vs. other initiatives). **Threshold: 14/20 for opportunity creation.**

## Lead Scoring Lifecycle Stages

| Stage | Score Range | Definition |
|---|---|---|
| IQL | 0-29 | Exchanged contact for content; no sustained engagement |
| MQL | 30-59 | Meets marketing engagement thresholds; not sales-validated |
| SAL | 60-74 | MQL reviewed and accepted by sales rep within SLA |
| SQL | 75+ | Passed discovery conversation; meets framework criteria for pipeline |

**Explicit scoring** (firmographics): company size +15, target industry +20, DM title +25; out-of-territory −20, student email −30.
**Implicit scoring** (behavioral): pricing page +20, demo request +30, case study download +10, webinar +15, return visit ≤7 days +10; −5/week inactivity.

## Process

**Stage 1 — Pre-Qualification (Automated/Marketing)**
1. Enrich lead data: Clearbit/ZoomInfo/Apollo for firmographic (size/industry/revenue/geo) and technographic (tech stack) attributes
2. Apply ICP fit scoring (explicit criteria as go/no-go gate)
3. Apply behavioral engagement scoring (implicit signals for prioritization)
4. Classify into lifecycle stage (IQL/MQL/SAL/SQL)

**Stage 2 — SDR/BDR Qualification (Framework Application)**
5. Select framework per deal context (see selection matrix)
6. Conduct discovery call applying framework criteria; each element scored 0-3 (unknown → strongly confirmed with evidence)
7. Apply advancement threshold: 60-70%+ of maximum score required; best-in-class 70%+ for commit forecast

**Stage 3 — SAL Handoff & Validation**
8. AE reviews and accepts/returns within 24-48 hours SLA; acceptance = MQL → SAL
9. AE conducts deeper qualification (MEDDIC/MEDDPICC); verifies SDR findings; fills gaps (Champion, Paper Process, Competition)
10. Qualified → pipeline opportunity with stage/close date/weighted value; unqualified → nurture with tags

**Stage 4 — Ongoing Deal Inspection**
11. Re-qualify at every stage gate; framework criteria re-evaluated before each advancement
12. Weekly pipeline reviews: MEDDPICC scores for all committed deals; flag any <70%
13. Update scores on new intelligence: champion leaves, competitor enters, budget cycle shifts

## Glossary

| Term | Definition |
|---|---|
| IQL | Information Qualified Lead — contact exchanged for content; no buying intent |
| MQL | Marketing Qualified Lead — meets engagement thresholds; not sales-validated |
| SAL | Sales Accepted Lead — MQL accepted by sales rep within agreed SLA |
| SQL | Sales Qualified Lead — vetted via discovery; meets framework criteria for pipeline |
| PQL | Product Qualified Lead — identified via product usage signals (PLG motion) |
| BANT | Budget/Authority/Need/Timeline — IBM-originated; transactional <$25K |
| MEDDIC | Metrics/Economic Buyer/Decision Criteria/Decision Process/Identify Pain/Champion — PTC 1990s; complex multi-stakeholder |
| MEDDPICC | MEDDIC + Paper Process + Competition; 73% of SaaS >$100K ARR use variant (SalesMotion 2025) |
| CHAMP | Challenges/Authority/Money/Prioritization — consultative mid-market; leads with pain |
| GPCTBA/C&I | Goals/Plans/Challenges/Timeline/Budget/Authority/Negative Consequences/Positive Implications — HubSpot |
| FAINT | Funds/Authority/Interest/Need/Timing — unplanned purchasing without traditional budget allocation |
| Economic Buyer | Individual with final approval authority; verified by past contract signing or stakeholder corroboration |
| Champion | Internal advocate: (a) wants you to win, (b) has influence demonstrated by actions, (c) shares intelligence |
| Compelling Event | External/internal deadline creating urgency (contract expiry/regulatory/board mandate/system EOL); absence = 3× no-decision risk |
| Explicit Scoring | Points for stated/verifiable attributes (title/size/industry/geo); measures your interest in prospect |
| Implicit Scoring | Points for behavioral signals (page views/downloads/demo requests); measures prospect's interest in you |
| Score Degradation (Decay) | Automatic score reduction from inactivity; prevents stale leads appearing sales-ready |
| Pipeline Coverage Ratio | Pipeline value ÷ quota; standard: 3× enterprise, 4× mid-market |
| Pipeline Velocity | (# opportunities × avg deal value × win rate) ÷ avg sales cycle length |
| Multi-Threading | Engaging multiple account stakeholders; reduces single-point-of-failure risk |
| Closed-Lost: No Decision | Prospect bought from no vendor; distinct from competitive loss; strongest qualification failure indicator |
| Paper Process | Post-verbal legal/procurement/security/compliance steps; source of 40%+ post-verbal attrition |
| ICP | Ideal Customer Profile — firmographic/technographic definition; anchor for fit-based scoring |
| SLA (Sales/Marketing) | Documented handoff timing (e.g., MQL actioned ≤24 hrs), response expectations, feedback cadence |

## Checklist

- [ ] ICP documented with firmographic criteria (employee count range, revenue band, industries, geos) and negative filters; reviewed quarterly
- [ ] Single qualification framework selected and enforced in CRM; custom fields for every element with dropdowns (not free text)
- [ ] Operational definitions for every framework criterion: written "confirmed" definition with acceptable evidence examples
- [ ] Lead scoring uses both fit (explicit) and engagement (implicit) dimensions with separate scores
- [ ] Negative scoring and decay rules implemented; disqualifying attributes carry negative values
- [ ] MQL→SAL→SQL handoff criteria documented and agreed; marketing and sales signed off; reviewed quarterly
- [ ] Disqualification criteria explicit; disqualification rate tracked as positive metric (~20% target)
- [ ] Win/loss analysis separately tracks "no decision" outcomes as distinct category
- [ ] Champion validation requires documented action (introduced to EB, arranged meeting, shared intel) — not just stated support
- [ ] Framework scores reviewed in weekly pipeline reviews; committed deals below threshold get remediation plan or move to nurture
- [ ] Lead response SLA ≤5 minutes for high-intent actions (demo requests, pricing page, inbound calls)
- [ ] Re-qualification at every pipeline stage gate (especially Champion, Timeline, Competition)
- [ ] Compliance controls embedded in outreach: CAN-SPAM unsubscribe, TCPA consent verification, GDPR legitimate interest, suppression list checks automated
- [ ] Scoring model recalibrated quarterly against retrospective closed-won conversion analysis

## References
CAN-SPAM 15 USC §7701 ($53,088/violation; opt-out ≤10 biz days); TCPA 47 USC §227 (one-to-one consent rule eff. Jan 27, 2025; prior express written consent for autodialed/prerecorded to mobile); GDPR Articles 6 & 22 (automated decision-making transparency; fines ≤€20M or 4% global revenue); CCPA/CPRA (data deletion/opt-out); CASL (express/implied consent; implied = 6 mo inquiry/2 yr purchase; $10M CAD/violation); TCPA consent retention ≥4 years; Ebsta × Pavilion B2B Benchmark 2025 (19% win rate; 70% miss quota; top performers 366% more likely to disqualify at Discovery); SalesMotion 2025; SiriusDecisions (aligned MQL definition = 24% faster revenue growth); MarketSource 2024 (89% of B2B purchases stalled)
