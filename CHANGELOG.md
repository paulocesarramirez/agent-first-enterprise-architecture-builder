# Changelog

All notable changes to this public framework are documented in this file.

This project follows controlled evolution: architecture and governance changes are deliberate, reviewable, and public-safe.

This changelog follows [Keep a Changelog](https://keepachangelog.com/) and [Semantic Versioning](https://semver.org/). The `[Unreleased]` section holds changes that are committed but not yet tagged as a numbered release.

## [Unreleased]

_No unreleased changes yet._

## [1.0.0] - 2026-06-25

### Added
- Enterprise-readiness roadmap artifacts:
  - Security and Compliance layer (`docs/02-framework/security-and-compliance-layer.md`)
  - Responsible AI and governance hierarchy (`docs/02-framework/responsible-ai-and-governance-hierarchy.md`)
  - Human-in-the-loop risk and failure governance (`docs/02-framework/human-in-the-loop-risk-and-failure-governance.md`)
  - Value and metrics pattern (`docs/02-framework/value-and-metrics.md`)
  - Human-orchestrated multi-agent pattern (`docs/03-agent-design-patterns/human-orchestrated-multi-agent-pattern.md`)
  - Model and build-surface selection guidance (`docs/05-copilot-implementation/model-and-build-surface-selection.md`)
  - Adoption maturity model (`docs/00-overview/adoption-maturity-model.md`)
- `ROADMAP.md` for versioned planning.

### Changed
- Implementation diagnostic/playbook expanded with cost/licensing and cross-path observability guidance.
- Layer 3 naming standardized to **Capability Generation Layer** in documentation references.
- README updated with an **Enterprise Governance & Readiness** section linking the new documents and surfacing the core principles: organization documentation governs **above Microsoft Responsible AI**, the **human is the primary orchestrator** (with Microsoft Copilot Cowork for execution), and **Grok** is recommended for a non-biased Personal Strategic AI Agent.

### Principles emphasized
- Organization-authored governance is the primary authority; platform Responsible AI (Microsoft RAI, Azure AI Content Safety) is subordinate reinforcement.
- Human-led, human-verified execution over fully autonomous multi-step reasoning.
- Human-as-primary-orchestrator for multi-agent work; Copilot Cowork executes the resulting knowledge work.
- Grok recommended for the non-biased Personal Strategic AI Agent role; Microsoft-native models for execution agents.
