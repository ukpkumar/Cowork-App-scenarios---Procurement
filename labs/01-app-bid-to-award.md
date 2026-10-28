# Lab A1 – Bid-to-award workspace

Illustrative scenario – fictional data.

## Scenario

A category manager has received three bids for a facilities management tender. Today the team compares bids by hand, writes the award memo, chases approvals by email, and sets up the supplier in a separate system. In this lab you build one app that runs the whole bid-to-award flow, with people approving every external step.

## What you will build

A "Bid-to-Award Workspace" app with these tabs: Bids, Compliance, Scoring, Recommendation, Approvals, Setup, Handoff.

| Step | What Cowork prepares | Who approves |
|---|---|---|
| 1 Compare bids | Pass/fail compliance first, then weighted scores with a citation for each | – |
| 2 Recommend supplier | Award recommendation memo and Tender Committee slides | Category manager reviews |
| 3 Route approvals | Approval request drafts to [DoA approvers] | Approvers per [DoA levels] |
| 4 Prepare setup | Supplier onboarding checklist and PO/contract data sheet for [Sourcing system] | – |
| 5 Notify stakeholders | Award and regret letters, stakeholder update | Sent only after approval |
| 6 Track handoff | Mobilisation milestones, owners, dates and weekly status | – |

## Practice data

Use these tabs in [Practice data workbook]: Tender, Evaluation_Criteria, Bids, Compliance, Technical_Scores, Evaluation_Summary, Approvals, Setup_Checklist, Handoff_Milestones.

The practice tender is RFP-2026-117, Integrated Facilities Management Services – [Head office], 3-year term, budget [Currency] 46.0m. Bidders are Bidder A, Bidder B and Bidder C. Evaluation is pass/fail compliance first, then Technical 60%, Commercial 30%, In-Country Value 10%.

## Steps

1. Open a new Cowork conversation and attach [Practice data workbook].
2. Paste the **Try this prompt**.
3. Read the plan and the list of tabs Cowork will read. Check it will not send anything. Approve.
4. Open the live preview and click through each tab.
5. Paste **Then try this** and check the change.

## Try this prompt

```text
/app Build a "Bid-to-Award Workspace" for practice tender RFP-2026-117 using the attached [Practice data workbook]. Before you build, show me your plan and the data you will access.
1. Run the pass/fail compliance checks first (trade licence, insurance, HSE certification, conflict-of-interest declaration, bid bond). Exclude failed bids from scoring and state the reason.
2. Score compliant bids: Technical 60%, Commercial 30%, In-Country Value 10%. Cite the source tab and evidence reference for every score.
3. Draft the award recommendation, approval requests to [DoA approvers], the supplier setup checklist, and award and regret letters. Hold every draft for my approval.
4. Add a handoff tracker with mobilisation milestones, owners and dates.
5. Use tabs: Bids, Compliance, Scoring, Recommendation, Approvals, Setup, Handoff. Add KPI cards for days in cycle, savings versus budget and approvals pending, and filters by tender and category.
Never send, award or approve anything automatically. Flag anything not evidenced in the files as "Needs confirmation".
```

## Then try this

```text
Add a savings-versus-budget card, and highlight any bidder whose price is more than 15% below the average of all bids for an abnormally-low-bid review.
```

## Check your result

- [ ] Bidder C is excluded because its HSE certificate has expired.
- [ ] Bidder A ranks first with 89.7; Bidder B second with 86.7.
- [ ] Savings versus budget shows 3.4m, days in cycle 24, approvals pending 2.
- [ ] Every score has a citation to a tab or evidence reference.
- [ ] Letters and approval requests are drafts; nothing was sent.
- [ ] No bid is flagged as abnormally low (the lowest is about 8% below the average).

## Discussion

- Why must compliance run before scoring?
- Where in your own process would the human checkpoints sit?
