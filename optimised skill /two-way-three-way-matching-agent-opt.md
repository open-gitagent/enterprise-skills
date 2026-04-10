---
name: two-way-three-way-matching-agent
description: >
  Validates invoices against POs and receipts through automated two-way and three-way matching, tolerance thresholds, and exception routing workflows.
metadata:
  vertical: procurement
  function: invoicing-&-payment
  author: enterprise-skill-builder
  version: "1.0.0"
  complexity: intermediate
  regulatory-references: "FAR, SOX, UCC"
---

## Role
Prevent overpayment and fraud by matching supplier invoices against POs, goods receipts, and inspection records via configurable tolerance engines with auditable exception routing.

## Matching Level Selection

| Factor | 2-Way | 3-Way | 4-Way |
|---|---|---|---|
| Transaction value | <$500, routine | >$10,000 or goods-based | Quality-critical goods |
| Goods vs. services | Pure services (SaaS, consulting) | Physical goods | Pharma, aerospace, defense |
| Vendor risk | Trusted ≥12 months, clean record | New vendors or prior discrepancies | Per FDA 21 CFR Part 211; AS9100 |
| Regulatory | Standard | SOX §404, COSO Principles 10/11, FAR/DFARS | FAR/DFARS government contracts |

## Tolerance Configuration

| Type | Common Range | System Config |
|---|---|---|
| Price | 0-5% or $0-$50 | SAP: key PP (price variance); Oracle: PRICE hold; D365: Price Tolerances Table/Group/All hierarchy |
| Quantity | 0-2% or ±5 units | SAP: key DQ (quantity variance); Oracle: QTY ORD / MAX QTY REC hold |
| Invoice total | 5-15% | SAP: key BD/BK; Oracle: AMT ORD hold |
| Tax | 1-2% or fixed $$ | Per jurisdiction |
| Missing GR | N/A | SAP: key DW (missing goods receipt blocks invoice) |

SAP config path: SPRO → Materials Management → Logistics Invoice Verification → Invoice Block → Set Tolerance Limits
D365 path: AP → Setup → Invoice Matching Setup → Price Tolerances

## Performance Benchmarks

| Metric | Best-in-Class | Average | Concerning |
|---|---|---|---|
| First-pass match rate | >85% | 60-70% | <50% |
| Exception rate | <5% | 23.2% (26% ↑ from 2017) | >30% (Ardent Partners 2024) |
| Cost per invoice (automated) | $2.81 | $2-$3 | $10-$15 manual |
| Invoice cycle time | <2 days | 3-5 days automated | ~14.6 days manual |
| Duplicate payments | <0.1% | 0.1-0.5% of disbursements (AFP) | >0.5% |

## Regulatory Framework

| Standard | Citation | Requirement |
|---|---|---|
| SOX | §302; §404(a)(b) | CEO/CFO certification; ICFR management assessment; external auditor testing of matching controls |
| COSO | Principle 10; Principle 11 | Preventive controls; SoD; IT application controls (tolerance config, exception routing) |
| GAAP | ASC 720 (expense recognition); ASC 405 (liabilities); ASC 405-50 (supplier finance) | Accrue received-not-invoiced; GR/IR clearing; SCF disclosure |
| IFRS | IAS 37 | Disputed invoices may require provision if obligation probable |
| Pharma | FDA 21 CFR Part 211 | Documented receipt/inspection → 4-way matching |
| Aerospace | AS9100 | Documented receiving inspection |
| Government | FAR/DFARS | Documented 3-way matching for contract payments |

## Process

**2-Way Match Workflow**
1. PO issued: item descriptions, quantities, unit prices, delivery terms, payment terms
2. Invoice received: logged via OCR/e-invoicing portal or manual entry
3. Header validation: vendor name/ID, PO number, currency, payment terms
4. Line comparison: each invoice line vs. PO line — item, quantity, unit price, extended amount
5. Tolerance check: variances evaluated against configured thresholds
6. Route: within tolerance → auto-approve; outside tolerance → exception queue with variance reason code

**3-Way Match Workflow (Steps 1-2 identical; adds prerequisite)**
3. GR posting: warehouse confirms delivery in ERP — actual quantities, condition, receipt date
4. Header validation: same as 2-way + confirm GRN exists for referenced PO
5. Three-document comparison: Invoice qty ≤ GRN qty ≤ PO qty; invoice unit price = PO unit price (within tolerance); invoice extended amount = GRN qty × PO unit price (within tolerance)
6. Tolerance check across price, quantity, and amount
7. Route: clean match → payment; exception → AP specialist, buyer, or receiving per exception type

**4-Way Extension (after GR posting)**
- 3a. Quality inspection: inspection slip / quality acceptance report → accepted qty
- Comparison: Invoice qty ≤ Accepted qty ≤ GRN qty ≤ PO qty

**Exception Resolution**
1. Categorize: price mismatch, quantity short, missing GR, duplicate invoice, missing PO reference
2. Route: price → buyer/procurement; quantity → receiving/warehouse; missing docs → supplier or requester
3. Investigate: root cause (supplier error, price change, partial shipment, data entry)
4. Resolve: PO amendment, credit memo, GR correction, invoice rejection, or tolerance override with documented approval
5. Escalate: unresolved >15 days → procurement manager or controller
6. Close: document reason code, approver, timestamp for audit trail

## Glossary

| Term | Definition |
|---|---|
| Blanket PO | Long-term PO authorizing repeated purchases up to max value; individual releases generate separate GRs |
| Credit Memo | Supplier document reducing amount owed; must be applied against open invoices during matching |
| ERS | Evaluated Receipt Settlement; eliminates supplier invoices — payment generated from PO terms + goods receipt |
| Exception (Matching) | Discrepancy exceeding tolerance thresholds requiring human review before payment |
| First-Pass Match Rate | % invoices matched without human intervention; key AP efficiency KPI |
| GR/IR Clearing Account | Intermediate ledger holding value of goods received-not-invoiced or invoiced-not-received; should trend to zero |
| GRN | Goods Receipt Note; created by receiving on delivery recording actual quantities, condition, date |
| Invoice Exception Rate | Exceptions ÷ total invoices received |
| MRBR | SAP transaction for reviewing and releasing invoices blocked by tolerance violations |
| Maverick Spend | Purchases outside contracted suppliers; creates non-PO invoices bypassing matching |
| Non-PO Invoice | Invoice without corresponding PO; requires separate approval workflow, not matching bypass |
| P2P | Procure-to-Pay; end-to-end from requisition to payment disbursement |
| Retroactive PO | PO created after goods delivered; defeats control purpose; flag POs created <24 hours of invoice |
| SoD | Segregation of Duties: PO creator ≠ GR poster ≠ invoice approver; enforced by system roles |
| STP | Straight-Through Processing; invoices auto-approved without human intervention |
| Tolerance Key | SAP config element (DW/DQ/PP/BD/BK) defining variance type and threshold blocking LIV |
| Touchless Processing Rate | % invoices processed end-to-end without any human interaction; superset of first-pass rate |

## Checklist

- [ ] Matching policy documented: transaction types assigned 2-way/3-way/4-way by category — not blanket rule
- [ ] Tolerance thresholds configured at appropriate granularity (legal entity, vendor group, item group); calibrated from 90-day exception volume data
- [ ] SoD enforced: PO creator ≠ GR poster ≠ invoice approver; system roles verified
- [ ] Retroactive PO volume monitored; POs created <24 hours of invoice receipt flagged
- [ ] GR/IR clearing account reconciled monthly; items >30 days investigated and accrued per ASC 405/ASC 720
- [ ] Duplicate detection checks: invoice number + vendor + amount + date + PO combinations (not just invoice number alone)
- [ ] Exception SLAs defined (e.g., 5 biz days price; 3 biz days quantity); escalation paths for aged items
- [ ] Tolerance override authority restricted to named roles (AP Manager, Controller); system-enforced with documented justification
- [ ] Non-PO invoices follow separate documented approval workflow
- [ ] Blanket PO matching validates release-level quantities AND cumulative spend vs. blanket ceiling
- [ ] UoM mapping maintained in item master to prevent false exceptions from unit-of-measure mismatches
- [ ] Matching KPIs tracked monthly: first-pass rate, exception rate, cycle time, cost per invoice
- [ ] Post-payment GR reversals monitored via automated report; reversal on paid invoice triggers recovery workflow
- [ ] Audit trail captures all matching outcomes, exception resolutions, tolerance overrides, approvals with timestamps and user IDs
- [ ] Annual tolerance review against prior year exception data to identify over-tight or over-loose thresholds

## References
Ardent Partners AP Metrics 2024 (59.3% PO-based; 23.2% exception rate; $2.81 best-in-class cost); AFP duplicate payments 0.1-0.5%; SOX §302/§404; COSO Principles 10/11; ASC 405/405-50/720; IAS 37; FDA 21 CFR Part 211; AS9100; FAR/DFARS; SAP MIRO/MRBR tolerance keys DW/DQ/PP/BD/BK; Oracle Fusion QTY ORD/PRICE/AMT ORD/MAX QTY REC; Dynamics 365 Matching Policy; NetSuite 3-Way Match Vendor Bill Approval; Tipalti; Stampli; Rillion; Coupa; SoftCo
