# 🌿 Branch Strategy

> Git Branching Model used by Project Sentinel

---

## Purpose

This document defines the branching strategy adopted by Project Sentinel.

Its purpose is to establish a simple, consistent and maintainable workflow that supports continuous development while preserving the stability of the repository.

The chosen model reflects the current nature of the project: a single maintainer, continuous experimentation, laboratory environments, documentation and automation.

As the project evolves, this strategy may also evolve.

---

## Why Branches Exist

Branches allow development to occur without affecting the stable version of the project.

They provide an isolated environment for experimentation, implementation and validation before changes become part of the main repository.

Using branches improves:

- Development organization
- Traceability
- Safe experimentation
- Incremental delivery
- Easier rollback when necessary

For Project Sentinel, branches are primarily intended for new features, laboratory development, documentation improvements and automation experiments.

---

## Selected Workflow

Project Sentinel adopts the **GitHub Flow** model.

```
main
 └── feature/...
```

The `main` branch always represents the latest stable version of the project.

All new work should be developed in dedicated branches and merged back into `main` only after completion.

This workflow was selected because it matches the project's current reality:

- Single developer
- Continuous evolution
- Documentation-driven development
- Laboratory experimentation
- Low operational complexity

---

## Branch Naming Convention

Branches should use clear and descriptive names.

Recommended patterns include:

```
feature/<name>
docs/<name>
lab/<technology>
automation/<name>
fix/<name>
```

Examples:

```
feature/wazuh-dashboard
docs/branch-strategy
lab/docker-networking
automation/log-parser
fix/readme-links
```

---

## Branch Lifecycle

The standard workflow is:

1. Create a branch from `main`.
2. Develop the intended change.
3. Validate the work.
4. Merge the branch into `main`.
5. Delete the branch after merge.

Branches should be short-lived and focused on a single objective.

---

## Best Practices

Project Sentinel follows these recommendations:

- Keep branches small and focused.
- Avoid long-lived branches.
- Use meaningful branch names.
- Merge completed work as soon as possible.
- Keep `main` stable at all times.
- Document important engineering decisions.
- Commit frequently with descriptive messages.

---

## Future Evolution

The current strategy intentionally prioritizes simplicity.

If Project Sentinel eventually becomes a collaborative project involving multiple contributors, the branching model may evolve to include additional workflows such as Git Flow or other strategies better suited for larger development teams.

Until then, GitHub Flow remains the official workflow of the project.