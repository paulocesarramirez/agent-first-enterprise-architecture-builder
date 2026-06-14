# Naming Conventions

## Purpose

Consistent naming makes the repository easier to navigate, maintain, and extend. These conventions apply to all files and folders in this repository.

## File Naming

### General Rules

- Use **kebab-case** (lowercase, words separated by hyphens)
- Be **descriptive** — the filename should communicate the content
- Avoid abbreviations unless they are universally understood
- Do not use spaces, underscores, or camelCase

### By File Type

| File Type | Convention | Example |
|-----------|------------|---------|
| Documentation | `descriptive-name.md` | `architecture-layers.md` |
| Example files | `descriptive-name.example.md` | `agent-design-template.example.md` |
| Diagrams | `descriptive-name.mmd` | `architecture-layers.mmd` |
| Placeholder files | `descriptive-name-placeholder.md` | `legal-agent-placeholder.md` |

### Special Prefixes and Suffixes

| Suffix/Prefix | Meaning |
|--------------|---------|
| `-example.md` | An illustrative, fictional example — not a real implementation |
| `-placeholder.md` | Content that is planned but not yet written |
| `-template.md` | A blank structure for adaptation |
| `-starter` (folder) | A starter kit ready for adaptation |

## Folder Naming

- Use **kebab-case** for folder names
- Top-level `docs/` folders use a numeric prefix: `00-`, `01-`, etc.
- The numeric prefix establishes reading order, not priority

## Document Titles (H1)

- Use **Title Case** for all H1 headings
- The title should match or closely reflect the filename (without hyphens and extension)
- Example: `architecture-layers.md` → `# Architecture Layers`

## Cross-References

When referencing another file:

- Use **relative paths** from the current file's location
- Use the document title as the link text
- Example: `[Architecture Layers](../02-framework/architecture-layers.md)`

## Agent Identifiers

When defining an agent in the contract:

- Use the format: `agent-[short-descriptive-slug]`
- Examples: `agent-pm-status-assistant`, `agent-editorial-review`, `agent-m365-activity-watcher`
- Identifiers should be stable — avoid changing them after deployment

## What to Avoid

| Avoid | Use Instead |
|-------|------------|
| `MyDocument.md` | `my-document.md` |
| `doc1.md`, `file_v2.md` | `descriptive-name.md` |
| `AGENT_PM.md` | `pm-assistant-example.md` |
| `architecture layers.md` | `architecture-layers.md` |
