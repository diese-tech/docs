# AGENTS.md

This file defines how AI assistants should work in this repository.

The goal is to preserve project direction, avoid unnecessary rewrites, and keep implementation safe.

---

## Project Purpose

[Explain what this project is and why it exists.]

---

## Current Phase

[Prototype / MVP / production / maintenance / client delivery]

---

## Product Priorities

Prioritize:

1. [Primary workflow]
2. [User clarity]
3. [Operational safety]
4. [Maintainability]
5. [Performance]

---

## Out of Scope

Do not add during this phase:

- [Feature]
- [Feature]
- [Feature]

If useful but out of scope, document as future work instead of implementing.

---

## Architecture Rules

Prefer:

- small reviewable changes
- explicit workflows
- reusable modules/components
- strong typing and validation
- low blast radius
- simple operational behavior

Avoid:

- speculative rewrites
- unrelated cleanup
- dependency sprawl
- hidden side effects
- large files that mix concerns

---

## AI Workflow Guardrails

Before implementation, debugging, migrations, refactors, or production fixes, review:

`docs/AI_WORKFLOW_GUARDRAILS.md`

Default behavior:

- smallest safe change
- lowest blast radius
- no unrelated file edits
- no speculative rewrites
- preserve existing behavior unless explicitly changed

---

## Build Order

1. Documentation and scope
2. Core workflow
3. Persistence / integrations
4. Error handling and operations
5. UI polish
6. Performance and scale improvements

---

## Final Rule

Do not optimize only for "it works."

Optimize for clarity, maintainability, and safe operation.
