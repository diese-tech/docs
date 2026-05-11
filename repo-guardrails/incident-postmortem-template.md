# Incident Postmortem Template

Use this document after outages, production failures, data issues, deployment mistakes, or operational incidents.

The goal is learning and prevention.

Not blame.

---

# Incident Summary

## Incident Name

[Answer]

## Date / Time

[Answer]

## Severity

- [ ] Low
- [ ] Medium
- [ ] High
- [ ] Critical

## Systems Affected

- [System]
- [System]

---

# What Happened

Provide a plain-English explanation.

[Answer]

---

# User Impact

What did users experience?

- [Impact]
- [Impact]

Duration:

[Answer]

Estimated affected users:

[Answer]

---

# Timeline

| Time | Event |
|---|---|
| [Time] | [Event] |
| [Time] | [Event] |
| [Time] | [Event] |

---

# Root Cause

What actually caused the issue?

[Answer]

Contributing factors:

- [Factor]
- [Factor]

---

# Detection

How was the issue discovered?

- [Monitoring]
- [User report]
- [Logs]
- [Manual observation]

Detection delay:

[Answer]

---

# Resolution

What fixed the issue?

[Answer]

Temporary mitigation:

[Answer]

Permanent fix:

[Answer]

---

# What Went Well

- [Success]
- [Success]

---

# What Went Poorly

- [Issue]
- [Issue]

---

# Prevention Actions

| Action | Owner | Status |
|---|---|---|
| [Action] | [Owner] | Pending |
| [Action] | [Owner] | Pending |

---

# Operational Lessons

What should change about:

- architecture?
- observability?
- deployment?
- testing?
- rollback?
- queue safety?
- documentation?
- alerting?

[Answer]

---

# Final Rule

A production incident is only wasted if nothing improves afterward.
