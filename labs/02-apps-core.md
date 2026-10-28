# Labs A2–A4 – Core procurement apps

Illustrative scenarios – fictional data. These labs use the ready-made tabs in [Practice data workbook].

---

## Lab A2 – Supplier performance and risk scorecard

### Scenario

Quarterly supplier reviews take days to assemble. KPIs sit in different files and risk flags are spotted late.

### What you will build

A scorecard app listing suppliers with on-time delivery, quality incidents, SLA breaches and invoice accuracy, trend arrows, risk flags and a drill-down per supplier.

### Practice data

Tabs: Suppliers, Supplier_KPIs, Contracts.

### Steps

1. Open a new Cowork conversation and attach [Practice data workbook].
2. Paste the **Try this prompt** and approve the plan.
3. Sort by risk and open the drill-down for the worst supplier.
4. Paste **Then try this**.

### Try this prompt

```text
/app Build a supplier performance and risk scorecard from the attached [Practice data workbook], using the Suppliers, Supplier_KPIs and Contracts tabs. Show me your plan and data access first.
List suppliers with scores for on-time delivery, quality incidents, SLA breaches and invoice accuracy for Q1 to Q3, with trend arrows and a drill-down per supplier.
Flag contracts expiring within 90 days, single-source dependencies and any "Review" result from [Screening source]. Add filters by category and strategic tier. Mark missing data as "Needs confirmation".
```

### Then try this

```text
For each Strategic supplier, draft a quarterly review pack and a meeting agenda as Word documents. Keep them as drafts for my review.
```

### Check your result

- [ ] Two suppliers show a worsening trend each quarter and one is improving.
- [ ] One supplier is flagged for screening review.
- [ ] Review packs are drafts; nothing was sent.

---

## Lab A3 – Contract renewal and obligations radar

### Scenario

Renewals are missed and auto-renewals slip through because notice deadlines are buried in contracts.

### What you will build

A radar app grouping contracts expiring in 30, 60 and 90 days, with auto-renewal and notice-deadline flags, key obligations, owners and a renew / re-tender / exit decision field.

### Practice data

Tab: Contracts.

### Steps

1. Open a new Cowork conversation and attach [Practice data workbook].
2. Paste the **Try this prompt** and approve the plan.
3. Check the auto-renewals with a notice deadline in the next 14 days.
4. Paste **Then try this** and review the schedule before approving it.

### Try this prompt

```text
/app Build a contract renewal and obligations radar from the Contracts tab of the attached [Practice data workbook]. Show me your plan and data access first.
Group contracts expiring in the next 30, 60 and 90 days. Flag auto-renewal clauses and any notice deadline in the next 14 days in red. List key obligations with owners, and add a decision field: Renew, Re-tender or Exit.
Do not change the source data.
```

### Then try this

```text
Every Monday at 8am, send me a weekly digest of contracts entering the 30, 60 and 90-day windows. Draft renewal or termination notices for my approval only; never send them to suppliers.
```

### Check your result

- [ ] Three contracts appear in each of the 30, 60 and 90-day windows.
- [ ] Two auto-renewals are flagged with notice deadlines inside 14 days.
- [ ] The weekly digest is addressed only to you; notices are drafts.
- [ ] You paused or deleted the scheduled digest after the lab.

---

## Lab A4 – Spend and savings tracker

### Scenario

Leadership asks where the money goes and what has been saved. The answer takes a week of spreadsheet work.

### What you will build

A tracker showing spend by category, supplier and business unit, the top-10 suppliers, off-contract spend and the savings pipeline against target.

### Practice data

Tabs: Spend, Savings_Pipeline.

### Steps

1. Open a new Cowork conversation and attach [Practice data workbook].
2. Paste the **Try this prompt** and approve the plan.
3. Find the two categories with the most off-contract spend.
4. Paste **Then try this**.

### Try this prompt

```text
/app Build a spend and savings tracker from the Spend and Savings_Pipeline tabs of the attached [Practice data workbook]. Show me your plan and data access first.
Show spend by category, supplier and business unit, the top-10 suppliers, off-contract spend (lines where On contract = N or the PO number is blank), and the savings pipeline by stage against the annual target.
Keep every amount in the currency recorded. Do not convert currencies unless I supply a rate; show other-currency lines separately.
```

### Then try this

```text
Draft a one-page monthly savings report for the Head of Procurement as a Word document: realised savings, pipeline, gap to target and the top three off-contract categories. Keep it as a draft for my review.
```

### Check your result

- [ ] Off-contract spend is about 8% and concentrated in Consultancy and Travel.
- [ ] The one non-[Currency] line is shown separately, not converted.
- [ ] The pipeline shows a gap to the annual target.
