# spec-interview

A Claude Code plugin for building comprehensive project specifications through systematic interviewing.

## Installation

Add the marketplace to Claude Code:

```bash
claude plugins add https://github.com/saenidev/spec-interview
```

Or clone and test locally:

```bash
git clone https://github.com/saenidev/spec-interview.git
cd spec-interview
claude --plugin-dir .
```

## Usage

```
/spec <project-name>
```

This starts an interactive interview process that gathers requirements across seven dimensions:

1. **Core Vision & Problem Space** - What problem are we solving?
2. **Users & Use Cases** - Who uses this and how?
3. **Technical Constraints** - Infrastructure, integrations, performance
4. **Tech Stack** - Languages, frameworks, build vs buy
5. **UX & Design** - Platform, accessibility, offline behavior
6. **Tradeoffs & Priorities** - Speed vs completeness, technical debt
7. **Risks & Concerns** - Blockers, assumptions, past failures

## Output

After the interview, a structured specification is saved to `specs/<project-name>.md` containing:

- Executive Summary
- Problem Statement
- Goals & Non-Goals
- User Personas & Journeys
- Technical Requirements
- Tech Stack with rationale
- UI/UX Requirements
- Success Metrics
- Risks & Mitigations
- Open Questions

## License

MIT
