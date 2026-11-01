---
name: bookkeeping-ops-context
description: Create or update the business bookkeeping context file every other skill in this library reads first — what the business is and how it's set up, its accounts and payment processors, bookkeeping software, who does the books and taxes, transaction volume, payroll and contractors, sales tax, and upcoming deadlines. Use at the start before using other bookkeeping ops skills, when someone says "set up my bookkeeping context," "here's my business," "remember my accounts," "my bookkeeper quit," or "update my deadlines," or whenever a skill keeps asking for the same background. It creates `.agents/bookkeeping-ops-context.md`.
metadata:
  version: 1.0.0
---

# Bookkeeping ops context

Every bookkeeping ops skill needs the same background: what the business is, how it's set up for taxes, which accounts money moves through, where the books live, who helps, and what's due when. This skill writes that down once, in one file, so no other skill has to ask again.

The file lives at `.agents/bookkeeping-ops-context.md`. If you find it at `.claude/bookkeeping-ops-context.md` instead, use it and offer to move it.

## What never goes in the file

This file sits in the person's own project folder, but treat it as something they might share with a bookkeeper or by accident. Never write down:

- Bank account numbers, card numbers, or routing numbers
- Social Security numbers, the business's tax ID number (EIN), or any government ID
- Passwords, PINs, security answers, or login usernames for banks, software or payment processors

If the person pastes any of these, leave them out and say so in one line. Name accounts by type, institution and last four digits only when two accounts would otherwise look the same ("Chase business checking," "Amex card ending 1002").

## Step 1: Check what exists

**If the file exists:** read it, give a three-line summary of what's in it, show the version and the last two changelog entries, and ask which sections to update. Only gather what's needed for those sections.

**If it doesn't exist,** offer two ways to start:

1. **Draft from what's here (faster):** read whatever the person has shared — last year's tax return summary, a bank statement list, a bookkeeper's handoff notes, a screenshot of their accounts — and draft every section. Then ask what's wrong and what's missing.
2. **Build it together:** walk through the sections one at a time, a few questions each. "Not sure" is a fine answer for anything.

## Step 2: Fill each section

Use only what the person or their documents say. Anything not given stays as "Not recorded." Mark estimates with "(est.)". A context file with gaps is useful; a context file with guesses breaks every skill that trusts it.

```markdown
# Bookkeeping ops context
**Version:** 1.0 · **Last updated:** [date] · **Kept up by:** [person]

## The business
- What it does, in one line:
- How it's set up for taxes: [sole proprietor / single-member LLC / multi-member LLC or partnership / S-corp / C-corp / not sure]
- State it's registered in, and states it sells into:
- Tax year: [calendar year / other]
- Year started:
- Owners, and who is in charge of the books:

## Money in and out
- Rough transactions a month across all accounts: [under 100 / 100–300 / 300–1,000 / over 1,000]
- Main ways customers pay (invoice, card, cash, marketplace):
- Personal and business money kept separate? [yes / mostly / no]

## Accounts
| Account | Type | Institution | Used for | Last month finished in the books |
|---|---|---|---|---|
Cover: bank accounts, credit cards (including personal cards used for business), payment processors (Stripe, Square, PayPal, Shopify, Amazon), and loans or lines of credit.

## Books and software
- Software the books are in, and whether they still have access:
- Accounting basis, if known: [cash (counted when money moves) / accrual (counted when earned or owed) / not sure]
- Last month they're confident is finished:
- Where receipts live:

## People who help
| Role | Who | What they do | How often |
|---|---|---|---|
Cover: bookkeeper, CPA or tax preparer, payroll provider. Note any provider that shut down or stopped responding, and whether the person has a copy of everything they did.

## Payroll, contractors and sales tax
- Employees and payroll provider, if any:
- Contractors paid during the year, roughly how many:
- States where they collect or may owe sales tax:

## Deadlines
| Deadline | Date | Set by | Notes |
|---|---|---|---|
Cover: tax return and extension dates, quarterly estimated taxes, any IRS or state letter (with its response date), loan applications, and accountant requests.

## Open questions
Things the business hasn't settled that skills should flag, not guess.

## Changelog
- [date] v1.0 — Created. [what it was drafted from]
```

## Step 3: Rules for the file

- **Their facts only.** Never fill a gap with a typical figure or a guess about how the business is set up. Leave it "Not recorded."
- **Decided vs. considering.** "Thinking about becoming an S-corp" goes under Open questions, not under The business.
- **No judgment.** Record where the books are, however far behind. Don't label anything as bad or late.
- **Plain words.** Write it so the owner, a new bookkeeper or a CPA can read it on day one.
- **One page if possible.** Link to statements and spreadsheets instead of copying them in.

## Step 4: Save and version

Save to `.agents/bookkeeping-ops-context.md` (create the `.agents/` folder if needed). On every real change, bump the version (1.0 → 1.1 for updated details, 2.0 for a big change like a new entity type, a new bookkeeper or a new state) and add a dated changelog line saying what changed.

When another skill learns something durable mid-task — a month finished, a new account, a new deadline, a bookkeeper hired — suggest adding it here rather than letting it get lost in that one output.

## Related skills

Every skill in this library reads this file first. The one that leans on it most today:

- **catch-up-plan** — uses Accounts, Books and software, People who help and Deadlines to size the backlog and build a dated plan, and takes back each month as it's finished
