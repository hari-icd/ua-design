---
component: Pill
category: components
figma_page: 12:539
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58178:4648
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58178-4624"
figma_in_page_doc_node_id: "58178:4624"
---

# Pill
Compact rounded labels for status, metadata, categories, and lightweight inline attributes.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Pill | Pill | Static label or metadata chip |
| Pill Group | Pill Group | Multiple related labels |

## Anatomy
- **Container**: Rounded surface that frames the label
- **Label**: Short text value
- **Leading icon**: Optional semantic or category icon
- **Trailing dismiss**: Optional remove affordance for removable pills
- **Color**: Semantic treatment for status or category

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Color | Default · Grey · Brand · Error · Warning · Success | Match semantic meaning |
| Size | sm · md | Use `sm` in dense rows |
| Icon | None · Leading · Trailing · Both | Use sparingly |
| Removable | True · False | Only when users can remove the value |
| State | Default · Hover · Focus · Disabled | Interactive only when removable/clickable |

## States
Default · Hover · Focus · Disabled

## Usage
**Use when**: A short status, category, filter value, or attribute needs to be visually grouped but not treated as a primary action.
**Avoid when**: The user is choosing among values — use Selection Pill. For alerts or feedback, use Alerts & Notifications.

## Best Practices
**Do**: Keep labels short, ideally one to three words.
**Do**: Use semantic colors consistently with the meaning of the status.
**Do**: Use removable pills only when the removal action is safe and expected.
**Don't**: Use pills as buttons for primary actions.
**Don't**: Use Error or Warning colors for visual emphasis without semantic meaning.

## Agent Contract
**Default choice**: Use Pill for static metadata and status labels.
**Semantic rule**: Color represents meaning, not decoration.
**Interaction rule**: If the pill changes selection state, use Selection Pill instead.
**Removal rule**: Show dismiss affordance only for removable values.
**Do not invent**: Do not create custom badges when Pill covers the metadata/status need.

## Related
- [Selection Pill](./selection-pill.md)
- [Alerts & Notifications](./alerts-notifications.md)
- [Tables](../application-components/tables.md)
