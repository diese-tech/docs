# Playbooks

Reusable project playbooks, templates, guardrails, prompts, and operating manuals for Diese projects.

This repo exists so new projects do not start from zero and important rules do not get trapped inside old chats or individual repositories.

---

## Purpose

Use this repo as the standard reference point for new apps, bots, client websites, automation systems, SaaS experiments, and AI-assisted builds.

Every serious new project should begin with:

- clear scope
- documented decisions
- AI implementation guardrails
- operating principles
- project-specific README/MVP/roadmap/task docs
- a lightweight understanding of risks, maintenance burden, and next actions

---

## Current Structure

### `00-start-here/`

Start here before creating or organizing a project.

- `how-to-use-this-repo.md`
- `operating-principles.md`
- `new-project-checklist.md`

### `01-starter-pack/`

Core templates for new repositories.

- `README-template.md`
- `MVP-template.md`
- `ROADMAP-template.md`
- `TASKS-template.md`
- `DECISIONS-template.md`

### `02-repo-guardrails/`

Reusable operational and engineering guardrails.

- `operations-guide-template.md`

### `03-codebase-understanding/`

Templates for explaining and auditing existing codebases.

- `client-explanation-template.md`

### `04-client-websites/`

Templates for client website discovery, delivery, and quality control.

- `pre-delivery-checklist.md`

### `05-prompts/`

Reusable prompts for Claude, Codex, audits, bug fixes, and documentation generation.

- `claude-planning-session.md`
- `codex-bugfix.md`
- `codex-docs-generation.md`
- `codebase-walkthrough-prompt.md`

### `06-decision-rubrics/`

Rubrics for project readiness, monetization, and strategic filtering.

- `mvp-readiness-checklist.md`
- `monetization-readiness.md`

---

## Default New Project Flow

1. Start with `00-start-here/new-project-checklist.md`.
2. Copy the relevant templates from `01-starter-pack/` into the new repo.
3. Fill in project-specific context before implementation.
4. Add AI guardrails before using Codex, Claude, or other implementation agents.
5. Use decision logs for architecture, product, deployment, auth, persistence, and operational choices.
6. Promote any reusable project-specific docs back into this repo after removing project-specific baggage.

---

## Operating Rule

This repo should reduce repeated thinking.

It should not become a dumping ground.

If a document does not help start, explain, operate, audit, deliver, or evaluate a project, it probably does not belong here.

---

## Naming Note

If this repository is renamed, update project references from:

`diese-tech/docs`

To the new repository name, such as:

`diese-tech/playbooks`
