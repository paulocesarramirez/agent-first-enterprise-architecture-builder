# Human-Orchestrated Multi-Agent Pattern

## Purpose

This pattern defines how to run multi-agent systems with the **human as primary orchestrator**.

Core rule:

> Specialized agents solve bounded problems.  
> The human composes outputs, validates core steps, and owns the strategic chain.

This reduces compounding error risk from autonomous agent-to-agent hand-offs.

---

## Pattern summary

### Roles

- **Human orchestrator (primary):** sets objective, delegates bounded tasks, validates outputs, and decides next action.
- **Specialized agents (bounded):** perform focused diagnosis or production tasks within declared scope.
- **Execution surface (Copilot Cowork):** executes resulting knowledge work after human orchestration.

### Flow

1. Human defines the strategic task.
2. Human assigns bounded sub-tasks to specialized agents.
3. Agents return outputs with traceable sources and confidence signals.
4. Human reviews and composes a final plan.
5. Human triggers Cowork (or equivalent execution surface) to carry out work.
6. Human verifies consequential outputs.

---

## Inter-agent contract requirements

When more than one agent is involved, require:

- **Handoff schema:** expected input/output fields and confidence markers.
- **Boundary statement:** what each agent can and cannot decide.
- **Escalation trigger:** when an agent must defer to the human.
- **Audit pointer:** where each handoff is logged.

Agents may exchange structured outputs, but strategic chaining stays human-led.

---

## Agent registry (minimum fields)

Maintain a registry with:

- Agent name and owner
- Single responsibility
- Allowed knowledge sources
- Allowed actions
- Disallowed actions
- Required human approval points
- Handoff interfaces

This registry keeps multi-agent behavior legible and governable.

---

## Reusable demo mapping

The live pattern (Commercial Agent → PM Assistant / M365 Watcher) should be generalized as:

- **Diagnosis agents:** detect or analyze bounded sub-problems.
- **Planning agent(s):** structure options and operational implications.
- **Execution support agent(s):** prepare deliverables for Cowork execution.

Human orchestration remains the top control point.

---

## Related documents

- [common-agent-contract.md](common-agent-contract.md)
- [README.md](README.md)
- [../02-framework/human-in-the-loop-risk-and-failure-governance.md](../02-framework/human-in-the-loop-risk-and-failure-governance.md)
- [../05-copilot-implementation/implementation-playbook.md](../05-copilot-implementation/implementation-playbook.md)
