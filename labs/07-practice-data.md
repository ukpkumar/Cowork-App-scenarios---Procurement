# Practice data workbook

Labs A1–A4 and several skill and plugin labs use one Excel workbook of fictional data, referred to as [Practice data workbook]. Every data tab is an Excel Table with one header row and units in the headers. Amounts are in [Currency] millions unless stated; one spend line is in a second currency and must not be converted. "As at" date: 27-Oct-2026.

Labs A5–A14 create their own small practice workbooks with the **Create practice data** prompt in each lab.

## Tabs by lab

| Lab | Tabs |
|---|---|
| A1 Bid-to-award | Tender, Evaluation_Criteria, Bids, Compliance, Technical_Scores, Evaluation_Summary, Approvals, Setup_Checklist, Handoff_Milestones |
| A2 Supplier scorecard | Suppliers, Supplier_KPIs, Contracts |
| A3 Contract radar | Contracts |
| A4 Spend and savings | Spend, Savings_Pipeline |

## Tab reference

| Tab | Content |
|---|---|
| Tender | RFP-2026-117, Facilities Management, 36-month term, budget 46.0, RFP issued 03-Sep-2026, bids closed 01-Oct-2026, evaluation started 03-Oct-2026, days in cycle (formula) = 24 |
| Evaluation_Criteria | Pass/fail checks (trade licence, insurance, HSE certification, conflict-of-interest declaration, bid bond). Technical 60 = service delivery 20, staffing and mobilisation 15, HSE and quality 10, technology and reporting 10, references 5. Commercial 30. In-Country Value 10 |
| Bids | Bidder A 42.6, Bidder B 45.1, Bidder C 38.9; price validity, mobilisation days, ICV certificate score, submitted date |
| Compliance | Each bidder against each pass/fail check with evidence reference. Bidder C: HSE certificate expired 31-Aug-2026, Fail |
| Technical_Scores | Bidder, sub-criterion, score 0–5, weighted points (formula), evidence reference, evaluator role |
| Evaluation_Summary | Bidder A 89.7 (rank 1), Bidder B 86.7 (rank 2), Bidder C excluded; savings versus budget 3.4; abnormally-low-bid check |
| Approvals | Category manager and finance approved; Legal and Head of Procurement pending; Tender Committee not yet requested. Pending = 2 |
| Setup_Checklist | Onboarding and PO/contract setup items; system = [Sourcing system] |
| Handoff_Milestones | About 10 milestones from contract signature to service go-live |
| Suppliers | About 20 suppliers with category, strategic tier, single-source flag, screening status and relationship owner role |
| Supplier_KPIs | Q1–Q3 2026 per supplier: on-time delivery, quality incidents, SLA breaches, invoice accuracy, spend. Two worsening, one improving, one "Review" screening flag |
| Contracts | About 25 contracts with end date, value, auto-renewal, notice period, notice deadline (formula), obligations, owner role, decision. Three in each 30/60/90-day window; two auto-renewal notice deadlines within 14 days |
| Spend | About 250 transactions Jan–Sep 2026; about 8% off-contract, mostly Consultancy and Travel; one line in a second currency |
| Savings_Pipeline | About 12 initiatives by stage; annual target 12.0; RFP-2026-117 target saving 3.4 |

## Scoring rules

- Compliance first; failed bids are excluded from ranking.
- Technical points = score ÷ 5 × weight.
- Commercial: lowest compliant price scores 30; others pro-rata (30 × lowest compliant price ÷ bid price).
- In-Country Value: ICV certificate score ÷ 50% benchmark × 10, capped at 10.
- Abnormally-low-bid check: flag any price more than 15% below the average of all bids.

## Build your own copy

If you do not have the workbook, ask Cowork:

```text
Create a fictional Excel workbook called "[Practice data workbook]" in [Practice folder] that follows the tab reference and scoring rules in this file exactly, with live formulas for all totals. Use Bidder A, Bidder B and Bidder C, roles instead of names, and no real company names. Check that Bidder A totals 89.7 and Bidder B 86.7 before saving.
```
