# Versions

## 1.4.0 — November 3, 2026

- **catch-up-plan** adds an S-corp books section: an owner payroll check up front (with December 31 as the last day to pay owner wages for the year), S-corp owner accounts in place of owner draws, a five-way sort for owner payments, how to book payroll once, owner health insurance on the W-2, reimbursement plans, owner loans, and a year-end tie-out
- Adds payroll deadlines (Form 941, W-2, Form 940, state unemployment with Colorado as the example), the per-shareholder penalty on late S-corp returns, and checking that last year's CPA adjustments were posted
- New rules: never suggest an owner salary amount, never relabel past distributions as wages, never backdate payroll

## 1.3.1 — November 2, 2026

- **quarterly-tax-set-aside** corrects how it describes self-employment tax and credits: it's figured separately from income tax, refundable credits can offset it at filing, and the set-aside keeps the full 14% until a CPA says otherwise. It also points to the adjusted gross income line on the 2025 Form 1040

## 1.3.0 — November 2, 2026

- New skill, **quarterly-tax-set-aside**: a quick path to the next due date and safe payment (from last year's return, using the IRS's own penalty rule), a set-aside rate on profit built from self-employment tax, the person's top federal bracket and their state's rate, spouse withholding as an option, uneven-income and income-drop flags, what to do if you already owe, loan notes, and how to record tax payments, delivered as an Excel workbook
- **bookkeeping-ops-context** adds a Taxes section
- **catch-up-plan** hands freelancers off to the new skill once income and costs are sorted
- The library's planning-not-advice rule now says exactly what's off limits: estimates of this year's tax, the April bill, or penalties

## 1.2.2 — November 2, 2026

- **catch-up-plan** now works through the months a deadline needs from oldest to newest, since each month's ending balance starts the next, and for a loan ends by pulling the profit and loss and balance sheet for the same date

## 1.2.1 — November 1, 2026

- **catch-up-plan** now says the 120-day rule comes from SBA's standard 7(a) checklist and that smaller SBA loans can follow the lender's own checklist, so the lender's list comes first
- The starting-point check now explains why it matters for loans: lenders compare books against tax returns, and SBA 7(a) loans over $500,000 must be checked against IRS tax transcripts before closing

## 1.2.0 — November 1, 2026

- **catch-up-plan** now sizes the backlog by timing the first month instead of a transactions-per-hour table, which had no published source behind it. Until month one is timed, it uses a 5–10 hour placeholder from a bookkeeping firm's published range, clearly marked
- Months are locked only where the software allows it (QuickBooks closing date, Xero lock date). Where it can't, such as Wave, the month's report is saved as the record instead, and the status is now Done rather than Locked

## 1.1.0 — November 1, 2026

Checked against current rules and prices.

- **catch-up-plan** now lists the actual upcoming dates through October 2027, adds the 1099-NEC deadline (February 1, 2027 for 2026 forms), and flags the January 2028 quarterly payment that moves for a weekend and a holiday
- The 1099-NEC check now uses $600 for payments made in 2025 or earlier and $2,000 for 2026, rising with inflation from 2027, so backlogs that reach into 2025 are checked against the right amount
- The starting-balance check now handles smaller S-corps and partnerships that don't file a balance sheet (Schedule L) with their return
- The revenue check notes the federal 1099-K threshold (over $20,000 and over 200 transactions) and that all processor income counts whether or not a form arrives
- Hire-help ranges now follow published 2026 pricing by how messy the books are, not just by volume
- SBA loan guidance now cites the 7(a) checklist's 120-day rule and the SBA rulebook update that took effect October 1, 2026
- **bookkeeping-ops-context** records 1099 deadlines and this year's actual dates

## 1.0.0 — November 1, 2026

First release.

- New foundation skill, **bookkeeping-ops-context**, that writes `.agents/bookkeeping-ops-context.md`; every other skill reads it first
- New skill, **catch-up-plan**: turns months of unfinished books into a deadline-first plan — two questions and a 10-minute first task, a check that starting balances match the last tax return, setup before sorting, a revenue check for payment processor fees and refunds, a do-it-yourself vs. hire estimate, and CPA questions, delivered as an Excel workbook
- Library website at charlenetstrain.github.io/bookkeeping-ops-skills, published from `site/` to GitHub Pages
- Installs as a Claude Code plugin, through `npx skills`, or by copying folders
- MIT license, contributing guide, skill request form, `validate-skills.sh`, and releases published from a button in Actions
