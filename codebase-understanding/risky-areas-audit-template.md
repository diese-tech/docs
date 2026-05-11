# Risky Areas Audit Template

Use this document to identify fragile, dangerous, high-blast-radius, or operationally sensitive parts of a codebase.

The goal is to reduce accidental outages and unsafe modifications.

---

# Audit Summary

## System Name

[Answer]

## Audit Date

[Answer]

## Overall Risk Level

- [ ] Low
- [ ] Medium
- [ ] High
- [ ] Critical

---

# Risk Categories

| Category | Risk Level | Notes |
|---|---|---|
| Auth | [Level] | [Notes] |
| Billing | [Level] | [Notes] |
| Database | [Level] | [Notes] |
| Queues | [Level] | [Notes] |
| Async workflows | [Level] | [Notes] |
| Deployments | [Level] | [Notes] |
| Multi-tenant isolation | [Level] | [Notes] |
| Integrations | [Level] | [Notes] |

---

# High-Risk Areas

## [Area Name]

### Why It Is Risky

[Explanation]

### Files Involved

- `[path]`
- `[path]`

### Failure Modes

- [Failure]
- [Failure]

### Operational Impact

[What happens if this breaks]

### Safe Change Guidance

[How to safely modify this area]

### Recommended Protections

- [Protection]
- [Protection]

---

# Observability Gaps

What dangerous areas lack:

- logging?
- metrics?
- alerts?
- validation?
- rollback support?

[Answer]

---

# Recommended Priorities

## Immediate

- [Action]
- [Action]

## Soon

- [Action]
- [Action]

## Eventually

- [Action]
- [Action]

---

# Final Rule

High-risk systems are not automatically bad.

High-risk systems without documentation, observability, or rollback paths are bad.
