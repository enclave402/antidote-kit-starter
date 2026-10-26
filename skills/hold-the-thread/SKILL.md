---
name: hold-the-thread
description: New chat, forgot what we were doing, starting from zero. Load at the start of a session or after any gap to re-establish context before other skills.
version: 1.1.0
license: PolyForm-Shield-1.0.0
metadata:
  category: session-harness
  author: sloppyxbaby
---

# Hold the Thread

## When to use

- At the start of every new session or chat.
- When you are returning to a repo after any gap.
- Before loading a task-specific skill.

## When NOT to use

- Mid-task, when context is already loaded and scoped.
- As a replacement for task-specific skills (`surgical-changes`, `context-lock`, etc.).

## Instructions

0. **Day 1 gate.** Read `AGENTS.md`. If the title still contains `<repo-name>` or **This project** is still the placeholder sentence, you are on Day 1. Follow `DAY1.md` only. Do not open `CONTEXT-MAP.md`, other skills, or Folder Discovery. Write the one next line. Stop.
1. Read `AGENTS.md` (already done if you just finished the gate).
2. Read `CLAUDE.md` only if Day 1 is done.
3. **Working memory (.context):** Use the `.context/` system (e.g. `.context/scratch/`) to keep active working notes, scratchpads, and execution logs as you work so context is never lost across turns. When orienting to a new session, do **not** ingest orphan `.tmp` files from `.context/scratch/` as context; prefer the map, decisions, and durable work records.
4. **Folder Discovery (if present, after Day 1):** read `docs/_registry/folders.discovery.json` if it exists. Do not invent folder purpose. Buyer door: `templates/FOLDER-DISCOVERY.md`.
5. Check for an in-flight work record (prefer durable surfaces over chat):
   - the **Next** line in `AGENTS.md`
   - `memory/todos.md` if it exists
6. State the session stance:
   - What you believe the user is trying to do.
   - What is already in flight.
   - What you will not do unless explicitly asked.
7. Load the task-specific skill that matches the request, if any. Not on Day 1.

## Output template

```
Session stance:
- User goal (as I understand it): <one sentence>
- In flight: <none / list>
- Folder Discovery: <loaded path | none>
- Loaded context: <files read>
- Out of scope for this turn: <what I will not assume or do>
- Next skill (if any): <skill name>
```

If nothing is in flight and the request is ambiguous, ask one clarifying question before proceeding.

**Done means:** Done means the owner's intent is restated and confirmed before work starts. If unsure or spec and tests conflict, stop and flag.
