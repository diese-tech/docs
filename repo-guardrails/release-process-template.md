# Release Process Template

Use this document to define how changes move from development to production safely.

The goal is to avoid shipping by vibes.

---

## Release Type

- [ ] Feature release
- [ ] Bug fix
- [ ] Hotfix
- [ ] Documentation update
- [ ] Refactor
- [ ] Migration
- [ ] Dependency update

---

## Release Summary

What is changing?

[Answer]

Why is it changing?

[Answer]

Who is affected?

[Answer]

---

## Pre-Release Checklist

- [ ] Scope is clearly defined
- [ ] Unrelated changes removed
- [ ] Tests/build pass locally
- [ ] Environment variables reviewed
- [ ] Database migrations reviewed
- [ ] Rollback path identified
- [ ] Known risks documented
- [ ] User-facing behavior reviewed

---

## Validation Steps

Before release:

1. [Step]
2. [Step]
3. [Step]

After release:

1. [Step]
2. [Step]
3. [Step]

---

## Risk Areas

| Area | Risk | Mitigation |
|---|---|---|
| [Area] | [Risk] | [Mitigation] |
| [Area] | [Risk] | [Mitigation] |

---

## Rollback Plan

How do we undo this release?

[Answer]

Rollback trigger:

[What problem means we roll back?]

Rollback steps:

1. [Step]
2. [Step]
3. [Step]

---

## Communication Notes

Does anyone need to know this changed?

- [ ] Users
- [ ] Client
- [ ] Admins
- [ ] Operators
- [ ] Internal only

Message:

[Answer]

---

## Release Notes

### Added

- [Change]

### Changed

- [Change]

### Fixed

- [Fix]

### Known Issues

- [Issue]

---

## Release Principle

A release is not complete when code deploys.

It is complete when the expected behavior is verified in the target environment.
