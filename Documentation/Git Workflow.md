# 🔄 Git Workflow

> Git Workflow of Project Sentinel

---

## Purpose

Describe the standard path a change takes inside Project Sentinel — from idea to
pushed history — so that any contributor, at any point in time, knows exactly what
step comes next and why it exists.

This document is the operational counterpart to [The Sentinel Principles](./The%20Sentinel%20Principles.md).
If the Principles are the constitution, this is the day-to-day manual.

---

## Why Git Workflow Matters

A workflow is not a sequence of Git commands — it's the physical trace of how we think
while building. Every step here exists to answer one question at the moment it matters:
*is this change ready to move forward?*

Without a defined workflow, quality depends on who is working and how much time they
have. With one, the process itself protects the outcome — regardless of who's driving.

---

## Workflow Overview

Every contribution to Project Sentinel follows the same lifecycle.

The workflow below represents the standard engineering process adopted by the project.
Each step builds on the previous one, ensuring that technical work remains traceable, documented, and reproducible over time.

```
Project Idea
    │
    ▼
Create Branch
    │
    ▼
Develop
    │
    ▼
Document
    │
    ▼
Commit
    │
    ▼
Review
    │
    ▼
Merge
    │
    ▼
Update CHANGELOG (when applicable)
    │
    ▼
Push
```

---

## The Journey, Step by Step

### 1. Project Idea

Every change starts as an idea, not as code. Before writing anything, check whether
related documentation already exists — a Lab, an ADR, a Research Note. Reinventing
what's already documented breaks the principle that *each piece of information should
exist in a single place*.

> **Mindset:** we don't start typing before we know what already exists.

### 2. Create Branch

Once the idea is scoped, it gets its own branch. Naming, scope, and lifetime of branches
follow **[Branch Strategy](./Branch%20Strategy.md)** — this document doesn't repeat those rules, only assumes them.

### 3. Develop

Work happens here. This is intentionally the least prescriptive step — engineering judgment governs, not process.

During development, experiments, prototypes and iterations are expected. 
The objective of this phase is not only to implement a solution, but also to validate that it solves the original problem before becoming part of the project's history.

### 4. Document

Documentation is not an afterthought tacked on before merge — it's part of development
itself. What gets documented, how, and in which format follows **[Documentation
Standards](./Documentation%20Standards.md)**. If the change introduces a new recurring artifact type, check whether it
needs a template — see **[Template Strategy](./Template%20Strategy.md)**.

> **Mindset:** if it isn't documented, it isn't finished.

### 5. Commit

Commits are written following **[Conventional Commits](./Conventional%20Commits.md)**. A commit message should let
someone understand *what* changed and *why* without opening the diff.

### 6. Review

Before merging, ask:

- Does the change solve the intended problem?
- Is the documentation up to date?
- Can another engineer understand this work months from now?

> **Mindset:** review checks the code *and* the trace it leaves behind.

### 7. Merge

Merge happens only after review is satisfied. No step is skipped because the change
"is small" — size doesn't exempt a change from the workflow.

### 8. Update CHANGELOG (when applicable)

Not every change warrants a CHANGELOG entry. Apply this step when the change is
user-facing, structural, or otherwise relevant to someone tracking the project's
evolution from the outside.

### 9. Push

From this point onward, the change becomes part of Project Sentinel's engineering history and serves as a foundation for future work.

---

## Related Handbook Documents

This workflow doesn't redefine what's already specified elsewhere. When in doubt,
these are the sources of truth:

- **[Branch Strategy](./Branch%20Strategy.md)** — branch naming, scope, lifetime
- **[Conventional Commits](./Conventional%20Commits.md)** — commit message format and semantics
- **[Documentation Standards](./Documentation%20Standards.md)** — how and when to document
- **[Template Strategy](./Template%20Strategy.md)** — when a document needs a standard structure

---

## Continuous Improvement

This workflow is reviewed the same way any other artifact in Sentinel is: when friction appears, when a step is consistently skipped, or when the project's reality no longer matches what's written here.
Adjustments follow the same Review → Adapt / Fork / Deprecate lifecycle defined in **[Template Strategy](./Template%20Strategy.md)**.