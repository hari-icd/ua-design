---
component: Code Snippet
category: components
figma_page: 1221:106300
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58150:73285
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58150-73281"
figma_in_page_doc_node_id: "58150:73281"
---

# Code Snippet
Read-only display block for presenting code, commands, or technical strings. Includes a copy-to-clipboard action and optional language/context label.

## Anatomy
- **Label**: Optional header above the code body (`Label=Yes`) — typically language name or context title
- **Code body**: Monospace text block with syntax-aware formatting
- **Copy button**: Trailing icon button — copies full content to clipboard

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Label | Yes · No | Adds a header row above the code block |

## States
Default (static display). Copy button has internal hover/active states.

## Usage
**Use when**: Showing API responses, code examples, CLI commands, config values, environment variables, or any content the user will copy/paste verbatim.
**Avoid when**:
- Content is editable → use Input or Textarea instead.
- Content is a short token/ID inline with text → use an inline copy field.
- Content is plain prose → use regular text; monospace formatting adds noise.

## Best Practices
**Do**: Use `Label=Yes` when showing multiple snippets on the same page to differentiate languages or contexts.
**Do**: Allow horizontal scroll for long single-line commands rather than wrapping.
**Don't**: Truncate code content — users rely on seeing the full value.
**Don't**: Embed interactive controls or form elements inside a code snippet.

## Agent Contract
**Default choice**: Use `Label=Yes` when multiple snippets appear on the same page; otherwise `Label=No` is acceptable.
**Content rule**: Code Snippet is read-only and must preserve full copyable content.
**Wrapping rule**: Prefer horizontal scroll for long commands or tokens instead of truncation.
**Interaction rule**: Only the copy action should be interactive inside the snippet.
**Do not invent**: Do not use Code Snippet for editable code; use an input or editor pattern instead.

## Related
- [Inputs](./inputs.md)
