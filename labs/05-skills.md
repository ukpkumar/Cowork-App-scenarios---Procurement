# Labs B1–B8 – Procurement skills

A skill is a reusable instruction you create once and trigger by a phrase. Cowork finds your custom skills automatically at the start of each session.

## How to create and add a skill (use for every lab)

1. Open a new Cowork conversation and type: `I would like help creating a skill.`
2. Paste the lab's **Create the skill** prompt.
3. Review the skill file Cowork drafts (name, description, trigger phrases, rules). Ask for changes in plain language until it is right.
4. Ask for the skill file as a download, then add it using the skill upload option available in your session (for example Add, then Upload New Skill).
5. Open a new conversation and paste the lab's **Use the skill** prompt to test it.

Tip: the fastest way to build a skill is to start from a prompt that already works, then ask Cowork to save it as a skill.

---

## Lab B1 – Procurement branding skill

### Scenario

Tender Committee decks, RFP cover packs and supplier briefings are rebuilt by hand on the corporate template every time, with inconsistent markings.

### What the skill does

Opens the approved template, adds the tender reference, confidentiality marking and a version and approval block, and stops if the template is unavailable. It never invents logos, figures or web addresses.

### Create the skill

```text
Create a skill called "[Company] procurement branding", triggered when I say "use the [Company] procurement template" or close variations.
Open the approved template from [Template library location] and build on its own layouts, fonts and colours. Add the tender reference on the cover, a "Confidential – Procurement" marking on every slide, and a version and approval block on the last slide.
Use it for Tender Committee award decks, RFP cover packs and supplier briefing decks.
If the template is unavailable, stop and tell me. Never invent logos, figures or web addresses, and never use a default theme instead.
```

### Use the skill

```text
Use the [Company] procurement template – build a five-slide Tender Committee award recommendation for RFP-2026-117 from the Evaluation_Summary tab of [Practice data workbook].
```

### Check your result

- [ ] The deck uses the approved template, not a default theme.
- [ ] Tender reference, confidentiality marking and approval block are present.

---

## Lab B2 – Bid evaluation skill

### Scenario

Each evaluator applies compliance checks and weightings slightly differently, so scores are hard to defend.

### What the skill does

Applies pass/fail compliance checks first, then weighted scoring to the tender's criteria, and cites the evidence for every score.

### Create the skill

```text
Create a skill called "Bid evaluation", triggered when I say "evaluate the bids for" followed by a tender reference.
Steps: 1) read the tender's evaluation criteria and the bids I attach or point to; 2) run every pass/fail check first and exclude failed bids with the reason; 3) score compliant bids against each weighted criterion using the scoring scale in the criteria; 4) cite the document, section or tab for every score; 5) produce an Excel evaluation matrix and a short summary of the ranking.
Mark any score without evidence as "Needs confirmation". Never recommend an award on my behalf; present the ranking for the evaluation panel to decide.
```

### Use the skill

```text
Evaluate the bids for RFP-2026-117 using [Practice data workbook].
```

### Check your result

- [ ] Bidder C is excluded on compliance before scoring.
- [ ] Every score has a citation.

---

## Lab B3 – Supplier letters skill

### Scenario

Award, regret and clarification letters are written from scratch and vary in tone.

### What the skill does

Drafts award letters, regret letters and clarification requests in the approved tone, always as drafts.

### Create the skill

```text
Create a skill called "Supplier letters", triggered when I say "draft the award letter", "draft the regret letters" or "draft a clarification request" for a tender reference.
Use a formal, courteous tone in British English. Award letters confirm the award subject to contract and list next steps. Regret letters thank the bidder, state the outcome without revealing other bidders' prices or scores, and offer a debrief. Clarification requests list numbered questions with a response deadline.
Always create Outlook drafts or Word documents for my review. Never send anything.
```

### Use the skill

```text
Draft the regret letters for RFP-2026-117 for Bidder B and Bidder C.
```

### Check your result

- [ ] Regret letters do not reveal other bidders' prices or scores.
- [ ] The letters are drafts.

---

## Lab B4 – RFP drafting skill

### Scenario

RFPs are assembled by copying old documents, so sections go missing and terms are out of date.

### What the skill does

Turns a short scope note into a structured RFP with standard sections, evaluation criteria and a submission checklist.

### Create the skill

```text
Create a skill called "RFP drafting", triggered when I say "draft an RFP for" followed by a short description.
Produce a Word RFP with these sections: introduction and background, scope of work, deliverables and service levels, timeline, submission instructions, evaluation criteria (pass/fail checks first, then weighted criteria that total 100%), commercial schedule, terms and conditions reference, and a bidder submission checklist.
Ask me for the scope, term, budget band and evaluation weighting if I have not provided them. Mark any assumption as "Needs confirmation". Use the [Company] procurement template skill if it is available.
```

### Use the skill

```text
Draft an RFP for cleaning and pest control services for [Head office], 3-year term, Technical 60%, Commercial 30%, In-Country Value 10%.
```

### Check your result

- [ ] All standard sections are present and the weights total 100%.
- [ ] Assumptions are marked "Needs confirmation".

---

## Lab B5 – Clarification response skill

### Scenario

Clarification answers must be consistent, anonymised and issued to all bidders at the same time.

### What the skill does

Anonymises bidder questions, groups duplicates, drafts answers from the tender documents and builds a numbered clarification bulletin.

### Create the skill

```text
Create a skill called "Clarification response", triggered when I say "prepare clarification answers for" followed by a tender reference.
Steps: remove bidder names and any identifying details from each question; group near-duplicate questions; draft an answer to each using only the tender documents I provide, citing the section; mark questions that need a policy decision as "Needs owner decision"; produce a numbered clarification bulletin in Word.
The bulletin is for issue to all bidders at the same time. Keep it as a draft for my approval and never send it.
```

### Use the skill

```text
Prepare clarification answers for RFP-2026-117 using "Clarifications – Practice.xlsx" from Lab A7.
```

### Check your result

- [ ] No bidder names appear in the bulletin.
- [ ] Duplicates are grouped and answers cite a section.

---

## Lab B6 – Negotiation brief skill

### Scenario

Negotiation preparation depends on who prepares it; briefs miss the walk-away point or the concession plan.

### What the skill does

Builds a standard two-page negotiation brief from price history, benchmarks and the team's position.

### Create the skill

```text
Create a skill called "Negotiation brief", triggered when I say "prepare a negotiation brief for" followed by a supplier and topic.
Produce a two-page Word brief: objectives, current position and price history, benchmark range with source type and date, the supplier's likely position, our opening position, target and walk-away point, a concession plan (what we give, what we get), five questions to ask, and risks.
Mark the brief "Confidential – internal". Never share it outside the negotiation team and never contact the supplier.
```

### Use the skill

```text
Prepare a negotiation brief for Supplier N managed print services using "Negotiation Prep – Practice.xlsx" from Lab A8.
```

### Check your result

- [ ] Target and walk-away prices are both present.
- [ ] The brief is marked internal.

---

## Lab B7 – Contract summary skill

### Scenario

Contract managers need the key terms of long contracts quickly: dates, renewal, obligations, liabilities and service credits.

### What the skill does

Produces a one-page contract summary and adds key dates and obligations to a register.

### Create the skill

```text
Create a skill called "Contract summary", triggered when I say "summarise the contract" followed by a file or contract reference.
Produce a one-page summary: parties, term, start and end dates, renewal and notice period, price and payment terms, key obligations for each party, service levels and service credits, liability cap, termination rights and any unusual clauses. Cite the clause number for every item.
Then list the key dates and obligations as rows I can add to the contract register. Mark anything not found as "Not found in contract". This is not legal advice; flag clauses for Legal review instead of interpreting them.
```

### Use the skill

```text
Summarise the contract in [Practice folder]/Practice Service Agreement.docx.
```

Tip: if you do not have a practice contract, first ask Cowork to "create a fictional 6-page service agreement for practice" and save it to [Practice folder].

### Check your result

- [ ] Every item cites a clause number.
- [ ] Missing items say "Not found in contract".

---

## Lab B8 – Supplier review pack skill

### Scenario

Quarterly business reviews with strategic suppliers need a consistent pack: performance, issues, improvement actions and the agenda.

### What the skill does

Builds a quarterly review pack and agenda for one supplier from KPI and contract data.

### Create the skill

```text
Create a skill called "Supplier review pack", triggered when I say "prepare the quarterly review for" followed by a supplier name.
Produce a short PowerPoint pack: KPI scorecard with trend for the last three quarters, open issues and SLA breaches, contract status and renewal date, improvement actions with owners, and topics for the supplier. Also produce a one-page meeting agenda in Word.
Use the [Company] procurement template skill if available. Use only the data provided and mark gaps as "Needs confirmation". Keep everything as drafts.
```

### Use the skill

```text
Prepare the quarterly review for the supplier with the worst trend in the Supplier_KPIs tab of [Practice data workbook].
```

### Check your result

- [ ] The pack shows three quarters of KPIs with trends.
- [ ] Agenda and pack are drafts.
