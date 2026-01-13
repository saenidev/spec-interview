---
description: Build a comprehensive project specification through systematic interviewing
argument-hint: <project-name>
allowed-tools: ["AskUserQuestion", "Write", "Read", "Glob", "Bash"]
---

# Project Specification Builder

Build a comprehensive specification for **$ARGUMENTS** by conducting a systematic interview.

## Interview Process

Use the AskUserQuestion tool to gather requirements across these dimensions. Ask 2-4 questions at a time, probing deeper into underlying needs and constraints. Skip questions that don't apply.

### Phase 1: Core Vision & Problem Space
- What problem does this solve? Who experiences this pain?
- What happens if this doesn't get built? What's the cost of the status quo?
- What does success look like? How will you measure it?
- What are the boundaries—what is explicitly NOT in scope?

### Phase 2: Users & Use Cases
- Who are the primary users? Secondary users?
- Walk through 2-3 critical user journeys in detail
- What are the edge cases that could break the experience?
- What existing workflows or tools will this replace or integrate with?

### Phase 3: Technical Constraints & Architecture
- What's the deployment environment? Any infrastructure constraints?
- What existing systems must this integrate with?
- What are the performance requirements? (latency, throughput, scale)
- What data needs to persist? What are the consistency requirements?
- Any security, compliance, or regulatory considerations?

### Phase 4: Tech Stack & Implementation
- Any preferred languages, frameworks, or tools?
- What's the team's expertise? Any technologies to avoid?
- Build vs buy decisions—what should be custom vs off-the-shelf?
- Testing strategy—what level of coverage is needed?

### Phase 5: UX & Design
- What's the target platform? (web, mobile, CLI, API)
- Any design system or brand guidelines to follow?
- Accessibility requirements?
- Offline/degraded mode behavior?

### Phase 6: Tradeoffs & Priorities
- What's more important: speed to market or feature completeness?
- Where can you accept technical debt? Where is quality non-negotiable?
- What would you cut if you had half the time?
- What would you add if you had twice the resources?

### Phase 7: Risks & Concerns
- What keeps you up at night about this project?
- What's been tried before? Why did it fail?
- What dependencies or external factors could block progress?
- What assumptions are you making that might be wrong?

## Interview Guidelines

- Ask 2-4 questions at a time using AskUserQuestion, grouped by theme
- Probe deeper when answers reveal interesting constraints or tensions
- Challenge assumptions respectfully—ask "why" and "what if"
- Note contradictions and help resolve them
- Adapt questions based on the project type (skip irrelevant ones)
- Continue interviewing until you have enough clarity to write a complete spec

## Output

After the interview is complete:

1. Create the `specs/` directory if it doesn't exist: `mkdir -p specs`
2. Synthesize all responses into a structured specification document saved to `specs/$ARGUMENTS.md` containing:

- **Executive Summary** - One paragraph overview
- **Problem Statement** - What we're solving and why it matters
- **Goals & Non-Goals** - Explicit scope boundaries
- **User Personas & Journeys** - Who uses this and how
- **Technical Requirements** - Architecture, integrations, constraints
- **Tech Stack** - Chosen technologies with rationale
- **UI/UX Requirements** - Design and interaction expectations
- **Success Metrics** - How we'll measure if this worked
- **Risks & Mitigations** - Known concerns and contingencies
- **Open Questions** - Items that still need resolution
