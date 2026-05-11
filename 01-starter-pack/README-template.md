# [Project Name]

[One sentence explaining what this project is.]

**Live app / demo:** [URL if applicable]

---

## Why It Exists

[Explain the real problem this project solves.]

Focus on the workflow or pain point, not the technology.

Good questions to answer:

- What is frustrating today?
- Who experiences the problem?
- What is the better future state?
- Why is this worth building now?

---

## What It Does

- [Core capability]
- [Core capability]
- [Core capability]

Keep this practical. A reader should understand the product without needing context from chat history.

---

## Who It Is For

Primary users:

- [User type]
- [User type]

Secondary users:

- [User type]

Not intended for:

- [Audience / use case]

---

## Current Phase

**Phase:** [Prototype / MVP / Production / Maintenance]

Current status:

[Short explanation]

Related docs:

- [MVP.md](./MVP.md)
- [ROADMAP.md](./ROADMAP.md)
- [TASKS.md](./TASKS.md)
- [DECISIONS.md](./DECISIONS.md)

---

## Current Scope

Included right now:

- [Feature]
- [Feature]
- [Feature]

Explicitly excluded right now:

- [Feature]
- [Feature]
- [Feature]

If something is excluded, do not build it unless the scope changes in `MVP.md` or `ROADMAP.md`.

---

## Stack

| Layer | Choice |
|---|---|
| Frontend | [Tech] |
| Backend | [Tech] |
| Database | [Tech] |
| Auth | [Tech / none] |
| Hosting | [Tech] |
| Integrations | [Tech] |

---

## Local Setup

1. Clone the repo.
2. Install dependencies.
3. Copy environment variables.
4. Run database migrations if applicable.
5. Start the development server.

Example:

```bash
npm install
cp .env.example .env.local
npm run dev
```

Open:

```text
http://localhost:3000
```

Adjust commands for the actual stack.

---

## Environment Variables

Document every required variable in `.env.example`.

| Variable | Required | Purpose |
|---|---|---|
| `[ENV_NAME]` | Yes/No | [Purpose] |
| `[ENV_NAME]` | Yes/No | [Purpose] |

Do not commit secrets.

---

## Core Workflows

### [Workflow Name]

1. [Step]
2. [Step]
3. [Step]

Expected result:

[Answer]

---

## Project Docs

- `README.md` — project overview and setup
- `AGENTS.md` — AI implementation rules
- `MVP.md` — MVP scope and acceptance criteria
- `ROADMAP.md` — phase-based product direction
- `TASKS.md` — active work tracking
- `DECISIONS.md` — decision log
- `docs/AI_WORKFLOW_GUARDRAILS.md` — implementation safety rules

Optional:

- `OPERATIONS.md` — day-to-day usage guide
- `RELEASE_PROCESS.md` — release checklist
- `docs/CODEBASE_WALKTHROUGH.md` — owner-friendly architecture explanation

---

## Required AI Workflow Review

Before AI-assisted implementation, debugging, refactoring, migrations, or production fixes, review:

`docs/AI_WORKFLOW_GUARDRAILS.md`

Default behavior:

- smallest safe change
- lowest blast radius
- no unrelated file edits
- no speculative rewrites
- preserve existing behavior unless explicitly changing it

---

## Testing / Validation

Minimum validation before merging:

- [ ] Project installs successfully
- [ ] Project builds successfully
- [ ] Core workflow works locally
- [ ] No obvious console/server errors
- [ ] Environment variable requirements are documented
- [ ] Any changed behavior is reflected in docs

Project-specific validation:

- [ ] [Check]
- [ ] [Check]

---

## Known Constraints

- [Constraint]
- [Constraint]
- [Constraint]

Be honest. Constraints are not failure; hidden constraints are failure.

---

## Operating Principle

[One sentence defining how this repo should be maintained.]

Example:

Move fast, but move surgically. Build the smallest useful system that can be understood, operated, and safely changed.
