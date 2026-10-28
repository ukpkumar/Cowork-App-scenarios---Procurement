# Labs C1–C6 – Procurement plugins

A plugin bundles several skills with connections to data and services into one package a team can install and share. Every category manager then follows the same process, branding and controls, and updates roll out centrally after review.

## How to build a plugin (use for every lab)

1. Make sure the skills listed in the lab exist and work (Part B). Create any that are missing.
2. Open a new Cowork conversation and paste the lab's **Create the plugin** prompt.
3. Review the plugin outline Cowork drafts: name, description, the skills included, trigger phrases and the connections it needs.
4. Ask for the plugin package and add it using the plugin option available in your session. Connections to systems such as [Sourcing system] need an approved connector; ask IT before connecting anything other than practice data.
5. Open a new conversation and paste the lab's **Use the plugin** prompt to test it end to end.

---

## Lab C1 – Procurement plugin

### Scenario

The team wants one package that gives every category manager the same procurement toolkit.

### Skills included

Procurement branding (B1), RFP drafting (B4), Bid evaluation (B2), Award recommendation memo, Supplier letters (B3), Onboarding and PO setup checklist, Contract renewal digest.

### Connections

SharePoint tender library, Outlook and Teams, [Sourcing system] via an approved connector.

### Create the plugin

```text
I would like to create a plugin called "[Company] Procurement" for the procurement team.
Bundle these skills: [Company] procurement branding, RFP drafting, Bid evaluation, Award recommendation memo, Supplier letters, Onboarding and PO setup checklist, Contract renewal digest. Create the Award recommendation memo, Onboarding and PO setup checklist, and Contract renewal digest skills if they do not exist, and show them to me first.
The plugin should read from the SharePoint tender library at [Practice folder] and use Outlook and Teams for drafts only. List [Sourcing system] as a future connection that needs IT approval.
Shared rules for every skill: never send, award, approve or pay anything; keep external messages as drafts; mark missing facts "Needs confirmation"; never share one bidder's information with another.
Write a short description and a list of trigger phrases so the team knows how to use it.
```

### Use the plugin

```text
Using the [Company] Procurement plugin, take RFP-2026-117 from evaluation to award: evaluate the bids, draft the award recommendation memo on the procurement template, draft the regret letters and prepare the onboarding checklist for the recommended bidder. Show me each output for approval.
```

### Check your result

- [ ] All seven skills are listed in the plugin.
- [ ] The end-to-end test produces four outputs, all as drafts.

---

## Lab C2 – Sourcing event plugin

### Scenario

Running a tender involves the same steps every time: draft the RFP, manage clarifications, evaluate, and recommend.

### Skills included

RFP drafting (B4), Clarification response (B5), Bid evaluation (B2), Award recommendation memo, Procurement branding (B1).

### Connections

SharePoint tender library, Outlook for drafts.

### Create the plugin

```text
I would like to create a plugin called "Sourcing Event" that runs a tender from RFP to award recommendation.
Bundle these skills: RFP drafting, Clarification response, Bid evaluation, Award recommendation memo, [Company] procurement branding.
Add a guided command "run sourcing event for" followed by a tender reference that checks which stage the tender is at (RFP, clarifications, evaluation, recommendation) and suggests the next step.
Shared rules: bidders' information is never mixed; clarification bulletins go to all bidders at the same time and only after my approval; nothing is sent automatically.
```

### Use the plugin

```text
Run sourcing event for RFP-2026-117. Tell me which stage it is at and prepare the next output.
```

### Check your result

- [ ] The plugin identifies the current stage correctly.
- [ ] It suggests and drafts the next output without sending it.

---

## Lab C3 – Supplier lifecycle plugin

### Scenario

From onboarding to quarterly reviews to risk follow-up, supplier management is split across people and files.

### Skills included

Onboarding checklist, Supplier review pack (B8), Supplier letters (B3), ESG questionnaire follow-up.

### Connections

Supplier master list in [Practice folder], Outlook for drafts, [Screening source] as a future connection.

### Create the plugin

```text
I would like to create a plugin called "Supplier Lifecycle" covering onboarding, performance reviews and risk follow-up.
Bundle these skills: Onboarding checklist, Supplier review pack, Supplier letters, ESG questionnaire follow-up. Create the Onboarding checklist and ESG questionnaire follow-up skills if they do not exist and show them to me first.
Add a command "supplier status for" followed by a supplier name that shows onboarding status, latest KPIs, open risk flags and contract renewal date in one summary.
Shared rules: bank details are never marked verified automatically; screening results come only from [Screening source]; all supplier communications are drafts.
```

### Use the plugin

```text
Supplier status for the supplier with the lowest governance score in "Supplier ESG – Practice.xlsx", then draft the follow-up letter.
```

### Check your result

- [ ] The status summary combines onboarding, KPIs, risk and renewal.
- [ ] The follow-up letter is a draft.

---

## Lab C4 – Contract management plugin

### Scenario

Contract managers need summaries, an obligations register, renewal alerts and notices from one place.

### Skills included

Contract summary (B7), Contract renewal digest, Supplier letters (B3), SLA service-credit notice.

### Connections

Contract library in [Practice folder], Outlook and Teams for drafts and digests.

### Create the plugin

```text
I would like to create a plugin called "Contract Management".
Bundle these skills: Contract summary, Contract renewal digest, Supplier letters, SLA service-credit notice. Create the Contract renewal digest and SLA service-credit notice skills if they do not exist and show them to me first.
Add a command "contract health for" followed by a contract reference that returns the summary, upcoming dates, unclaimed service credits and open obligations.
Shared rules: cite clause numbers; flag legal interpretation for Legal review; renewal and termination notices are drafts only; digests go only to me unless I approve another recipient.
```

### Use the plugin

```text
Contract health for the contract with the nearest auto-renewal notice deadline in the Contracts tab of [Practice data workbook].
```

### Check your result

- [ ] The result shows the notice deadline and what to decide.
- [ ] Any notice is a draft.

---

## Lab C5 – Procure-to-pay exceptions plugin

### Scenario

Invoice exceptions, price overcharges and missing receipts are handled one by one, with no shared view between procurement and accounts payable.

### Skills included

Three-way match triage, Price compliance check, Supplier query letters, Exceptions summary.

### Connections

Practice PO, receipt and invoice extracts in [Practice folder]; [Sourcing system] as a future connection.

### Create the plugin

```text
I would like to create a plugin called "Procure-to-Pay Exceptions".
Create and bundle these skills: Three-way match triage (classify invoice exceptions as Price, Quantity, No receipt or No PO with a tolerance setting), Price compliance check (compare invoiced prices with the valid contract rate), Supplier query letters (one draft per supplier listing the lines in question), and Exceptions summary (a weekly view of open exceptions by owner and age). Show me each skill before adding it.
Shared rules: never approve, release or block a payment; never change source data; all supplier communications are drafts.
```

### Use the plugin

```text
Using the Procure-to-Pay Exceptions plugin, triage "Three-Way Match – Practice.xlsx" and check "Price Compliance – Practice.xlsx", then give me one exceptions summary and the supplier query drafts.
```

### Check your result

- [ ] Exceptions from both files appear in one summary.
- [ ] No payment action is taken; queries are drafts.

---

## Lab C6 – Category management plugin

### Scenario

Category managers need spend insight, market context, negotiation preparation and a category strategy, built the same way each year.

### Skills included

Spend analysis, Market research summary, Negotiation brief (B6), Category strategy document.

### Connections

Spend extract in [Practice folder], web research from reputable public sources.

### Create the plugin

```text
I would like to create a plugin called "Category Management".
Bundle these skills: Spend analysis (spend by supplier and business unit, off-contract spend, top suppliers), Market research summary (reputable public sources only, every figure with source and date, never invented links), Negotiation brief, and Category strategy document (a Word strategy with current state, market, opportunities, sourcing plan and savings targets). Create any skill that does not exist and show it to me first.
Add a command "category review for" followed by a category name that runs spend analysis, market research and drafts the category strategy.
Shared rules: keep amounts in their recorded currency; label anything unverified; strategy documents are drafts for my review.
```

### Use the plugin

```text
Category review for Travel using the Spend tab of [Practice data workbook].
```

### Check your result

- [ ] Spend figures match the practice data.
- [ ] Every market figure has a source and date.
- [ ] The category strategy is a draft.
