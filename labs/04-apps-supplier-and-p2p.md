# Labs A10–A14 – Supplier and procure-to-pay apps

Illustrative scenarios – fictional data. Each lab starts with a **Create practice data** prompt. Run it first in the same conversation, then run the app prompt.

---

## Lab A10 – Supplier onboarding tracker

### Scenario

After award, a new supplier must submit documents, pass screening and have bank details verified before a PO can be raised. Status is tracked in emails and nobody knows what is blocking go-live.

### What you will build

An onboarding tracker showing each new supplier's checklist (trade licence, insurance, tax registration, bank letter, screening, code of conduct), document expiry dates, blockers and days to ready.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Open the supplier with the most blockers.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "Supplier Onboarding – Practice.xlsx" in [Practice folder] with 8 new suppliers and one row per checklist item: Supplier, Item (Trade licence, Insurance, Tax registration, Bank letter, Screening, Code of conduct), Status (Received, Verified, Missing, Expired), Document expiry date, Owner role, Target go-live date.
Make one supplier's insurance expired and one supplier's bank letter "Received" but not "Verified". Show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Supplier Onboarding Tracker" from "Supplier Onboarding – Practice.xlsx". Show me your plan and data access first.
Show each supplier's checklist progress as a percentage, blockers in red, documents expiring within 60 days and days until target go-live.
A supplier is "Ready for PO" only when every item is Verified and no document has expired. Bank details must be verified by a second person: show this as a separate check, never mark it complete automatically.
```

### Then try this

```text
For each supplier with a missing or expired item, draft a polite request email listing exactly what is needed. Keep the drafts for my approval.
```

### Check your result

- [ ] No supplier with an expired or unverified item shows "Ready for PO".
- [ ] Bank verification is a separate, manual check.
- [ ] Request emails are drafts.

---

## Lab A11 – Supplier ESG and risk questionnaire tracker

### Scenario

Strategic suppliers must complete an annual ESG and risk questionnaire. Responses arrive late and are scored inconsistently.

### What you will build

A tracker showing questionnaire status per supplier, scores by section (environment, social, governance, cyber, business continuity), red flags and follow-up actions.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Open the supplier with the lowest governance score.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "Supplier ESG – Practice.xlsx" in [Practice folder] with 12 strategic suppliers: Supplier, Questionnaire sent date, Response date (blank for 3), and scores 0 to 5 for Environment, Social, Governance, Cyber and Business continuity, plus a Comments column.
Give one supplier a Governance score of 1 and one supplier a Cyber score of 2. Show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Supplier ESG and Risk Tracker" from "Supplier ESG – Practice.xlsx". Show me your plan and data access first.
Show response status, an overall score (average of the five sections) and a heat map by section. Flag any section scored 2 or below as a red flag, and any questionnaire outstanding for more than 30 days.
Add a follow-up actions list with owner role and due date, and mark missing responses as "Needs confirmation" rather than scoring them.
```

### Then try this

```text
Draft a follow-up letter to each supplier with a red flag, asking for an improvement plan within 30 days. Keep the drafts for my approval.
```

### Check your result

- [ ] Two suppliers show red flags (Governance and Cyber).
- [ ] Missing responses are not scored.
- [ ] Follow-up letters are drafts.

---

## Lab A12 – Three-way match exceptions queue

### Scenario

Invoices that do not match the purchase order and goods receipt sit in a queue. Accounts payable and procurement argue about who should resolve each one.

### What you will build

An exceptions queue comparing PO, goods receipt and invoice for each line, classifying the exception (price, quantity, no receipt, no PO), the amount at risk and the owner.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Filter to price exceptions.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "Three-Way Match – Practice.xlsx" in [Practice folder] with three tabs: POs (40 lines: PO number, line, supplier, item, quantity, unit price, [Currency]), Receipts (goods received quantity per PO line, with 4 lines missing) and Invoices (invoiced quantity and unit price per PO line, with 5 price differences and 3 quantity differences, plus 2 invoices with no PO number).
Show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Three-Way Match Exceptions" queue from "Three-Way Match – Practice.xlsx". Show me your plan and data access first.
Match each invoice line to its PO line and goods receipt. Classify exceptions as Price, Quantity, No receipt or No PO, calculate the amount at risk, and suggest an owner (procurement for price and No PO, the requester for receipts, accounts payable for quantity).
Add a tolerance setting (default 2%) so small differences are not flagged. Never approve or release a payment.
```

### Then try this

```text
Group the exceptions by supplier and draft one query email per supplier listing the lines and the differences. Keep the drafts for my approval.
```

### Check your result

- [ ] Exceptions are classified into the four types.
- [ ] Differences within the tolerance are not flagged.
- [ ] No payment action exists in the app; supplier queries are drafts.

---

## Lab A13 – Contract price compliance checker

### Scenario

Suppliers sometimes invoice above the agreed contract rate. Overcharges are only found in audits months later.

### What you will build

A checker comparing invoiced unit prices against the contract rate card, showing overcharges by supplier and item, the total recoverable amount and repeat offenders.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Sort suppliers by recoverable amount.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "Price Compliance – Practice.xlsx" in [Practice folder] with two tabs: Rate_Card (5 suppliers, 30 items, contract unit price, valid from, valid to) and Invoice_Lines (200 lines: invoice number, date, supplier, item, quantity, invoiced unit price).
Make about 6% of lines priced above the rate card, concentrated in two suppliers, and include 5 lines dated outside the rate card validity. Show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Contract Price Compliance" checker from "Price Compliance – Practice.xlsx". Show me your plan and data access first.
Compare each invoice line with the rate card price valid on the invoice date. Show overcharges by supplier and item, the recoverable amount (difference times quantity) and suppliers with repeat overcharges.
Flag lines dated outside any valid rate as "No valid rate – Needs confirmation" instead of treating them as overcharges.
```

### Then try this

```text
Draft a recovery claim letter to each supplier with overcharges, with a line-by-line schedule attached as an Excel file. Keep everything as a draft for my approval.
```

### Check your result

- [ ] Two suppliers account for most overcharges.
- [ ] Lines outside the rate validity are flagged separately.
- [ ] Claim letters are drafts.

---

## Lab A14 – SLA service-credit calculator

### Scenario

Service contracts include service credits when SLAs are missed, but credits are rarely claimed because calculating them is tedious.

### What you will build

A calculator that applies each contract's SLA targets and credit rules to monthly performance data, shows credits due per supplier and month, and tracks whether each credit has been claimed.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Change one SLA target and check the credits recalculate.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "SLA Credits – Practice.xlsx" in [Practice folder] with two tabs: SLA_Rules (4 service contracts: supplier, SLA metric such as response time or availability, target, credit percentage per breach band, monthly fee in [Currency], credit cap percentage) and Performance (6 months of actual results per contract and metric).
Make two contracts miss their SLA in at least two months and one contract hit the credit cap. Show me the workbook before saving.
```

### Try this prompt

```text
/app Build an "SLA Service-Credit Calculator" from "SLA Credits – Practice.xlsx". Show me your plan and data access first.
For each contract and month, compare actual results with the target, apply the credit percentage for the breach band to the monthly fee, and apply the credit cap. Show credits due by supplier and month, the total, and a status field: Not claimed, Claimed, Agreed, Disputed.
Show the calculation for every credit so it can be checked.
```

### Then try this

```text
Draft a service-credit notice to each supplier with unclaimed credits, showing the months, metrics, targets, actual results and amounts. Keep the drafts for my approval.
```

### Check your result

- [ ] Two contracts show credits due; one is limited by the cap.
- [ ] Every credit shows its calculation.
- [ ] Notices are drafts.
