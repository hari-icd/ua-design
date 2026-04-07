---
component: Loading Indicator
category: components
figma_page: 22:20377
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 45:35792
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=45-35788"
figma_in_page_doc_node_id: "45:35788"
---

# Loading Indicator
Animated spinner or dot ring communicating that an async process is in progress. Always animated in production — static in Figma.

## Anatomy
- **Track**: Background ring (visible on Line styles)
- **Indicator**: Animated arc (Line) or orbiting dots (Dot circle) showing indeterminate progress
- **Container**: Fixed square bounding box; sizes the indicator proportionally

## Variants
| Property | Values | Container size |
|----------|--------|----------------|
| Style | Line simple · Line spinner · Dot circle | — |
| Size | xs · sm · md · lg · xl | ~48 · 68 · 84 · 100 · 112px |

### Style Guide
- **Line simple**: Thin static arc — minimal weight. Use for inline/embedded loading (e.g., inside a button or table cell).
- **Line spinner**: Rotating arc with tail — higher visual prominence. Use for section or page-level loading.
- **Dot circle**: Ring of animated dots — softer feel. Use for cards, modals, or empty states.

## States
Single state (always loading). No Default/Hover/Disabled variants.

## Usage
**Use when**: An async operation will take >300ms and the UI is blocked or content is pending.
**Avoid when**:
- Content structure is known → use Skeleton loaders instead.
- Progress is determinate → use a Progress Bar or Progress Steps.
- Operation is <300ms → show nothing (prevents flicker).

## Best Practices
**Do**: Match size to context — `xs/sm` for buttons or inline, `md/lg` for cards, `xl` for full-page.
**Do**: Center the indicator within its loading region.
**Don't**: Show multiple loading indicators simultaneously on the same view.
**Don't**: Use a loading indicator for synchronous operations.

## Agent Contract
**Default choice**: Use `Line spinner` for section/page loading and `Line simple` for inline/button loading.
**Timing rule**: Show only when the operation is expected to take more than 300ms.
**Scope rule**: One loading indicator per blocked region; avoid multiple simultaneous spinners on one view.
**Progress rule**: Use Progress Steps or a progress bar for determinate progress.
**Do not invent**: Do not use custom spinners when the Loading Indicator family covers the state.

## Related
- [Progress steps + Timeline](../application-components/progress-steps-timeline.md)
- [Buttons](./button.md)
