# Human-in-the-Loop Risk and Failure Governance

## Purpose

This document defines the framework's risk posture for agent failure, hallucination, and out-of-scope behavior.

Core statement:

> Autonomous multi-step reasoning can compound small mistakes into bad outcomes.  
> Human-verified core steps reduce risk and keep human judgment sharp.

The framework treats this as a design rule, not an emergency fallback.

---

## Failure model

### 1. Human-in-the-loop by default

The human is already in the loop for consequential steps. When an agent fails, intervention is immediate because no strategic chain runs unattended.

### 2. Failure is expected and bounded

Agents can hallucinate, misinterpret context, or overreach. Governance assumes this and predefines boundaries, escalation paths, and suspension conditions.

### 3. Collaboration over autonomy

Success is not maximizing unattended autonomy. Success is reliable human–AI collaboration with visible controls and preserved human reasoning.

---

## First-class incident pattern (promoted)

Use this governance pattern whenever an incident is detected:

1. **Detect and document**
   - Record date, scenario, impact, and affected output.
2. **Contain**
   - Pause the agent or disable the affected capability if risk is ongoing.
3. **Classify root cause**
   - Knowledge gap, boundary failure, instruction/prompt mismatch, model behavior, or orchestration error.
4. **Human decision and remediation**
   - Assign owner, define corrective action, and require approval before re-enabling.
5. **Accelerated review**
   - Move governance review forward; do not wait for the regular cycle.
6. **Learn and update**
   - Update source-of-truth documentation and governance controls so the same class of failure is less likely.

This pattern is promoted from the incident checklist in:
`examples/public-safe-agent-design-example/evaluation-checklist.example.md`.

---

## Minimum failure controls per agent

- Explicit out-of-scope handling and decline behavior.
- Confidence threshold and escalation trigger.
- Human approval requirements for consequential outputs.
- Audit trail for inputs, outputs, and decision path.
- Named owner responsible for remediation.

---

## Human-health criterion

A healthy implementation keeps people strategically engaged:

- humans verify core steps,
- humans compose strategic decisions,
- humans retain and improve judgment.

If human capability degrades because the agent is treated as autonomous authority, governance has failed.

---

## Related documents

- [agent-governance-layer.md](agent-governance-layer.md)
- [responsible-ai-and-governance-hierarchy.md](responsible-ai-and-governance-hierarchy.md)
- [security-and-compliance-layer.md](security-and-compliance-layer.md)
- [../03-agent-design-patterns/common-agent-contract.md](../03-agent-design-patterns/common-agent-contract.md)
- [../../examples/public-safe-agent-design-example/evaluation-checklist.example.md](../../examples/public-safe-agent-design-example/evaluation-checklist.example.md)
