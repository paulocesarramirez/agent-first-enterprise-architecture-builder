# Public Demo Scope

## What Is Demonstrated Publicly

This repository is a **public-safe demonstration** of an agent-first enterprise architecture framework. The following elements are intentionally included for public view:

### Included in This Repo

| Content | Location | Purpose |
|---------|----------|---------|
| Architectural principles | `docs/01-principles/` | Establish the foundation |
| Four-layer framework model | `docs/02-framework/` | Show the structural approach |
| Agent design patterns | `docs/03-agent-design-patterns/` | Illustrate how agents are designed |
| Generic examples | `examples/` | Provide safe, adaptable templates |
| Mermaid diagrams | `examples/diagrams/` | Visualize the architecture |
| Starter kits | `starter-kits/` | Enable adoption |

### Illustrative, Not Operational

All examples use fictional organizations, placeholder names, and generic processes. Nothing in this repository reflects a specific live deployment.

## What Is Intentionally Excluded

The following content exists in a private implementation of this framework and is **not** included here:

- Real organizational principles tied to a specific company
- Internal business rules and decision logic
- Live agent prompts connected to production systems
- Integration configurations for actual Microsoft 365 tenants
- Confidential process maps or operational data

## Why This Boundary Exists

Publishing the full system would:

1. Expose proprietary business logic
2. Create security risks for connected systems
3. Reduce the framework's usefulness as a generic reference

The public version is designed to be **maximally useful without being maximally complete**. See [`docs/04-demo/what-is-public-vs-private.md`](../04-demo/what-is-public-vs-private.md) for a deeper explanation.

## Demo Audience

This public demo is aimed at:

- Organizations evaluating whether to build an agent-first architecture
- Architects who want a reference model to adapt
- Teams using GitHub Copilot who want to understand how to structure AI-assisted work
