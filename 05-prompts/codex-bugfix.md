# Codex Bugfix Prompt

```text
Review the repository before making changes.

Goal:
Fix the reported issue with the smallest safe modification possible.

Bug description:
[INSERT ISSUE]

Requirements:
- Preserve unrelated behavior.
- Avoid speculative refactors.
- Avoid cleanup unrelated to the bug.
- Keep blast radius low.
- Follow repository guardrails and AGENTS.md.
- Review docs/AI_WORKFLOW_GUARDRAILS.md before implementation.

Before coding:
1. Explain likely root causes.
2. Identify affected files.
3. Explain the safest fix path.
4. Identify potential side effects.

Implementation rules:
- Prefer incremental changes.
- Preserve existing workflows.
- Keep async behavior retry-safe.
- Do not add dependencies without justification.

After implementation:
1. Summarize what changed.
2. Explain why the fix is safe.
3. Explain remaining risks.
4. Explain how to validate the fix.
5. Confirm unrelated behavior was preserved.
```