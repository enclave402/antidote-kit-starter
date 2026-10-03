---
name: context-lock
description: Forgot mid-task, opened too many files, lost the middle. Use at the start of a multi-file task. Load only the files that matter.
version: 1.1.0
license: PolyForm-Shield-1.0.0
metadata:
  category: cognitive-scaffolding
  author: sloppyxbaby
  storytelling_audit: "2026-07-21"
  audit_grade: "B+ → A-"
---

# Context Lock

## When to use

- Starting work on a new task.
- The task touches more than one file or module.
- You are entering an unfamiliar part of the codebase.

## When NOT to use

- Continuing an already-scoped task where context is already loaded.

## The Problem

You ask the agent to fix a bug in the checkout flow. The agent opens the checkout component. Then the payment hook. Then the cart store. Then the user model. Then the database schema. Thirty files later, the agent is lost. It can't remember which file had the bug. It starts making changes to files that have nothing to do with checkout. It renames variables in the user profile page. It adds a new table column. The original bug — a missing null check in checkout — is still there, buried under thirty files of context noise.

This is context overload. The agent thinks more context is better. It's not. Every extra file is a distraction. Every unrelated module is noise. The agent's working memory is finite. Load too much, and the important stuff falls out the middle.

## The Fix

Context Lock forces the agent to identify exactly what matters and ignore everything else. Before touching any code, the agent states the locked scope: these files, these functions, nothing else. The out-of-scope list is as important as the in-scope list. It says: "I see these other files. I am not touching them."

## Instructions

1. Read `AGENTS.md` if not already loaded.
2. Read the closest `CLAUDE.md` in the directory hierarchy.
3. Locked constraints must come from durable files (`CLAUDE.md`, ADRs, decision logs), not from ephemeral scratch (`*.tmp`).
4. Check `docs/_registry/doc_index.json` for relevant reference docs.
5. Identify the specific files and functions directly involved.
6. Load only those files. Do not bulk-read unrelated modules.
7. State the locked scope before proceeding.

## Output template

```
Locked scope: <files/functions>
Reference docs: <paths>
Out of scope: <what is intentionally ignored>
```

## Storytelling note

The "villain" is context bloat — the false belief that more context is better. The "hero" is discipline. The "fix" is simple: name what matters, ignore the rest.

**Done means:** Done means the task the owner asked for is finished using only the files you locked, with the checks named; at the end the owner-check-in shows what you did vs what they asked; the owner answers pass/fail (intent) and yes/no (satisfied). If unsure or spec and tests conflict, stop and flag.
