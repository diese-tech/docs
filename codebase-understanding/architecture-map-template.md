# Architecture Map Template

Use this document to explain the high-level structure of a system.

The goal is rapid understanding.

Someone should be able to read this and understand:
- how data flows
- what systems exist
- where responsibilities live
- where failures can occur

---

# System Summary

## What This System Does

[Answer]

## Primary Users

- [User type]
- [User type]

## Core Workflow

[One paragraph describing the system flow.]

---

# System Components

| Component | Purpose | Technology |
|---|---|---|
| Frontend | [Purpose] | [Tech] |
| API | [Purpose] | [Tech] |
| Database | [Purpose] | [Tech] |
| Queue / Workers | [Purpose] | [Tech] |
| External services | [Purpose] | [Tech] |

---

# Request Flow

## User Action Example

Example:

User submits a form.

Flow:

1. Frontend validates input
2. API receives request
3. Database stores record
4. Queue job created
5. Worker processes async work
6. UI updates user state

---

# Data Flow

## Source of Truth

[Database / API / file storage / external service]

## Important Data Objects

- [Object]
- [Object]
- [Object]

## Derived Data

[What gets computed, cached, or projected]

---

# Async Workflows

| Workflow | Trigger | Worker / Queue | Failure Risk |
|---|---|---|---|
| [Workflow] | [Trigger] | [Worker] | [Risk] |
| [Workflow] | [Trigger] | [Worker] | [Risk] |

---

# External Services

| Service | Why It Exists | Failure Impact |
|---|---|---|
| [Service] | [Purpose] | [Impact] |
| [Service] | [Purpose] | [Impact] |

---

# Operational Risks

- [Risk]
- [Risk]
- [Risk]

---

# Scaling Risks

What breaks first under scale?

- [Risk]
- [Risk]

---

# Safe Modification Zones

Usually safe:

- [Area]
- [Area]

Requires caution:

- [Area]
- [Area]

Do not casually touch:

- [Area]
- [Area]

---

# Final Rule

Good architecture maps reduce fear.

If a system feels impossible to understand, the architecture probably needs simplification.
