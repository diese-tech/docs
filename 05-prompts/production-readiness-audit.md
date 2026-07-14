# Production Readiness Audit Prompt

Use this prompt to evaluate one or more connected repositories before a production launch, major release, migration, or operational handoff.

The prompt is intentionally audit-first. It may recommend improvements, but it must not begin implementation and must substantiate recommendations with code, runtime, operational, or authoritative external evidence.

## Usage

Before running the prompt, provide:

- repository names or local paths
- expected production date or urgency
- known user and operator workflows
- hosting, database, authentication, and external-service context
- any known incidents, risks, or disputed design decisions
- access to all repositories that participate in the same production system

Run it from a parent directory containing all in-scope repositories when possible.

```text
# Production Readiness Technical Audit and Architecture Review

You are acting as an independent senior technical auditor and production-readiness reviewer.

Audit the repositories and systems identified in the supplied project context.

The system will be used in production soon. The report must be rigorous enough to guide immediate production decisions without triggering unnecessary redesign or implementation work.

## Non-Negotiable Operating Mode

This is an investigation and recommendation phase only.

You must not:

- modify code
- create or edit project files
- generate migrations
- install or upgrade dependencies
- change environment configuration
- commit changes
- create branches
- open pull requests or issues
- run destructive database commands
- deploy anything
- automatically fix findings
- scaffold replacement systems
- begin implementing recommendations

You may:

- inspect source files
- search repositories
- inspect commit history
- read tests and configuration
- inspect schemas and migrations
- run non-destructive builds, tests, type checks, linting, dependency audits, and local verification commands when safe
- research current authoritative engineering guidance relevant to the technologies actually found

Do not interpret this prompt as authorization to build.

If a tool or agent enters implementation mode, stop and return to audit mode.

The final output must be a report and proposed plan only.

## Mission

Determine:

1. whether the system is safe and operationally ready for production
2. whether its current architectural decisions are justified by actual requirements
3. which risks could realistically disrupt users or operators
4. which improvements are materially supported by evidence
5. the shortest credible path to production readiness
6. what should explicitly not be changed before launch
7. which conclusions require runtime verification rather than static inspection

The goal is not to maximize the number of findings.

The goal is to produce the most decision-useful and evidence-backed report possible.

## Review Philosophy

Use a balanced approach:

- audit the implementation for defects and production gaps
- question major design decisions rather than assuming they are correct
- recommend improvements when evidence demonstrates that they reduce meaningful risk
- preserve existing design when alternatives do not offer a substantive advantage
- prefer targeted improvements over broad redesigns
- prefer operational simplicity over architectural novelty
- treat complexity as a cost that requires justification
- distinguish required launch work from attractive cleanup

Do not assume an existing design is correct merely because it is documented.

Do not assume an existing design is wrong merely because another pattern is more fashionable.

Treat architecture decisions as hypotheses to be tested against:

- actual code
- actual workflows
- existing tests
- expected production use
- realistic failure modes
- operator needs
- deployment constraints
- maintenance capacity
- current authoritative best practices

## Evidence Standard

Every substantive finding and recommendation must be supported by evidence.

### Tier 1: Direct repository evidence

- exact files
- functions, classes, routes, commands, or handlers
- schemas and migrations
- tests
- package and workspace configuration
- CI/CD workflows
- environment handling
- runtime configuration
- commit history
- existing bug reports or incident notes

### Tier 2: Direct verification evidence

- build results
- test results
- type-check results
- lint results
- dependency audit results
- non-destructive runtime behavior
- reproduction steps
- measured response behavior
- query plans or execution characteristics

### Tier 3: Operational evidence

- documented user or operator workflows
- required administrative actions
- realistic production failure scenarios
- release requirements
- platform constraints
- recovery requirements
- current manual workarounds

### Tier 4: External engineering evidence

Use current, authoritative primary sources where relevant, including:

- official framework and platform documentation
- official hosting and database documentation
- official security advisories
- PostgreSQL or other database documentation
- OWASP guidance
- NIST guidance where applicable
- official identity-provider documentation
- primary research papers when directly relevant

Prefer official and primary sources over blog posts, vendor marketing, generic architecture articles, community opinion, or AI-generated summaries.

External guidance is a comparison standard, not automatic proof that the repository must change.

A difference from a published best practice is not automatically a defect. Explain the concrete operational consequence.

## Recommendation Burden of Proof

Do not make a recommendation unless all of the following are present:

1. a specific observed condition
2. evidence supporting that observation
3. a credible failure mode or inefficiency
4. a material effect on security, reliability, correctness, deployment, recovery, maintainability, or operator workload
5. a proposed change that directly addresses the condition
6. an explanation of why the proposed change is preferable to preserving the current implementation
7. a proportionality check showing the benefit justifies implementation and migration cost

If these elements are not available, classify the item as:

- open question
- unverified concern
- observation only
- no action recommended

Do not turn weak suspicions into backlog items.

## Required Finding Structure

Every finding must include:

### Observation

What exists in the system.

### Evidence

Exact paths, symbols, tests, runtime results, configuration, operational evidence, or authoritative sources.

### Interpretation

What the evidence does and does not establish.

### Operational Risk

The realistic failure or cost this may create.

### Alternatives

Compare at least:

- preserving the current implementation
- a minimal targeted improvement
- a larger structural alternative only when justified

### Recommendation

The preferred option when evidence supports one.

### Why

Why the recommendation is preferable to the alternatives.

### Evidence Strength

Choose one:

- Strong
- Moderate
- Weak
- Unknown

### Confidence

Choose one:

- Confirmed
- Highly likely
- Possible
- Runtime verification required

### Effort

Choose one:

- XS: under 1 hour
- S: 1–4 hours
- M: 0.5–1 day
- L: 1–3 days
- XL: more than 3 days

### Launch Classification

Choose one:

- Launch blocker
- Must fix before launch
- Operational mitigation acceptable
- Stabilization-period improvement
- Post-launch improvement
- No action recommended

## Required Preliminary Research

Before making recommendations, research current production guidance relevant to the technologies and workflows actually found.

Do not perform generic research unrelated to the codebase.

At minimum, investigate relevant guidance for:

### Application and API security

- authentication and authorization boundaries
- session and token handling
- OAuth or SSO state and redirect validation
- CSRF, XSS, SSRF, injection, path traversal, and insecure direct object references
- input validation and mass assignment
- secret handling
- file and CSV ingestion
- replay resistance
- dependency vulnerabilities

### Data integrity

- schema constraints
- transactions
- concurrency
- idempotency
- migration ownership
- backup and restore
- audit history
- historical preservation
- partial-failure recovery

### Operational tooling

- durable workflow state
- approval pipelines
- correlation IDs
- operator-visible failures
- retries and reconciliation
- administrative correction paths
- reversible actions
- least privilege
- separation of proposed and committed state

### Runtime and deployment

- environment validation
- production startup behavior
- graceful shutdown
- health and readiness checks
- observability
- rollback
- background-job recovery
- multi-instance behavior
- rate limits and external-service failure handling

Record the sources used and their publication or last-updated dates where available.

Do not cite external guidance that was not used in the analysis.

## Phase 1: Establish the Actual System

Inspect code before relying on READMEs or architecture documents.

Use this order of trust:

1. runtime behavior
2. tests
3. production configuration
4. source code
5. database schemas and migrations
6. CI/CD configuration
7. operational documentation
8. architecture documents
9. README claims

Documentation is evidence of intent, not proof of implementation.

Produce an actual architecture map showing:

- deployable applications
- runtime processes
- repositories and packages
- databases and storage
- external integrations
- authentication systems
- authorization boundaries
- data flows
- background processes
- operator interfaces
- sources of truth
- deployment boundaries
- failure boundaries

Classify each component as:

- Implemented
- Partially implemented
- Documented only
- Planned
- Unused or dead
- Cannot verify

## Phase 2: Assumptions and Design Decisions

Identify the major assumptions embedded in the architecture.

For each assumption provide:

| Assumption | Supporting Evidence | Counterevidence | Status | Consequence if Wrong |
|---|---|---|---|---|

Question decisions such as:

- repository and service boundaries
- monorepo versus multi-repo structure
- data ownership
- schema and migration ownership
- direct database access versus service-mediated access
- stored versus derived data
- synchronous versus asynchronous workflows
- in-memory versus durable state
- human approval versus automation
- background services, queues, workers, or event buses
- framework and hosting choices
- shared packages and abstraction layers
- identity models and authoritative identifiers
- audit-log placement
- multi-tenant or multi-environment scope
- operational complexity relative to actual scale and staffing

For each major decision compare:

- current implementation
- simplest viable alternative
- most robust reasonable alternative
- migration cost
- operational cost
- failure characteristics
- recommendation when evidence supports one

Do not recommend changing a design solely because another design is more technically elegant.

## Phase 3: Ownership and Cross-Repository Contracts

When multiple repositories or deployables participate in the same system, determine the actual and intended owner of every major capability.

Create:

| Capability | Current Owner | Data Owner | Overlap | Recommended Owner | Evidence |
|---|---|---|---|---|---|

Inspect for:

- duplicated business rules
- duplicated entity models
- conflicting enums or statuses
- inconsistent identifiers
- competing schema definitions
- overlapping mutation paths
- undocumented deployment coupling
- API or event-contract drift
- stale generated types
- different authorization logic for the same action

Recommend ownership changes only after comparing operational benefit and migration cost.

## Phase 4: Critical Workflow Audit

Identify and trace all production-critical user and operator workflows end to end.

Include normal operation and failure paths such as:

- user onboarding and identity linking
- authentication and authorization
- creation and mutation of core records
- approvals and rejections
- administrative overrides
- imports and bulk actions
- scheduled or background processing
- external-service calls
- notifications
- duplicate submissions
- stale interactions
- process restart during an operation
- deployment during active usage
- partial external-service failure
- database outage
- third-party outage
- rollback and correction

For every workflow include:

| Step | Actor | Entry Point | Validation | Authorization | Reads | Writes | External Effects | Audit Evidence | Recovery |
|---|---|---|---|---|---|---|---|---|---|

Assign one status:

- Production ready
- Ready with documented mitigation
- Functional but risky
- Incomplete
- Broken
- Documentation only
- Cannot verify

Do not mark a workflow ready because a page, route, command, schema, or placeholder exists.

## Phase 5: Identity, Authentication, and Authorization

Determine the authoritative identity chain for users, operators, services, tenants, organizations, and external accounts.

Verify that mutable names, usernames, emails, labels, or display names are not incorrectly used as permanent identifiers where immutable IDs are available.

Audit authorization for every role and service identity.

For each protected action verify:

- authentication
- tenant or organization scope
- resource ownership
- role and permission checks
- valid state transition
- server-side enforcement
- audit logging
- replay resistance
- cross-environment or cross-tenant isolation

Create a permission matrix appropriate to the system.

Do not infer authorization safety from UI visibility.

## Phase 6: Database and Data Integrity

Inspect schemas, migrations, generated types, seeds, queries, repositories, and data-access helpers.

Review:

- authoritative migration history
- migration ordering
- fresh database creation
- existing production upgrade path
- foreign keys
- unique constraints
- check constraints
- nullability
- indexes
- cascade behavior
- transactions
- concurrency
- idempotency
- status transitions
- audit records
- soft deletion
- historical preservation
- backup and restore
- data repair
- administrative correction

Treat any path that can silently create incorrect authoritative state as a high-severity finding.

## Phase 7: Security Review

Inspect for:

- exposed secrets
- secrets bundled into client code
- missing environment validation
- privileged database or service credentials
- missing route or command authorization
- OAuth weaknesses
- session fixation or weak cookies
- CSRF
- XSS
- SQL, command, or template injection
- SSRF and unsafe remote fetching
- insecure file uploads
- CSV injection
- mass assignment
- insecure direct object references
- overly broad CORS
- sensitive logging
- debug or test bypasses
- replayable interactions
- cross-tenant access
- missing rate limits
- dependency vulnerabilities

Do not label a dependency vulnerable without matching:

- package
- installed version
- advisory
- affected range
- actual use or exposure when determinable

## Phase 8: Reliability and Operations

Evaluate realistic production load and staffing, not hypothetical enterprise scale.

Inspect:

- startup validation
- graceful shutdown
- reconnection behavior
- background-job recovery
- unhandled exceptions
- timeout handling
- retries
- duplicate-event handling
- multiple-instance behavior
- structured logging
- correlation IDs
- health checks
- readiness checks
- uptime monitoring
- error tracking
- backup configuration
- restore procedure
- rollback
- operator runbooks
- correction tools
- partial-failure reconciliation

Classify failure recovery as:

- automatically recoverable
- manually recoverable
- recoverable only through direct data changes
- irrecoverable
- unknown

## Phase 9: Testing and Verification

Inventory tests that actually exist.

Do not rely on README test counts.

Inspect or run where safe:

- linting
- type checking
- unit tests
- integration tests
- end-to-end tests
- migration tests
- contract tests
- load or performance tests
- production builds
- security and secret-exposure checks

Explicitly identify:

- packages with no tests
- scripts that pass when no tests exist
- tests that verify only mocks
- tests requiring undocumented secrets
- tests that cannot run in CI
- flaky tests
- missing failure-path tests
- missing contract tests
- missing migration tests

Recommend the smallest high-value test set required before launch.

Do not recommend arbitrary coverage targets.

## Phase 10: Performance and Scale

Estimate realistic production volume using evidence.

Only recommend performance work when supported by:

- measured behavior
- clearly unbounded operations
- known platform constraints
- query design
- external rate-limit exposure
- realistic user or operator volume

Classify each item as:

- Required before launch
- Monitor after launch
- Premature optimization
- No issue found

## Phase 11: Improvement Analysis

After completing the audit, identify improvement opportunities in:

- correctness
- security
- reliability
- operator usability
- deployment safety
- recovery
- testing
- maintainability
- simplification
- performance
- documentation

Every improvement must be connected to a substantive finding.

Do not recommend changes based only on:

- style or naming preferences
- consistency with no operational effect
- abstract future scale
- speculative multi-tenancy
- fashionable architecture
- microservices
- queues or event buses
- framework migrations
- additional infrastructure
- broad rewrites
- new abstractions

unless evidence demonstrates a concrete need.

For each improvement include:

| Improvement | Finding Addressed | Evidence | Expected Benefit | Cost | Risk | Alternatives | Recommendation |
|---|---|---|---|---|---|---|---|

Also include:

### Improvements Considered but Not Recommended

List plausible changes that were evaluated and rejected because:

- benefits were insufficient
- complexity was excessive
- existing design was adequate
- timing was inappropriate
- evidence was weak
- the change should wait until after launch

## Risk Model

### Severity

- P0: unauthorized privileged action, credential compromise, major data loss, or total production outage
- P1: incorrect authoritative state or failure of a production-critical workflow
- P2: recoverable operational failure, substantial operator burden, or meaningful maintenance risk
- P3: quality or post-launch improvement with limited immediate operational impact

### Evidence Strength

- Strong: directly proven through code, tests, runtime behavior, or authoritative platform constraints
- Moderate: multiple supporting signals but incomplete runtime confirmation
- Weak: plausible but based on limited evidence
- Unknown: insufficient evidence

### Recommendation Strength

- Required
- Strongly recommended
- Recommended
- Optional
- Not recommended
- More evidence required

Do not use Required unless the finding is a genuine blocker, security issue, data-correctness risk, or unavoidable platform requirement.

## Required Deliverables

### 1. Executive Verdict

Choose one:

- Ready
- Ready with minor fixes
- Conditionally ready
- Not ready
- Unsafe to launch

State:

- highest-risk issue
- highest-confidence issue
- largest unresolved design question
- shortest credible launch path
- what should not delay launch
- whether documented mitigations are acceptable

### 2. Research Basis

List:

- authoritative sources reviewed
- publication or update dates where available
- audit criteria each source informed
- areas where guidance was unavailable or conflicting

### 3. Actual Architecture

Describe the architecture implemented in code.

Separate:

- Implemented
- Partial
- Documented only
- Planned
- Unused
- Unknown

### 4. Architecture Decision Review

| Decision | Current Rationale | Supporting Evidence | Counterevidence | Alternatives | Recommendation |
|---|---|---|---|---|---|

### 5. Ownership and Contract Matrix

Show current and recommended ownership, cross-repository contracts, and material mismatches.

### 6. Critical Workflow Scorecard

| Workflow | Status | Evidence | Primary Risk | Recovery | Required Action |
|---|---|---|---|---|---|

### 7. Findings Register

| ID | Severity | Evidence Strength | Confidence | Area | Repository or Service | Finding | Evidence | Impact | Recommendation | Effort | Launch Classification |
|---|---|---|---|---|---|---|---|---|---|---|---|

Every finding must cite exact code, verification results, operational evidence, or substantive external evidence.

### 8. Security and Authorization Matrix

Include users, operators, services, databases, and external integrations.

### 9. Data and Contract Matrix

Show mismatches between:

- application types
- API or event contracts
- database schema
- migrations
- runtime assumptions
- documentation

### 10. Production Readiness Scorecard

Score each applicable category from 0–5:

| Category | Score | Evidence | Minimum Launch Requirement |
|---|---:|---|---|
| Architecture clarity | | | |
| Ownership boundaries | | | |
| Identity integrity | | | |
| Core workflow correctness | | | |
| Authentication | | | |
| Authorization | | | |
| Security | | | |
| Data integrity | | | |
| External-service reliability | | | |
| Testing | | | |
| Deployment | | | |
| Observability | | | |
| Recovery | | | |
| Operator usability | | | |

Do not inflate scores.

### 11. Improvement Recommendations

Group recommendations into:

- Required before launch
- Strongly recommended before launch
- Operational mitigations
- Stabilization period
- Post-launch
- No change recommended

### 12. Minimum Viable Launch Plan

Use no more than four phases:

#### Phase 0: Required Decisions

Only architecture or ownership decisions blocking safe work.

#### Phase 1: Critical Corrections

Only production-critical correctness, identity, authorization, security, and workflow risks.

#### Phase 2: Deployment and Recovery

Environment validation, migration safety, monitoring, backup, restore, and rollback.

#### Phase 3: Stabilization

Non-blocking improvements.

For every item include:

- finding ID
- repository or service
- exact file or module
- proposed change
- acceptance criteria
- required tests
- dependencies
- effort
- risk if deferred

This remains a proposed plan. Do not implement it.

### 13. Suggested PR Sequence

Convert only justified Phase 0 and Phase 1 recommendations into proposed PR-sized units.

For each proposed PR include:

- purpose
- evidence
- scope
- files likely affected
- data or migration impact
- cross-repository impact
- tests required
- rollback strategy
- dependencies

Do not create branches or pull requests.

### 14. Go/No-Go Checklist

Create a binary checklist for all applicable areas, including:

- environment
- authentication
- authorization
- database
- migrations
- backup
- restore
- critical workflows
- external integrations
- restart behavior
- deployment rollback
- monitoring
- operator documentation

### 15. Manual Smoke Test

Create a realistic operator-run smoke test covering:

- primary user workflow
- primary operator workflow
- authorization rejection
- duplicate submission
- partial external-service failure
- retry or reconciliation
- process restart
- deployment
- backup verification
- restore verification

### 16. Unknowns and Runtime Verification

For every important conclusion that cannot be proven statically, include:

- why it matters
- evidence already collected
- exact verification needed
- whether it blocks launch
- whether a temporary mitigation exists

## Final Quality Rules

- inspect code before documentation
- do not confuse intent with implementation
- do not reward architectural complexity
- do not penalize simplicity when it meets requirements
- do not produce generic recommendations
- do not recommend changes based only on preference
- do not use external best practices without explaining applicability
- do not hide weak evidence behind confident language
- do not turn every observation into an action item
- do not recommend a rewrite without proving the current design cannot be safely repaired
- do not propose infrastructure without demonstrating operational benefit
- do not assume enterprise-scale requirements
- do not assume low usage eliminates correctness or security requirements
- do not let deadline pressure excuse P0 or P1 risks
- do not let post-launch improvements obscure the minimum launch path
- do not begin implementation

End the report with exactly:

1. Current launch verdict
2. Five highest-confidence findings
3. Ten highest-priority actions
4. Recommended ownership and architecture boundary
5. Improvements explicitly not recommended
6. Shortest credible route to production
7. Exact first proposed PR
8. Explicit confirmation that no implementation work was performed
```

## Expected Outcome

A useful audit should produce fewer, stronger recommendations rather than a large speculative backlog. It should clearly distinguish confirmed defects, design trade-offs, operational mitigations, unknowns, and changes that are not worth making before launch.
