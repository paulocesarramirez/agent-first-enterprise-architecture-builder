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

**Suggested storage:** place image files in `assets/visuals/` and reference them with relative paths. Use descriptive, kebab-case names such as `example-pm-assistant-overview.png`.

---

## What the demo shows

### 1. The agent ecosystem at a glance

A high-level view of the four agents operating under one shared architecture and governance model.

> _Screenshot placeholder — replace with a public-safe image._
>
> `![Agent ecosystem overview](../../assets/visuals/example-agent-ecosystem-overview.png)`
>
> **Caption:** _The four active agents (PM Assistant, M365 Watcher, Commercial Agent, Editorial Assistant) operating under a shared source of truth._

---

### 2. PM Assistant

Coordinates project work, surfaces priorities, and supports planning while keeping decisions with humans.

> _Screenshot placeholder — replace with a public-safe image._
>
> `![PM Assistant](../../assets/visuals/example-pm-assistant.png)`
>
> **Caption:** _PM Assistant proposing next actions; the human approves before anything proceeds._

---

### 3. M365 Watcher

Monitors the Microsoft 365 environment and signals relevant changes back into the workflow.

> _Screenshot placeholder — replace with a public-safe image._
>
> `![M365 Watcher](../../assets/visuals/example-m365-watcher.png)`
>
> **Caption:** _M365 Watcher detecting and routing a relevant signal across the workspace._

---

### 4. Commercial Agent

Supports commercial activity with structured, governed assistance grounded in the source of truth.

> _Screenshot placeholder — replace with a public-safe image._
>
> `![Commercial Agent](../../assets/visuals/example-commercial-agent.png)`
>
> **Caption:** _Commercial Agent generating a structured draft for human review (placeholder data shown)._

---

### 5. Editorial Assistant

Helps produce and refine content while preserving human editorial judgment.

> _Screenshot placeholder — replace with a public-safe image._
>
> `![Editorial Assistant](../../assets/visuals/example-editorial-assistant.png)`
>
> **Caption:** _Editorial Assistant suggesting revisions; final editorial control stays with the human._

---

### 6. The Microsoft 365 execution layer

Where the architecture becomes action — SharePoint, Teams, Planner, Outlook, and Microsoft 365 Copilot.

> _Screenshot placeholder — replace with a public-safe image._
>
> `![Microsoft 365 execution layer](../../assets/visuals/example-m365-execution-layer.png)`
>
> **Caption:** _Agents operating within the existing Microsoft 365 environment rather than a separate tool._

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

They are **evidence of the pattern**, not a blueprint of the private system. Use them alongside:

- [architecture-overview.md](architecture-overview.md) — the layered model behind what you see
- [category-definition.md](category-definition.md) — the category this work defines
- [../04-demo/demo-architecture.md](../04-demo/demo-architecture.md) — how the demo is structured

---

## Summary

The public demo scope shows **what was built and that it works**, through public-safe screenshots, while keeping every confidential operational detail private. It demonstrates the framework in practice without becoming an export of the private system.
