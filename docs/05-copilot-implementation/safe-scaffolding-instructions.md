# Safe Scaffolding Instructions

## Purpose

This document describes how to safely add new content to this repository — whether you are working manually or using GitHub Copilot. "Safe scaffolding" means creating well-structured, public-appropriate content without accidentally exposing private information or breaking the repository's structure.

## The Scaffolding Checklist

Before creating any new file, confirm:

- [ ] **Is this content public-safe?** — No proprietary data, credentials, or internal system details
- [ ] **Does it belong in this repo?** — Is it an architectural pattern, principle, example, or framework element?
- [ ] **Is there already a file for this?** — Check existing files before creating a duplicate
- [ ] **What folder does it belong in?** — Use the folder structure in [`repo-implementation-guidelines.md`](repo-implementation-guidelines.md)
- [ ] **Does the filename follow conventions?** — See [`naming-conventions.md`](naming-conventions.md)

## Scaffolding New Documents

### Step 1: Choose the Right Folder

| Content Type | Folder |
|-------------|--------|
| High-level orientation | `docs/00-overview/` |
| Foundational principle | `docs/01-principles/` ⚠️ requires discussion |
| Framework layer documentation | `docs/02-framework/` |
| Agent design pattern or example | `docs/03-agent-design-patterns/` |
| Demo or scenario content | `docs/04-demo/` |
| Implementation guidance | `docs/05-copilot-implementation/` |
| FAQ answer | `docs/06-faq/` |
| Illustrative example | `examples/public-safe-*/` |
| Architecture diagram | `examples/diagrams/` |
| Starter kit content | `starter-kits/[kit-name]/` |

### Step 2: Create the File

Follow the markdown standards in [`markdown-standards.md`](markdown-standards.md).

Start every document with:

```markdown
# [Title in Title Case]

## Purpose

[One paragraph explaining what this document covers and why it exists.]
```

### Step 3: Add Cross-References

After creating a new file:

1. Add a link to it from the most relevant existing document
2. If it's a new agent design, add it to [`docs/03-agent-design-patterns/README.md`](../03-agent-design-patterns/README.md)
3. If it's a new example, ensure it ends in `.example.md`

### Step 4: Review for Public Safety

Read through the new content and ask:

- Does this contain any real names, systems, or credentials? → Remove
- Does this reveal operational specifics of a real organization? → Remove or generalize
- Could an attacker use any of this information? → Remove

## Using GitHub Copilot for Scaffolding

When using Copilot to generate new content in this repo:

1. Copilot will follow the instructions in `.github/copilot-instructions.md` automatically
2. Always review Copilot's output before committing — check for accidentally specific content
3. Use placeholder names like `[YourOrg]`, `[YourSystem]`, `[YourProcess]` when Copilot uses specifics
4. If Copilot generates content that doesn't fit the structure, ask it to regenerate with the correct folder and naming context

## What Not to Scaffold

- Do not create files that contain real business logic or rules
- Do not create files in `docs/01-principles/` without prior discussion with maintainers
- Do not create agent design files that reference private systems
- Do not create files outside the defined folder structure without a documented reason
