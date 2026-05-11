# Codex Safe Implementation Prompt

```text
Review the repository before making changes.

Goal:
Implement the requested change using the smallest safe modification possible.

Requirements:
- Preserve existing behavior unless explicitly changing it.
- Avoid speculative refactors.
- Avoid unrelated cleanup.
- Do not rewrite working systems casually.
- Keep blast radius low.
- Preserve architecture consistency.
- Follow repository guardrails and AGENTS.md instructions.
- Review docs/AI_WORKFLOW_GUARDRAILS.md before implementation.

Before coding:
1. Explain the likely affected files.
2. Explain the implementation plan.
3. Identify risks.
4. Explain rollback approach.

Implementation rules:
- Prefer incremental changes.
- Prefer explicit workflows.
- Prefer maintainable solutions over clever ones.
- Do not introduce dependencies without justification.
- Preserve observability and operational clarity.
- Keep async workflows retry-safe.

After implementation:
1. Summarize what changed.
2. List changed files.
3. Explain what could still break.
4. Explain how to validate the change.
5. Confirm unrelated behavior was preserved.
```
