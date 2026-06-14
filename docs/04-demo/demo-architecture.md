# Demo Architecture

## What Is Being Demonstrated

This demo is a **public-safe view of the live EmprendHEC ecosystem** — the real-world reference implementation of the four-layer, agent-first framework described in this repository. It shows how the layers operate as one integrated system, not as isolated components.

The view here is **structural**: site organization, folder structure, agent names, and how each artifact maps to a framework layer. It deliberately stops at the boundary of confidential operational detail (actual prompts, business rules, pricing, client data).

> The demo is **one private implementation example** of the public framework. The screenshots in [`Screenshots/`](Screenshots/) and in [`../00-overview/public-demo-scope.md`](../00-overview/public-demo-scope.md) illustrate the approach; they are not a release of the private operational system.

See [`what-is-public-vs-private.md`](what-is-public-vs-private.md) for the exact boundary.

---

## The Demo Organization

- **Name:** EmprendHEC ([www.emprendhec.com](https://www.emprendhec.com))
- **Type:** Education- and entrepreneurship-focused initiative
- **Mission:** Transform leaders, education, and communities through AI with purpose
- **M365 footprint:** SharePoint, Teams, Planner, Outlook, Microsoft Loop, Copilot Notebooks, Forms, Excel, Word, Microsoft 365 Copilot
- **Workspace:** A private Microsoft 365 group hosting the SharePoint site *"EmprendHEC - Arquitectura Información"*

EmprendHEC operates its internal work through a shared, governed agent ecosystem grounded in a single source of truth.

---

## Architecture in the Demo

Each framework layer maps to concrete, public-safe artifacts in the live environment.

```
EmprendHEC Agent-First Architecture

Layer 1: Knowledge  — SharePoint site "EmprendHEC - Arquitectura Información"
├── README — Arquitectura Información y Agentes EmprendHEC   (library usage guide)
├── Guías por área/                                          (operational guides per area)
│   ├── Guía Operativa EmprendHEC Comercial
│   ├── Guía Operativa EmprendHEC de Proyectos e Información
│   ├── Guía Operativa EmprendHEC Editorial
│   ├── Manual de Identidad EmprendHEC
│   ├── Guía de Marca EmprendHEC (Agent-Ready)
│   └── Plantillas Oficiales/                                (official base templates)
├── Agentes/                                                 (agent architecture + per-agent design)
└── Reportes Mensuales Monitoreo M365/                       (monthly M365 monitoring reports)

Layer 2: Governance — shared agent contract (in Agentes/)
├── 00-Arquitectura-Agentes-EmprendHEC         (Level 0 architecture)
├── 01-Principios-Comunes-Agentes-EmprendHEC   (common principles)
├── 02-Contrato-Interaccion-Agentes-EmprendHEC (interaction contract)
├── 03-Convenciones-Agentes-y-Guías-EmprendHEC (naming & structure conventions)
└── 04-Guia-de-Marca-EmprendHEC                (brand source of truth for agents)

Layer 3: Generation — Microsoft 365 Copilot agents
├── One "Diseño de Agente" design doc per agent, grounded in Layers 1 & 2
└── Agents published and run from the M365 Copilot Agent Store

Layer 4: Execution — Microsoft 365
├── SharePoint  (document operations + system of record)
├── Teams       (communication & execution surface)
├── Planner     (task & action management)
├── Outlook     (email & personal control)
├── Microsoft Loop / Copilot Notebooks (shared reasoning & drafting)
└── Forms · Excel · Word (capture, tariffs, official templates)
```

---

## Agents in the Demo

The live ecosystem runs a shared set of governed agents, each published in the Microsoft 365 Copilot Agent Store and grounded in the same source of truth.

| Agent | Purpose | Generation (Layer 3) | Execution (Layer 4) | Status |
|-------|---------|----------------------|---------------------|--------|
| PM Assistant | Project and information coordination | M365 Copilot agent | Planner + SharePoint | Active |
| M365 Watcher | Microsoft 365 monitoring & monthly reporting | M365 Copilot agent | Microsoft Graph + SharePoint | Active |
| Commercial Agent (Agente Comercial) | Prospect qualification, proposals, and close with purpose | M365 Copilot agent | SharePoint + Outlook + Teams | Active |
| Editorial Assistant | Content review against brand voice & style | M365 Copilot agent | SharePoint | Active |
| Accountant Agent (Agente Contable) | Finance-area assistance | M365 Copilot agent | M365 | Expansion |
| Legal Agent (Agente Legal) | Legal-area assistance | M365 Copilot agent | M365 | Expansion |

> Each agent enforces **single responsibility**: it operates only within its defined scope, consults the institutional sources before acting, and defers to human judgment on strategic decisions. For example, the Commercial Agent qualifies and proposes but never confirms prices, discounts, or dates outside what is documented — and it delegates Microsoft 365 questions to the PM Assistant and the M365 Watcher report.

---

## How an Agent Is Designed (Layer 3 detail)

Every agent in the demo is defined by a public-safe **agent design document** with a consistent structure, mirroring the [common agent contract](../03-agent-design-patterns/common-agent-contract.md):

1. **Resumen ejecutivo** — what the agent does and the role boundary it preserves
2. **Prompt de Instrucciones** (system instructions) — *private implementation detail*
3. **Knowledge (fuentes)** — which institutional sources it must consult (mandatory vs. optional)
4. **Parámetros y límites** — autonomy, explicit prohibitions, strict priorities
5. **Comportamiento esperado** — expected behavior across typical situations
6. **Casos de uso de prueba** — test cases that validate scope is respected
7. **Interacción con el ecosistema** — input/output contract and explicit frontier with other agents

The structure is public; the operational content of the prompt and knowledge sources stays private.

---

## What the Demo Shows

1. **Knowledge is structured** so agents have authoritative, current sources to consult (SharePoint library with a clear README, area guides, and conventions)
2. **Governance is shared and consistent** across every agent (one architecture, common principles, an interaction contract, and a brand source of truth)
3. **Generation is grounded, not free-floating** (each agent design doc references Layers 1 and 2)
4. **Execution happens inside Microsoft 365** (agents act within the existing environment, not a separate tool) and remains **human-approved, auditable, and reversible**

---

## What the Demo Does Not Show

- The actual content of EmprendHEC's knowledge base
- Production prompts and internal system instructions
- Real client, customer, or personnel data
- Confidential business rules, pricing, or decision criteria
- Integration, security, and access-control configuration

See [`what-is-public-vs-private.md`](what-is-public-vs-private.md) for the full boundary explanation.

---

## Screenshots

Public-safe screenshots of this live environment are in [`Screenshots/`](Screenshots/) and cataloged in [`screenshots-and-diagrams.md`](screenshots-and-diagrams.md). They are **evidence that the pattern works**, not a blueprint of the private system.
