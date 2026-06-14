# Implementation Diagnostic

## Purpose

This is the **first step** when someone says to Copilot (or GitHub Copilot):

> _"I want this implemented for my company, using this repository as the reference."_

Before proposing anything, Copilot should run a **short, friendly diagnostic** to understand the organization's Microsoft stack and preferred build style. The diagnostic produces one output: a **recommended implementation path** that the [implementation-playbook.md](implementation-playbook.md) then expands into concrete steps.

> Keep it simple. This is a conversation, not a form to fear. Ask the questions in plain language, accept partial answers, and infer sensible defaults when the user is unsure.

---

## How Copilot should run this

1. Ask the questions in **Part A** (one block, conversational — not an interrogation).
2. Map the answers using the **decision table** in **Part B**.
3. Confirm the recommended **path** with the user in plain language, and explain *why*.
4. Hand off to [implementation-playbook.md](implementation-playbook.md) for the chosen path.

> **Golden rule:** never block on a perfect answer. If the user doesn't know, note the assumption, pick the safe default, and move on.

---

## Part A — The diagnostic questions

Copy/ask these. Short answers are fine.

### 1. Company context
- What is your organization's name (or a placeholder like `[YourOrg]`)?
- Roughly how big is it (just you, small team, mid-size, large)?
- What industry are you in, and do you have any compliance/data-residency constraints?

### 2. Microsoft 365 foundation
- Do you use Microsoft 365 today? Which plan family (Business Basic/Standard/Premium, or Enterprise E3/E5)?
- Do you have **SharePoint**, **Teams**, **Planner**, and **Outlook** available?

### 3. Copilot subscriptions
- Do you have **Microsoft 365 Copilot** (the paid add-on)?
- Or only **Microsoft 365 Copilot Chat** (the included/free experience)?
- Do you have **Copilot Studio** licensing?

### 4. Azure & developer platform
- Do you have an **Azure subscription**?
- Do you have access to **Azure AI Foundry** (models + Agent Service)?
- Does your team write code, or prefer to avoid it?

### 5. Power Platform & data
- Do you use **Power Platform** (Power Apps, Power Automate)?
- Do you use **Microsoft Fabric** or another central data platform?

### 6. Preferred build style
Which best describes how you'd like to build?
- **No-Code** — configure, don't program. Fastest start.
- **Low-Code** — visual builders plus some connectors/automation.
- **Pro-Code** — full control with code and custom orchestration.
- **Not sure** — let the diagnostic recommend.

### 7. Goal & starting point
- Which area do you want to start with (e.g., commercial, projects, editorial/content, finance, legal)?
- Are you starting fresh, or do you already have documented processes/guides?

---

## Part B — Decision table (answers → recommended path)

The three build styles map directly to a Microsoft implementation surface:

| Path | Means | Primary build surface | Typical prerequisites |
|------|-------|------------------------|------------------------|
| **No-Code** | Declarative agents grounded on your Microsoft 365 knowledge | **Declarative agents** (Copilot agent builder in Microsoft 365 Copilot) | Microsoft 365 Copilot license + SharePoint |
| **Low-Code** | Visual agents with topics, actions, connectors, and automation | **Microsoft Copilot Studio** | Copilot Studio license + Power Platform |
| **Pro-Code** | Custom agents with full orchestration and models | **Azure AI Foundry** + **Microsoft Agent Framework** | Azure subscription + Azure AI Foundry access + developers |
| **Hybrid** | Start simple, extend where needed | Mix of the above (e.g., No-Code agents now, Pro-Code later) | Whatever you already have, grown over time |

### Mapping logic

Use the **first** row that matches, then confirm with the user:

| If the user… | Recommend |
|--------------|-----------|
| Has Microsoft 365 Copilot + SharePoint, wants the fastest start, and prefers not to code | **No-Code** (Declarative agents) |
| Needs custom actions, connectors, automation, or multiple channels, and has Copilot Studio / Power Platform | **Low-Code** (Copilot Studio) |
| Needs full control, custom orchestration, advanced models/tools, and has Azure AI Foundry + developers | **Pro-Code** (Azure AI Foundry + Microsoft Agent Framework) |
| Wants to begin quickly **and** anticipates advanced needs later, or has mixed licensing across teams | **Hybrid** |
| Is unsure, but has Microsoft 365 Copilot | **No-Code** to start (it is the lowest-risk entry; you can grow into Hybrid) |
| Has no Microsoft 365 Copilot and no Azure today | Start with the **Knowledge layer only** (structure the source of truth in SharePoint), then revisit paths once licensing is in place |

> **Note on licensing:** Copilot recommends a path; it does not provision licenses. If a prerequisite is missing, say so plainly and offer the closest path the user *can* start today (often the Knowledge layer plus No-Code).

---

## Part C — Diagnostic summary (what Copilot produces)

After the questions, Copilot should produce a short, public-safe summary like this:

```
Diagnostic summary for [YourOrg]

- Microsoft 365: [plan]  ·  SharePoint/Teams/Planner: [yes/no]
- Copilot: [M365 Copilot / Copilot Chat / Copilot Studio]
- Azure / AI Foundry: [yes/no]
- Power Platform / Fabric: [yes/no]
- Preferred style: [No-Code / Low-Code / Pro-Code / Hybrid]
- Starting area: [e.g., Commercial]
- Starting point: [fresh / existing docs]

➡ Recommended path: [No-Code | Low-Code | Pro-Code | Hybrid]
   Why: [one or two plain-language reasons]

Next: open implementation-playbook.md and follow the [path] track.
```

> Keep this summary public-safe: no credentials, tenant IDs, client names, or confidential business detail. Use placeholders where appropriate.

---

## What this diagnostic is **not**

- It is not a licensing or security assessment.
- It does not collect secrets, tenant IDs, or confidential data.
- It does not lock the user in — paths can change, and **Hybrid** exists precisely for that.

---

## Related documents

- [repo-implementation-guidelines.md](repo-implementation-guidelines.md) — the overall "implement for your company" entry point
- [implementation-playbook.md](implementation-playbook.md) — step-by-step build for the recommended path
- [../00-overview/architecture-overview.md](../00-overview/architecture-overview.md) — the four-layer model behind the playbook
- [../02-framework/architecture-layers.md](../02-framework/architecture-layers.md) — the layered framework in detail
