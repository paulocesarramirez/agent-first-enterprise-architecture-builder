# Accountant Agent — Placeholder

> This agent design is planned but not yet documented. This placeholder reserves the space and outlines the intended scope.

---

## Intended Purpose

The Accountant Agent is designed to support financial operations teams by assisting with routine financial analysis, reconciliation support, and reporting tasks.

## Planned Capabilities

- Summarizing financial data from connected reporting sources
- Flagging variances against budget or forecast
- Drafting commentary for financial reports
- Supporting period-end close checklists

## Design Considerations

This agent operates in a high-consequence domain. The governance requirements are correspondingly strict:

- All outputs require qualified human review before use
- The agent must not make accounting entries or approve transactions
- Strong audit logging is required for compliance purposes
- Access to financial data must follow least-privilege principles

## Status

- [ ] Agent contract drafted
- [ ] Knowledge sources identified
- [ ] Governance requirements defined
- [ ] Owner assigned
- [ ] Approved for design

## Related Examples

- [`commercial-agent-example.md`](commercial-agent-example.md) — Similar scope in the commercial domain
- [`common-agent-contract.md`](common-agent-contract.md) — Template to complete when ready

---

> To contribute this agent design, follow the process in [`CONTRIBUTING.md`](../../CONTRIBUTING.md) and use [`public-agent-template.md`](public-agent-template.md).
