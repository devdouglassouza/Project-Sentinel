# 📄 Template Strategy

> Template Strategy of Project Sentinel

---

## Purpose

Define how Project Sentinel creates, uses, and maintains documentation templates — ensuring consistency, reproducibility, and long-term clarity across all technical artifacts.
---

## Why Templates Exist

Templates exist to remove ambiguity from how something is documented, so that effort goes into what is being documented. They encode lessons learned about what a good ADR, lab, or runbook needs to contain — so that quality doesn't depend on memory, mood, or how much time was available that day.
---

## Engineering Philosophy

A template is not bureaucracy — it's engineered structure. It should answer, for any future reader (including a future version of the author): what was the context, what was done, why, and what came out of it. If a template can't "teach" someone who has forgotten the original work, it isn't doing its job.

Templates are living artifacts. They evolve with the project instead of being fixed on day one and never revisited.

---

## Benefits

Using templates provides several long-term advantages:

- Consistent documentation structure
- Faster document creation
- Reduced knowledge loss
- Easier onboarding
- Improved maintainability
- Better comparison between similar artifacts

---

## What Requires a Template

Any artifact that will be repeated (multiple labs, multiple incidents, multiple ADRs)
Any artifact whose absence of structure would compromise reproducibility or comparison
Any artifact meant to be read by someone other than the author, later, out of context

---

## What Does NOT Require a Template

Exploratory notes, brainstorms, or thinking-in-progress
One-off content with no expectation of repetition
Content where imposing structure early would suppress useful exploration

---

## Template Organization

All reusable documentation templates are stored under Documentation/Templates/. Templates should represent stable document structures rather than project-specific content. The goal is to separate reusable engineering patterns from the documents created from them.

Documentation/
└── Templates/
    ├── adr-template.md
    ├── lab-template.md
    ├── playbook-template.md
    ├── readme-template.md
    ├── incident-report-template.md
    ├── research-notes-template.md
    └── runbook-template.md

---

## Current Official Templates

| Template          | Purpose                |
| ----------------- | ---------------------- |
| ADR Template      | Architecture decisions |
| Lab Template      | Hands-on labs          |
| Playbook Template | Operational procedures |
| README Template   | Repository overview    |
| Incident Report   | Security incidents     |
| Research Notes    | Study documentation    |
| Runbook           | Operational execution  |

---

## Template Lifecycle

TTemplates evolve through four possible paths when they stop fitting reality:

Review — recognize that the template no longer represents reality; understand why.
Adapt — the deviation is isolated; adjust the existing template.
Fork/Create new — the deviation is structural and recurring enough to represent a distinct type of document.
Deprecate — the document type no longer applies to the project; retire the template.

Every change to a template should be traceable — ideally through the same version control history as the rest of the project.

---

## Continuous Improvement

Templates are reviewed periodically, not only when something breaks. Feedback from actual usage — friction points, missing sections, redundant fields — feeds back into revisions. The goal is a template that gets quieter over time: less overhead, more signal.