# Source of Truth

## Principle

> Agents reason from a single, human-curated source of truth — not from improvised, scattered, or self-generated knowledge.

## What This Means

In this framework, knowledge is **architecture, not an afterthought**. Before any agent is built, the organization defines an authoritative body of knowledge — principles, processes, rules, semantics, and decision boundaries — that agents read from and remain accountable to.

The source of truth is:

- **Single** — one authoritative reference, not competing copies
- **Human-curated** — maintained and approved by people, not silently rewritten by agents
- **Authoritative** — when an agent and the source of truth disagree, the source of truth wins
- **Transversal** — shared across agents so they reason consistently

This is what makes capability *generated from architecture* possible: agents are coherent because they draw from the same well.

## Why This Principle Is Foundational

Without a single source of truth, agentic systems tend to:

- contradict each other across teams and tasks
- hallucinate rules that were never agreed
- duplicate and drift away from the real process
- become impossible to audit or correct at the root

A single source of truth creates a forcing function: **every agent answer must be traceable back to curated, approved knowledge.**

## Grounding the Source of Truth — the "IQ" Layers

In a Microsoft environment, the source of truth is made operational by grounding agents in defined knowledge sources. Microsoft exposes these as composable "IQ" grounding layers. An organization selects the layers that match what it actually needs.

| Grounding layer | What it grounds the agent in | Typical use |
|-----------------|------------------------------|-------------|
| **Work IQ** | Microsoft 365 work content and signals (documents, messages, collaboration context) | Day-to-day operational work grounded in the organization's own content |
| **Web IQ** | Public web knowledge | Up-to-date, external, public information |
| **Foundry IQ** | Knowledge curated through Azure AI Foundry | Pro-code, governed knowledge for custom agents |
| **Fabric IQ** | Enterprise data modeled in Microsoft Fabric | Analytics- and data-grounded reasoning |

> The reference implementation at EmprendHEC currently grounds agents primarily in **Work IQ** and **Web IQ**. The framework deliberately extends to **Foundry IQ** and **Fabric IQ** as well, because the right combination depends on each organization's needs — not on a fixed recipe.

The principle stays constant regardless of layer: **the agent is grounded in curated knowledge, and humans govern what that knowledge contains.**

## From Source of Truth to the Right Agent

Once the architecture and source of truth are defined, an organization can use **GitHub Copilot** to help build *exactly the agents each use case requires*. The same governed knowledge can power agents at three levels of sophistication:

| Build approach | Platform | When to use |
|----------------|----------|-------------|
| **Declarative agents** | Microsoft 365 Copilot | Lightweight agents grounded in M365 content, defined through configuration |
| **Low-code agents** | Copilot Studio | Orchestrated agents that compose multiple IQ grounding layers without heavy code |
| **Pro-code agents** | Azure AI Foundry + Microsoft Agent Framework | Fully custom agents needing advanced control, tools, and governance |

The architecture is the constant; the build approach is the variable. A company picks the level that fits each use case — but every agent, at every level, still reasons from the same governed source of truth.

## Practical Implications

| Design Decision | Source-of-Truth Approach |
|-----------------|--------------------------|
| Where agents get their facts | From curated knowledge and chosen IQ grounding layers — never improvised |
| Who maintains the knowledge | Humans curate and approve; agents do not silently edit it |
| Choosing a build approach | Driven by the use case (declarative, low-code, or pro-code), not by default habit |
| Resolving contradictions | The source of truth is authoritative over any individual agent output |

## What This Principle Does Not Mean

- It does not mean a single giant file — the source of truth can be structured across well-organized, governed knowledge.
- It does not mean only one grounding layer — multiple IQ layers can combine, as long as the knowledge stays curated and authoritative.
- It does not mean knowledge is frozen — it evolves under governance (see below).

## Related Principles

- [`human-first-purpose.md`](human-first-purpose.md) — Humans curate the knowledge agents depend on
- [`governance-and-evolution.md`](governance-and-evolution.md) — The source of truth evolves only through human-approved change
- [`public-repo-boundary.md`](public-repo-boundary.md) — Real source-of-truth content stays private; only structure and patterns are public
