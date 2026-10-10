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

## New projects — 10 October 2026 (status supplement)

The original **7 October 2026 PDF remains an unchanged historical snapshot**. The following projects are additional portfolio entries, not retroactive amendments to its scientific-audit findings. Their status must not be interpreted as equivalent to the audited projects in that PDF.

| Project | Focus | Current evidence / qualification | Discussion status |
| --- | --- | --- | --- |
| [Research & Innovation Monitor](https://github.com/AdebanjiAdelowo/research-innovation-monitor) | Scientific literature retrieval, grounded generation, topic/trend analytics, agents | Reported: 115 offline tests; local comparisons on LitSearch, SciFact, SCIDOCS and DAPFAM; important negative results for small-model reranking/decomposition and RAG abstention. Larger GPU experiments are pending. Verify repository visibility/access and the benchmark-text Git-history audit before treating its linked results as published. | **DISCUSS WITH QUALIFICATION** — reported local results, independent audit pending. |
| Micro-Doppler Multimodal Intelligence | Radar signal processing, time-frequency classification, sensor fusion | Parallel project under development; availability of paired multimodal data, independent splits and validated results not yet established here. | **AUDIT PENDING** |
| Multimodal Visual RAG | Visual/document retrieval, OCR, image-language evidence grounding | Parallel project under development; benchmark selection, retrieval evaluation and grounded-generation results not yet established here. | **AUDIT PENDING** |
| Legal Research RAG | Case-law retrieval, citation verification and grounded summarization | Parallel project under development; jurisdiction, dataset licensing, temporal evaluation and citation accuracy require verification. | **AUDIT PENDING** |
| Electricity Demand Forecasting | Statistical/deep-learning forecasting, calibrated intervals, anomaly analysis | Parallel project under development; temporal backtests, leakage checks and forecast-vs-baseline comparisons remain to be verified. | **AUDIT PENDING** |
| Bus Scheduling & Route Optimization | Public-transport demand modelling, mathematical optimization, robust scheduling | Parallel project under development; passenger-demand provenance, feasibility checks and held-out scenario evaluation remain to be verified. | **AUDIT PENDING** |

**Source/status caution:** This supplement records the development status described in the working project discussions as of 10 October 2026, not a completed independent audit of the five parallel repositories. URLs are included only where a repository name is known; no claim is made that a link is publicly accessible. Before a PhD application, update each row from its actual tests, numerical results, limitations and public GitHub URL.
