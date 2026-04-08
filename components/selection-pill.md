---
component: Selection Pill
category: components
figma_page: 22081:8383
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58179:1960
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58179-1936"
figma_in_page_doc_node_id: "58179:1936"
---

# Selection Pill
Selectable pill controls for compact filters, segments, and option groups.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Selection Pill | Selection Pill | Individual selectable option |
| Selection Pill Group | Selection Pill Group | Related single-select or multi-select options |

## Anatomy
- **Container**: Rounded selectable surface
- **Label**: Option text
- **Leading icon**: Optional option cue
- **Selected indicator**: Visual state showing active selection
- **Group wrapper**: Layout that keeps related options together

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Selected | True · False | Current option state |
| State | Default · Hover · Focus · Disabled | Standard interaction states |
| Icon | On · Off | Use when it improves recognition |
| Selection Type | Single · Multi | Group-level behavior |
| Size | sm · md | Use `md` by default |

## States
Default · Hover · Focus · Selected · Disabled

## Usage
**Use when**: Users choose one or multiple compact options, especially filters or lightweight segments that should stay visible.
**Avoid when**: The value is static metadata — use Pill. For many options, use Dropdown.

## Best Practices
**Do**: Keep groups small enough to scan in one row or predictable wrap.
**Do**: Use exactly one selected option in single-select groups unless an explicit "All" or empty state exists.
**Do**: Make selected state visually distinct and accessible.
**Don't**: Use selection pills for primary actions.
**Don't**: Mix single-select and multi-select behavior in one group.

## Agent Contract
**Default choice**: Use Selection Pill for compact visible filter or segment choices.
**Selection rule**: Define whether the group is single-select or multi-select before composing it.
**Scale rule**: Use Dropdown for large option sets or options requiring search.
**Metadata rule**: Use Pill, not Selection Pill, for non-interactive labels.
**Do not invent**: Do not create custom chip filters when Selection Pill covers the interaction.

## Related
- [Pill](./pill.md)
- [Dropdowns](./dropdowns.md)
- [Tabs](./tabs.md)
