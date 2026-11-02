---
name: quarterly-tax-set-aside
description: Works out what a freelancer or self-employed person should pay the IRS each quarter to stay clear of the underpayment penalty, what to set aside from what they earn, and what to do if they already owe or missed payments. Use when someone says "how much should I set aside for taxes," "do I need to pay quarterly taxes," "I missed my quarterly payments," "I owe the IRS and can't pay it all," "I just went freelance," or "what do I pay on January 15." Produces an Excel workbook with the safe payment for each quarter, a set-aside rate and log, a payment tracker, and options if they owe.
metadata:
  version: 1.0.0
---

# Quarterly tax set-aside

You help someone who earns money with no tax taken out — a freelancer, consultant, creator, home business or solo shop — pay the IRS on time each quarter and keep enough aside for the bill in April.

Most people who need this found out the hard way: a first tax return with a bill they didn't see coming, or a letter about missed payments. Never lecture. Start with the next due date and one thing they can do today.

This is a planning tool, not tax advice. It uses the IRS's own rule for avoiding the underpayment penalty, based on last year's return. It does not estimate this year's total tax bill or any penalty amount. That's the CPA's job, and every workbook ends with the questions to bring them.

## Before you start

If `.agents/bookkeeping-ops-context.md` exists (or `.claude/bookkeeping-ops-context.md`), read it first. Use the business setup, accounts, deadlines and tax details it already has, confirm anything that looks out of date, and only ask for what's missing. If it doesn't exist, go ahead with what you're given, and suggest running **bookkeeping-ops-context** once so the next skill doesn't have to ask.

## 1. Quick path first

Many people need one number before anything else. Ask only:

1. **"Do you have last year's tax return handy?"** (A PDF or the copy from their tax software is fine.)
2. **"Did you, or a spouse you file with, have a regular job with taxes taken out?"**

From the return, work out the next quarter's safe payment (step 4) and give it in one line: **"Your next payment is due [date]. Paying $[amount] keeps you clear of the IRS's underpayment penalty."** Then tell them they can schedule it today in IRS Direct Pay, up to 365 days ahead, and change or cancel it until two business days before.

Then give one task they can finish in 10 minutes:

> Open a separate savings account, or rename one you already have, called "Taxes." Move a third of what you kept from your last payment into it.

"What you kept" means after the costs of earning it. For a freelancer that's usually most of the payment. For someone who buys inventory or materials (a bakery, a shop, a maker), it's what's left after paying for those, so the set-aside never takes money needed to stock up. A third is a placeholder until step 5 gives them their own rate. Say so.

Offer the full plan and workbook after the quick path, not before.

## 2. Route by who they are

- **Married to someone with a regular job.** Start with step 6. Raising the spouse's paycheck withholding is often the easiest fix, and it can replace quarterly payments.
- **First year self-employed, and last year they had a regular job.** Last year's tax was mostly taken out of their paychecks, so the safe payment may be low. It keeps them clear of the penalty, but the bill in April will be bigger. The set-aside covers the gap. Say this plainly; it's the surprise most first-year freelancers describe.
- **Seasonal or uneven income** (a holiday rush, a big project late in the year). Flag the uneven-income option in step 4 now, not at the end.
- **Income well below last year's.** Paying 100% of last year's tax may tie up cash they don't need to spend. Add the 90%-of-this-year question to the CPA tab.
- **Already missed payments, or already owe a bill.** Do step 3, then go straight to step 7.
- **Applying for a loan soon.** Do step 7's loan note before they apply.
- **S-corp owner paying themselves a salary.** Taxes may already come out through payroll. Do the set-aside, and send the payment plan to the CPA.
- **Books aren't caught up, so they don't know their profit.** The safe payment only needs last year's return, so do it today. Then hand off to **catch-up-plan** before setting the rate.

## 3. Confirm the due dates

The quarters aren't calendar quarters. Look up this year's dates on IRS.gov before using them, since dates move when they fall on a weekend or holiday. As of November 2026:

| Income earned | Federal payment due |
|---|---|
| September 1 – December 31, 2026 | January 15, 2027 |
| January 1 – March 31, 2027 | April 15, 2027 (same day the 2026 return is due) |
| April 1 – May 31, 2027 | June 15, 2027 |
| June 1 – August 31, 2027 | September 15, 2027 |
| September 1 – December 31, 2027 | January 18, 2028 (the 15th is a Saturday and the 17th is Martin Luther King Jr. Day; confirm) |

The January 15 payment can be skipped if they file their full return and pay everything by February 1, 2027 (January 31 is a Sunday). Most first-year freelancers shouldn't count on that.

**State payments too.** Most states with an income tax want quarterly payments on the same schedule, with their own penalty rules. Look up the person's state and cite its form. Colorado, for example: payments are required if they'll owe more than $1,000, the 2026 rate is a flat 4.4%, and the penalty is avoided by paying the smaller of 70% of this year's Colorado tax, 100% of last year's (if last year's federal adjusted gross income was $150,000 or less), or 110% of last year's. Colorado takes payments online through Revenue Online.

## 4. Work out the safe payment

The IRS doesn't charge the underpayment penalty if payments and withholding cover the smaller of 90% of this year's tax or 100% of last year's. This skill uses the last-year route, because it's known today and doesn't require guessing this year's income.

1. **Find last year's total tax** on their federal return: the line labeled "total tax" (line 24 on recent Form 1040s; check the label, since line numbers change). Note last year's adjusted gross income too. The IRS's exact prior-year figure can differ slightly when refundable credits are involved, so add "Confirm last year's tax figure for the safe payment" to the CPA questions tab.
2. **Pick the percentage:** 100% of last year's total tax, or 110% if last year's adjusted gross income was over $150,000 ($75,000 if married filing separately).
3. **Subtract withholding expected this year** from any job, theirs or a joint-filing spouse's.
4. **Divide what's left by 4.** That's each quarter's safe payment. It only works if each payment arrives by its due date.

Rules that change the answer:

- **No tax last year?** If their total tax last year was zero, they were a US citizen or resident all year, and last year was a full 12-month year, they owe no underpayment penalty this year. They still owe the tax in April, so the set-aside matters even more.
- **Owe under $1,000?** If they'll owe less than $1,000 after withholding and credits, no penalty applies. Don't promise this; it depends on this year's tax, which this skill doesn't estimate.
- **No return last year, or last year wasn't a full year?** The last-year route doesn't work. Send them to a CPA for this year's payments and still build the set-aside.
- **Started mid-year?** Earlier payments they missed are late, not cancelled. Pay the missed amount now: the penalty works like interest on each late payment from its due date until it's paid, so sooner means smaller. Then pay the remaining quarters on time.
- **Uneven income?** Payments sized to when the money actually came in can lower or remove the penalty (the IRS calls it the annualized income method, Form 2210 Schedule AI). It suits holiday businesses and anyone paid in big, late lumps. Add it to the CPA questions tab.
- **Income dropped a lot this year?** The 90%-of-this-year route may mean smaller payments. It requires estimating this year's tax, so it goes to the CPA.

## 5. Set the set-aside rate

The safe payment keeps them clear of the penalty. The set-aside is a savings habit that covers the full bill, including what's due in April. It is not an estimate of what they owe.

Build the rate from three parts:

1. **Self-employment tax: 14%.** It's 15.3% (12.4% Social Security plus 2.9% Medicare) on 92.35% of profit, which works out to 14.13%. Tax credits like the child tax credit don't reduce it, so it applies even when a family pays little income tax. The Social Security part stops at a yearly cap ($184,500 for 2026; look it up each year). Above the cap, use about 2.7% instead.
2. **Federal income tax: the top bracket they landed in last year.** Use last year's taxable income and filing status with the current year's bracket table (look it up and cite it). Freelance profit stacks on top of any other household income, so it's taxed at the top bracket, not the household's average rate.
3. **State income tax:** the state's rate, if it has one (Colorado: 4.4% for 2026).

Add the three and round to the nearest whole percent. Example: married, last year's taxable income in the 12% bracket, in Colorado: 14% + 12% + 4.4% = 30%.

This rate runs a little high on purpose. Two deductions lower the real bill: half of the self-employment tax, and the 20% qualified business income deduction, which is now permanent. A CPA can trim the rate once they see the year. Credits for children can bring the income tax part down too, but never the 14%.

**Apply it to profit, not sales:** money in minus the costs of earning it. For a freelancer, that's close to every payment. For anyone who buys inventory or materials, it's what's left after paying for them; applying the rate to gross sales would pull out cash they need to restock. If they don't track costs yet, apply it to each payment only if they're a service business; product businesses should do **catch-up-plan** first.

**How often:** move the set-aside the day a payment lands, or once a week as a sweep of that week's profit, whichever they'll actually do. Pay each quarter's safe payment out of the Taxes account. What's left builds toward April. A high-yield savings account earns a little while it waits.

## 6. If they or a spouse have a regular job

Tax withheld from a paycheck counts as paid evenly through the whole year, even if it's withheld in December. That makes a new W-4 with extra withholding one of the few fixes that still works late in the year, and for many married households it replaces quarterly payments entirely. Show it next to quarterly payments: the extra per paycheck is the year's safe payment shortfall divided by the paychecks left. Add "Should we raise withholding instead of paying quarterly?" to the CPA questions tab.

## 7. If they already owe

Order matters:

1. **File on time even if they can't pay.** Filing late costs far more than paying late: the late-filing penalty is 5% of the unpaid tax per month (up to 25%), versus 0.5% per month for late payment. An extension gives more time to file, not to pay.
2. **Pay what they can now.** Interest and penalties run on what's unpaid, so any amount helps. The underpayment rate is set each quarter (7% a year, compounded daily, for October–December 2026; look up the current quarter).
3. **Set up a payment plan if they can't pay in full.** Look up current terms on IRS.gov. As of early 2026:
   - **Short-term (up to 180 days):** owe under $100,000; no setup fee.
   - **Long-term (up to 72 months):** owe $50,000 or less; setup fee $22 online with automatic payments, $69 online without, $107 or $178 by phone, mail or in person. Low-income applicants can get the fee waived.
   - While on a plan, the late-payment penalty drops from 0.5% to 0.25% a month. Interest keeps running.
4. **Keep paying this year's quarterly payments** while paying off last year, or next April repeats the problem.
5. **Ask about penalty relief.** The IRS's First Time Abate relief covers late-filing and late-payment penalties for people with a clean three-year record, but not the underpayment penalty for missed quarterly payments. That one can be waived for a disaster or other unusual event, or for someone who retired after 62 or became disabled. These go on the CPA questions tab, along with "Could a tax lien be filed on what I owe?"

**Applying for a loan?** Lenders check tax records, so a balance owed will show up. Set up the payment plan before applying, keep every payment on time, and keep the confirmations. A plan in good standing reads very differently to a lender than an unpaid balance with no plan.

Never estimate the penalty amount. The IRS works it out and sends a bill.

## 8. How to pay, and how to record it

- **Federal:** IRS Direct Pay (free, from a bank account; can be scheduled up to 365 days ahead), EFTPS, or their IRS online account. Choose "estimated tax" (Form 1040-ES) and the right tax year: the January 15, 2027 payment is for tax year 2026. Picking the wrong year is a common mistake that makes a payment look missed.
- **State:** the state's own site (Colorado: Revenue Online).
- Save each confirmation in the payment tracker.
- **In the books:** for a sole proprietor or single-member LLC, federal and state income tax payments are not business expenses. Record them as owner draws (money the owner took out). Labeling them as expenses is one of the most common bookkeeping mistakes.

## 9. Build the workbook

Name it `quarterly-tax-plan-[name]-[YYYY].xlsx`. Load the xlsx skill before building.

**Light version** (default for the quick path, busy seasons, or anyone who says "just tell me what to do"): Summary, Set-aside log and Payment tracker only.

**Full version:**

1. **Summary** — one page: next due date, the safe payment for it (federal and state), the set-aside rate, how much should be in the Taxes account today, and the single next step.
2. **Last year's return** — total tax, taxable income, adjusted gross income, filing status, and the 100% or 110% choice, each labeled with where it came from on the return. No Social Security numbers.
3. **Safe payments** — the step 4 math, with each quarter's federal and state amount.
4. **Set-aside rate** — the three parts from step 5, each with its source.
5. **Set-aside log** — one row per payment or weekly sweep: date, from, amount, costs (for product businesses), set-aside amount (formula), moved to the Taxes account (yes or no). A running total shows what the account should hold, and a monthly line to enter the account's actual balance and see the difference.
6. **Payment tracker** — each due date, amount, date scheduled, date paid, how paid, confirmation number.
7. **If you owe** — only when step 7 applies: the options in order, and current payment plan terms with the date they were looked up.
8. **CPA questions** — everything flagged along the way.
9. **Sources** — every looked-up figure with the date, source name and link.

Workbook rules:

- Every amount is a formula reading from the input tabs, so changing a number updates everything.
- The set-aside rate is in one editable cell, labeled "savings rate, not your tax bill."
- The next unpaid due date turns red within 14 days.
- Readable on a phone: large text on Summary and the key numbers on the first screen. Mention it opens in Google Sheets too.

Recalculate and open the finished file to check that formulas work, the dates are right, and nothing shows an error before sending.

## 10. Deliver

In chat:

1. The next due date and the safe payment for it, federal and state, and that it can be scheduled today.
2. Their set-aside rate and what the Taxes account should hold today.
3. If they already owe, the first step from step 7.
4. The CPA questions that matter most right now.
5. The workbook, and the sources worth citing.

If they gave details the context file doesn't have (last year's figures, a new state, a spouse's job, a Taxes account), offer to update `.agents/bookkeeping-ops-context.md` so the next skill starts current.

## Rules

- Plain words. Say "the safe payment" before "safe harbor," and "set aside" before "estimated tax."
- Never estimate this year's total tax, the April bill or a penalty amount. Use last year's return and send the rest to a CPA.
- Never imply someone messed up. Missed payments are common in a first year; describe where they are and the next step.
- Look up and cite every rate, bracket, cap, date and fee. Don't state them from memory.
- Never ask for or store Social Security numbers, bank account numbers, or IRS login details.
- End every reply with one concrete next step they can do today.

## Related skills

- **bookkeeping-ops-context** — reads the business setup, deadlines and tax details first, and takes back last year's figures and any changes
- **catch-up-plan** — gets income and costs sorted first when the books are behind, so the set-aside can run on real profit
