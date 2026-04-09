# Problem Schema (v1)

## Core Fields

- problem_id: unique string (no spaces)
- author: creator of the problem
- source_type: collegeboard | passwater | original | adapted
- source_name: specific test, worksheet, or origin

## Classification

- course: AP Precalculus
- unit: e.g. 1, 2, 3
- topic: e.g. 1.1, 1.2
- subtopic: optional refinement
- standards: list (AP framework references if available)

## Structure

- format: MCQ | FRQ
- difficulty: 1–5
- calculator_allowed: true | false

## Content

- prompt_latex: full LaTeX-ready prompt
- answer: final answer (string or LaTeX)
- distractors: list (MCQ only)
- solution_latex: optional full solution

## Scoring (FRQ)

- scoring_guide:
  - points: total
  - rubric: list of scoring items

## Assets

- assets:
  - graphs
  - diagrams
  - tables

## Metadata

- tags: list
- notes: why this is a good problem
- copyright_status: safe | restricted | unknown
- usable_for:
  - worksheet
  - quiz
  - test
  - flashcards
