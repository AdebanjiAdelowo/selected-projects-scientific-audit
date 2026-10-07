# Selected Projects Scientific Audit

This repository tracks the scientific review of my selected research and technical projects, with particular emphasis on their suitability for PhD and research applications.

## Purpose

The audit asks, for each project:

1. What problem is actually being solved?
2. Is the mathematical or physical problem meaningful and sufficiently specified?
3. What is the exact governing model, including domain, initial/boundary conditions, parameters, and assumptions?
4. Is the chosen numerical or machine-learning method appropriate?
5. Is the method consistent, stable, and capable of convergence where those concepts apply?
6. Does the implementation actually solve the stated problem?
7. What do the numerical experiments and figures establish, and what do they not establish?
8. Are reduced-order or learned formulations scientifically consistent with the full problem?
9. Are the conclusions supported by the evidence?
10. What should be corrected, rerun, or qualified?

## Discussion-status labels

- **STRONG TO DISCUSS** — audited and suitable for substantive discussion when the documented limitations are preserved.
- **DISCUSS WITH QUALIFICATION** — scientifically meaningful, but a correction, convergence issue, or pending verification must be disclosed.
- **DO NOT USE AS A HEADLINE YET** — an important verification or scope issue remains unresolved.
- **AUDIT PENDING** — not yet reviewed under the same problem–method–implementation framework.

## Current application review

The current review document is:

`selected_projects_phd_discussion_status_2026-10-07.pdf`

It is a snapshot of the audit as of **7 October 2026**. Statuses are not permanent rankings. They will be updated as targeted verification, corrected experiments, and project-specific scientific audits are completed.

## Important interpretation

A negative result is not automatically a defect. The audit explicitly distinguishes among:

- wrong or under-specified problems;
- inappropriate methods;
- implementation defects;
- insufficient validation;
- unsupported claims;
- limitations of a model or experimental design; and
- genuine negative scientific results.

Corrections are documented rather than hidden. Historical results that depend on a superseded numerical formulation are treated as provisional until rerun.

## Repository status

The detailed per-project audit documents currently live with their corresponding project repositories. This repository is the portfolio-level index and application-facing discussion guide.

Final per-project PDFs will be added only after outstanding verification and reruns are resolved, so that the documents do not freeze stale numerical conclusions.
