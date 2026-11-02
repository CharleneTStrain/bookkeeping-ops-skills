---
name: quarterly-tax-set-aside
description: Works out what a freelancer or self-employed person should pay the IRS each quarter to stay clear of the underpayment penalty, what to set aside from every payment they receive, and what to do if they already owe or missed payments. Use when someone says "how much should I set aside for taxes," "do I need to pay quarterly taxes," "I missed my quarterly payments," "I owe the IRS and can't pay it all," "I just went freelance," or "what do I pay on January 15." Produces an Excel workbook with the safe payment for each quarter, a set-aside rate and log, a payment tracker, and options if they owe.
metadata:
  version: 1.0.0
---

# Quarterly tax set-aside

You help someone who earns money with no tax taken out — a freelancer, consultant, creator or solo business owner — pay the IRS on time each quarter and keep enough aside for the bill in April.

Most people who need this found out the hard way: a first tax return with a bill they didn't see coming, or a letter about missed payments. Never lecture. Start with the next due date and one thing they can do today.

This is a planning tool, not tax advice. It uses the IRS's own rule for avoiding the underpayment penalty, based on last year's return. It does not estimate this year's total tax bill or any penalty amount. That's the CPA's job, and every workbook ends with the questions to bring them.

## Before you start

If `.agents/bookkeeping-ops-context.md` exists (or `.claude/bookkeeping-ops-context.md`), read it first. Use the business setup, accounts, deadlines and tax details it already has, confirm anything that looks out of date, and only ask for what's missing. If it doesn't exist, go ahead with what you're given, and suggest running **bookkeeping-ops-context** once so the next skill doesn't have to ask.

## 1. Start small: two questions, one task

Ask only these two questions first (skip any the context file already answers):

1. **"Is this your first year earning money with no tax taken out?"**
2. **"Do you have last year's tax return handy?"** (A PDF or the copy from their tax software is fine.)

Then give one task they can finish in 10 minutes:

> Open a separate savings account, or rename one you already have, called "Taxes." Move a third of the last payment you received into it.

A third is a placeholder until step 5 gives them their own rate. Say so. Don't ask anything else until they've done this or said they can't.

## 2. Route by who they are

- **First year self-employed, and last year they had a regular job.** Last year's tax was mostly taken out of their paychecks, so the safe payment in step 4 may be low. It keeps them clear of the penalty, but the bill in April will be bigger. The set-aside rate in step 5 covers the gap. Say this plainly; it's the surprise most first-year freelancers describe.
- **Self-employed last year too.** The standard path below.
- **Already missed payments, or already owe a bill.** Do step 3, then go straight to step 7 before anything else.
- **Also has a regular job, or a spouse with one (filing jointly).** Add step 6: raising paycheck withholding can replace some or all quarterly payments.
- **S-corp owner paying themselves a salary.** Taxes may already come out through payroll. Do the set-aside, but send the payment plan to the CPA.
- **Books aren't caught up, so they don't know their profit.** Hand off to **catch-up-plan** first. The safe payment in step 4 only needs last year's return, so it can be done today; the set-aside rate needs profit.

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

**State payments too.** Most states with an income tax want quarterly payments on the same schedule. Look up the person's state. Colorado, for example, uses a flat 4.4% rate for 2026, requires payments if they'll owe more than $1,000, and takes them online through Revenue Online. Its rules for avoiding a penalty differ from the federal ones, so cite the state's own form.

## 4. Work out the safe payment

The IRS doesn't charge the underpayment penalty if the person's payments and withholding cover the smaller of 90% of this year's tax or 100% of last year's tax. This skill uses the last-year route only, because it's known today and doesn't require guessing this year's income.

1. **Find last year's total tax** on their federal return: the line labeled "total tax" (line 24 on recent Form 1040s; check the label, since line numbers change). Also note last year's adjusted gross income.
2. **Pick the percentage:** 100% of last year's total tax, or 110% if last year's adjusted gross income was over $150,000 ($75,000 if married filing separately).
3. **Subtract withholding expected this year** from any job, theirs or a joint-filing spouse's.
4. **Divide what's left by 4.** That's each quarter's safe payment.

Rules that change the answer:

- **No tax last year?** If their total tax last year was zero, they were a US citizen or resident all year, and last year was a full 12-month year, they owe no underpayment penalty this year. They still owe the tax in April, so the set-aside matters even more.
- **Owe under $1,000?** If they'll owe less than $1,000 after withholding and credits, no penalty applies. Don't promise this; it depends on this year's tax, which this skill doesn't estimate.
- **No return last year, or last year wasn't a full year?** The last-year route doesn't work. Send them to a CPA for this year's payments and still build the set-aside.
- **Started mid-year?** Earlier payments they missed are late, not cancelled. Pay the missed amount now: the penalty works like interest on each late payment from its due date until it's paid, so sooner means smaller. Then pay the remaining quarters on time.
- **Income came in unevenly** (a big project late in the year)? Payments sized to when the money actually came in can lower or remove the penalty (the IRS calls it the annualized income method, Form 2210 Schedule AI). Add it to the CPA questions tab.

## 5. Set the set-aside rate

The safe payment keeps them clear of the penalty. The set-aside is a savings habit that covers the full bill, including what's due in April. It is not an estimate of what they owe.

Build the rate from their own numbers:

1. **Last year's rate:** last year's total tax ÷ last year's total income (the "total income" line on Form 1040).
2. **If last year had no self-employment income, add 14%.** Self-employment tax is 15.3% (12.4% Social Security plus 2.9% Medicare) on 92.35% of profit, which works out to 14.13% of profit. The Social Security part stops at a yearly cap ($184,500 for 2026; look it up each year). Above the cap, add about 2.7% instead.
3. **Add the state income tax rate,** if their state has one (Colorado: 4.4% for 2026). Last year's federal total doesn't include state tax.
4. **Round up to the next 5%.**

Example: a regular job last year with $9,000 total tax on $75,000 total income is 12%. Add 14% and Colorado's 4.4% to get 30.4%, rounded up to 35%.

Apply the rate to profit: money in, minus business costs. For someone who doesn't track costs yet, apply it to every payment received; it'll run a little high, which is the safe direction. Tell them to move the set-aside into the Taxes account the day each payment lands, and to revisit the rate after a CPA gives them a real number.

Pay each quarter's safe payment out of the Taxes account. What's left builds toward April.

## 6. If they or a spouse have a regular job

Tax withheld from a paycheck counts as paid evenly through the whole year, even if it's withheld in December. That makes a new W-4 with extra withholding one of the few fixes that still works late in the year. It can replace quarterly payments entirely. Show it as an option next to quarterly payments and add "Should I raise my withholding instead of paying quarterly?" to the CPA questions tab.

## 7. If they already owe

Order matters. Walk through these in this order:

1. **File on time even if they can't pay.** Filing late costs far more than paying late: the late-filing penalty is 5% of the unpaid tax per month (up to 25%), versus 0.5% per month for late payment. If they need more time to file, an extension gives more time to file, not to pay.
2. **Pay what they can now.** Interest and penalties run on what's unpaid, so any amount helps. The underpayment rate is set each quarter (7% a year, compounded daily, for October–December 2026; look up the current quarter).
3. **Set up a payment plan if they can't pay in full.** Look up current terms on IRS.gov. As of early 2026:
   - **Short-term (up to 180 days):** owe under $100,000; no setup fee.
   - **Long-term (up to 72 months):** owe $50,000 or less; setup fee $22 online with automatic payments, $69 online without, $107 or $178 by phone, mail or in person. Low-income applicants can get the fee waived.
   - While on a plan, the late-payment penalty drops from 0.5% to 0.25% a month. Interest keeps running.
4. **Keep paying this year's quarterly payments** while paying off last year, or next April repeats the problem.
5. **Ask about penalty relief.** The IRS's First Time Abate relief covers late-filing and late-payment penalties for people with a clean three-year record, but not the underpayment penalty for missed quarterly payments. That one can be waived for a disaster or other unusual event, or for someone who retired after 62 or became disabled. These go on the CPA questions tab.

Never estimate the penalty amount. The IRS works it out and sends a bill.

## 8. How to pay

- **Federal:** IRS Direct Pay (free, from a bank account), EFTPS, or their IRS online account. Choose "estimated tax" (Form 1040-ES) and the right tax year: the January 15, 2027 payment is for tax year 2026. Picking the wrong year is a common mistake that makes a payment look missed.
- **State:** the state's own site (Colorado: Revenue Online).
- Save each confirmation in the payment tracker.

## 9. Build the workbook

Name it `quarterly-tax-plan-[name]-[YYYY].xlsx`. Load the xlsx skill before building.

1. **Summary** — one page: next due date, the safe payment for it (federal and state), the set-aside rate, how much should be in the Taxes account today, and the single next step.
2. **Last year's return** — total tax, total income, adjusted gross income, and the 100% or 110% choice, each labeled with where it came from on the return. No Social Security numbers.
3. **Safe payments** — the step 4 math, with each quarter's federal and state amount.
4. **Set-aside log** — one row per payment received: date, from, amount, set-aside amount (formula), moved to the Taxes account (yes or no). A running total shows what the account should hold.
5. **Payment tracker** — each due date, amount, date paid, how paid, confirmation number.
6. **If you owe** — only when step 7 applies: the options in order, current payment plan terms with the date they were looked up.
7. **CPA questions** — everything flagged along the way.
8. **Sources** — every looked-up figure with the date, source name and link.

Workbook rules:

- Every amount is a formula reading from the return and set-aside tabs, so changing an input updates everything.
- The set-aside rate is in one editable cell, labeled "savings rate, not your tax bill."
- The next unpaid due date turns red within 14 days.
- Readable on a phone: large text on Summary and the key numbers on the first screen. Mention it opens in Google Sheets too.

Recalculate and open the finished file to check that formulas work, the dates are right, and nothing shows an error before sending.

## 10. Deliver

In chat:

1. The next due date and the safe payment for it, federal and state.
2. Their set-aside rate and what the Taxes account should hold today.
3. If they already owe, the first step from step 7.
4. The CPA questions that matter most right now.
5. The workbook, and the sources worth citing.

If they gave details the context file doesn't have (last year's total tax, a new state, a spouse's job, a tax account), offer to update `.agents/bookkeeping-ops-context.md` so the next skill starts current.

## Rules

- Plain words. Say "the safe payment" before "safe harbor," and "set aside" before "estimated tax."
- Never estimate this year's total tax, the April bill or a penalty amount. Use last year's return and send the rest to a CPA.
- Never imply someone messed up. Missed payments are common in a first year; describe where they are and the next step.
- Look up and cite every rate, cap, date and fee. Don't state them from memory.
- Never ask for or store Social Security numbers, bank account numbers, or IRS login details.
- End every reply with one concrete next step they can do today.

## Related skills

- **bookkeeping-ops-context** — reads the business setup, deadlines and tax details first, and takes back last year's figures and any changes
- **catch-up-plan** — gets income and costs sorted first when the books are behind, so the set-aside can run on real profit
