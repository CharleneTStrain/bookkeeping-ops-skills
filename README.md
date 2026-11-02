# Bookkeeping Ops Skills for AI Agents

Open-source skills for getting a small business's books caught up before a deadline someone else set — a tax date, an IRS letter, a lender, an accountant — keeping them caught up, and paying quarterly taxes on time. Built for small business owners, freelancers and solo operators in the US. Works with Claude Code, the Claude app, OpenAI Codex, Cursor, and any agent that supports the [Agent Skills spec](https://agentskills.io).

**Browse every skill at [charlenetstrain.github.io/bookkeeping-ops-skills](https://charlenetstrain.github.io/bookkeeping-ops-skills/).**

Built by [Charlene Strain](https://www.linkedin.com/in/charlene-strain). Sibling libraries: [Money Ops Skills](https://github.com/CharleneTStrain/money-ops-skills) and [Product Ops Skills](https://github.com/CharleneTStrain/product-ops-skills).

**Contributions welcome.** Have a better way to run one of these, or a skill to add? [Open a PR](#contributing) or [request a skill](https://github.com/CharleneTStrain/bookkeeping-ops-skills/issues/new?template=skill-request.yml).

> These skills are planning tools, not tax or accounting advice. They lay out the work, the order and the trade-offs so you can decide. Anything about what you'll owe, penalties, payroll or sales tax goes to a CPA.

## Contents

- [What are skills?](#what-are-skills)
- [How the skills work together](#how-the-skills-work-together)
- [The rules every skill follows](#the-rules-every-skill-follows)
- [All skills](#all-skills)
- [Install](#install)
- [Use](#use)
- [Contributing](#contributing)

## What are skills?

A skill is a markdown file of instructions an AI agent follows for one specific job. Add these to your setup, and when you say "I'm six months behind on my books and my accountant needs them by April," the agent recognizes the job and works through it the same careful way every time.

## How the skills work together

Everything starts with **bookkeeping-ops-context**. Run it once and it writes `.agents/bookkeeping-ops-context.md`: how the business is set up, its accounts and payment processors, its software, who does the books and taxes, payroll, contractors, sales tax, and deadlines. Every other skill reads that file first, so it only asks you for what's specific to the job. It never stores account numbers, tax ID numbers, or passwords.

```
          ┌──────────────────────────────────────┐
          │        bookkeeping-ops-context       │
          │    (read by every other skill first) │
          └───────────────────┬──────────────────┘
                              │
             ┌────────────────┴────────────────┐
             ▼                                 ▼
┌───────────────────────────┐     ┌───────────────────────────┐
│     Getting caught up     │     │       Quarterly taxes     │
├───────────────────────────┤     ├───────────────────────────┤
│       catch-up-plan       │     │  quarterly-tax-set-aside  │
└───────────────────────────┘     └───────────────────────────┘
```

The chains that come up most:

- **Bookkeeping ops context → Catch-up plan:** write down the business once, then get a dated plan that finishes before the deadline
- **Catch-up plan → Quarterly tax set-aside:** sort the year's income and costs, then work out what to pay each quarter and what to set aside

Each skill ends with a **Related skills** section naming what it hands off to and why.

## The rules every skill follows

- **Deadline first.** Every plan works backwards from the date someone else set.
- **Their books, not averages.** Plans are built from the business's own accounts and volume. Estimates are marked as estimates.
- **Planning, not tax advice.** No guesses at this year's tax bill or any penalty. Quarterly payments use the IRS's own rule based on last year's return; everything else goes to a CPA.
- **No judgment.** Skills describe where the books are and the next step, never that someone fell behind on purpose.

## All skills

### Start here

| Skill | What it does |
|---|---|
| [Bookkeeping ops context](skills/bookkeeping-ops-context/) | Writes down your business setup, accounts, software, helpers and deadlines once, so every other skill can read it |

### Getting caught up

When months of books are unfinished and a deadline is coming.

| Skill | What it does | Output |
|---|---|---|
| [Catch-up plan](skills/catch-up-plan/) | Turns months of unfinished books into a deadline-first plan, with a do-it-yourself vs. hire estimate and questions for your CPA | Excel workbook: summary, accounts, backlog, week-by-week plan, CPA questions, stay-caught-up routine |

### Quarterly taxes

When no one takes taxes out of your pay.

| Skill | What it does | Output |
|---|---|---|
| [Quarterly tax set-aside](skills/quarterly-tax-set-aside/) | Works out each quarter's safe payment from last year's return, a set-aside rate on your profit, and what to do if you already owe | Excel workbook: safe payments, set-aside rate and log, payment tracker, options if you owe, CPA questions |

More skills coming: a loan-ready books skill for owners who need lender-ready statements.

## Install

### Option 1: CLI (recommended)

Use [`npx skills`](https://github.com/vercel-labs/skills) to install into whichever agents you have:

```bash
# Install all skills
npx skills add CharleneTStrain/bookkeeping-ops-skills

# Install specific skills
npx skills add CharleneTStrain/bookkeeping-ops-skills --skill bookkeeping-ops-context quarterly-tax-set-aside

# See what's available
npx skills add CharleneTStrain/bookkeeping-ops-skills --list
```

If you run it from inside a Claude Code session, name the agent so the skills land where Claude Code reads them:

```bash
npx skills add CharleneTStrain/bookkeeping-ops-skills -a claude-code
```

### Option 2: Claude Code plugin

```
/plugin marketplace add CharleneTStrain/bookkeeping-ops-skills
/plugin install bookkeeping-ops-skills
```

Outside an interactive session, use the CLI version:

```bash
claude plugin marketplace add CharleneTStrain/bookkeeping-ops-skills
claude plugin install bookkeeping-ops-skills@bookkeeping-ops-skills
```

### Option 3: Clone and copy

```bash
git clone https://github.com/CharleneTStrain/bookkeeping-ops-skills.git
cp -r bookkeeping-ops-skills/skills/* ~/.claude/skills/
```

Use `~/.claude/skills/` for every project, or `.claude/skills/` inside one project.

### Option 4: Claude app

Zip any skill folder from `skills/` and upload it under **Customize → Skills → Upload a skill**. Upload **bookkeeping-ops-context** too, so the others have something to read.

### Option 5: Fork it

Fork the repo, change the skills to match your business or the clients you help, and install from your fork.

## Use

Once installed, ask in plain words:

```
"Set up my bookkeeping context from last year's tax return and my account list"
→ bookkeeping-ops-context

"I'm eight months behind on my books and taxes are due April 15"
→ catch-up-plan

"My bookkeeper quit and I don't know what she finished"
→ bookkeeping-ops-context, then catch-up-plan

"My accountant needs my numbers in three weeks. Can I do this myself?"
→ catch-up-plan

"I just went freelance. How much should I set aside for taxes?"
→ quarterly-tax-set-aside

"I missed my quarterly payments and owe the IRS. What now?"
→ quarterly-tax-set-aside
```

Or call one directly:

```
/bookkeeping-ops-context
/catch-up-plan
/quarterly-tax-set-aside
```

## Contributing

Found a better way to run one of these, or have a skill to add? PRs and issues are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md), and run `./validate-skills.sh` before you open a PR.

## License

[MIT](LICENSE). Use these however you want.
