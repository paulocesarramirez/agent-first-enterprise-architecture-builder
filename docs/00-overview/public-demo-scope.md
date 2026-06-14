# Public Demo Scope

## Purpose of this document

This document defines **what the public demo shows** and **what it deliberately leaves out**. It also hosts the **public-safe screenshots** of what has actually been built, so readers can see the framework working in a real environment without exposing confidential operational detail.

> The demo is **one private implementation example** of the public framework. The screenshots here illustrate the approach; they are not a release of the private operational system.

---

## What the demo is

The demo is the live, working ecosystem at **EmprendHEC**, built on the architecture-first, human-first principles in this repository. It currently coordinates real internal work through four active agents:

- **PM Assistant**
- **M365 Watcher**
- **Commercial Agent**
- **Editorial Assistant**

These agents share a single source of truth, operate under human governance, and run on a Microsoft 365 execution layer.

---

## Screenshot ground rules (read before adding images)

All screenshots in this document must be **public-safe**. Before adding an image, confirm it does **not** reveal:

- real client, customer, or personnel names or PII
- confidential business rules, pricing, or internal decision logic
- private prompts, knowledge-base contents, or system instructions
- secrets, credentials, tenant IDs, endpoints, or connector configuration

If an image would expose any of the above, **redact, blur, or recreate it with placeholder data** before adding it.

**Storage:** the public-safe screenshots for this demo live in [`../04-demo/Screenshots/`](../04-demo/Screenshots/) and are cataloged in [../04-demo/screenshots-and-diagrams.md](../04-demo/screenshots-and-diagrams.md). The selection below highlights one representative image per framework layer; the catalog lists all of them.

---

## What the demo shows

The screenshots below walk the four layers of the framework — from the knowledge base, through governance and agent design, to a live agent answering a real query inside Microsoft 365.

### 1. Knowledge layer — the source of truth in SharePoint

The SharePoint site *"EmprendHEC - Arquitectura Información"* holds the structured knowledge every agent consults: a README that explains the library, area guides, brand and identity manuals, and the `Agentes` and monthly-monitoring folders.

![EmprendHEC SharePoint knowledge library](<../04-demo/Screenshots/01-Screenshot Librería Principal-Arquitectura de Información.png>)

**Caption:** _The institutional knowledge base — one structured, governed source of truth rather than scattered files._

---

### 2. Governance layer — the shared agent contract

The `Agentes/` folder holds the documents every agent inherits: the architecture, the common principles, the interaction contract, and naming conventions — plus a dedicated subfolder per agent.

![Agentes folder with shared agent contract](<../04-demo/Screenshots/02-Screenshot-Carpeta Agentes.png>)

**Caption:** _Common principles and an interaction contract that every agent must respect — governance applied consistently._

---

### 3. Generation layer — how an agent is designed

Each agent is defined by a public-safe design document: executive summary, knowledge sources, parameters and limits, expected behavior, and test cases. The instruction prompt itself stays private.

![Commercial Agent design document](<../04-demo/Screenshots/08-Screenshot-Diseño de Agente Comercial.png>)

**Caption:** _The Commercial Agent design doc — grounded in the knowledge and governance layers, with the prompt kept private._

---

### 4. Generation layer — the agents published in Microsoft 365

The agents are published in the Microsoft 365 Copilot Agent Store, where the team invokes them as part of normal work.

![EmprendHEC agents in the Microsoft 365 Copilot Agent Store](<../04-demo/Screenshots/09-Screenshot-Vista Agentes en M365.png>)

**Caption:** _PM Assistant, M365 Watcher, Commercial Agent, and Editorial Assistant — running inside Microsoft 365, not a separate tool._

> **Living proof.** This is not a staged demo tenant. These agents are deployed in EmprendHEC's own Microsoft 365 environment and are used to run real internal work **on a daily basis** — the company operates this way today. That is the point of the framework: it is validated in live operation, not just described on paper.

---

### 5. Execution layer — an agent at work

A worked example: the Commercial Agent responds to a real query, grounded in the commercial operative guide and bounded by its defined scope.

![Commercial Agent answering a query in Microsoft 365 Copilot](<../04-demo/Screenshots/10-Screenshot-Vista Agente Comercial.png>)

**Caption:** _The Commercial Agent assisting with commercial work; the human stays in control of every strategic decision._

> The remaining screenshots — the `Guías por área` folder, the README, the identity manual, the Agent-Ready brand guide, and the commercial operative guide — are in the [full catalog](../04-demo/screenshots-and-diagrams.md).

---

## What the demo does *not* show

To preserve the public/private boundary, the demo and these screenshots intentionally exclude:

- the private knowledge base and its actual contents
- production prompts and internal system instructions
- real client, customer, or personnel data
- confidential business rules, pricing, and decision criteria
- integration, security, and access-control configuration

For the full rationale, see [what-is-public-vs-private.md](../04-demo/what-is-public-vs-private.md) and [../01-principles/public-repo-boundary.md](../01-principles/public-repo-boundary.md).

---

## How to read the screenshots

The screenshots are meant to answer one question: **"Does this approach actually work in a real organization?"**

Several of the document screenshots are captured with the Word **Navigation Pane** open, showing each document's full heading outline — visible evidence that these are complete, structured, real documents from a working implementation, not slides or mockups.

They are **evidence of the pattern**, not a blueprint of the private system. Use them alongside:

- [architecture-overview.md](architecture-overview.md) — the layered model behind what you see
- [category-definition.md](category-definition.md) — the category this work defines
- [../04-demo/demo-architecture.md](../04-demo/demo-architecture.md) — how the demo is structured

---

## Summary

The public demo scope shows **what was built and that it works**, through public-safe screenshots, while keeping every confidential operational detail private. It demonstrates the framework in practice without becoming an export of the private system.
