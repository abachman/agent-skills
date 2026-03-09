---
title: "Adaptive Prompting in Middle-School Algebra Tutors"
authors: "Lee, A.; Gomez, T.; Rathi, N."
year: 2024
venue: "Journal of Learning Analytics"
source_type: "pdf"
source_ref: "<local-pdf-path>"
triage_label: "Read deeply"
confidence: "high"
domains: [educational-data-mining, learning-research]
methods: [quasi-experimental, log-analysis, hierarchical-modeling]
status: "processed"
---

# 2024 - Lee - Adaptive Prompting in Middle-School Algebra Tutors

## TL;DR

- Quasi-experimental classroom study found adaptive hint sequencing improved problem completion and reduced time-on-task versus static hints.
- Methods are reusable for product experimentation because logging schema, model features, and outcome definitions are explicit.

## Research Question

- Do adaptive hint policies improve algebra learning process outcomes relative to static hints in authentic classroom usage?

## Study Design

- Design type: Quasi-experimental, two-condition comparison across matched classrooms.
- Unit of analysis: student-problem attempt.
- Comparison/baseline: static hint condition.

## Population & Context

- Participants: Grade 7 learners in public schools.
- Setting: In-class tutoring platform use across 6 weeks.
- Sample size: 418 students, 31,204 attempts.

## Variables & Operationalization

- Independent variables: hint policy (adaptive vs static), prior proficiency covariates.
- Dependent variables: completion rate, median solve time, delayed quiz score.
- Key constructs: productive struggle operationalized as retries before success.

## Measures & Instruments

- Instruments/measures used: platform telemetry + delayed quiz.
- Reliability/validity evidence: quiz internal consistency reported (alpha = 0.82).
- Notes: delayed quiz form described in appendix.

## Analysis Pipeline

- Preprocessing: removed malformed events and merged contiguous idle periods.
- Statistical/modeling approach: hierarchical mixed-effects regression with class-level random intercepts.
- Evaluation strategy: condition effect estimates with confidence intervals.

## Threats to Validity

- Internal validity: non-random class assignment; authors include matching and covariate controls.
- External validity: only algebra context and one platform.
- Measurement validity: productive struggle proxy may miss off-platform support.

## Replicability Signals

- Protocol detail: high; logging schema and feature definitions are explicit.
- Data/code/materials availability: analysis code and schema shared.
- Missing details (`Not reported`): full teacher implementation fidelity checklist.

## Method Reuse Potential

- Reusable now: telemetry feature definitions and mixed-effects model structure.
- Requires adaptation: hint taxonomy mapping for other subjects.
- Avoid or caution: transfer claims to non-tutor settings.

## Comparison Hooks

- Compare against: randomized tutor studies with similar outcomes.
- Contradictions/tensions to watch: whether faster solve time reflects shallower learning.

## Evidence Table

| Claim | Evidence | Pointer |
| --- | --- | --- |
| Unit of analysis is student-problem attempt | "We model each student-problem interaction as one observation." | p. 6 |
| Non-random assignment handled with matching + covariates | "Classrooms were matched on prior achievement... models include prior score and school indicators." | p. 7 |
| Quiz reliability is reported | "The delayed transfer quiz showed acceptable reliability (alpha = .82)." | p. 9 |
| Code and schema are available | "Analysis scripts and event schema are available in the public repository." | p. 14 |

## Extraction Warnings

- None.

## Tags

- #paper
- #methods
- #educational-data-mining
- #learning-research
- #quasi-experimental
