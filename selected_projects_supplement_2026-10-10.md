# Selected Projects — Research and AI Supplement (10 October 2026)

This is an **addendum**, not a replacement for the [scientific audit PDF dated 7 October 2026](selected_projects_phd_discussion_status_2026-10-07.pdf). It records additional projects under development and does **not** imply they have undergone the same full scientific audit as the original portfolio entries.

## Project additions

| Project | Research contribution / evaluation focus | Evidence and audit status |
| --- | --- | --- |
| Research & Innovation Monitor | Hybrid scholarly/patent retrieval, reranking, grounded generation, query decomposition, quantitative trend analysis. | **DISCUSS WITH QUALIFICATION** — reported 115 passing offline tests and local benchmark runs; negative reranker, decomposition and abstention findings should be retained. GPU ablations pending. Benchmark-text history rewrite/publication verification was still outstanding in the latest report. |
| Micro-Doppler Multimodal Intelligence | Radar STFT, spectrogram classification, noise robustness, subject/session-independent generalization, optional truly paired sensor fusion. | **AUDIT PENDING** — research/implementation initiated in parallel; final dataset, evaluation and outcomes not yet verified. |
| Multimodal Visual RAG | OCR versus vision retrieval, visual evidence selection, source-grounded multimodal answers, citation/abstention evaluation. | **AUDIT PENDING** — no independently verified results supplied. |
| Legal Research RAG | Jurisdiction-aware case retrieval, legal-domain embedding baselines, citation verification, temporal validity. | **AUDIT PENDING** — benchmark license, evaluation and results unverified. |
| Electricity Demand Forecasting | Statistical and neural baselines, leakage-free rolling backtests, probabilistic forecasting, anomalies. | **AUDIT PENDING** — no independently verified forecast results supplied. |
| Bus Scheduling & Route Optimization | Passenger demand prediction, constrained fleet/schedule optimization, scenario-based robustness and simulation. | **AUDIT PENDING** — data and optimizer validation still to be established. |

## PhD discussion guidance

Emphasize the already verified numerical-PDE / scientific-ML projects from the 7 October PDF. Discuss Research & Innovation Monitor as a complementary information-retrieval and reproducible-experiment project, qualifying the local 3B-model scale and pending GPU results. Do not claim numerical results for the five parallel projects until their own audit documents establish them.

## Publication checks

Before replacing this interim supplement with formal scientific-audit status, check each project's exact repository URL, public availability, implemented features, executable tests, provenance, dataset restrictions, metrics, confidence intervals, failure modes and known scientific limitations. Never promote *AUDIT PENDING* solely because code exists.
