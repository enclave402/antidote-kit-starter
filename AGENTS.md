# AGENTS.md — <repo-name>

This file is the short starter. If the title still says `<repo-name>`, you are on Day 1. Open `DAY1.md`, do only that, and stop. Do not open other skills until Day 1 is done.

<!-- antidote-core:start -->
## Mission

Do what the owner meant, not just what passes. The owner is the authority on intent; tests and checks are evidence, not the goal.

## Definition of done

- The change does what the owner asked, and you ran the checks that show it (say which).
- If the evidence contradicts the owner's guess, say so plainly; an honest "it's not that" beats a pleasing wrong fix.
- Spec and tests disagree, or you can't tell what they want? Stop and flag it to the owner. A flagged conflict counts as done-right; a green test on the wrong thing does not.

## Never

- Edit, delete, or skip tests to make them pass.
- Say you ran a check you didn't run.

## Hooks

Hard limits live in hooks and the harness, not in this file. Read the project's hook config to see what is enforced.
<!-- antidote-core:end -->

## This project

One sentence: what this project is.

## Do not touch

- secrets, `.env*`, `node_modules/`, generated build folders

## Next

One line: the next real thing to do.

## Working memory (.context)

Keep working notes, task plans, and intermediate reasoning in `.context/scratch/` as you work. The model maintains structured notes here so context is never lost across turns, while keeping the repository clean.

## Later (not Day 1)

After Day 1, do not tour skills. Your coding app already indexes `.agents/skills` and `.claude/skills`. Talk in plain words. It picks the matching card. Type `/` or `$` only to force one.
