# Antidote Kit Starter

Your coding agent forgets your rules. This starter keeps them in plain files in your repo, and the agent reads them every session.

Free. Two skills. Fifteen minutes, then stop. The full kit lives at https://sloppyxbaby.com.

## Start

1. Copy these files into your project folder. There is nothing to install.
2. Tell your coding agent: **Read DAY1.md and start.**
3. Fill in `AGENTS.md` together: what the project is, and what must not be touched.
4. Do one small real thing. When it works, add one line at the bottom of `AGENTS.md`: what you did, and what comes next.
5. Stop.

Cursor, Codex, Copilot look in `.agents/skills/`. Claude Code looks in `.claude/skills/`. Both point at the same cards in `skills/`.

## What is in the starter

| File | What it does |
|---|---|
| `AGENTS.md` | The short file your agent reads first |
| `CLAUDE.md` | Tells Claude Code what to load |
| `DAY1.md` | The Day 1 start |
| `context.json` | What to load, in what order |
| `skills/hold-the-thread/` | Starting every session from zero; guessing what was in flight |
| `skills/context-lock/` | Constraints evaporating mid-task |

## The full kit

Essential has all 10 core skills. Professional has all 15, plus Cursor rules, memory templates, and advanced patterns. One-time purchase, no subscription: https://sloppyxbaby.com/#pricing

## License

PolyForm Shield 1.0.0 (see `LICENSE.md`). Use it in any project, including paid client work. Do not resell it, repackage it, or ship it inside a product that competes with the Antidote Kit.
