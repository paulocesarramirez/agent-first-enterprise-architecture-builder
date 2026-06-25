# Value and Metrics Pattern

## Purpose

This document defines a public-safe pattern for measuring agent value in enterprise adoption.

The framework measures operational results **and** human strategic health.

---

## KPI categories

| KPI category | What to measure | Example public-safe metric |
|---|---|---|
| Time saved | Reduction in repetitive effort | `% reduction in preparation time for [YourProcess]` |
| Output quality | Better consistency and fewer corrections | `% outputs accepted without rework` |
| Adoption | Healthy usage by intended users | `% target users active weekly` |
| Deflection | Lower load on manual triage | `% routine requests handled before escalation` |
| Human strategic engagement (required) | Preservation of human reasoning role | `% consequential decisions with documented human verification` |

---

## Human-first success criterion

A "good" agent implementation must leave humans sharper, not more dependent.

Track at least one metric that confirms:

- humans still verify core steps,
- humans still own strategic decisions,
- humans are not bypassed in consequential workflows.

---

## Measurement cadence

- **Weekly:** usage/adoption and operational health.
- **Monthly:** value trend (time, quality, deflection).
- **Quarterly:** governance and human-engagement review.

Use trend comparisons rather than one-time snapshots.

---

## Public-safe reporting format

Use placeholders and non-sensitive aggregates:

- `[YourOrg] Agent Value Report — [Month/Quarter]`
- `%` deltas and counts without private client or employee data
- narrative lessons learned without exposing confidential workflows

---

## Related documents

- [human-in-the-loop-risk-and-failure-governance.md](human-in-the-loop-risk-and-failure-governance.md)
- [agent-governance-layer.md](agent-governance-layer.md)
- [../05-copilot-implementation/implementation-playbook.md](../05-copilot-implementation/implementation-playbook.md)
