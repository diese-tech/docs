# How To Use This Repo

This repo is the reusable operating system for Diese projects.

Use it to avoid starting from zero when creating new apps, websites, bots, automation systems, client work, or AI-assisted builds.

---

## Default Rule

Every new project should reference this repo.

At minimum, new repos should start with:

- README.md
- AGENTS.md
- MVP.md
- ROADMAP.md
- TASKS.md
- DECISIONS.md
- docs/AI_WORKFLOW_GUARDRAILS.md

---

## Folder Map

### 00-start-here

How to use the docs system and decide what to copy into new projects.

### 01-starter-pack

Core files every serious repo should start from.

### 02-repo-guardrails

Reusable operating rules for engineering, releases, incidents, operations, and repo health.

### 03-codebase-understanding

Templates for explaining existing codebases, mapping architecture, and identifying risky areas.

### 04-client-websites

Client discovery, content intake, design DNA, delivery, and handoff templates.

### 05-prompts

Reusable prompts for Claude, Codex, audits, implementation, bug fixes, and documentation generation.

### 06-decision-rubrics

Scorecards for deciding whether a project is worth building, maintaining, monetizing, or expanding.

---

## How To Start A New Project

1. Use `01-starter-pack`.
2. Copy the core templates into the new repo.
3. Rename `*-template.md` files to normal project docs.
4. Fill in project-specific details.
5. Keep exclusions explicit.
6. Add `AGENTS.md` before asking AI to implement.
7. Add `docs/AI_WORKFLOW_GUARDRAILS.md` before production-sensitive work.

---

## How To Improve This Repo

When a project creates a useful repeatable document:

1. Remove project-specific details.
2. Turn it into a generic template.
3. Save it in the relevant numbered folder.
4. Update the README if it becomes a core workflow.

---

## Principle

This repo should reduce repeated thinking.

It should not become a dumping ground.
