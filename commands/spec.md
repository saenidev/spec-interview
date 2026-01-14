---
description: Build a comprehensive project specification through systematic interviewing
argument-hint: <project-name>
allowed-tools: ["AskUserQuestion", "Write", "Read", "Glob", "Bash"]
---

If `$ARGUMENTS` is empty, use AskUserQuestion to ask: "What would you like to name this project specification?" Use the response as the project name for all references below.

Your task is to build a spec for **$ARGUMENTS** (or the name provided above).

Use AskUserQuestion to interview me and gather requirements about the project—implementation, UI & UX, tech stack, concerns, tradeoffs, etc.

Make sure questions are not obvious and probe deeper into the underlying needs and constraints.

Interview me continually and systematically until the spec is complete. Document all responses and insights into a comprehensive specification saved to `SPEC.md`.
