---
component: Side Panel
category: application-components
figma_page: 9501:2358
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58182:2406
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58182-2382"
figma_in_page_doc_node_id: "58182:2382"
---

# Side Panel
Slideout surface for contextual detail, editing, filters, or secondary workflows without leaving the current page.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Side Panel | Side Panel | Standard slideout container |
| Side Panel Header | Side Panel Header | Title, description, and close action |
| Side Panel Body | Side Panel Body | Scrollable content region |
| Side Panel Footer | Side panel footer | Anchored actions or message footer |

## Anatomy
- **Panel surface**: Elevated container attached to the side of the viewport
- **Header**: Title, optional description, and close affordance
- **Body**: Scrollable content, form, details, or list
- **Footer**: Optional fixed action area
- **Scrim/underlay**: Optional page overlay when focus should stay in the panel
- **Close affordance**: Dismiss action when safe to close

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Width | sm · md · lg · Custom | Match task complexity |
| Footer | None · Double Button · Message | Use footer when confirmation is needed |
| State | Open · Loading · Error · Empty | Reflect panel content lifecycle |
| Placement | Right · Left | Right is the default for contextual detail |

## States
Open · Loading · Error · Empty · Dismissed

## Usage
**Use when**: Users need contextual detail, filtering, or lightweight editing while preserving page context.
**Avoid when**: The task is blocking and must be completed before continuing — use Modals. For large multi-step work, use a dedicated page or full-screen modal.

## Best Practices
**Do**: Keep the parent page context visible when the panel is supporting a selection or table row.
**Do**: Use Side panel footer for Save/Cancel or Apply/Clear actions.
**Do**: Keep the header fixed when body content scrolls.
**Don't**: Stack multiple side panels.
**Don't**: Use a side panel for passive notifications or short confirmations.

## Agent Contract
**Default choice**: Use Side Panel for contextual details, filters, and lightweight edit forms.
**Footer rule**: Use Side panel footer when the user must apply or save changes.
**Scroll rule**: Keep header/footer fixed and body scrollable for long content.
**Escalation rule**: Use Modal for blocking confirmation and a full page for complex multi-step tasks.
**Do not invent**: Do not stack side panels or use custom slideouts when Side Panel covers the need.

## Related
- [Section Footers](./section-footers.md)
- [Modals](./modals.md)
- [Headers](./headers.md)
