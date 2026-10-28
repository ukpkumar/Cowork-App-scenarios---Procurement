# Labs A5–A9 – Sourcing apps

Illustrative scenarios – fictional data. Each lab starts with a **Create practice data** prompt. Run it first in the same conversation, then run the app prompt.

---

## Lab A5 – Sourcing request intake and triage

### Scenario

Business units send purchase requests by email in different formats. Procurement spends time working out the category, value, route to market and owner before any sourcing starts.

### What you will build

An intake app where requests are logged, classified by category, checked against [DoA levels] and sourcing thresholds, and assigned to a category manager with a recommended route to market.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Submit one new request through the app form.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "Sourcing Requests – Practice.xlsx" in [Practice folder] with two tabs.
Requests: 30 rows with Request ID, Date received, Business unit, Requester role, Description, Estimated value ([Currency] m), Needed by, Existing contract (Y/N).
Rules: Category list (Facilities, IT services, Professional services, Travel, Marketing, Security) with category manager role, and value bands for route to market: below 0.1m direct purchase, 0.1m to 1m three quotes, above 1m formal tender.
Use fictional data only and show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Sourcing Request Intake" app from "Sourcing Requests – Practice.xlsx". Show me your plan and data access first.
Include a request form, a triage queue and a dashboard. For each request, suggest the category from the description, apply the value bands to recommend the route to market (direct purchase, three quotes or formal tender), and assign the category manager role from the Rules tab.
Flag requests needed in under 30 days and requests where an existing contract could be used instead. Mark any guess as "Needs confirmation" so a category manager can accept or change it.
```

### Then try this

```text
Add a "Send back for information" action that drafts a short email to the requester listing what is missing. Keep it as a draft; do not send.
```

### Check your result

- [ ] Every request has a suggested category and route to market.
- [ ] Urgent requests and existing-contract matches are flagged.
- [ ] Suggestions can be accepted or changed by a person.

---

## Lab A6 – Sourcing pipeline and workload board

### Scenario

The Head of Procurement cannot see at a glance which sourcing events are at which stage, which are late, and which category managers are overloaded.

### What you will build

A pipeline board showing sourcing events by stage (Planning, RFP issued, Evaluation, Approval, Awarded), days in stage, forecast award date and workload per category manager.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Drag one event to a new stage and confirm the counts update.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "Sourcing Pipeline – Practice.xlsx" in [Practice folder] with 25 sourcing events: Event ID, Title, Category, Category manager role, Estimated value ([Currency] m), Stage (Planning, RFP issued, Evaluation, Approval, Awarded), Stage entered date, Planned award date, Business owner role.
Make three events late against the planned award date and give one category manager role twice the average workload. Show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Sourcing Pipeline Board" from "Sourcing Pipeline – Practice.xlsx". Show me your plan and data access first.
Show a board with one column per stage, a card per event with value and days in stage, and a red flag where today is past the planned award date. Add a workload chart by category manager role and filters by category and value band.
Add KPI cards: total pipeline value, events per stage and late events.
```

### Then try this

```text
Every Sunday at 8am, send me a short Teams summary of late events and events that moved stage in the past week. Show me the first summary for approval before scheduling.
```

### Check your result

- [ ] Three events are flagged late.
- [ ] One category manager role clearly carries the highest workload.
- [ ] The weekly summary goes only to you; pause it after the lab.

---

## Lab A7 – Tender clarification log

### Scenario

During a live tender, bidders send clarification questions. Procurement must answer consistently and share every answer with all bidders without revealing who asked.

### What you will build

A clarification log app that records each question, removes the bidder's identity, tracks the answer owner and due date, and produces a consolidated clarification bulletin for all bidders.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Answer one open question in the app.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "Clarifications – Practice.xlsx" in [Practice folder] for tender RFP-2026-117 with 15 clarification questions: Question ID, Date received, Bidder (Bidder A, B or C), Question text, Topic (Scope, Commercial, Legal, Technical), Answer owner role, Due date, Answer text (blank for 6 questions), Status.
Include two questions that are near-duplicates from different bidders. Show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Tender Clarification Log" for RFP-2026-117 from "Clarifications – Practice.xlsx". Show me your plan and data access first.
Show open and answered questions by topic and owner, with overdue answers flagged. Group near-duplicate questions so they get one answer.
Never show bidder names outside the internal view: the bulletin view must list questions and answers anonymously.
```

### Then try this

```text
Create Clarification Bulletin No. 1 as a Word document containing all answered questions, anonymised and numbered, ready to issue to all bidders at the same time. Keep it as a draft for my approval.
```

### Check your result

- [ ] The two near-duplicate questions are grouped.
- [ ] The bulletin contains no bidder names.
- [ ] The bulletin is a draft; nothing was sent to bidders.

---

## Lab A8 – Negotiation preparation cockpit

### Scenario

Before a negotiation, the category manager pulls together price history, benchmarks, the supplier's position and the team's walk-away point from several sources.

### What you will build

A negotiation cockpit showing price history, benchmark range, target and walk-away price, a concession plan and the questions to ask.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Change the target price and watch the concession plan update.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "Negotiation Prep – Practice.xlsx" in [Practice folder] for a renewal with "Supplier N" for managed print services.
Tabs: Price_History (8 quarters of unit prices and volumes), Benchmarks (5 anonymised market rates with source type and date), Supplier_Proposal (proposed price, term, volume commitment, service levels), Our_Position (target price, walk-away price, must-haves, nice-to-haves).
Show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Negotiation Prep Cockpit" from "Negotiation Prep – Practice.xlsx". Show me your plan and data access first.
Show the price trend, the benchmark range compared with the supplier's proposal, and our target and walk-away prices. Calculate the annual value of the gap between proposal and target.
Add a concession planner: list what we can offer (term, volume, payment terms) and what we ask for in return. Mark benchmark figures with their source type and date.
```

### Then try this

```text
Draft a two-page negotiation brief in Word: objectives, opening position, concession plan, five questions to ask and the walk-away point. Keep it as a draft and mark it Confidential – internal.
```

### Check your result

- [ ] The proposal is shown against the benchmark range.
- [ ] The annual gap is calculated from the practice data.
- [ ] The brief is marked internal and kept as a draft.

---

## Lab A9 – Conflict-of-interest declarations register

### Scenario

Every evaluator must declare conflicts of interest before seeing bids. Declarations are collected by email and are hard to audit.

### What you will build

A register app showing, per tender, each evaluator's declaration status, any declared interest, the decision taken and the evidence date, with evaluators blocked from scoring until they have declared.

### Steps

1. Open a new Cowork conversation.
2. Paste **Create practice data** and approve.
3. Paste the **Try this prompt** and approve the plan.
4. Filter to RFP-2026-117 and check who cannot score yet.
5. Paste **Then try this**.

### Create practice data

```text
Create a fictional Excel workbook called "COI Declarations – Practice.xlsx" in [Practice folder] with 20 rows: Tender ref, Evaluator role, Declaration date (blank if not submitted), Interest declared (Y/N), Description, Decision (No conflict, Mitigated, Recused), Approved by role.
For RFP-2026-117 include one evaluator who has not declared and one who declared an interest with Bidder B. Show me the workbook before saving.
```

### Try this prompt

```text
/app Build a "Conflict-of-Interest Register" from "COI Declarations – Practice.xlsx". Show me your plan and data access first.
Show each tender with its evaluators and declaration status. Mark evaluators with no declaration as "Cannot score yet" and evaluators with an undecided interest as "Decision needed".
Add an audit view listing every declaration with its date and decision. Do not display personal details beyond the role.
```

### Then try this

```text
Draft a reminder email to each evaluator role that has not declared for RFP-2026-117. Keep the drafts for my approval; do not send.
```

### Check your result

- [ ] One evaluator shows "Cannot score yet" for RFP-2026-117.
- [ ] The declared interest with Bidder B shows its decision.
- [ ] Reminders are drafts.
