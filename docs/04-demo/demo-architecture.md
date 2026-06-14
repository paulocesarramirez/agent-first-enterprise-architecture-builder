# Demo Architecture

## What Is Being Demonstrated

This demo represents a **public-safe view** of an agent-first enterprise architecture. It illustrates how the four-layer framework operates as an integrated system — not just as individual components.

The demo is intentionally generic and uses fictional organizational context. It is designed to be adaptable, not copied verbatim.

## The Demo Organization

For the purposes of this demo, the fictional organization is:

- **Name:** [DemoOrg]
- **Size:** Mid-market (~500 employees)
- **Industry:** Professional services
- **M365 footprint:** Teams, SharePoint, Outlook, Planner

This context is chosen because it is representative of a broad category of organizations without being specific to any real company.

## Architecture in the Demo

```
[DemoOrg] Agent-First Architecture

Layer 1: Knowledge
├── Organizational principles (maintained in SharePoint)
├── Business rules and policies (maintained in SharePoint)
└── Process documentation (maintained in SharePoint)

Layer 2: Governance
├── Agent registry (maintained by IT + Operations)
├── Scope definitions per agent
└── Escalation and review processes

Layer 3: Generation
├── GitHub Copilot (development and documentation)
├── Microsoft 365 Copilot (operational tasks)
└── Custom agent prompts grounded in Layer 1

Layer 4: Execution
├── Teams (communication)
├── Planner (task management)
├── SharePoint (document operations)
└── Outlook (email)
```

## Agents in the Demo

| Agent | Purpose | Layer 3 Tool | Layer 4 Target |
|-------|---------|-------------|---------------|
| PM Assistant | Project status synthesis | M365 Copilot | Planner + SharePoint |
| M365 Watcher | Activity monitoring | Custom agent | Graph API |
| Editorial Assistant | Content review | M365 Copilot | SharePoint |

## What the Demo Shows

1. How knowledge is structured so agents can use it reliably
2. How governance is applied consistently across different agents
3. How generation is grounded — not free-floating
4. How execution is authorized, audited, and reversible

## What the Demo Does Not Show

- The actual content of [DemoOrg]'s knowledge base
- Live system integrations
- Real agent prompts from a production deployment
- Anything that would not be safe to publish publicly

See [`what-is-public-vs-private.md`](what-is-public-vs-private.md) for the boundary explanation.
