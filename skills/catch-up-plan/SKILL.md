---
name: catch-up-plan
description: Turns months of unfinished bookkeeping into a dated catch-up plan and Excel workbook, ordered by the nearest deadline. Use when a small business owner, freelancer or solo operator says "I'm behind on my books," "I haven't done my bookkeeping in months," "my accountant needs my numbers," "my bookkeeper quit," "I got a letter from the IRS," "I need my books done for a loan," or has a tax deadline coming and unfinished books. Produces a workbook with the backlog, a week-by-week plan, a do-it-yourself vs. hire estimate, and questions for their CPA.
metadata:
  version: 1.4.0
---

# Catch-up plan

You help someone who is months behind on their books get caught up before a deadline someone else set, then stay caught up.

Most people who need this didn't fall behind on purpose. A tax date crept up, a bookkeeper disappeared, or the business got busy. Never lecture. Start with the deadline and work backwards.

This is a planning tool, not tax or accounting advice. Say once, briefly, that you're not a CPA, and send anything about what they'll owe to one.

## Before you start

If `.agents/bookkeeping-ops-context.md` exists (or `.claude/bookkeeping-ops-context.md`), read it first. Use the business setup, accounts, software, helpers and deadlines it already has, confirm anything that looks out of date, and only ask for what's missing. If it doesn't exist, go ahead with what you're given, and suggest running **bookkeeping-ops-context** once so the next skill doesn't have to ask.

## 1. Start small: two questions, one task

Ask only these two questions first (skip any the context file already answers):

1. **"What date do you need your books done by, and who set it?"**
2. **"What's the last month you're confident is finished?"** ("Never" or "not sure" is a fine answer.)

Then give one task they can finish in 10 minutes:

> Log in to your main business bank account and download the statement for every month since the last finished one, as PDFs. Save them in one folder called "Catch-up statements."

Don't ask anything else until they've done this or said they can't. Getting one thing finished matters more than getting every detail up front.

## 2. Route by who they are

After the two questions, place them in one of three paths. Ask one question if it isn't clear: "Is this for a business with its own bank account, or mostly you working on your own?"

- **Freelancer or solo with one account and no bookkeeping software.** Use the light path: one account, a simple spreadsheet instead of six tabs, and no categories beyond the ones on the Schedule C tax form. If their real question is "how much do I owe or set aside?", sort the income and expenses first, then hand off to **quarterly-tax-set-aside**.
- **Small business (the standard path).** Everything below.
- **S-corp.** The standard path plus the S-corp books section after step 6. Ask about owner payroll in step 4, not at the end: it's the item with a hard December 31 deadline.
- **Seeking a loan, or more than 1,000 transactions a month.** Use the standard path to get current. Lenders usually also want statements prepared on an accrual basis (income and costs counted when earned or owed, not when cash moves), a list of who owes the business money and whom it owes, and a list of existing loans. Put "Ask your CPA whether your books need to be on an accrual basis for the lender" on the CPA questions tab.

## 3. Confirm the deadline

| Deadline | Usual date | Who sets it |
|---|---|---|
| Individual or single-member LLC tax return | April 15 | IRS |
| Extension deadline for that return | October 15 | IRS |
| S-corp or partnership return | March 15 (extension: September 15) | IRS |
| Quarterly estimated taxes | April 15, June 15, September 15, January 15 | IRS |
| 1099-NEC forms to contractors and the IRS | January 31 | IRS |
| S-corp owner wages for the year | December 31 (last day wages can be paid for that year) | IRS |
| Payroll reports (Form 941) | April 30, July 31, October 31, January 31 | IRS |
| W-2 and W-3 forms, and the yearly unemployment return (Form 940) | January 31 | IRS |
| State payroll and unemployment reports | Varies; Colorado's unemployment report is due the last day of the month after each quarter | State |
| IRS or state letter | The response date printed on the letter | IRS or state |
| Loan application | The date the lender gave | Lender |
| Accountant request | The date the CPA gave | CPA |

Look up this year's actual dates on IRS.gov before using them: dates move to the next business day when they fall on a weekend or holiday, and disaster areas sometimes get extensions. As of November 2026, the next ones are:

- December 31, 2026: last day an S-corp can pay its owner 2026 wages through payroll
- January 15, 2027: last 2026 quarterly estimated payment
- February 1, 2027: 1099-NEC forms, W-2s and W-3, and the fourth-quarter 2026 payroll report (Form 941) (January 31 is a Sunday). Form 940 is usually due the same day; confirm.
- March 15, 2027: S-corp and partnership returns for 2026. A late S-corp return carries a penalty for each shareholder for each month it's late, even when no tax is due, so this date is firm.
- April 15, 2027: individual and single-member LLC returns for 2026, and the first 2027 quarterly payment
- October 15, 2027: extended individual returns

Watch for January 2028: the 15th is a Saturday and the 17th is Martin Luther King Jr. Day, so look up where the last 2027 quarterly payment lands.

For SBA loans, look up how recent the statements must be and cite it. SBA's standard 7(a) submission checklist asks for a current income statement and balance sheet dated the same day, within 120 days of submission, plus three years of year-end statements or tax returns. SBA's rulebook for these loans was updated on October 1, 2026 (SOP 50 10 8.1), so confirm the current requirement with the lender. Smaller SBA loans can follow the lender's own checklist instead, which is one more reason to ask the lender for their list first. If there's no outside deadline, set one 6 weeks out so the plan has a finish line.

If the deadline is less than 2 weeks away, say so plainly and make "Ask your CPA about filing an extension" the first step on the Summary tab. An extension gives more time to file, not more time to pay.

## 4. Take stock (after the first task)

Ask for whatever the context file doesn't already have, together in one message:

- What kind of business is it, and is it set up as a sole proprietor, LLC or S-corp? ("I'm not sure" is fine; it's on their last tax return.)
- Which accounts touch the business? Include personal cards used for business.
- Roughly how many transactions a month across all of them: under 100, 100–300, 300–1,000, or over 1,000?
- What software are the books in now, if any? Do they still have access?
- Did a bookkeeper or service do this before? Do they have a copy of everything they did?
- Is there anything scary in the pile: an IRS or state letter, missed payroll filings, unpaid sales tax, missed quarterly payments?
- **For an S-corp:** does the owner get paid through payroll? Is there a payroll provider, and were the quarterly payroll reports filed? If the owner has only been moving money to themselves by transfer, flag it on the Summary tab and the CPA questions tab right away (see S-corp books).

If a provider shut down or vanished, the first task is getting their data out: statements straight from each bank, plus whatever exports the old provider allows. Don't plan around data they can't reach.

## 5. Check the starting point

Before catching up any month, make sure the last finished month is actually right. Everything after it builds on it.

- **Sole proprietor or single-member LLC:** total income and total expenses in the books for the last filed year should match the last Schedule C.
- **S-corp or partnership:** the year-end balances in the books (cash, loans, what's owed) should match the balance sheet on the last filed return (Schedule L). Smaller businesses can skip Schedule L: an S-corp when total receipts and year-end assets were both under $250,000, and a partnership when receipts were under $250,000, assets under $1 million and a few other conditions are met. If their return has no Schedule L, match total income and expenses to the return instead, and match each account's year-end balance to its December statement.
- **Every path:** the ending balance of each bank and card account at the last finished month should match that month's statement exactly.

For a loan, this check matters twice: lenders compare the books against the tax returns, and for SBA 7(a) loans over $500,000 they must check the numbers against IRS tax transcripts and resolve any real gap before closing.

Also check that last year's year-end adjustments from the CPA (the changes they made when preparing the return) were posted to the books. Unposted adjustments are a common reason opening balances don't match.

If anything doesn't match, make "Fix starting balances" the first row of the Plan and add the mismatch to the CPA questions tab. If there are no prior books, the starting point is the opening balance on the first statement in the backlog.

## 6. Set up before sorting

Do these once, before any month gets sorted:

1. **Set up the categories (chart of accounts).** Use the software's default list for their industry, or the Schedule C categories on the light path. Add only what's missing.
2. **Record credit cards and loans as what's owed, not as spending.** Card payments and loan payments are transfers, not expenses. Only the interest on a loan is an expense.
3. **Mark transfers between their own accounts as transfers**, so the same money isn't counted twice.
4. **For an S-corp, set up the owner accounts** from the S-corp books section before sorting anything.

## S-corp books

An S-corp's books treat the owner differently from a sole proprietor's. Do this section whenever the business is an S-corp. The bookkeeper finds and sorts; the CPA decides amounts.

1. **Check for owner payroll first.** The IRS requires an S-corp to pay an owner who works in the business a reasonable salary through payroll before taking other money out, and it can reclassify those other payments as wages. Look for a payroll provider, an officer compensation account and filed payroll reports. If the owner has only taken transfers:
   - Flag it on the Summary tab and the CPA questions tab now.
   - Before December 31, there's still time to set up payroll and pay the owner wages for this year. Wages count in the quarter they're paid, so a December wage goes on the fourth-quarter payroll report. The CPA decides the amount.
   - Once the year closes, tax pros say money already taken can't be relabeled as wages; the fix is payroll going forward. Confirm with the CPA.
   - Some states treat owners as employees for unemployment premiums even when payroll was never run. Colorado, for example, counts corporate officers as employees and includes S-corp distributions in wages for unemployment. Add the state question to the CPA tab.
2. **Set up the owner accounts:** shareholder distributions, shareholder contributions, loan to shareholder, loan from shareholder, common stock, additional paid-in capital, retained earnings, officer compensation (the owner's wages), payroll tax expense, and payroll liabilities. Retire "owner draw"; that's a sole proprietor's account.
3. **Sort every payment between the owner and the business into one of five:** wages (only through payroll), a distribution, a reimbursement, a loan (to or from the owner), or a contribution (money the owner put in). Personal spending from the business account is a distribution. So are the owner's personal tax payments. Distributions are never business expenses and never payroll.
4. **Book payroll from the payroll report, once.** Gross wages go to officer compensation, the company's share of payroll taxes to payroll tax expense, withholdings and taxes owed to payroll liabilities, and net pay comes out of the bank. Payroll liabilities should drop to zero after each tax deposit. If the payroll provider already posts to the books, don't also record the bank withdrawals as expenses, or payroll gets counted twice.
5. **Owner health insurance.** If the company paid or reimbursed the owner's health insurance, it has to show up on the owner's W-2 (box 1 only, not the Social Security and Medicare boxes), or the owner loses their personal deduction. Check this before the last payroll of the year so the payroll provider can add it. If the owner paid premiums personally and wasn't reimbursed, ask the CPA.
6. **Reimbursements.** Paying the owner back for home office, mileage or phone costs is tax-free only under a written reimbursement plan (an accountable plan): a business purpose, records turned in reasonably fast, and any extra paid back. No written plan or no receipts: don't book them as tax-free; flag for the CPA.
7. **Loans between the owner and the company.** Keep money lent to the owner and money borrowed from the owner in two separate accounts, each backed by a written note and real repayments. No note or no repayments: flag for the CPA.
8. **Basis.** Distributions above what the owner has put in and earned can be taxable. The bookkeeper doesn't track this; give the CPA the year's totals for distributions, contributions and owner loans, and they'll handle it (Form 7203).

**Year-end tie-out:** the payroll reports and W-2s match the payroll accounts, payroll liabilities are cleared, and the totals for distributions, contributions and owner loans are on the CPA questions tab. Look up this year's Social Security wage limit ($184,500 for 2026) and state payroll rates (Colorado's paid leave premium is 0.88% for 2026) before using them.

## 7. Size the backlog

Months behind = months from the last finished month to the most recent full month.

Size it by timing it, not by a rule of thumb. How long a month takes depends on the number of accounts, how messy the books are and how familiar the person is with their software, so a table can be off by double either way.

1. **Make the first month in the plan a timed month.** Ask them to note how long it takes, start to finish.
2. **Until then, use a placeholder:** 5–10 hours per month of backlog, one bookkeeping firm's published range for a small business's monthly bookkeeping. Mark it "placeholder — replace after month one" in the workbook.
3. **After month one, replace the placeholder** with their real time and let the plan recalculate. Later months usually go a little faster once categories and rules are set up, so don't add extra time for that.
4. **Flag what will make it slower:** personal and business money mixed in the same account, missing receipts, and more than one account per month. Name these on the Summary tab so the timed month is read in context.

If they have more than 1,000 transactions a month, recommend help before timing anything.

## 8. Order the work

1. **Get every statement downloaded**, from every account on the Accounts tab.
2. **Fix starting balances** if step 5 found a mismatch.
3. **Finish the months the deadline needs.** For a tax return, that's the full tax year. For a loan, it's the latest months plus year-to-date. For an IRS letter, it's the year named in the letter. Work through these months oldest to newest, since each month's ending balance is the next month's starting balance.
4. **Then fill in the rest**, oldest first.
5. **For a loan, pull the profit and loss and the balance sheet for the same end date**, inside the lender's window, once the last month is matched to the bank.

Within each month, in this order:

1. **Sort** each transaction into a category.
2. **Separate personal from business.** Personal spending from a business account goes to owner draws (money the owner took out), not expenses. For an S-corp, it goes to shareholder distributions instead.
3. **Check the revenue.** Payment processors deposit money with their fees already taken out, and refunds come back later. Record the full sale amount as income and the fee as an expense, so income in the books matches the processor's monthly report, not the bank deposit. Check that refunds and chargebacks are recorded, and that no transfer between their own accounts is counted as income. Processors send a 1099-K only above the federal threshold (over $20,000 and over 200 transactions; some states set lower thresholds), so don't wait for a form: all of it is income whether or not one arrives.
4. **Match to the bank.** The month's ending balance in the books must match the statement exactly, to the cent.
5. **Lock the month if the software allows it**, so nothing in it changes by accident. QuickBooks calls this a closing date and Xero calls it a lock date. Some programs can't lock past months (Wave, for one). Then save a PDF of the month's profit and loss report next to that month's statement as the record of what was finished, and tell them not to edit that month without noting why. Either way, mark the month Done.

Also check contractors: look up the current threshold for sending a 1099-NEC. It rose from $600 to $2,000 for payments made in 2026, and goes up with inflation each year starting in 2027. Payments made in 2025 or earlier still use $600, which matters for a backlog that reaches into 2025. List anyone paid over the threshold for each year, and add any missed 1099s to the CPA questions tab.

## 9. Do it yourself or hire help

Show both side by side on the Summary tab.

**Do it yourself:** the placeholder (or timed) hours per month times months behind, divided by the hours per week they say they can give. If the finish date lands after the deadline, say so plainly and recommend help.

**Hire help:** published 2026 ranges for catch-up work are about $150–$300 per month of backlog for simple books, $300–$600 for typical books, and $600–$1,200 or more for messy ones (several accounts, mixed personal and business money, missing statements, S-corps and partnerships). How messy the books are often matters more than how many months are behind. Pick the range that fits, show a low, middle and high estimate, mark them as market ranges rather than quotes, and say real quotes depend on the books. Look up current ranges if this skill's figures are more than a year old.

Recommend help when any of these is true: the deadline is under 3 weeks away, the DIY finish date misses the deadline, they have more than 1,000 transactions a month, there are payroll or sales tax filings missing, or there's an IRS or state letter.

Give them these questions to ask any bookkeeper:

- Will you do a paid review of my books first, then give me a fixed price and a finish date?
- Do I have to sign up for monthly service to get the catch-up done?
- Will I own the files, and can I export everything if you close or I leave?
- Will you talk to my CPA directly?

Tell them they can hand over this workbook so the bookkeeper starts with the accounts, backlog and open questions already listed. Don't recommend specific bookkeepers, firms or software brands.

## 10. Flag what needs a CPA

Put these on the CPA questions tab instead of answering them:

- Any IRS or state letter
- Starting balances that don't match the last return
- Missed quarterly estimated payments, or a large expected bill
- Missed payroll tax filings or 1099s
- Sales tax owed in any state
- Whether to file an extension or set up an IRS payment plan
- Whether the books need to be on an accrual basis (for a lender)
- For an S-corp: the owner's salary amount, any catch-up wage before December 31, late or corrected payroll reports, past years when the owner was paid only by transfer, state unemployment on owner pay, owner health insurance paid personally, reimbursements without a written plan, owner loans without a note, and the owner's basis

Never estimate penalties or say whether someone will owe. Never suggest a salary amount or a salary-to-distribution split.

## 11. Build the workbook

Name it `catch-up-plan-[business-name]-[YYYY-MM-DD].xlsx`. Load the xlsx skill before building. On the light path, make only Summary, Backlog and Stay caught up.

1. **Summary** — one page, readable at a glance: deadline, months behind, estimated hours, DIY vs. hire cost, finish date, and the single next step.
2. **Accounts** — every bank account, card, payment processor and loan that touches the business, with the last finished month and whether statements are downloaded. No account numbers.
3. **Backlog** — one row per account per month, with status (Not started / Statements in / Sorted / Matched to bank / Done), whether it's locked in the software, and hours per month (placeholder until month one is timed).
4. **Plan** — a week-by-week schedule in the order from step 8, ending at least 7 days before the deadline.
5. **CPA questions** — everything from step 10 that applies, with the month or account it came from.
6. **Stay caught up** — the routine from step 12.

Workbook rules:

- Every total and date is a formula reading from the Accounts and Backlog tabs, so changing an estimate or a status updates the plan.
- Placeholder hours and cost ranges are visibly marked; the timed first month replaces the placeholder in one cell.
- A progress bar on Summary: months Done out of months behind.
- The finish date turns red when it lands after the deadline.
- Readable on a phone: large text on Summary and the key numbers on the first screen. Mention it opens in Google Sheets too.

The workbook doubles as an intake packet: if they hire a bookkeeper, they can hand it over on day one.

Recalculate and open the finished file to check that formulas work, the dates are right, and nothing shows an error before sending.

## 12. Stay caught up

The last tab is how this doesn't happen again:

- **Every week, 20 minutes:** sort new transactions and snap photos of receipts.
- **Every month, within 10 days of month end:** match each account to its statement, check revenue against the processor's report, and lock the month (or save its report, if the software can't lock).
- **Every quarter:** set aside money for taxes, pay quarterly estimates, and export a copy of the books.
- **Always:** keep business money in its own bank account and card.
- **S-corp, every payroll:** check payroll liabilities clear after each deposit. **Every December:** confirm owner wages for the year are paid through payroll and owner health insurance is on the W-2.

## 13. Deliver

In chat:

1. The deadline, the finish date, and whether they'll make it.
2. The single next step they can do today.
3. Do-it-yourself vs. hire, in one or two lines.
4. Anything that needs a CPA now.
5. The workbook.

If they gave details the context file doesn't have, or that differ from it (a new account, a finished month, a new deadline, a new bookkeeper), offer to update `.agents/bookkeeping-ops-context.md` so the next skill starts current. As months are marked Done, offer to update the last finished month there too.

## Rules

- Plain words. Say "match to the bank," not "reconcile," and "categories," not "chart of accounts," unless they use the term first.
- Lead with the date and the next step, not the size of the mess.
- If they say they're embarrassed, say once that this is common and move straight to the plan.
- Never imply they're behind on purpose or doing it wrong. State where they are and the next step.
- Never estimate taxes or penalties. That's the CPA's job.
- For an S-corp, never suggest a salary amount, never relabel past distributions as wages, and never backdate payroll.
- Never ask for or store account numbers, tax ID numbers or passwords.
- End every reply with one concrete next step they can do today.

## Related skills

- **bookkeeping-ops-context** — reads the business setup, accounts and deadlines first, and takes back each finished month and any new details
- **quarterly-tax-set-aside** — once income and costs are sorted, works out each quarter's safe payment and what to set aside

Coming next in this library: a loan-ready books skill for owners who need lender-ready statements once they're caught up.
