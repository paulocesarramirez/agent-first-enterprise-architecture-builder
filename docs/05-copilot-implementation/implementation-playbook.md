# Implementation Playbook

## Purpose

This is the **second step** of "I want this implemented for my company." Once the [implementation-diagnostic.md](implementation-diagnostic.md) has produced a recommended **path** (No-Code, Low-Code, Pro-Code, or Hybrid), this playbook turns that path into **concrete, ordered steps** — always using **this repository as the source of truth**.

> The framework is the reusable layer. **You** supply your own knowledge, governance, and execution context. Copilot helps you assemble it, in detail, on the surface that fits your stack.

---

## How to use this with Copilot

Tell Copilot:

> _"Use this repository as the reference framework. My recommended path is **[path]**. Walk me through the playbook step by step, adapting each step to my organization."_

Copilot should then:
1. Follow **Part 1 (Universal foundation)** — the same for every path.
2. Follow the **path-specific track** in **Part 2**.
3. Apply the **public/private boundary** at every step (see [safe-scaffolding-instructions.md](safe-scaffolding-instructions.md)).

---

## The mental model

You are reproducing the framework's four layers in **your** environment:

```
Knowledge  →  Governance  →  Capability Generation  →  Execution
(source of    (shared agent   (build your    (run inside
 truth in      contract)       agents)        Microsoft 365)
 SharePoint)
```

The repository gives you the **patterns and templates** for each layer. The path you chose only changes **how you build the Capability Generation layer** (the agents themselves). Layers 1, 2, and 4 are largely the same across paths.

---

## Part 1 — Universal foundation (all paths)

Do these first, regardless of path. They are what made the EmprendHEC demo work.

### Step 1 — Establish the Knowledge layer (your source of truth)

Goal: a single, structured knowledge base your agents can consult.

1. Create a SharePoint site for your architecture (e.g., *"[YourOrg] - Information Architecture"*).
2. Recreate the public-safe structure from the demo:
   - a **README** explaining what does and does not belong in the library
   - a **Guides** area (operational guides per business area)
   - an **Agents** area (shared agent contract + one subfolder per agent)
   - a place for recurring **reports/monitoring**
3. Write your guides using [guide-template.md](guide-template.md).
4. Follow [naming-conventions.md](naming-conventions.md) for files and folders.

Reference: [../02-framework/knowledge-architecture.md](../02-framework/knowledge-architecture.md) and [../01-principles/source-of-truth.md](../01-principles/source-of-truth.md).

> ✅ Outcome: a clean, authoritative knowledge base — even before any agent exists.

### Step 2 — Establish the Governance layer (the shared agent contract)

Goal: every agent inherits the same principles and boundaries.

1. Adopt the common agent contract: shared principles, an interaction contract, and conventions.
2. Define your non-negotiables: human approval, single source of truth, transparency, controlled evolution.

Reference: [../03-agent-design-patterns/common-agent-contract.md](../03-agent-design-patterns/common-agent-contract.md) and [../02-framework/agent-governance-layer.md](../02-framework/agent-governance-layer.md).

> ✅ Outcome: a governance baseline that applies to every agent you will build.

### Step 3 — Design your first agent (on paper, before building)

Goal: a clear, public-safe design before touching any tool.

1. Pick the area from your diagnostic (e.g., commercial, projects, editorial).
2. Write an agent design document using [agent-design-template.md](agent-design-template.md).
3. Declare the **single responsibility**, governing sources, inputs/outputs, boundaries, autonomy level, and human-oversight points.
4. Study a worked example: [../03-agent-design-patterns/commercial-agent-example.md](../03-agent-design-patterns/commercial-agent-example.md).

> ✅ Outcome: a design doc that any of the three build surfaces can implement.

Now continue to **Part 2** for your path.

---

## Part 2 — Path-specific build (the Capability Generation layer)

### 🟢 No-Code track — Declarative agents

Best when: you have Microsoft 365 Copilot + SharePoint and want the fastest, lowest-risk start.

1. Confirm prerequisites: Microsoft 365 Copilot license; your Knowledge layer lives in SharePoint.
2. Open the **agent builder in Microsoft 365 Copilot** (Copilot → create agent).
3. Configure the agent from your Step 3 design:
   - **Name & description** — from the design doc
   - **Instructions** — translate the design's purpose, single responsibility, and boundaries into the instruction field
   - **Knowledge** — point it at the specific SharePoint sites/folders that are its governing sources
   - **Starter prompts** — a few from your design's expected use cases
4. Test against the design's use cases; verify it stays in scope and defers to humans.
5. Publish to the people who need it.

> Keep instructions public-safe in the repo; the live instruction content stays in your tenant.

### 🟡 Low-Code track — Microsoft Copilot Studio

Best when: you need custom actions, connectors, automation, or multiple channels.

1. Confirm prerequisites: Copilot Studio license + Power Platform environment.
2. Create a new agent in **Copilot Studio**.
3. Ground it with **Knowledge sources** pointing at your SharePoint source of truth.
4. Implement behavior from your design:
   - **Topics** for structured conversations
   - **Actions / connectors** (Power Platform, Power Automate) for the inputs/outputs in the design
   - **Guardrails** matching the design's boundaries and autonomy level
5. Add human-in-the-loop approval steps where the design requires oversight.
6. Test, then publish to your chosen channels (Teams, web, etc.).

Reference: [../02-framework/generation-layer.md](../02-framework/generation-layer.md).

### 🔵 Pro-Code track — Azure AI Foundry + Microsoft Agent Framework

Best when: you need full control, custom orchestration, advanced tools/models, or multi-agent systems.

1. Confirm prerequisites: Azure subscription, Azure AI Foundry access, developers.
2. In **Azure AI Foundry**, set up your project and choose your model deployment.
3. Build the agent with the **Microsoft Agent Framework**:
   - Encode the design's **single responsibility** and **boundaries** as system instructions and policy
   - Wire **tools/functions** for the design's inputs/outputs
   - Implement **grounding/retrieval** against your source of truth (e.g., your knowledge index)
   - Add **human-approval gates** for steps the design marks as oversight-required
4. Add tracing/evaluation so outputs are auditable (a governance requirement).
5. Deploy and integrate into your Microsoft 365 execution surfaces.

> Keep prompts, keys, endpoints, and tenant detail **out** of any public repo. The public layer is the design and the pattern, never the live configuration.

### 🟣 Hybrid track — start simple, extend where needed

Best when: you want to move now and grow later, or licensing differs across teams.

A common, healthy progression:
1. **Now:** stand up the Knowledge + Governance layers (Part 1) and ship a **No-Code** agent for your first area.
2. **Next:** when you hit a need for automation or connectors, rebuild or extend that agent in **Low-Code** (Copilot Studio).
3. **Later:** for advanced orchestration or multi-agent scenarios, implement specific agents in **Pro-Code** (Azure AI Foundry + Microsoft Agent Framework).

Because every agent shares the same design doc and governance contract, you can **change the build surface without changing the architecture.**

---

## Part 3 — Execution & governance (all paths)

Regardless of path, finish here.

### Step 4 — Wire the Execution layer

Put the agent to work inside your existing Microsoft 365 environment:
- **SharePoint** — documents and system of record
- **Teams** — where people invoke and collaborate with the agent
- **Planner / Outlook** — tasks and communication

Reference: [../02-framework/microsoft-execution-layer.md](../02-framework/microsoft-execution-layer.md).

### Step 5 — Operate under governance

- **AI proposes, humans decide** — keep approval where your design requires it.
- **Single source of truth** — agents read from the knowledge base, not parallel undocumented knowledge.
- **Controlled evolution** — changes to guides/prompts go through review; no hidden drift.

Reference: [../01-principles/governance-and-evolution.md](../01-principles/governance-and-evolution.md).

### Step 5.5 — Observability and evaluation (all paths, required)

Observability is a governance requirement for **No-Code, Low-Code, and Pro-Code** alike.

- Define a minimum telemetry set: requests, outputs, escalations, human approvals, and incidents.
- Keep audit logs for governance review and incident response.
- Run continuous evaluation against quality, scope integrity, and human-oversight compliance.
- Use the same evaluation posture across every build surface.

### Step 5.6 — Cost and licensing governance

Before scaling, validate cost fit for your chosen path:

- **M365 Copilot per-seat** (predictable seat-based productivity use)
- **Copilot Studio message capacity** (conversation/action volume sensitivity)
- **Azure consumption** (pro-code flexibility with variable usage cost)

Revisit path selection if capability fit and budget fit diverge.

### Step 6 — Expand the ecosystem

Repeat Steps 3 → 5 for the next area (projects, editorial, finance, legal). Each new agent reuses the same knowledge base and governance contract — this is how the system scales coherently.

---

## Definition of done

You have implemented the framework when:

- [ ] A structured **source of truth** exists in SharePoint, written with the repo's templates and conventions.
- [ ] A **shared governance contract** applies to every agent.
- [ ] At least one **agent design doc** exists and is implemented on your chosen surface.
- [ ] The agent runs inside **Microsoft 365** with **human oversight** where the design requires it.
- [ ] Nothing confidential (prompts, keys, client data) has leaked into any public repo.

---

## Related documents

- [implementation-diagnostic.md](implementation-diagnostic.md) — choose your path first
- [repo-implementation-guidelines.md](repo-implementation-guidelines.md) — the overall entry point
- [safe-scaffolding-instructions.md](safe-scaffolding-instructions.md) — how to keep everything public-safe
- [naming-conventions.md](naming-conventions.md) — file and folder naming
- [model-and-build-surface-selection.md](model-and-build-surface-selection.md) — model and surface guidance
- [../02-framework/value-and-metrics.md](../02-framework/value-and-metrics.md) — value measurement pattern
- [../00-overview/architecture-overview.md](../00-overview/architecture-overview.md) — the layered model
