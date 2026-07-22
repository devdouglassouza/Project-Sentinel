# 📝 Conventional Commits

> Commit message convention adopted by Project Sentinel

---

## Purpose

This document defines the commit message convention adopted by Project Sentinel.

Its purpose is to ensure that every commit clearly communicates the evolution of the project, making the repository easier to understand, maintain and navigate over time.

Rather than recording the developer's effort, commit messages should record meaningful changes to the project's capabilities, documentation or architecture.

---

## Why Commit Messages Matter

Every commit represents a point in the project's history.

Well-written commit messages allow anyone to understand:

- What changed.
- Why it changed.
- How the project evolved.

A clean commit history is part of the project's documentation.

---

## Adopted Convention

Project Sentinel follows the Conventional Commits specification.

Each commit message should follow the format:

```
<type>: <short description>
```

Examples:

```
docs: add Branch Strategy documentation

feat: create Docker lab

fix: correct firewall rule

refactor: simplify parser structure
```

---

## Commit Types

### docs

Documentation changes.

Examples:

```
docs: update README

docs: add ADR template
```

---

### feat

Introduces a new capability or feature.

Examples:

```
feat: create Wazuh deployment scripts

feat: add Docker Compose environment
```

---

### fix

Corrects incorrect behavior.

Examples:

```
fix: resolve Docker networking issue
```

---

### refactor

Improves internal implementation without changing behavior.

---

### chore

Repository maintenance tasks.

Examples:

```
chore: reorganize project structure

chore: update dependencies
```

---

### test

Adds or updates automated tests.

---

### build

Changes related to the build system or dependencies.

---

### ci

Changes to Continuous Integration workflows.

---

### perf

Performance improvements.

---

### style

Formatting or code style changes without behavioral impact.

---

## Commit Philosophy

A commit should describe how the project evolved, not how much work was performed.

Good commit messages answer:

- What changed?
- What capability was added, improved or corrected?

Avoid generic messages such as:

```
Update

Corrections

Final version

Test

Changes
```

---

## Sentinel Recommendations

Project Sentinel primarily uses the following commit types:

- docs
- feat
- fix
- refactor
- chore

Other commit types may be used when appropriate.

The objective is consistency rather than quantity.