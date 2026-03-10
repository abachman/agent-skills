---
name: triaging-methods-papers
description: Quickly triages and summarizes research papers for methods-building in educational psychology, EDM, HCI, cognitive science, and learning research. Use when given a PDF path, DOI, or URL and the goal is building a personal knowledge base with strict evidence grounding.
---

# Triaging Methods Papers

## Overview

Use this skill to rapidly extract method-relevant knowledge from papers and generate durable Obsidian notes.

Primary goal: methods-building for a personal knowledge base.

## Defaults

- Output directory: `Papers/`
- Filename format: `YYYY - FirstAuthor - Short Title.md`
- Triage labels: `Read deeply`, `Read selectively`, `Skim`, `Archive`
- Evidence strictness: major claims must include quote + page (PDF) or section (DOI/URL)
- Missing info policy: use `Not reported` (never infer)

## Input Types

- PDF path (local file)
- DOI
- URL to paper or full text

Normalize all inputs into one extraction object:

- title
- authors
- year
- venue
- abstract
- sections (if available)
- citations for evidence pointers

## Workflow

1. Confirm the task uses a methods-building lens (default for this skill).
2. Ingest paper from PDF, DOI, or URL.
3. Run quick triage using `references/methods-rubric.md`.
4. Extract methods-first details using `references/domain-lenses.md`.
5. Draft note with `templates/paper-method-note.md`.
6. Verify grounding:
   - Every major methods claim has evidence pointer.
   - Any unknown details are `Not reported`.
7. Save note to `Papers/` using `YYYY - FirstAuthor - Short Title.md`.
8. If filename collision occurs, append a short suffix: `... - a.md`, `... - b.md`.

## Triage Rubric

Use weighted judgment (not strict math unless requested):

- Method transferability
- Internal validity quality
- Measurement quality and operationalization clarity
- Replicability signals
- Context portability

Return one label:

- `Read deeply`: high methods reuse + strong trust signals
- `Read selectively`: useful method ideas with moderate limitations
- `Skim`: low reuse or narrow context fit
- `Archive`: weak relevance for current methods-building goals

## Required Output

Always produce a structured markdown note following `templates/paper-method-note.md`.

Include these sections at minimum:

- TL;DR
- Research Question
- Study Design
- Population & Context
- Variables & Operationalization
- Measures & Instruments
- Analysis Pipeline
- Threats to Validity
- Replicability Signals
- Method Reuse Potential
- Comparison Hooks
- Evidence Table
- Triage Label
- Tags

## Grounding Rules

- No free-floating claims.
- Evidence table must map claim -> source pointer.
- Source pointer format:
  - PDF: `p. X` or `pp. X-Y`
  - Web text: `Section: <heading>`
- If extraction is uncertain due to scan/OCR quality, add an `Extraction Warnings` section.

## Domain Scope

Prioritize these fields:

- educational psychology
- educational data mining
- human-computer interaction
- cognitive science
- learning research / learning sciences

Use domain-specific prompts from `references/domain-lenses.md`.

## Output Location Constraint

Generated notes belong in `Papers/` only. Do not nest beyond one level in the vault.

## Examples

- Strong note: `examples/good-note.md`
- Weak note anti-pattern: `examples/weak-note.md`
