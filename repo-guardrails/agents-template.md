# AGENTS Template

This document defines repository-specific implementation behavior for AI-assisted development.

The goal is to keep implementation aligned with the product direction, architecture constraints, and operational safety requirements.

---

## Product Priority

Prioritize:

1. [Primary user flow]
2. [Operational reliability]
3. [Performance]
4. [Maintainability]
5. [Scalability]

---

## Do Not Add During Current Phase

Do not add:

- [Feature]
- [Feature]
- [Feature]

If a feature seems useful but is outside scope, document it as future work instead of implementing it.

---

## Design Direction

The product should feel:

- [Trait]
- [Trait]
- [Trait]

Avoid:

- [Trait]
- [Trait]
- [Trait]

---

## Architecture Rules

Preferred structure:

- Reusable components
- Modular services
- Explicit workflows
- Strong typing
- Queue-safe operations
- Clear boundaries between systems

Avoid:

- Tight coupling
- Giant files
- Hidden side effects
- Unbounded async behavior
- Large speculative rewrites

---

## Domain Language

Use consistent terminology.

Examples:
- Customer
- Session
- Match
- Inquiry
- Draft
- Operator

Do not casually rename concepts.

---

## Code Quality Rules

Prefer:

- Small reviewable changes
- Clear file names
- Accessible UI
- Strong typing
- Retry-safe workflows
- Explicit validation
- Minimal dependencies

Before adding a dependency, justify why it is needed.

---

## AI Workflow Review

Before implementation, debugging, migrations, or refactors, review:

`docs/AI_WORKFLOW_GUARDRAILS.md`

Default behavior:

- smallest safe change
- lowest blast radius
- no unrelated file edits
- no speculative rewrites
- no hidden architectural changes

---

## Preferred Build Order

1. Foundation and structure
2. Core workflows
3. Persistence
4. Operational safety
5. UI polish
6. Performance improvements
7. Expansion features

---

## Final Rule

Optimize for systems that are understandable, operable, and recoverable.

Not just systems that “work.”
