# Defect Taxonomy — PSVS

## Purpose
This taxonomy supports consistent inspection of informal requirements S1-S12.

| ID | Category | Definition | Example from PSVS |
|---|---|---|---|
| T01 | Ambiguity | A requirement permits two or more reasonable interpretations. | S5 does not define what qualifies as an emergency or a valid requesting party. |
| T02 | Vagueness | A requirement uses imprecise wording without measurable thresholds. | S2 says a chamber holds a “large number” of boxes. |
| T03 | Incompleteness | Necessary information or an operating condition is missing. | S9 does not define a viability threshold or the deadline for flagging. |
| T04 | Contradiction | Requirements impose conflicting obligations under the same conditions. | S7's absolute limit conflicts with S8 if maintenance warming is not an explicit exception. |
| T05 | Non-verifiability | Compliance cannot be objectively checked using defined criteria. | S12 says “good audit trail” without measurable acceptance criteria. |
| T06 | Redundancy | A requirement duplicates or overlaps another without adding a distinct obligation. | S6's general temperature safety overlaps S7's specific temperature limit, though S6 may have broader intent. |
| T07 | Infeasibility | A requirement may be impractical or impossible under stated conditions and assumptions. | S7's “never” guarantee does not specify treatment of sensor failure, power loss, or equipment malfunction. |
| T08 | Untraceability | A requirement or action lacks a defined link to related artifacts or evidence. | S9 does not require a traceable link from a viability flag to the sample and regeneration action. |

## Inspection Method
Inspect each requirement for clarity, completeness, consistency, feasibility, measurability, and traceability. Inspect related requirements together, particularly S4/S5, S6/S7, S7/S8, and S9/S12.

## Classification Rules
1. Give each distinct finding a unique defect ID.
2. Record all affected requirement IDs.
3. Include exact wording as evidence.
4. Use cross-requirement IDs when the issue depends on more than one requirement.
5. Avoid counting the same underlying issue more than once unless the corrective actions are genuinely independent.
6. Treat severity as a preliminary risk judgment and justify it.

## Severity Scale

| Severity | Definition |
|---|---|
| Critical | Could undermine ownership controls, emergency authorization, or a fundamental seed-preservation constraint. |
| High | Could cause significant operational, compliance, or seed-preservation failure. |
| Medium | Creates material uncertainty that must be resolved for implementation or verification. |
| Low | Limited impact, such as avoidable overlap or documentation inefficiency. |
