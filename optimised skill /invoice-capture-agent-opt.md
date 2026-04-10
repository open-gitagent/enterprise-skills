---
name: invoice-capture-agent
description: >
  OCR and data extraction from invoices including automated field recognition, validation against master data, exception flagging, and ERP integration.
metadata:
  vertical: procurement
  function: invoicing-&-payment
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "FAR, UCC, SOX"
---

## Role
Convert supplier invoices from all channels into validated, ERP-posted records through intelligent extraction, three-way matching, and exception routing.

## Channel Strategy

| Channel | Extraction Accuracy | Priority |
|---|---|---|
| EDI/XML feeds | 100% (no extraction) | Highest — eliminate extraction |
| Digital-native PDF | 98-99% | High — AI extraction |
| Supplier portal | 98-99% | High — structured at submission |
| Email-attached PDF | 95-99% (AI/IDP) | Medium — automate |
| Scanned paper | 80-90% | Low — preprocess first |
| Fax | 80-90% | Lowest — migrate away |

**Decision hierarchy:** Eliminate paper → migrate to portals/e-invoicing → automate remaining unstructured.

## Validation Tiers

| Tier | Type | Checks |
|---|---|---|
| a | Structural | All mandatory fields populated and correctly formatted |
| b | Referential | PO exists/open; vendor active in master; GL codes open for posting period; currency matches |
| c | Arithmetic | Line total = qty × unit price ± rounding; subtotal = Σ lines; total = subtotal + tax − discounts |
| d | Business Rules | Duplicate check; amount vs. PO tolerance; currency consistent; tax rates per jurisdiction |

## KPI Benchmarks (APQC/Ardent Partners/Medius 2025)

| Metric | Bottom | Median | Top Performer |
|---|---|---|---|
| Cost per invoice | $10.00+ | $5.78 | $2.05 |
| Cycle time (receipt → approval) | 11+ days | 5-7 days | 3.1 days |
| Touchless/STP rate (PO invoices) | <30% | 49.2% | 92.3% |
| Non-PO auto-routing | <50% | 75% | 99.6% |
| Exception rate | 30%+ | 15-20% | <9% |
| Invoices per AP FTE (annually) | ~5,000 | 9,483 | 24,284 |
| Field-level extraction accuracy | 85-90% | 95% | 98-99% |
| Early payment discount capture | <10% | 25-40% | 70%+ |

## Tolerance & Routing Thresholds

| Decision | Threshold | Notes |
|---|---|---|
| Auto-approve price variance | ±2-5% low-value; ±1-2% high-value POs | Stampli: 3-5% for immaterial variances |
| Zero tolerance | Serialized/regulated goods quantity | No override |
| Confidence threshold for STP | 95%+ all fields | Below → human review queue |
| Duplicate detection lookback | 12-18 months | Multi-field fuzzy match: vendor + amount ± tolerance + date ± 30 days + normalized invoice number |

## Process

1. **Invoice Receipt & Channel Normalization** — Ingest from email/EDI/portal/paper/e-invoicing networks (Peppol, ZATCA Fatoora, Italy SDI); normalize to common internal format; assign tracking ID + timestamp; log channel of origin
2. **Document Classification & Pre-processing** — Classify: invoice/credit note/debit note/proforma/statement; deskew/denoise/contrast-enhance scans (improves accuracy 15-30% per Artificio); split multi-page; reject non-invoices
3. **Data Extraction** — Header: vendor, invoice number, date, due date, payment terms, PO number, currency, tax ID; lines: description/qty/UOM/unit price/line total/SKU/tax per line; summary: subtotal/tax/shipping/discounts/grand total; banking details
4. **Validation & Enrichment** — All 4 tiers (structural/referential/arithmetic/business rules); tax rate verification per jurisdiction (GST/VAT/sales tax); duplicate detection; assign confidence scores per field
5. **Confidence-Based Routing** — All fields ≥95% + all validations pass → auto-matching; 1-3 low-confidence fields → human review (flagged fields only); structural/referential failures → exception queue; rejected docs → return to sender with reason
6. **Human Review & Correction** — Present only flagged fields (reduces review time 60-70%); side-by-side original + extracted data; capture corrections as ML training data; enforce four-eyes: reviewer ≠ approver (SOX §404 segregation of duties)
7. **ERP Posting & Handoff** — Export: IDOC for SAP; validate vendor/GL/cost center/currency at posting; alert AP within 15 minutes of failure; confirm posting; archive original image linked to ERP transaction; WORM storage for SOX compliance

## Glossary

| Term | Definition |
|---|---|
| STP (Straight-Through Processing) | Invoice processed receipt → ERP posting with zero human intervention; top performers 92.3% |
| Three-Way Match | PO + goods receipt + invoice agreement on item/qty/price before payment; primary billing fraud control |
| IDP (Intelligent Document Processing) | OCR + NLP + ML for contextual data extraction from unstructured documents |
| Field-Level Accuracy | % of individual fields correctly extracted; one wrong character = 0% for that field |
| Confidence Score | 0-100% certainty per extracted field; below threshold triggers human review |
| Tolerance Threshold | Permissible variance (1-5%) between invoice and PO; auto-matching proceeds within threshold |
| Exception Queue | Workflow holding area for invoices failing validation; classified by type and routed to owner |
| Non-PO Invoice | Invoice without corresponding PO (utilities/services/subscriptions); requires manual GL coding |
| GRN (Goods Receipt Note) | Warehouse confirmation of physical receipt; third leg of three-way matching |
| Duplicate Detection Window | 12-18 month lookback for potential duplicates by vendor/number/amount/date |
| GL Coding | General ledger account assignment to line items; critical for non-PO invoices |
| E-Invoicing Clearance Model | Gov't-mandated real-time invoice validation before buyer receipt (Italy, Saudi Arabia, Poland) |
| Peppol Access Point | Certified provider connecting to Peppol e-invoicing network for cross-border exchange |
| PO Flip | Supplier creates invoice from buyer's PO, pre-populating all fields; eliminates extraction errors |
| DPO | Days Payable Outstanding = (AP ÷ COGS) × Days; invoice capture speed directly impacts |
| Vendor Master File | ERP record: vendor name/address/bank accounts/tax IDs/payment terms; validation anchor |
| Two-Way Match | PO vs. invoice only (no GRN); acceptable for services/<$1,000/trusted vendors |
| WORM Storage | Write Once Read Many — tamper-proof storage required by SOX for financial documents |
| Benford's Law Analysis | Leading-digit distribution test; deviations signal fraud or data manipulation |
| Early Payment Discount (EPD) | Supplier discount (typically 1-2%) for accelerated payment (e.g., 2/10 Net 30) |

## Checklist

- [ ] All intake channels documented with volume % and accuracy rate per channel
- [ ] Extraction accuracy benchmarked on ≥200 actual supplier invoices (not vendor test data)
- [ ] Confidence thresholds configured per field type (higher for amounts, lower for descriptions)
- [ ] Tolerance thresholds tiered by spend category, invoice value band, and supplier risk rating
- [ ] Duplicate detection uses fuzzy multi-field matching against 18-month lookback
- [ ] Non-PO invoice workflows have AI-suggested GL coding and designated approval routing
- [ ] Exception queue classifies by type (price/qty mismatch, missing PO/receipt, duplicate, vendor not in system) and routes to correct resolver
- [ ] Human review corrections fed into ML training pipeline on ≥monthly cycle
- [ ] Segregation of duties enforced: no single user can capture, code, approve, and pay (SOX §404)
- [ ] Document retention meets jurisdictional requirements: 5 yr vendor invoices (SOX §103), 7 yr AP ledgers, 7 yr audit workpapers (SOX §802)
- [ ] Tax validation rules configured per jurisdiction (VAT rates, GST, reverse-charge, withholding)
- [ ] E-invoicing compliance verified: Germany receipt capability (Jan 2025), Peppol readiness Belgium (Jan 2026), ZATCA integration Saudi (Wave 24: SAR 750K+ turnover, Apr-Jun 2026)
- [ ] Failed ERP postings trigger alerts within 15 minutes; queued for retry with descriptive errors
- [ ] Scanned document preprocessing (deskew/denoise/contrast) enabled for all paper-origin invoices
- [ ] Month-end surge capacity tested at 3× average daily volume without accuracy degradation

## References
SOX §302/404/802 (segregation of duties; 5-yr invoice retention; 7-yr AP ledgers; 20-yr imprisonment altered records); IRS Rev. Proc. 98-25; IRC §6001; EU EN 16931; Peppol BIS Billing 3.0; ViDA 2028; Germany B2B e-invoice mandatory Jan 1, 2025; Belgium Peppol B2B Jan 1, 2026; Poland KSeF mandatory large taxpayers Feb 1, 2026; ZATCA Phase 2 Wave 24 (SAR 750K+, Apr-Jun 2026); ACFE 2024 (5% revenue lost without 3-way match; billing fraud 20% of occupational fraud, median $100K loss; 3-way match reduces fraud 60-80%); Ardent Partners 2024 ($12.88/invoice manual, $2.78 automated); Medius 2025; APQC; IFOL AP Automation Trends 2025; Artificio; AIMultiple
