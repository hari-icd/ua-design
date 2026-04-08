---
component: Modals
category: application-components
figma_page: 172:4293
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58153:21596
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58153-21592"
figma_in_page_doc_node_id: "58153:21592"
---

# Modals
Overlay surfaces for focused tasks, confirmations, previews, and blocking decisions. Use modals when users must address content without leaving the current page.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Modal header | Modal header | Title, description, and close affordance |
| Modal actions | Modal actions | Footer action group |
| Modal Unit | Modal Unit | Standard composed modal container |
| Modal Full Screen | Modal Full Screen | Large immersive modal experience |
| Popover modal | Popover modal | Smaller contextual overlay |
| Popover header | Popover header | Header for popover-style modal |
| Docs | Docs | Documentation-oriented modal content pattern |

## Anatomy
- **Overlay/container**: Modal surface above the page
- **Header**: Title, optional description, and close action
- **Body**: Focused content or form
- **Footer/actions**: Primary and secondary actions
- **Close affordance**: Dismiss action when safe to close

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Standard · Full Screen · Popover | Choose by task size and context |
| Actions | Single · Double · Custom | Use double actions for confirm/cancel flows |
| Header | On · Off | Most modals should include a header |
| Size | Default · Full Screen · Contextual | Use full screen for complex flows |

## States
Open · Loading · Error · Dismissed

## Usage
**Use when**: Users must complete a focused task, confirm an important action, or inspect contextual content without navigating away.
**Avoid when**: The task is part of the main page flow — use inline content, side panel, or a dedicated page instead.

## Best Practices
**Do**: Make the primary action explicit and outcome-oriented.
**Do**: Use full-screen modals only for complex or immersive workflows.
**Do**: Keep destructive confirmations clear and specific.
**Don't**: Nest modals inside modals.
**Don't**: Use a modal for passive information that does not require focus.

## Agent Contract
**Default choice**: Use Modal Unit for standard focused tasks and Modal Full Screen for complex immersive flows.
**Focus rule**: Use modals only when the user must address the content before continuing.
**Action rule**: Use Modal actions with clear primary/secondary hierarchy.
**Dismissal rule**: Provide a close affordance when dismissal is safe.
**Do not invent**: Do not nest modals or use modals for passive inline information.

## Related
- [Buttons](../components/button.md)
- [Section Footers](./section-footers.md)
- [Headers](./headers.md)
