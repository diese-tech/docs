# Codebase Walkthrough Prompt

```text
Review this repository and generate a complete owner-friendly codebase walkthrough.

Goal:
Explain how the system works so the owner can:
- confidently maintain it
- explain it to clients
- onboard collaborators
- understand where important logic lives
- make safer changes later

Output:
1. Executive summary
2. Main user workflows
3. Folder and file map
4. Data flow explanation
5. External services and integrations
6. Environment variables
7. Important logic paths
8. Risky / high-blast-radius areas
9. Operational concerns
10. Common client questions and answers
11. Debugging guide
12. Future improvement opportunities

Rules:
- Use plain English first.
- Reference real files and folders.
- Separate business logic from implementation details.
- Explain why systems exist, not just what they do.
- Identify uncertainty instead of hallucinating.
- Do not rewrite or redesign the system.
```