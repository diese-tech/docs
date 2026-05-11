# Project Documentation Kit

Use this structure for most serious repositories.

The goal is to prevent projects from becoming undocumented chaos.

---

# Recommended Core Docs

## README.md

Purpose:
- Explain the project
- Explain why it exists
- Explain the current scope
- Explain setup
- Link all supporting docs

Should answer:
- What is this?
- Why was it built?
- How do I run it?
- What phase is it in?

---

## AGENTS.md

Purpose:
- Define repository-specific AI implementation behavior
- Prevent scope drift
- Define architecture constraints
- Preserve product direction

Should answer:
- What should AI prioritize?
- What should AI avoid?
- What architectural rules matter?

---

## docs/AI_WORKFLOW_GUARDRAILS.md

Purpose:
- Define engineering safety rules
- Reduce blast radius
- Encourage scalable operational thinking

Should answer:
- What are the safety rules?
- How should async systems behave?
- What architectural defaults are preferred?

---

## MVP.md

Purpose:
- Define the smallest useful version of the product

Should include:
- Included features
- Excluded features
- Acceptance criteria
- Emotional/user success condition

---

## ROADMAP.md

Purpose:
- Define phased development direction

Should include:
- Current phase
- Deliverables
- Completion criteria
- Future phases

---

## TASKS.md

Purpose:
- Track active implementation work

Should include:
- In progress
- To do
- Done
- Blocked

Keep it lightweight.

---

## DECISIONS.md

Purpose:
- Record important architectural and product decisions

Should include:
- Decision
- Reasoning
- Tradeoffs
- Alternatives rejected

This prevents repeated debates and forgotten context.

---

## OPERATIONS.md

Purpose:
- Explain how the product is used day to day

Should include:
- Roles
- Workflows
- Status flows
- Edge cases
- Limitations
- Troubleshooting

Write for operators, not engineers.

---

## RELEASE_PROCESS.md

Purpose:
- Define how releases happen safely

Should include:
- Release checklist
- Validation steps
- Rollback process
- Environment requirements
- Deployment sequence

---

# Documentation Philosophy

Good docs should:

- reduce repeated explanations
- preserve architectural intent
- lower onboarding time
- reduce AI hallucination risk
- clarify scope
- improve operational safety
- make future scaling easier

---

# Important Rule

Do not wait until the project is “serious” to document it.

Projects become serious because they were documented early.
