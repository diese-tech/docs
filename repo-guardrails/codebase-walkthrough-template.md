# Codebase Walkthrough Template

Use this template when Codex, Claude, or another AI assistant needs to explain a codebase back to the owner.

The goal is not just technical documentation. The goal is owner confidence.

This document should help the owner understand what the app does, where important logic lives, how to explain the system to clients, and where changes can be made safely.

---

## Intended Use

Use this when:

- A repo was built with AI assistance
- The owner needs to understand how the app works
- A client may ask how the system operates
- A handoff is needed before maintenance or refactor work
- The repo has grown beyond what can be understood from README alone

---

## AI Prompt

```text
Review this repository and create a codebase walkthrough for the owner.

Goal:
Explain how the app works in plain English so a non-senior developer can confidently explain it to a client, maintain it, and know where to make safe changes.

Output:
1. Executive summary
2. Main user flows
3. Folder and file map
4. Data model explanation
5. External services and integrations
6. Environment variables
7. Important logic paths
8. Risky areas / do-not-touch zones
9. Common client questions and plain-English answers
10. Debugging guide
11. Suggested future improvements

Rules:
- Explain what each important part does and why it matters.
- Reference actual files and folders.
- Separate business logic from technical implementation.
- Use plain English first, technical detail second.
- Call out uncertainty instead of guessing.
- Do not rewrite code.
- Do not make architecture changes.
- Do not invent features that are not present in the repo.
```

---

# Codebase Walkthrough

## 1. Executive Summary

### What This App Does

[Explain the app in plain English.]

### Who Uses It

- [User type]
- [User type]
- [Admin / operator / client role]

### What Problem It Solves

[Explain the real-world workflow, frustration, or business problem.]

### Current Maturity

[Prototype / MVP / production-ready / internal tool / client-facing]

---

## 2. Main User Flows

### Flow 1: [Name]

Plain-English explanation:

[What happens from the user’s perspective.]

Technical path:

1. [User action]
2. [Route / component / API involved]
3. [Data read/write]
4. [Result shown to user]

Important files:

- `[path]` — [what it does]
- `[path]` — [what it does]

---

### Flow 2: [Name]

Plain-English explanation:

[What happens from the user’s perspective.]

Technical path:

1. [User action]
2. [Route / component / API involved]
3. [Data read/write]
4. [Result shown to user]

Important files:

- `[path]` — [what it does]
- `[path]` — [what it does]

---

## 3. Folder and File Map

### Root-Level Files

- `README.md` — [purpose]
- `AGENTS.md` — [purpose]
- `.env.example` — [purpose]
- `package.json` / `requirements.txt` — [purpose]

### Main App Folders

- `[folder]` — [what lives here]
- `[folder]` — [what lives here]
- `[folder]` — [what lives here]

### Most Important Files

| File | Purpose | Safe to Edit? |
|---|---|---|
| `[path]` | [purpose] | [Yes / Caution / No] |
| `[path]` | [purpose] | [Yes / Caution / No] |
| `[path]` | [purpose] | [Yes / Caution / No] |

---

## 4. Data Model Explanation

### Where Data Lives

[Database, JSON files, local storage, external API, Supabase, Airtable, etc.]

### Main Data Objects

#### [Object Name]

Plain English:

[What this object represents.]

Important fields:

- `[field]` — [meaning]
- `[field]` — [meaning]
- `[field]` — [meaning]

Where it is used:

- `[path]`
- `[path]`

---

## 5. External Services and Integrations

| Service | What It Does | Where It Is Used |
|---|---|---|
| [Service] | [Purpose] | `[path]` |
| [Service] | [Purpose] | `[path]` |

### Integration Notes

[Explain any important API keys, permissions, rate limits, webhook behavior, or deployment constraints.]

---

## 6. Environment Variables

| Variable | Required? | Purpose | Notes |
|---|---|---|---|
| `[ENV_NAME]` | Yes/No | [purpose] | [notes] |
| `[ENV_NAME]` | Yes/No | [purpose] | [notes] |

### Setup Risks

- [Risk]
- [Risk]

---

## 7. Important Logic Paths

### [Feature / Workflow]

Plain English:

[What the logic is responsible for.]

Technical detail:

- Entry point: `[path]`
- Main logic: `[path]`
- Data layer: `[path]`
- Output/UI: `[path]`

What could break:

- [Risk]
- [Risk]

---

## 8. Risky Areas / Do-Not-Touch Zones

These areas require caution.

| Area | Why It Is Risky | Change Guidance |
|---|---|---|
| `[path or system]` | [risk] | [guidance] |
| `[path or system]` | [risk] | [guidance] |

Examples:
- Auth logic
- Payment logic
- SMS sending
- Database migrations
- Multi-tenant access rules
- Queue workers
- Webhooks
- Production environment config

---

## 9. Common Client Questions and Plain-English Answers

### Q: How does this app work?

A: [Plain-English answer]

### Q: Where is the data stored?

A: [Plain-English answer]

### Q: What happens when a user submits [thing]?

A: [Plain-English answer]

### Q: Can this scale?

A: [Honest answer with constraints]

### Q: What would be needed for the next phase?

A: [Plain-English answer]

---

## 10. Debugging Guide

### If [Problem] Happens

Check:

1. `[path or service]`
2. `[path or service]`
3. `[path or service]`

Likely causes:

- [Cause]
- [Cause]

Fix direction:

[What to investigate or change.]

---

## 11. Safe Change Map

### Usually Safe to Change

- Copy/content files
- Styling tokens
- Non-critical UI components
- Static config
- Documentation

### Change With Caution

- API routes
- Data schema
- Auth checks
- Background jobs
- External service integrations

### Do Not Change Casually

- Database migrations
- Tenant isolation logic
- Payment flows
- Webhooks
- Production environment variables
- Retry/idempotency logic

---

## 12. Suggested Future Improvements

### High Value / Low Risk

- [Improvement]
- [Improvement]

### High Value / Higher Risk

- [Improvement]
- [Improvement]

### Not Recommended Yet

- [Feature]
- [Feature]

---

## Final Owner Summary

If you need to explain this project quickly, say:

[Two to four sentence summary the owner can confidently use with a client.]
