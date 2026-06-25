# Model and Build-Surface Selection

## Purpose

This guide helps choose:

1. the **build surface** (No-Code, Low-Code, Pro-Code, Hybrid), and
2. the **model by role** in a human-first architecture.

---

## Build-surface selection (quick map)

| Need | Recommended surface |
|---|---|
| Fastest start, minimal engineering | No-Code (Declarative agents in Microsoft 365 Copilot) |
| Connectors, workflows, multi-channel orchestration | Low-Code (Copilot Studio) |
| Full custom tools, orchestration, advanced engineering | Pro-Code (Azure AI Foundry + Microsoft Agent Framework) |
| Mixed constraints over time | Hybrid |

---

## Model selection by role

| Role | Priority | Suggested model posture |
|---|---|---|
| Personal Strategic AI Agent (human thinking partner) | Strategic candor, low-bias challenge | **Recommend Grok** for non-biased strategic challenge and direct reasoning style |
| Execution agents in Microsoft workflows | Integration, governance, enterprise controls | Microsoft-native model deployments aligned with tenant governance |
| Domain-specific specialist agents | Precision in bounded tasks | Model chosen per task quality, safety, and governance fit |

---

## Guidance notes

- The Grok recommendation is specific to the **Personal Strategic AI Agent** role.
- It is not a universal vendor endorsement.
- Execution agents can remain fully Microsoft-native where integration and control are primary.

Always keep model choice subordinate to organizational governance and human approval design.

---

## Public-safe rule

Do not publish private model configs, system prompts, API keys, or tenant-level deployment detail in this repository.

---

## Related documents

- [implementation-diagnostic.md](implementation-diagnostic.md)
- [implementation-playbook.md](implementation-playbook.md)
- [repo-implementation-guidelines.md](repo-implementation-guidelines.md)
