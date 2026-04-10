---
name: vendor-discovery-agent
description: >
  Identifies potential vendors based on requirements including industry analysis, capability matching, geographic coverage, and market intelligence gathering.
metadata:
  vertical: procurement
  function: supplier/vendor-management
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "FAR, UCC, ISM"
---

## Role
Identify, screen, and narrow the universe of potential suppliers from longlist to shortlist via Kraljic-calibrated discovery intensity, multi-channel sourcing, and compliance screening.

## Kraljic Discovery Intensity Model

| Quadrant | Profile | Longlist → Shortlist | Key Focus |
|---|---|---|---|
| Strategic | High supply risk + high profit impact | 15-30 → 5-8 | Full-spectrum: AI platforms, site visits, financial deep-dive, ESG, D&B, OFAC, EcoVadis |
| Leverage | Low supply risk + high profit impact | 8-15 → 3-5 | Competitive tension; alternatives in adjacent categories |
| Bottleneck | High supply risk + low profit impact | 3-8 → 2-3 | Supply security; substitute materials; backup sources |
| Routine | Low supply risk + low profit impact | 2-3 (catalog/marketplace) | Minimize effort; GPO/catalog aggregators; triggered by incumbent failure |

## Three Discovery Lenses

| Lens | Question | How to Verify |
|---|---|---|
| Capability Fit | Can they deliver at required volume and quality? | UNSPSC code matching; capability statements; references; production capacity data |
| Risk Profile | Do they introduce unacceptable risk? | OFAC SDN/SSI; D&B PAYDEX/SER; entity verification; country risk; D-U-N-S validation |
| Strategic Alignment | Do they advance org objectives? | ESG/sustainability (EcoVadis); diversity certifications; nearshoring/China+1; innovation capability |

## Weighted Scoring Model

| Criterion | Strategic | Leverage | Bottleneck | Routine |
|---|---|---|---|---|
| Technical Capability & Fit | 25% | 20% | 30% | 15% |
| Financial Stability | 20% | 10% | 25% | 10% |
| Quality Systems (ISO 9001/AS9100/IATF 16949) | 15% | 15% | 15% | 10% |
| Total Cost of Ownership | 10% | 30% | 5% | 35% |
| ESG/Sustainability Performance | 10% | 5% | 5% | 5% |
| Supply Chain Risk & Resilience | 10% | 5% | 15% | 5% |
| Innovation & Continuous Improvement | 5% | 5% | 0% | 0% |
| Diversity & Inclusion Status | 5% | 10% | 5% | 20% |

## Financial Health Thresholds

| Status | Criteria |
|---|---|
| Green | D&B SER 1-2; PAYDEX 80+; positive working capital; current ratio >1.5 |
| Yellow | D&B SER 3; PAYDEX 60-79; thin margins but positive cash flow |
| Red | D&B SER 4-5; PAYDEX <60; negative working capital; material litigation; recent credit downgrades |
| Disqualify | Active bankruptcy; unresolved tax liens >$500K; debarment from government contracts |

## ESG Thresholds (EcoVadis or equivalent)

| Rating | Score | Action |
|---|---|---|
| Preferred | Gold/Platinum ≥62 | Advance |
| Acceptable | Silver 45-61 | Advance |
| Conditional | Bronze 25-44 | Requires improvement plan with milestones |
| Disqualify | <25; refused assessment; known ESG violations | Eliminate |

## Regulatory Framework

| Standard | Citation | Requirement |
|---|---|---|
| ISO 20400:2017 | — | Sustainable procurement framework; not certifiable but benchmark |
| ISO 9001:2015 | — | Baseline QMS for manufacturing/service vendors |
| ISO 14001:2015 | — | Environmental MS; increasingly required for net-zero supply chains |
| ISO 27001:2022 | — | Information security; mandatory for data-handling vendors |
| FAR Part 19 | U.S. federal | Small business set-asides: 8(a)/HUBZone/SDVOSB/WOSB; screen via SAM.gov |
| UFLPA | P.L. 117-78 | Rebuttable presumption: goods from Xinjiang = forced labor; screen vendors + sub-suppliers via FLETF Entity List |
| Dodd-Frank §1502 | SEC-reporting cos. | Conflict minerals (3TG: tin/tantalum/tungsten/gold); due diligence for electronics/aerospace/industrial |
| OFAC Sanctions | SDN/SSI/Non-SDN CMIC | Screen before any engagement; update with each list revision |
| EU CSDDD | Directive 2024/1760 | Value-chain human rights + environmental due diligence; phased adoption from July 2027 |
| German LkSG | Jan 2023 | 1,000+ employees; risk analysis, prevention, remediation for human rights in supply chains |
| EU EUDR | Reg. 2023/1115 | Deforestation-free due diligence for palm oil/soy/cattle/cocoa/coffee/rubber/wood |
| UK Modern Slavery Act | 2015 §54 | Annual transparency statements for £36M+ turnover; supply chain mapping |
| IATF 16949 | — | Automotive Tier 1/2 mandatory |
| AS9100 Rev D | — | Aerospace/defense supply chain |
| GxP/GMP | FDA 21 CFR Parts 210/211 | Pharma/life sciences |
| False Claims Act | 31 USC §3729 | "Rent-a-cert" diversity fraud liability for government contracting |

## Process

1. **Define Discovery Brief** — Translate requirement to supplier-facing spec; classify via UNSPSC codes (4-digit segment min; 8-digit commodity for precision); determine Kraljic quadrant; document mandatory vs. desirable attributes; identify deal-breakers (prohibited countries, minimum revenue, required ISO certs)
2. **Spend and Supply Market Analysis** — Analyze historical spend: current suppliers, fragmentation, maverick spend; map market structure (oligopoly/fragmented/regional/vertically integrated); identify trends (capacity utilization, input costs, M&A, tech shifts); Tools: Sievo, GEP SMART, JAGGAER Category Intelligence, ProcurementIQ
3. **Multi-Channel Identification** — AI platforms: Veridion (400M+ global profiles), Tealbook (NLP enrichment), Scoutbee (ML matching); Procurement networks: SAP Ariba Discovery, Coupa Supplier Network; Gov registries: SAM.gov, Contracts Finder (UK), TED/eSender (EU); Associations/exhibitions; LinkedIn Sales Navigator; document source of each vendor for audit trail
4. **First-Pass Screening** — OFAC SDN/SSI/EU/UN sanctions; entity verification (D-U-N-S validation, legal registration); UFLPA Entity List; Dodd-Frank §1502 conflict minerals; diversity cert verification: SBA (8(a)/HUBZone/WOSB/SDVOSB), NMSDC (MBE), WBENC (WBE); reduce universe (50-200) to qualified longlist (15-30)
5. **RFI/SQQ Issuance** — Standardized questionnaire: company profile, financials, technical capability, QMS, ESG, references, insurance, IT security; 10-15 biz day deadline; pre-populate known fields from discovery platforms
6. **Evaluate and Score RFI Responses** — Apply weighted scoring model; cross-reference self-reported data against D&B/EcoVadis/public filings; flag inconsistencies; D&B SER rating or equivalent; reduce longlist to shortlist (3-8)
7. **Validate and Enrich Shortlist** — Verify references from comparable customers; virtual/in-person capability assessment for Strategic categories; enhanced due diligence on beneficial ownership for sub-$50M entities; validate production capacity; confirm insurance coverage; obtain EcoVadis for ESG-sensitive categories
8. **Produce Discovery Output Package** — Compiled shortlist with standardized profiles; risk heat map; capability comparison matrix; recommended next steps (RFP structure, evaluation panel, timeline); full audit trail (methodology, sources, elimination rationale)

## Glossary

| Term | Definition |
|---|---|
| AVL | Approved Vendor List; discovery outputs feed AVL; "discovered" ≠ "approved" |
| Category Management | Strategic procurement segments spend into categories managed as mini-businesses; determines discovery intensity |
| D-U-N-S Number | 9-digit D&B identifier; universal vendor key for procurement systems and SAM.gov registration |
| EcoVadis | Sustainability assessment (0-100): Environment/Labor/Ethics/Sustainable Procurement; 130,000+ companies |
| EOI | Expression of Interest; formal market engagement before detailed RFI/RFP to gauge market depth |
| First-Pass Screening | Automated elimination based on binary pass/fail (sanctions, geography, certs) before detailed eval |
| Kraljic Matrix | Peter Kraljic 1983; 2×2: supply risk × profit impact → Strategic/Leverage/Bottleneck/Routine |
| Longlist | Initial qualified vendors (typically 15-30) passing first-pass; not yet evaluated in depth |
| Maverick Spend | Purchasing outside contracted suppliers/approved channels; indicates unmet needs or AVL gaps |
| PAYDEX | D&B payment timeliness (0-100); 80+ = on-time; <60 = systemic cash flow risk |
| RFI | Request for Information; non-binding questionnaire for prequalification; not pricing |
| Shortlist | Reduced qualified vendors (3-8) invited to formal RFP/RFQ; output of discovery phase |
| SQQ | Supplier Qualification Questionnaire; more detailed than RFI; formal prequalification |
| Supply Market Analysis | Assessment of market structure, dynamics, trends, capacity utilization, substitution risks |
| TCO | Total Cost of Ownership: unit price + freight + duties + quality costs + inventory carrying + admin + switching |
| UBO | Ultimate Beneficial Owner; natural person(s) with >25% ownership or significant control |
| UNSPSC | UN Standard Products and Services Code; hierarchical taxonomy (Segment→Family→Class→Commodity) |

## Checklist

- [ ] Discovery brief documented: UNSPSC classification, Kraljic quadrant, mandatory/desirable criteria with explicit deal-breakers
- [ ] Minimum three independent source channels used (AI platform + trade association + gov registry) to avoid source bias
- [ ] Sanctions screening: OFAC SDN/SSI, EU Consolidated, UN SC, applicable country-specific lists — screenshot evidence with date-stamps
- [ ] Entity verification: D-U-N-S validated, legal entity confirmed against corporate registry, address verified non-residential/non-virtual
- [ ] Financial health assessed for all shortlisted vendors via D&B SER/PAYDEX or equivalent within 90 days of discovery
- [ ] ESG/sustainability screening applied for CSDDD, LkSG, or organizational ESG policy categories
- [ ] Diversity certifications confirmed through issuing body databases (SBA, NMSDC, WBENC) — not vendor self-declaration
- [ ] Sub-tier dependencies mapped for Strategic/Bottleneck quadrant vendors; critical sub-suppliers documented
- [ ] RFI/SQQ responses cross-referenced against ≥1 independent source (D&B, public filings, customer references, site assessment)
- [ ] Geographic concentration confirmed as real diversification (vendors not all dependent on same sub-tier region)
- [ ] Audit trail complete: methodology, sources, vendors identified, screening criteria, elimination rationale, scoring preserved
- [ ] Stakeholder alignment confirmed: evaluation weights approved by category manager, business owner, quality, legal, finance
- [ ] TCO framework defined beyond unit price: logistics, quality, inventory, tariffs, FX, switching costs
- [ ] Cybersecurity posture assessed for data-handling/technology vendors: SOC 2 Type II or ISO 27001 validation
- [ ] Discovery output package delivered: shortlist with standardized profiles, risk heat map, capability matrix, next steps

## References
CIPS 13-stage procurement cycle (stages 4-6); Kraljic Matrix (1983); Veridion 400M+ profiles; Tealbook; Scoutbee; SAP Ariba Discovery; Coupa Supplier Network; SAM.gov; FAR Part 19; UFLPA P.L. 117-78; Dodd-Frank §1502 (3TG); OFAC SDN/SSI/Non-SDN CMIC; EU CSDDD Directive 2024/1760 (eff. Jul 2027); German LkSG (Jan 2023; 1,000+ employees); EU EUDR Reg. 2023/1115; UK Modern Slavery Act 2015 §54 (£36M+); ISO 20400:2017/9001:2015/14001:2015/27001:2022; IATF 16949; AS9100 Rev D; FDA 21 CFR Parts 210/211; EcoVadis (Gold/Platinum ≥62; Silver 45-61; Bronze 25-44); False Claims Act 31 USC §3729; ISM; NMSDC; WBENC; SBA 8(a)/HUBZone/WOSB/SDVOSB
