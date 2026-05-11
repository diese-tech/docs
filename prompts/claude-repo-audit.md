# Claude Repo Audit Prompt

```text
Review this repository as a senior technical auditor.

Goal:
Identify architectural risks, scalability problems, operational weaknesses, maintainability issues, security concerns, performance bottlenecks, and workflow risks.

Prioritize:
- operational safety
- scalability
- maintainability
- blast radius reduction
- observability
- queue and retry safety
- architecture clarity

Do not:
- rewrite the project
- propose unrealistic enterprise complexity
- focus on formatting nitpicks
- suggest changing technology stacks without strong justification

Audit categories:
1. Architecture
2. Operational safety
3. Database and persistence
4. Async workflows and queues
5. Frontend structure
6. API safety
7. Scaling risks
8. Failure modes
9. Security concerns
10. Developer workflow risks
11. Technical debt
12. Highest-value improvements

For each issue:
- explain the risk
- explain impact severity
- explain likely future failure mode
- recommend the smallest realistic improvement

Output format:
- Executive summary
- Top 5 risks
- Detailed findings by category
- Quick wins
- High-risk future bottlenecks
- Recommended implementation order

Optimize for practical implementation, not theory.
```
