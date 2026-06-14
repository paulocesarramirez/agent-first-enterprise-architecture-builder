# Repo Implementation Guidelines

## Purpose

This document describes how this repository is structured, maintained, and extended. It is the authoritative reference for anyone contributing to or using this repo as a template.

## Repository Principles

1. **One concept per file** — Each document covers a single, focused topic
2. **Structure before content** — Folder organization reflects conceptual architecture
3. **Public-safe by default** — Every file must pass the public-safe test before being added
4. **Maintained, not accumulated** — Files are updated when their content changes; outdated content is removed, not left in place

## Folder Structure

| Folder | Purpose |
|--------|---------|
| `docs/00-overview/` | High-level orientation for new readers |
| `docs/01-principles/` | Foundational, non-negotiable principles |
| `docs/02-framework/` | The four-layer architectural model |
| `docs/03-agent-design-patterns/` | Agent contracts, templates, and examples |
| `docs/04-demo/` | Illustrative scenarios and demo context |
| `docs/05-copilot-implementation/` | How this repo itself is built (meta-layer) |
| `docs/06-faq/` | Common questions answered concisely |
| `examples/` | Safe, adaptable examples and diagrams |
| `starter-kits/` | Ready-to-adapt starting points |
| `assets/` | Visual assets (logos, diagrams, visuals) |
| `.github/` | GitHub-specific files (templates, Copilot instructions) |

## Adding New Content

Before adding a new file:

1. Confirm the content is **public-safe** (see [`docs/01-principles/public-repo-boundary.md`](../01-principles/public-repo-boundary.md))
2. Identify the correct **folder** for the content type
3. Follow the **naming conventions** in [`naming-conventions.md`](naming-conventions.md)
4. Follow the **markdown standards** in [`markdown-standards.md`](markdown-standards.md)
5. Add cross-references from related documents to the new file

## Modifying Existing Content

- **`docs/01-principles/`** — Do not modify without explicit discussion. These are foundational.
- **`docs/02-framework/`** — Changes here have wide impact; review all cross-references.
- **Examples** — Can be added or improved freely, as long as they remain public-safe.
- **Templates** — Changes should be backward-compatible.

## Using GitHub Copilot in This Repo

This repo includes a `copilot-instructions.md` file that guides Copilot's behavior. When working in this repo:

- Copilot will apply the naming conventions and structure automatically
- Copilot will flag content that may not be public-safe
- Copilot should not modify `docs/01-principles/` without instruction

See [`.github/copilot-instructions.md`](../../.github/copilot-instructions.md) for the full instructions.

## Review Process

All changes should be reviewed against:

- [ ] Public-safe test passed
- [ ] Naming conventions followed
- [ ] Markdown standards followed
- [ ] Cross-references added/updated
- [ ] No modifications to principles without discussion
