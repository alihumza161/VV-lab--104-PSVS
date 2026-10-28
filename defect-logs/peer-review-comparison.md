# Peer-Review Comparison — PSVS

## Review Details

| Field | Details |
|---|---|
| Author | [Your name] |
| Reviewer | [Classmate's name] |
| Review date | [YYYY-MM-DD] |
| Requirements inspected | S1-S12 |
| Author log | `defect-logs/defect-log.md` |

## Comparison Table

| Comparison ID | Requirement ID | Author Defect ID | Reviewer Defect ID | Finding | Classification |
|---|---|---|---|---|---|
| PR01 | [Sx] | [Dx or None] | [Dx or None] | [Describe finding] | [Shared / Author only / Reviewer only / Disputed] |
| PR02 | [Sx] | [Dx or None] | [Dx or None] | [Describe finding] | [Shared / Author only / Reviewer only / Disputed] |
| PR03 | [Sx] | [Dx or None] | [Dx or None] | [Describe finding] | [Shared / Author only / Reviewer only / Disputed] |

Add one row for each distinct finding in the union of both logs. Match findings by underlying issue, not just defect ID.

## Defects Missed by the Author

| Finding | Requirement ID | Reviewer's Evidence | Decision | Rationale |
|---|---|---|---|---|
| [Finding] | [Sx] | [Evidence] | [Accepted / Rejected] | [Reason] |

## Detection Rate

Let A be the set of distinct valid defects identified by the author and B be the set identified by the reviewer.

**Author detection rate = |A| / |A ∪ B| × 100%**

| Metric | Value |
|---|---:|
| Author's distinct valid defects, |A| | [Enter count] |
| Reviewer's distinct valid defects, |B| | [Enter count] |
| Shared defects, |A ∩ B| | [Enter count] |
| Union of distinct defects, |A ∪ B| | [Enter count] |
| Author detection rate | [Calculate]% |

Deduplicate matching findings before calculating the union. Do not invent reviewer results; complete this section after exchanging logs with a classmate.

## Conclusion
[Summarize findings missed, disputed classifications, and changes made after peer review.]
