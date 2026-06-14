# Microsoft Execution Layer

## Purpose

The Execution Layer is where agents **take action** in connected enterprise systems. In the reference implementation of this framework, Microsoft 365 and the Microsoft 365 Agents SDK serve as the primary execution environment. The principles apply to any enterprise platform.

## What Execution Covers

Execution includes any agent action that changes state in a system:

| Action Type | Microsoft 365 Examples |
|-------------|----------------------|
| **Communication** | Sending emails via Outlook, posting to Teams channels |
| **Document operations** | Creating, updating, or organizing files in SharePoint or OneDrive |
| **Calendar management** | Scheduling meetings, updating availability |
| **Task and project management** | Creating tasks in Planner, updating project status |
| **Data retrieval** | Querying structured data from connected sources |
| **Workflow triggering** | Initiating Power Automate flows or approval workflows |
| **Notifications** | Sending structured alerts or summaries to stakeholders |

## Architecture in the Microsoft Context

```
Agent (defined in Layer 2/3)
    │
    ▼
Microsoft 365 Agents SDK / Copilot Studio
    │
    ├── Microsoft Graph API
    │       ├── Outlook / Exchange
    │       ├── SharePoint / OneDrive
    │       ├── Teams
    │       └── Planner / To Do
    │
    └── Power Platform
            ├── Power Automate
            └── Dataverse
```

## Execution Governance Requirements

Execution is the highest-consequence layer. It requires the most stringent governance:

1. **Least-privilege access** — Agents should have only the permissions needed for their defined tasks
2. **Action confirmation** — High-impact actions (e.g., sending external communications, deleting files) should require explicit confirmation
3. **Audit trail** — All actions taken should be logged with enough detail to reconstruct what happened and why
4. **Rollback capability** — Where possible, actions should be reversible
5. **Rate limiting** — Agents should not be able to take actions at a volume that could cause harm

## Integration with the Agent Governance Layer

Every execution capability must be:

- Listed in the agent's scope definition
- Authorized through the governance layer
- Bounded by the agent's role and purpose

An agent that drafts documents (Layer 3) should not automatically have permission to send those documents (Layer 4) unless that is part of its defined and authorized scope.

## Platform-Agnostic Note

While this document references Microsoft 365, the execution layer principles apply to any enterprise system:

- Salesforce, ServiceNow, SAP, Workday
- Custom APIs and internal tools
- Database write operations
- External communications platforms

The pattern is the same: **governed access, logged actions, human override**.

## Related Documents

- [`architecture-layers.md`](architecture-layers.md) — Layer 4 context
- [`agent-governance-layer.md`](agent-governance-layer.md) — Governs what execution is permitted
- [`docs/06-faq/how-this-relates-to-microsoft-365.md`](../06-faq/how-this-relates-to-microsoft-365.md)
