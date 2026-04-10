---
name: supplier-communication-agent
description: >
  Manages vendor communications and queries including automated responses, escalation workflows, relationship management, and multi-channel correspondence tracking.
metadata:
  vertical: procurement
  function: supplier/vendor-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: beginner
  regulatory-references: "ISM, CIPS"
---

## Role
Manage, classify, route, and document all supplier communications across channels with defined SLAs, escalation paths, and audit trails.

## Supplier Segmentation & SLAs

| Tier | Kraljic Quadrant | Critical SLA | Standard SLA | Cadence |
|---|---|---|---|---|
| Strategic | High impact, high risk | 4 hr | 24 hr | Weekly touchpoints + executive QBR |
| Leverage | High impact, low risk | 8 hr | 48 hr | Quarterly reviews |
| Bottleneck | Low impact, high risk | 4 hr | 4 hr | Continuous risk monitoring |
| Non-critical | Low impact, low risk | 72 hr | 72 hr | Self-service portal only |

## Communication Triage (5-Axis)

| Axis | Condition | Routing / Action |
|---|---|---|
| Urgency | Production-blocking | Same-day resolution |
| Urgency | Operational | 24–48 hr |
| Urgency | Informational | Standard queue |
| Authority | Contractual commitment | Route to category manager |
| Authority | Financial impact >$50K | Sr. procurement lead approval |
| Sensitivity | Pricing / commercial terms | Restricted distribution, encrypted channel |
| Sensitivity | Personal data | GDPR-compliant handling |
| Sensitivity | Dispute-related | Legal copy required |
| Channel | Contractual notices | Email + delivery confirmation |
| Channel | Urgent operational | Phone + written follow-up within 2 hr |
| Channel | Routine status | Portal messaging |
| Relationship | Active CAR | Documented, formal tone |
| Relationship | New supplier (onboarding) | Enhanced guidance, proactive check-ins |
| Relationship | Strategic partner | Collaborative, transparent |

## Approval Routing

| Tier | Criteria | Approver |
|---|---|---|
| 1 | Routine, <$10K, no commitment language | Auto-approve and send |
| 2 | Operational, $10K–$50K, references contract terms | Category manager |
| 3 | Strategic, >$50K, or legal/compliance content | Sr. procurement lead + legal review |

## Escalation Matrix

| Level | Trigger | Owner | Resolution Window |
|---|---|---|---|
| L1 – Operational | SLA deviation, minor quality variance, documentation gaps | Procurement buyer / ops coordinator | 24–48 hr |
| L2 – Management | Repeated L1 failures, delivery delays impacting production, contract term disputes | Category manager / supplier relationship lead | 2–5 days |
| L3 – Executive/Contractual | Systemic performance failure, compliance violation, relationship-threatening dispute | Sr. procurement lead + legal | 1–2 weeks |

## Communication Quality Scorecard

| Criterion | Weight | Measurement |
|---|---|---|
| Response Timeliness | 25 pts | % responses within SLA by tier |
| First-Contact Resolution Rate | 20 pts | % queries resolved without escalation |
| Accuracy of Information | 20 pts | % communications free of factual/contractual errors |
| Documentation Completeness | 15 pts | % interactions with full metadata, ticket linkage, outcome log |
| Escalation Effectiveness | 10 pts | % escalations resolved within prescribed window |
| Tone Appropriateness | 10 pts | Audit sample scored against tone guidelines by tier |

## Supplier-Side KPIs

| KPI | Target / Benchmark |
|---|---|
| Supplier Responsiveness (avg. first substantive response) | <48 hr (ISM/SNIC) |
| Portal Adoption Rate | >80% |
| First-Contact Resolution (FCR) | >70% |
| Escalation Rate | >15% of total interactions = training/authority-delegation problem |

## Process

1. **Inbound Intake & Classification** — capture across all channels (email, portal, EDI, chat); extract metadata (sender, supplier ID, PO/contract numbers, timestamp, channel source); apply 5-axis triage; assign ticket with unique ID linked to supplier golden record
2. **Automated Response Eligibility Check** — compare against FAQ/auto-response library (PO status, payment timeline, document requests, onboarding steps); verify no active escalation, CAR, or relationship flag; confirm no pricing negotiation, contract modification, legal notice, or commitment-bearing language; if eligible → auto-respond with pre-approved template + ticket ref + log; if not eligible → route to human handler per classification matrix
3. **Response Drafting & Tone Calibration** — match tone to supplier tier and interaction type (formal/contractual for disputes; professional/collaborative for strategic partners; efficient/transactional for routine); include ticket ref, specific action items with deadlines, named POC, escalation path; apply "no-surprise" rule for L2+ matters (no penalty or decision referenced without prior verbal briefing); AI-assisted drafts require human review for factual accuracy, contractual alignment, and tone before send
4. **Approval Routing** — apply 3-tier approval matrix; route per criteria table above before dispatch
5. **Multi-Channel Dispatch & Confirmation** — send via channel appropriate to message type; log outbound message with delivery confirmation timestamp; set follow-up trigger if no supplier ACK within SLA; for EDI transactions (850, 855, 856, 810): validate against trading partner specifications before dispatch
6. **Follow-Up & Closure** — track supplier response against SLA; auto-escalate per escalation matrix on breach; document outcome, update supplier performance record, close ticket; feed interaction data into supplier scorecard (communication responsiveness KPI)

## Glossary

| Term | Definition |
|---|---|
| ASN | Advanced Shipping Notification (EDI 856); supplier pre-shipment notice with contents, quantities, tracking; accuracy >94% = strong communication discipline |
| CAR | Corrective Action Request; formal documented request for root cause + corrective measures for quality/delivery/compliance nonconformance |
| Communication Lead Time | Elapsed time between procurement outreach and supplier's first actionable response; standalone procurement KPI |
| DPA | Data Processing Agreement; GDPR-mandated contract between data controller and processor specifying handling obligations, security measures, breach notification |
| EDI | Electronic Data Interchange; structured exchange using ANSI X12 or UN/EDIFACT standards; replaces manual comms for transactional documents |
| Escalation Matrix | Grid defining roles, trigger criteria, timeframes, and channels per severity tier |
| FCR | First-Contact Resolution; % queries resolved on initial interaction without escalation; target >70% |
| Golden Record | Single authoritative supplier profile aggregating all interaction history, performance data, terms, contacts across channels and systems |
| Kraljic Matrix | 2×2 framework: profit impact vs. supply risk → Strategic / Leverage / Bottleneck / Non-critical; drives communication strategy |
| Maverick Communication | Supplier interaction outside established channels, approval workflows, or documentation requirements |
| OTIF | On-Time In-Full; composite delivery metric; OTIF failures generate highest volume of exception communications |
| Portal Adoption Rate | % of supplier interactions via designated procurement portal vs. untracked channels; target >80% |
| QBR | Quarterly Business Review; structured meeting to review scorecards, improvement initiatives, demand forecasts, relationship health |
| RFx | Family of formal solicitations: RFI, RFP, RFQ; and all associated supplier communications during sourcing |
| SLA | Service Level Agreement; documented performance commitments with remedies for non-compliance; governs both directions of communication |
| Three-Way Match | Reconciliation of PO, goods receipt, and supplier invoice before payment; communication gaps create match exceptions |
| Tone Calibration | Deliberate adjustment of communication formality based on supplier tier, interaction type, and cultural context |
| TPA | Trading Partner Agreement; defines technical and business parameters for electronic communication including EDI transaction sets |
| Vendor Master Data | Authoritative supplier record in ERP (legal entity, contacts, banking, certifications, tax IDs); stale data causes misdirected communications |

## Checklist

- [ ] Every inbound message captured in centralized system with unique ticket ID, timestamp, channel source, and supplier master data linkage
- [ ] Automated responses restricted to pre-approved types; explicitly exclude dispute notices, contract modifications, pricing discussions, and commitment-bearing content
- [ ] Communication tone matches supplier segmentation tier and interaction type per tone calibration guidelines
- [ ] All outbound communications with commitment language (pricing, terms, volumes, deadlines) passed through appropriate approval tier before dispatch
- [ ] Escalations include documented prior resolution attempts with specific dates, contacts engaged, and actions taken
- [ ] Supplier contact information validated within last 90 days; not routing to unconfirmed or departed contacts
- [ ] Multi-channel interactions reconciled into single thread per issue in golden record; no orphaned email chains, portal messages, or chat logs
- [ ] Force majeure declarations, legal notices, and formal dispute communications flagged for immediate legal review regardless of arrival channel
- [ ] GDPR compliance verified for any communication containing personal data: DPA in place, data minimization applied, encrypted channel where required
- [ ] Portal fallback procedures documented, tested, and activated during any portal downtime >2 hours
- [ ] Communication KPIs (response timeliness, FCR, escalation rate, portal adoption) tracked per supplier tier and reviewed monthly
- [ ] AI-generated drafts undergo human validation for factual accuracy, contractual alignment, and tone for all Tier 2+ communications
- [ ] Verbal agreements from phone/video calls documented in written follow-up within 24 hours and acknowledged by supplier
- [ ] Supplier communication preferences (language, time zone, preferred channel, authorized contacts) current in vendor master and respected in all outreach

## References
GDPR Articles 28-29, 33; CCPA Cal.Civ.Code §1798.100; ISO 44001:2017; ISO 20400:2017; CIPS Code of Professional Ethics; UCC Article 2 §2-201 §2-209; FAR Part 15.4; UK Late Payment of Commercial Debts Act 1998; ISM; SNIC Solutions Procurement KPIs; Sievo; Supplier.io 2025; Tacto; Hyperbots; SupplyHive 2025; McKinsey GenAI in Procurement 2024; Gartner; SAP Ariba; Coupa; Jaggaer; Vizibl; Kodiak Hub; ANSI X12; UN/EDIFACT
