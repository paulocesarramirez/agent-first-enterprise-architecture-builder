# Guide Template

## Purpose

This document provides a **public-safe elemental template** for writing an operational guide
(**Guía Operativa**) under the
**Agent-First Enterprise Architecture Builder** framework.

It is intentionally generic.

It is designed to preserve the architecture and writing pattern of the framework without exposing confidential operational details.

This template should help GitHub Copilot generate:
- public-safe documentation scaffolds
- reusable guides
- architecture-aligned operating documents

---

## Naming pattern

Recommended filename pattern:

`[NN]-[Guide-Type]-[Topic].md`

Examples:
- `01-Operating-Principles.md`
- `02-Naming-Conventions.md`
- `03-Continuous-Evolution-Process.md`

Avoid:
- vague names
- “final”
- “v1-final”
- project-specific confidential titles

---

## Standard structure

# `[Guide Title]`

## 1. Purpose of this Guide
Explain:
- why the guide exists
- what part of the system it governs
- why it matters to overall architecture coherence

### Template prompt
> This guide defines how `[domain or process]` should be governed inside the architecture.

---

## 2. Scope
Clarify:
- what is covered
- what is not covered
- what belongs to another guide or another layer

### Template prompt
> This guide applies to `[scope]` and does not cover `[exclusions]`.

---

## 3. Governing Principles
List the principles that govern the guide.

Examples:
- source of truth first
- human approval where needed
- explicit structure
- no undocumented improvisation
- architecture before execution

---

## 4. Operational Rules
Document the core rules.

Rules should be:
- explicit
- short
- testable
- non-ambiguous

### Recommended pattern
- Rule 1: `[clear rule]`
- Rule 2: `[clear rule]`
- Rule 3: `[clear rule]`

---

## 5. Process or Flow
Describe the process at a high level.

This may include:
- sequence of steps
- decision checkpoints
- escalation points
- review gates

If the full internal process is confidential, publish only the public-safe pattern.

---

## 6. Roles and Responsibilities
State who does what.

Recommended categories:
- human role
- agent role
- system role
- approval role

Make responsibility boundaries explicit.

---

## 7. Inputs and Outputs
Document:
- expected inputs
- resulting outputs
- approved formats where relevant

Keep examples public-safe.

---

## 8. Exceptions and Prohibitions
State what should not happen.

Examples:
- no undocumented changes
- no bypassing governance
- no confidential data in public-safe examples
- no role confusion

---

## 9. Related Documents
List related guides, architecture docs, templates, or agent designs.

This helps GitHub Copilot maintain cross-reference structure.

---

## 10. Change and Evolution Rule
Document how this guide evolves.

Recommended pattern:
- changes are deliberate
- changes are reviewed
- architecture changes precede guide changes
- no hidden drift

---

## Writing guidelines

When using this template:

- write with strong headings
- prefer explicit rules over narrative vagueness
- separate principle from process
- separate public-safe pattern from confidential implementation
- preserve architecture-first logic
- maintain human-centered language

---

## Public-safe note

A public guide must not reveal:
- confidential operational details
- customer or client information
- secrets
- internal business logic not approved for release

If a topic is conceptually important but operationally sensitive:
publish the structure, not the confidential implementation.

---

## Minimal example skeleton

# Example Guide Title

## 1. Purpose
This guide defines how `[topic]` is governed inside the architecture.

## 2. Scope
Applies to `[scope]`. Does not apply to `[excluded scope]`.

## 3. Governing Principles
- Principle 1
- Principle 2
- Principle 3

## 4. Operational Rules
- Rule 1
- Rule 2
- Rule 3

## 5. Process or Flow
Describe the high-level pattern here.

## 6. Roles and Responsibilities
- Human:
- Agent:
- Approval owner:

## 7. Inputs and Outputs
- Inputs:
- Outputs:

## 8. Exceptions and Prohibitions
- Prohibition 1
- Prohibition 2

## 9. Related Documents
- Related doc 1
- Related doc 2

## 10. Change Rule
Describe how this guide evolves.
