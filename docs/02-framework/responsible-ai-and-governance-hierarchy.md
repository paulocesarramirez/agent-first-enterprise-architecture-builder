# Responsible AI and Governance Hierarchy

## Purpose

This document defines how Responsible AI is positioned in this framework.

Core rule:

> **Organization-authored governance is the top authority.**  
> **Platform Responsible AI controls are complementary, subordinate safety nets.**

This preserves human ownership of intent, boundaries, and accountability.

---

## Explicit hierarchy

1. **Organization documentation (primary authority)**
   - Human-authored principles, purpose, boundaries, approval rules.
2. **Framework governance implementation**
   - Knowledge Architecture + Agent Governance Layer operationalize those principles.
3. **Platform Responsible AI controls (subordinate)**
   - Microsoft Responsible AI, Azure AI Content Safety, and other platform guardrails enforce generic safety baselines.

Platform controls are necessary but not sufficient: they are generic and vendor-defined, while organizational governance is specific and human-owned.

---

## Why governance sits above platform RAI

- Organizational intent is contextual and strategic.
- Human accountability must remain local to the organization.
- Platform controls enforce broad safety classes but cannot encode each organization's mission-specific decision boundaries.

Therefore, this framework implements principles *above* platform RAI and uses platform RAI as reinforcement.

---

## Principle-to-control bridge (complementary model)

| Human-first principle | Framework behavior | Complementary platform control |
|---|---|---|
| AI proposes, humans decide | Human approval gates for consequential actions | Content safety and policy filtering for unsafe prompts/output |
| Single source of truth | Grounding only from approved knowledge sources | Data access controls, sensitivity labels, DLP |
| Controlled evolution | Human review for changes to guides, prompts, and scope | Audit logs, change history, policy monitoring |
| Transparency and auditability | Declared ownership, traceability, and escalation rules | Platform telemetry, audit records, and compliance logging |

---

## Public-safe wording rule

When describing Responsible AI in this repository, always state:

- governance originates in organization documentation,
- framework governance operationalizes it,
- platform RAI is subordinate reinforcement.

Never present platform RAI as the top layer of governance.

---

## Related documents

- [architecture-layers.md](architecture-layers.md)
- [agent-governance-layer.md](agent-governance-layer.md)
- [security-and-compliance-layer.md](security-and-compliance-layer.md)
- [human-in-the-loop-risk-and-failure-governance.md](human-in-the-loop-risk-and-failure-governance.md)
