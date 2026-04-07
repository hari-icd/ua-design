---
component: Tables
category: application-components
figma_page: 21:7605
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 55:22832
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=55-22828"
figma_in_page_doc_node_id: "55:22828"
---

# Tables
Data display components for scanning, comparing, sorting, and acting on structured records.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Table | Table | Composed table pattern |
| Table cell | Table cell | Individual body cell |
| Col Header Cell | Col Header Cell | Column header container |
| _Col Header Text | _Col Header Text | Header text content and sort affordance |

## Anatomy
- **Header row**: Column labels and optional sort controls
- **Body rows**: Records displayed in cells
- **Cell content**: Text, badges, avatars, controls, or custom content
- **Selection controls**: Optional checkbox selection for bulk workflows
- **Actions**: Row-level or table-level actions
- **Pagination/loading state**: External or composed table controls when needed

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Cell Type | Text · Custom · Action · Selection | Match the data/content need |
| Header State | Default · Hover · Sorted | Use sorted state for active sort column |
| Row State | Default · Hover · Selected · Disabled | Selected supports bulk actions |
| Density | Default · Compact | Compact for dense operational tables |

## States
Default · Hover · Selected · Disabled · Sorted · Loading · Empty

## Usage
**Use when**: Users need to scan or compare multiple records across consistent columns.
**Avoid when**: Content is unstructured, narrative, or card-like — use a list or card layout instead.

## Best Practices
**Do**: Keep column labels short and specific.
**Do**: Align numeric values consistently.
**Do**: Use selection only when bulk actions are available.
**Do**: Provide an empty state when no rows exist.
**Don't**: Put too many actions in every row — use overflow menus when needed.
**Don't**: Use tables for small two-column details; use description lists or cards.

## Agent Contract
**Default choice**: Use Table for structured records with comparable columns.
**Density rule**: Use compact density only for operational tables where scanning efficiency matters.
**Selection rule**: Use row selection only when bulk actions are available.
**State rule**: Account for Loading and Empty states in table experiences.
**Do not invent**: Do not use tables for small key-value detail blocks or unstructured content.

## Related
- [Checkbox & Radio](../components/checkbox-radio.md)
- [Dropdowns](../components/dropdowns.md)
- [Headers](./headers.md)
