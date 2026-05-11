# Operating Principles

This repo exists to prevent repeated reinvention across projects.

The goal is not to create documentation theater.

The goal is to create reusable systems that make future projects faster, safer, easier to explain, and easier to maintain.

---

## 1. Every New Project Starts With Context

Do not start from a blank repo.

Every serious project should begin with:

- clear purpose
- MVP scope
- roadmap
- task tracker
- decision log
- AI implementation rules
- workflow guardrails

This protects future-you from archaeology.

---

## 2. Documentation Should Reduce Repeated Thinking

A good document answers questions that would otherwise be asked repeatedly.

If a document does not reduce friction, clarify direction, or preserve context, it probably does not belong here.

---

## 3. Scope Control Beats Feature Momentum

Projects fail when future ideas invade MVP scope.

Every MVP should define:

- what is included
- what is excluded
- why exclusions exist
- what success looks like

Deferred features are not failures.

They are protection.

---

## 4. AI Needs Guardrails Before Implementation

AI is useful for speed, but dangerous without boundaries.

Before AI-assisted implementation, define:

- product priority
- out-of-scope features
- architecture rules
- safety constraints
- rollback expectations
- validation requirements

AI should extend the system, not randomly reshape it.

---

## 5. Move Fast, But Move Surgically

The default implementation posture:

- smallest safe change
- lowest blast radius
- no unrelated cleanup
- no speculative rewrites
- no dependency sprawl
- preserve existing behavior unless explicitly changing it

Speed without discipline creates future drag.

---

## 6. Operational Clarity Is Product Quality

A project is not healthy just because it runs.

It should be understandable, observable, recoverable, and explainable.

Good projects make it clear:

- where data lives
- where workflows start
- what happens when things fail
- what should not be touched casually
- how to validate changes

---

## 7. Decisions Need Memory

When a choice matters, record the reasoning.

A future maintainer should understand:

- why the system looks this way
- what tradeoffs were accepted
- what alternatives were rejected
- when the decision should be revisited

The point is not bureaucracy.

The point is preventing repeated confusion.

---

## 8. Templates Should Stay Generic, But Opinionated

Templates should be reusable across projects.

They should not contain project-specific baggage.

But they should still carry strong opinions about quality, scope, safety, and maintainability.

Generic does not mean vague.

---

## 9. Do Not Build Documents Just To Have Documents

Every file in this repo should have a job.

If a template does not support project creation, client delivery, codebase understanding, AI workflow, or decision-making, it probably does not belong.

---

## 10. The System Should Compound

Each project should improve the framework.

When a repo produces a useful repeatable pattern:

1. remove project-specific details
2. convert it into a reusable template
3. add it to this repo
4. use it on the next project

This is how the operating system improves over time.
