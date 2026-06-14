# How This Relates to Microsoft 365

## The Relationship

Microsoft 365 is referenced in this framework as the **primary execution layer** in the reference implementation. It is not a requirement — it is a context.

The architectural principles and four-layer model apply regardless of which platforms an organization uses.

## Why Microsoft 365 Is the Reference Platform

The reference implementation uses Microsoft 365 because:

1. **Breadth of coverage** — M365 covers communication (Teams, Outlook), documents (SharePoint, OneDrive), tasks (Planner), and data (Power Platform)
2. **Agent infrastructure across build styles** — the Microsoft stack supports the full spectrum: Declarative agents (No-Code), Copilot Studio (Low-Code), and Azure AI Foundry with the Microsoft Agent Framework (Pro-Code)
3. **Enterprise prevalence** — M365 is the dominant enterprise platform, making examples broadly relevant
4. **Copilot integration** — GitHub Copilot (used to maintain this repo) and Microsoft 365 Copilot (used in the execution layer) are part of the same ecosystem

## What M365 Provides in This Architecture

| M365 Component | Role in the Framework |
|----------------|----------------------|
| SharePoint | Knowledge base storage and maintenance |
| Teams | Agent output delivery and collaboration |
| Outlook | Email-based agent actions |
| Planner | Task and project management actions |
| Power Automate | Workflow orchestration |
| Microsoft Graph API | Programmatic access to M365 data |
| Declarative agents (Copilot agent builder) | No-Code agent authoring grounded on M365 knowledge |
| Copilot Studio | Low-code agent configuration |
| Azure AI Foundry + Microsoft Agent Framework | Pro-code agents with full orchestration |
| Microsoft 365 Copilot | AI assistance embedded in M365 apps |

## Choosing a build style

The framework maps three build styles to Microsoft surfaces:

| Style | Surface |
|-------|---------|
| **No-Code** | Declarative agents (Microsoft 365 Copilot agent builder) |
| **Low-Code** | Microsoft Copilot Studio |
| **Pro-Code** | Azure AI Foundry + Microsoft Agent Framework |

The [implementation diagnostic](../05-copilot-implementation/implementation-diagnostic.md) recommends the right style for your stack, and the [implementation playbook](../05-copilot-implementation/implementation-playbook.md) walks through building on it.

## If You Don't Use Microsoft 365

The framework's four layers apply to any technology stack:

| Layer | M365 Example | Alternative Examples |
|-------|-------------|---------------------|
| Knowledge | SharePoint | Confluence, Notion, Google Drive, custom wiki |
| Governance | Custom + M365 admin | Any governance tooling |
| Generation | M365 Copilot, GitHub Copilot | Any LLM or AI assistant |
| Execution | Microsoft Graph, Power Automate | Salesforce API, ServiceNow, custom APIs |

The architecture is the pattern. The technology is the implementation detail.

## Microsoft Is Not the Framework Author

This framework is not affiliated with, endorsed by, or created by Microsoft. It references Microsoft 365 as a technology context, not as a business relationship. See the [DISCLAIMER](../../DISCLAIMER.md) for details.
