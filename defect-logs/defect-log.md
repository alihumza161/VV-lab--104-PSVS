# Requirements Defect Log — PSVS


| Defect ID | Req ID | Category | Description | Evidence | Severity | Suggested fix | Status |
|---|---|---|---|---|---|---|---|
| D01 | S1 | Ambiguity | Registration status and the meaning of a registered depositor are not defined. | “registered depositors” | Medium | Define registration criteria, approval authority, and active/inactive status. | Open |
| D02 | S2 | Vagueness | “Large number” is not a measurable capacity. | “a large number of boxes” | Medium | Replace with a numeric capacity or refer explicitly to S3. | Open |
| D03 | S3 | Incompleteness | Behavior when a chamber reaches capacity is not specified. | “hold at most 50,000 boxes” | High | Specify capacity checking and rejection or alternative-storage behavior. | Open |
| D04 | S4, S5 | Ambiguity / potential contradiction | Ownership-based withdrawal restriction and emergency release authority may conflict if emergency release bypasses depositor authorization. | S4 restricts withdrawal to the depositor; S5 permits release to any requesting party. | Critical | Define whether S5 is an explicit exception, who authorizes it, and how release is recorded. | Open |
| D05 | S5 | Ambiguity | Emergency conditions, authority role, and requester eligibility are undefined. | “In an emergency” / “any requesting party” | High | Define emergency criteria, authorized roles, requester checks, and approval steps. | Open |
| D06 | S6 | Vagueness | “Safe temperature” has no numeric range or conditions. | “a safe temperature” | Medium | Specify acceptable temperature range and monitoring conditions. | Open |
| D07 | S7, S8 | Potential contradiction | The absolute -18°C upper limit conflicts with warming to 0°C if both apply at the same time. | S7: “never rise above -18°C”; S8: “warmed to 0°C” | Critical | Define an authorized maintenance exception, duration, monitoring, and recovery requirements. | Open |
| D08 | S8 | Incompleteness | Maintenance warming duration and return-to-temperature requirements are missing. | “During maintenance, a chamber may be warmed to 0°C.” | High | Define maximum duration, authorization, cooling procedure, and recovery criteria. | Open |
| D09 | S9 | Non-verifiability | “Low viability” and “promptly” lack thresholds and time limits. | “low viability” / “promptly” | High | Define species-appropriate viability thresholds and maximum flagging delay. | Open |
| D10 | S10 | Ambiguity | The denominator for the 20% quota is unclear. | “20% of its boxes of a species per year” | High | Define the quota basis, annual period, and treatment of new deposits and redeposits. | Open |
| D11 | S10 | Incompleteness | Quota accumulation and enforcement behavior are not specified. | “per year” | High | Define counting rules, reset date, and rejection behavior when the limit is reached. | Open |
| D12 | S11 | Incompleteness | Re-inspection criteria, responsible role, and approval outcome are unspecified. | “only after re-inspection” | Medium | Define inspection checklist, authorized inspector, and pass/fail handling. | Open |
| D13 | S12 | Non-verifiability | “Good audit trail” has no measurable completeness, integrity, or retention criteria. | “a good audit trail” | Medium | Define required events/fields, retention, access control, and integrity protection. | Open |
| D14 | S6, S7 | Redundancy / overlap | General temperature safety overlaps the specific temperature limit, but S6 may cover requirements beyond the upper bound. | “safe temperature” / “never rise above -18°C” | Low | Clarify S6's additional scope or consolidate it with measurable temperature constraints. | Open |
| D15 | S9, S12 | Untraceability | A regeneration flag is not explicitly linked to the affected sample and audit record. | S9 requires flagging; S12 requires an audit trail, without a required link. | Medium | Require unique sample identifiers and links between flags, actions, and audit events. | Open |
| D16 | S7 | Infeasibility / robustness concern | An absolute “never” limit does not specify assumptions or fault handling for power, sensor, or equipment failure. | “shall never rise above -18°C” | High | Define monitoring, alarms, backup provisions, and fault-response requirements. | Open |
| D17 | S5 | Incompleteness | Post-release accountability and notification to the depositor are not addressed. | Emergency release has no stated review or notification process. | Medium | Define notification, approval evidence, and post-event review requirements. | Open |
| D18 | S10, S12 | Untraceability | The audit trail is not explicitly required to record quota calculations and decisions. | S10 sets a quota; S12 does not specify quota-related audit fields. | Medium | Record depositor, species, date, quantity, quota balance, and authorization for each withdrawal. | Open |

## Cross-Requirement Findings

| Finding | Requirements | Issue |
|---|---|---|
| D04 | S4 / S5 | Ownership restriction versus emergency release authority. |
| D07 | S7 / S8 | Normal temperature limit versus maintenance warming. |
| D14 | S6 / S7 | General safe-temperature wording overlaps a specific limit. |
| D15 | S9 / S12 | Missing explicit traceability between regeneration flags and audit records. |
| D18 | S10 / S12 | Missing explicit audit linkage for quota enforcement. |

