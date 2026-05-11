# DECISIONS Template

Use this document to preserve important architectural, operational, and product reasoning.

Without decision logs, projects slowly accumulate:

- forgotten tradeoffs
- repeated debates
- accidental regressions
- architecture drift
- unclear historical context

This document explains not just what changed, but why.

---

# Decision Entry Format

## [Date] — [Decision Title]

### Decision

Describe the actual decision.

[Answer]

---

### Why This Decision Was Made

Explain the reasoning.

Questions to answer:

- What problem existed?
- Why was this option chosen?
- What constraints influenced the choice?
- What alternatives were considered?

[Answer]

---

### Expected Benefits

- [Benefit]
- [Benefit]
- [Benefit]

---

### Tradeoffs

No decision is free.

- [Tradeoff]
- [Tradeoff]
- [Tradeoff]

---

### Alternatives Considered

| Alternative | Why It Was Rejected |
|---|---|
| [Alternative] | [Reason] |
| [Alternative] | [Reason] |

---

### Risks Introduced

- [Risk]
- [Risk]

---

### Future Revisit Conditions

This decision should be revisited if:

- [Condition]
- [Condition]

Examples:

- scale changes
- architecture bottlenecks appear
- operational burden becomes too high
- cost changes significantly
- user workflows change

---

### Related Files

- `[path]`
- `[path]`
- `[path]`

---

### Operational Notes

Any deployment, migration, monitoring, or rollback concerns:

[Answer]

---

# What Should Be Logged

Log:

- architecture decisions
- database decisions
- persistence/storage changes
- auth strategy changes
- deployment changes
- queue/worker changes
- API contract changes
- dependency decisions
- operational workflow changes
- scaling strategy changes

Do not log:

- typo fixes
- formatting changes
- trivial copy edits
- obvious low-impact work

---

# Decision Philosophy

A good decision log reduces fear.

Future maintainers should be able to understand:

- why the system looks the way it does
- what constraints existed
- what tradeoffs were accepted
- what assumptions might no longer be true
