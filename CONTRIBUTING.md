# Contributing

Thanks for helping make these skills better. Improvements to existing skills and new skills are both welcome.

## Suggest a skill

[Open a skill request](https://github.com/CharleneTStrain/bookkeeping-ops-skills/issues/new?template=skill-request.yml) with the bookkeeping job, what you'd hand the agent, and what you'd want back. Please leave out account numbers and other personal details.

## Add a skill

1. **Make the folder:** `skills/your-skill-name/` — lowercase, hyphens only.
2. **Write `SKILL.md`** with front matter:

   ```yaml
   ---
   name: your-skill-name
   description: What it does in one sentence. Use when [the phrases and situations that should trigger it].
   metadata:
     version: 1.0.0
   ---
   ```

   The `name` must match the folder. The description is how agents decide when to use the skill, so name the real words people say ("I'm behind on my books," "my bookkeeper quit").

3. **Add the context check** right after the opening paragraph — copy the `## Before you start` section from any existing skill.
4. **Write the steps.** Numbered steps, a template for the output, and the rules the output must follow.
5. **End with `## Related skills`** — the skills it hands off to, each with a few words on why.
6. **Write `README.md`** in the same folder: the problem, what it does, what you use it with, what you get.
7. **Add it to the README table** in the right category, and to the skill data in `site/index.html`.
8. **Run `./validate-skills.sh`** and fix anything it flags.

## The rules every skill follows

These run through the whole library. A skill that breaks one won't be merged.

- **Deadline first.** Work backwards from the date someone else set: a tax date, a letter, a lender, an accountant.
- **Their books, not averages.** Build every plan from the business's own accounts and volume. If a number is missing, ask or mark it as an estimate; never fill it with a "typical" one.
- **Current rules, looked up and cited.** Tax dates, 1099 thresholds, sales tax rules and lender requirements change. Look them up and say where they came from; never state them from memory.
- **Planning, not tax advice.** Never estimate what someone owes or what a penalty will be. Send those questions to a CPA. No specific bookkeeper, firm or software picks.
- **No judgment.** Describe where the books are and the next step. Never imply someone fell behind on purpose.
- **Nothing sensitive stored.** No account numbers, tax ID numbers, Social Security numbers, or passwords in any file a skill writes.
- **Plain words.** Say "match to the bank" before "reconcile." Define terms like "accrual" the first time they appear.
- **Under 500 lines.** Move long reference material into a `references/` folder inside the skill.

## Improve a skill

Edit the `SKILL.md`, bump the patch version in its front matter (1.0.0 → 1.0.1, or 1.1.0 for a new step or output), and say in the PR what was going wrong and how the change fixes it. A before-and-after example helps a lot.

## Commit messages

Describe what the skill does or what changed for the person using it, not just the file name. "Plan tab now finishes a week before the deadline" beats "update catch-up-plan."
