# Markdown Standards

## Purpose

Consistent markdown formatting ensures documents are readable in GitHub, VS Code, and any markdown-rendering environment. These standards apply to all `.md` files in this repository.

## Document Structure

Every document should follow this structure:

```markdown
# Title (H1) — one per document

## Introduction or Purpose paragraph

## Section (H2)

### Sub-section (H3) — use sparingly

Content...
```

### Rules

- **One H1 per document** — the document title
- **H2 for major sections** — the primary organizational unit
- **H3 for sub-sections** — only when a section genuinely has sub-parts
- **No H4 or deeper** — restructure the document instead

## Tables

Use tables for structured comparisons and reference data:

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Value    | Value    | Value    |
```

- Always include a header row
- Align column separators for readability (optional but preferred)
- Keep table content concise — use links for detail

## Code Blocks

Use fenced code blocks with a language identifier:

````markdown
```markdown
Example content
```
````

- Use `mermaid` for diagrams
- Use `markdown` for markdown examples
- Use `json`, `yaml`, `python`, etc. as appropriate

## Lists

Use **unordered lists** (`-`) for items without inherent order:

```markdown
- Item one
- Item two
- Item three
```

Use **ordered lists** (`1.`) for sequential steps:

```markdown
1. First step
2. Second step
3. Third step
```

- Do not mix ordered and unordered lists at the same level
- Keep list items parallel in structure (all noun phrases, or all sentences)

## Emphasis

| Markdown | Use For |
|----------|---------|
| `**bold**` | Key terms, critical information |
| `*italic*` | Titles of documents, gentle emphasis |
| `` `code` `` | File names, paths, code terms, identifiers |

Do not use bold for decorative purposes. Use it only when the emphasis is meaningful.

## Links

Internal links use relative paths:

```markdown
[Link text](../folder/filename.md)
```

External links use the full URL:

```markdown
[Link text](https://example.com)
```

- Link text should be descriptive, not "click here" or "this document"
- All internal links must point to files that exist

## Callout Blocks

Use blockquotes for important callouts or notes:

```markdown
> **Note:** This content is illustrative only.
```

For placeholder or draft content, use an italicized note at the top:

```markdown
> *This document is a placeholder. Full content coming soon.*
```

## Front Matter

This repository does not use YAML front matter in documentation files. Keep documents clean markdown only.

## File Endings

All files must end with a single newline character. No trailing blank lines beyond one.
