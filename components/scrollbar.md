---
component: Scrollbar
category: components
figma_page: 30309:23743
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58179:1265
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58179-1261"
figma_in_page_doc_node_id: "58179:1261"
---

# Scrollbar
Scroll affordance for constrained content areas, panels, menus, and dense lists.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Scrollbar | Scrollbar | Vertical or horizontal scroll indicator |
| Scroll Area | Scroll Area | Content container with visible overflow affordance |

## Anatomy
- **Track**: Full scrollable range
- **Thumb**: Current viewport position and approximate viewport size
- **Scrollable content**: Area clipped by the container
- **Edge spacing**: Padding that prevents content from colliding with the scrollbar

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Orientation | Vertical · Horizontal | Match content overflow direction |
| State | Default · Hover · Dragging · Disabled | Dragging only during direct manipulation |
| Visibility | Auto · Always | Prefer auto unless the area must signal overflow |
| Size | sm · md | Use `sm` in compact overlays |

## States
Default · Hover · Dragging · Disabled

## Usage
**Use when**: A fixed-height or fixed-width area contains overflow content and users need a visible scroll affordance.
**Avoid when**: The full content can fit naturally in the page flow. Do not add nested scrollbars unless the parent container must remain fixed.

## Best Practices
**Do**: Keep scrollbars inside the scroll container edge.
**Do**: Preserve enough right or bottom padding so content does not sit under the scrollbar.
**Do**: Use one primary scroll area per panel when possible.
**Don't**: Create nested scroll areas unless the interaction requires independent scrolling.
**Don't**: Use custom scrollbars for decoration when there is no overflow.

## Agent Contract
**Default choice**: Use Scrollbar only for constrained overflow regions.
**Containment rule**: Keep the scrollbar visually attached to the scroll area it controls.
**Nesting rule**: Avoid nested scrolling; prefer a single scroll body plus fixed header/footer.
**Visibility rule**: Use always-visible scrollbar when discoverability of overflow is important.
**Do not invent**: Do not draw decorative scrollbar tracks without scrollable content.

## Related
- [Side Panel](../application-components/side-panel.md)
- [Dropdowns](./dropdowns.md)
- [Tables](../application-components/tables.md)
