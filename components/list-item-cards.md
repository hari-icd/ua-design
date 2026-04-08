---
component: List Item Cards
category: components
figma_page: 122:3484
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58178:1761
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58178-1757"
figma_in_page_doc_node_id: "58178:1757"
---

# List Item Cards
Compact card-like rows for showing selectable or actionable records with richer content than a plain list item.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| List Item Card | List Item Card | Single card row with title, metadata, and actions |
| List Item Card Group | List Item Card Group | Stacked related records |

## Anatomy
- **Container**: Card surface or row wrapper that groups the record
- **Title**: Primary label for the item
- **Supporting text**: Optional description, metadata, or status copy
- **Leading content**: Optional icon, avatar, thumbnail, or selection control
- **Trailing content**: Optional action, badge, chevron, or overflow menu
- **Divider/spacing**: Separates stacked cards when used in a group

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| State | Default · Hover · Focus · Selected · Disabled | Use selected only for persistent selection |
| Leading Content | None · Icon · Avatar · Checkbox · Thumbnail | Match the record type |
| Trailing Content | None · Chevron · Button · Badge · Menu | Match the available action |
| Supporting Text | On · Off | Use when the title alone is not enough |
| Density | Comfortable · Compact | Compact for side panels or dense lists |

## States
Default · Hover · Focus · Selected · Disabled

## Usage
**Use when**: Users need to scan records that include labels plus secondary context, status, or per-item actions.
**Avoid when**: The data needs column comparison across many rows — use Tables instead. For simple menu choices, use Dropdown list items.

## Best Practices
**Do**: Keep the title concise and place disambiguating details in supporting text.
**Do**: Use one primary row action pattern consistently across a list.
**Do**: Use Selected state only when the item remains selected after interaction.
**Don't**: Mix unrelated record types in one card group.
**Don't**: Put too many controls in a single row; move complex actions to a detail view or side panel.

## Agent Contract
**Default choice**: Use List Item Card for record lists that need more context than a plain dropdown or table row.
**Selection rule**: Use selection controls only when bulk or persistent selection is available.
**Action rule**: Use trailing chevron for navigation and trailing menu/button for item actions.
**Density rule**: Use compact density in side panels and comfortable density in page content.
**Do not invent**: Do not create custom record rows when List Item Cards or Tables cover the need.

## Related
- [Tables](../application-components/tables.md)
- [Dropdowns](./dropdowns.md)
- [Avatar](./avatar.md)
