# Problem Ingestion Workflow (v1)

## Goal
Convert any source problem into a standardized YAML file that matches problem-schema.md exactly.

---

## Rules (STRICT)

1. NEVER skip fields
2. NEVER rename fields
3. ALWAYS output valid YAML
4. If unknown → use null (not blank)
5. prompt_latex must be clean LaTeX (no plaintext formatting)
6. Do not invent math
7. Preserve original intent of the problem
8. Tag difficulty realistically (AP level)

---

## Output Format

You must output ONLY this format:

problem_id:
author:
source_type:
source_name:

course: AP Precalculus
unit:
topic:
subtopic:
standards:

format:
difficulty:
calculator_allowed:

prompt_latex: |

answer: |

distractors:

solution_latex: |

scoring_guide:

assets:

tags:

notes:

copyright_status:

usable_for:

---

## Instructions for Claude

When given a problem:

1. Classify it (unit, topic)
2. Convert prompt to LaTeX
3. Extract correct answer
4. Generate distractors if missing (MCQ only)
5. Assign difficulty (1–5)
6. Tag concepts
7. Add short note explaining why it's a good problem

---

## Important

- Prefer accuracy over completeness
- Do NOT rush classification
- If unsure → flag in notes
