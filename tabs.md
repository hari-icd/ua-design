---
component: Tabs
category: components
figma_page: 20:3102
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 45:35804
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=45-35800"
figma_in_page_doc_node_id: "45:35800"
---

# Tabs
Navigation pattern for switching between related views or content sections within the same context. Multiple tab families serve different structural and semantic needs.

## Tab Families
| Family | Frame | Use for |
|--------|-------|---------|
| Horizontal tabs | Horizontal tabs | Standard top-nav tabs |
| Vertical tabs | Vertical tabs | Side-nav or settings tabs |
| Filter Tabs | Filter Tabs Base | Filtering/segmenting a list or dataset |
| Folder Tabs | _Folder Tab base / _Folder tab base double line | Layered document/section navigation |
| Progress Tabs | Progress Tab base | Step-based wizard navigation |
| Step Arrows | Step Arrows | Arrow-chevron stepper navigation |

## Anatomy (Tab Item)
- **Label**: Tab name text
- **Badge**: Optional count/status indicator (`Badge=True`)
- **Active indicator**: Underline (Horizontal) or left border (Vertical) on `Current=True` tab
- **Destructive marker**: Visual warning on tabs with destructive content (`Destructive=True`)

## Variants (Tab Base)
| Property | Values | Notes |
|----------|--------|-------|
| Align | Horizontal · Vertical | Horizontal = top bar, Vertical = side |
| Size | sm | Single size in current DS |
| Current | True · False | Active/selected tab |
| Badge | True · False | Count badge visible |
| Destructive | True · False | Tab contains destructive or warning content |
| State | Default · Hover · Focus · Disabled | — |

## States
Default · Hover · Focus · Disabled

## Usage
**Use when**: Content splits into 2–7 parallel sections the user switches between without losing context.
**Avoid when**:
- Steps are sequential and must be completed in order → use Progress Steps instead.
- Filtering a dataset → use Filter Tabs or a Dropdown.
- Only 2 options → consider a Toggle/Segmented control.
- More than 7 tabs → rethink the IA or use a sidebar nav.

## Family Selection Rules
- **Horizontal tabs**: Default for most page-level tab navigation (detail pages, settings).
- **Vertical tabs**: Settings pages, left-rail navigation within a panel.
- **Filter Tabs**: Filtering or segmenting a list — semantically a filter, not navigation.
- **Folder Tabs**: Document/file-style interfaces with layered context.
- **Progress Tabs**: Multi-step wizards where tabs double as progress indicators — use with Progress Steps component.

## Best Practices
**Do**: Always have exactly one `Current=True` tab visible.
**Do**: Use `Badge=True` to surface counts (unread items, errors) without requiring tab activation.
**Do**: Keep tab labels short — 1–2 words; use nouns not verbs (e.g., "Overview" not "View Overview").
**Do**: Use `Destructive=True` on tabs that surface deletion or irreversible actions.
**Don't**: Use tabs for sequential flows — use Progress Steps.
**Don't**: Disable a tab without explaining why — prefer hiding it or showing an empty state.
**Don't**: Nest tabs within tabs — creates disorienting hierarchy.

## Agent Contract
**Default choice**: Use Horizontal tabs for page-level parallel sections and Vertical tabs for settings/panel navigation.
**Current rule**: Exactly one tab should have `Current=True`.
**Count rule**: Use tabs for 2–7 related sections; reconsider IA above 7 tabs.
**Flow rule**: Use Progress Steps for required sequential flows.
**Do not invent**: Do not nest tabs within tabs or use tabs for unrelated global destinations.

## Related
- [Progress Steps + Timeline](./progress-steps-timeline.md)
- [Navigation](./navigation.md)
- [Headers](./headers.md)
