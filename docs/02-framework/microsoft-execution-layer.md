# Microsoft Execution Layer

## Purpose

This document expands **Layer 4** of the
**Agent-First Enterprise Architecture Builder** framework: the **Execution Layer**, with a focus on its implementation across Microsoft technologies.

This is where the architecture **becomes action** — the environment where users, agents, workflows, and knowledge interact in practice.

This document is public-safe and intended for learning, adaptation, and implementation guidance.

---

## Why this layer comes last

Execution comes last by design. The tools an organization uses are powerful, but they are not the starting point.

> The tools do not define the organization.
> The architecture defines how the tools should be used.

When execution is chosen first, organizations tend to bend their logic to fit the tool. In this framework, the tool serves capability that was generated from governed architecture — not the other way around.

---

## Why Microsoft

This framework is especially well-suited to a Microsoft environment because the same ecosystem spans the full agent journey:

- a productivity surface where people already work (Microsoft 365)
- a low-code orchestration surface (Copilot Studio)
- a pro-code platform for custom agents (Azure AI Foundry + Microsoft Agent Framework)
- composable knowledge grounding (the "IQ" layers)

This lets governed architecture run where work actually happens, without forcing people into a separate tool.

---

## Execution environments

The Execution Layer may include:

| Environment | Role in execution |
|-------------|-------------------|
| **SharePoint** | Document and knowledge surfaces where content lives |
| **Teams** | Where collaboration and agent interaction happen |
| **Planner** | Where tasks and work are tracked |
| **Outlook** | Where communication and signals flow |
| **Microsoft 365 Copilot** | Where agents assist users in context |
| Other governed environments | Additional tools used under the same architecture |

The specific mix depends on the organization. What stays constant is that every environment operates under the governance defined upstream.

---

## How agents are built and run

The same governed architecture can be executed through agents at three levels of sophistication. The organization chooses per use case.

| Build approach | Platform | Runs as |
|----------------|----------|---------|
| **Declarative agents** | Microsoft 365 Copilot | Lightweight agents grounded in M365 content |
| **Low-code agents** | Copilot Studio | Orchestrated agents composing multiple IQ layers |
| **Pro-code agents** | Azure AI Foundry + Microsoft Agent Framework | Fully custom agents with advanced control and tools |

### Grounding in execution

Agents are grounded through the **IQ** layers selected for the use case:

- **Work IQ** — Microsoft 365 work content and signals
- **Web IQ** — public web knowledge
- **Foundry IQ** — knowledge curated via Azure AI Foundry
- **Fabric IQ** — enterprise data modeled in Microsoft Fabric

> The reference implementation at EmprendHEC runs agents grounded primarily in **Work IQ** and **Web IQ**, and the framework extends to **Foundry IQ** and **Fabric IQ** as needs require.

---

## What execution must preserve

Running in real tools does not relax governance. The Execution Layer must preserve everything defined upstream:

- **Grounding** — agents read from the source of truth
- **Boundaries** — agents stay within their declared scope
- **Human oversight** — people remain in the critical path for consequential decisions
- **Auditability** — actions and outputs remain traceable
- **Controlled evolution** — changes happen through human-approved updates

A more capable execution environment never means weaker governance.

---

## What this layer does *not* do

- It does not define the knowledge — that is the [Knowledge Architecture Layer](knowledge-architecture.md).
- It does not set the rules of conduct — that is the [Agent Governance Layer](agent-governance-layer.md).
- It does not design the capability — that is the [Capability Generation Layer](generation-layer.md).

This layer **runs** capability that has already been governed and generated.

---

## Relationship to the other layers

**Knowledge Architecture** (defines truth)
→ **Agent Governance** (protects coherence)
→ **Capability Generation** (enables operational design)
→ **Execution** (runs the system in practice) ← *this layer*

Execution is the visible end of a deliberate chain. By the time work reaches a Microsoft tool, it is already grounded, bounded, and approved.

---

## Human-centered interpretation

This layer keeps **human judgment above uncontrolled automation**, even inside highly capable tools. Agents accelerate and assist within the environments people already use; humans keep deciding what matters.

Infrastructure becomes more agentic here; **purpose and direction remain human.** This is **Agent-First Infrastructure, Human-First Purpose** at the point of execution.

---

## Public vs private application

This repository shares the public **pattern** for execution.

A private implementation may include:

- real connector and integration configuration
- tenant IDs, endpoints, credentials, and secrets
- production agent prompts and access rules
- live operational content inside the tools

Those private details must never appear in the public repo. The public repo shares the **execution pattern**, not the operational environment.

See [`../01-principles/public-repo-boundary.md`](../01-principles/public-repo-boundary.md).

---

## Final summary

The Microsoft Execution Layer:

1. Is where architecture **becomes action** in real tools
2. Spans SharePoint, Teams, Planner, Outlook, and Microsoft 365 Copilot
3. Runs agents as **declarative, low-code, or pro-code**, grounded through the **IQ** layers
4. **Preserves** grounding, boundaries, oversight, auditability, and controlled evolution

Architecture comes first. Execution comes last — and runs under everything defined before it.

---

## Related documents

- [`architecture-layers.md`](architecture-layers.md) — The full four-layer model
- [`knowledge-architecture.md`](knowledge-architecture.md) — The source of truth executed here
- [`agent-governance-layer.md`](agent-governance-layer.md) — The governance execution must preserve
- [`generation-layer.md`](generation-layer.md) — Where the executed capability is designed
- [`../06-faq/how-this-relates-to-microsoft-365.md`](../06-faq/how-this-relates-to-microsoft-365.md) — How the framework relates to Microsoft 365
