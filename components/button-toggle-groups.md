---
component: Button+Toggle Groups
category: components
figma_page: 16:399
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58200:1532
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58200-1508"
figma_in_page_doc_node_id: "58200:1508"
---

# Button+Toggle Groups
Grouped controls for presenting a compact set of visible actions or mutually exclusive options in one horizontal or wrapped cluster.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Button group | Button group | Cluster of related action buttons |
| Toggle group | Toggle group | Visible segmented set of selectable options |

## Anatomy
- **Group container**: Shared wrapper that aligns the controls as one unit
- **Item button/toggle**: Individual action or option within the group
- **Selected/active item**: The currently active toggle in a selection group
- **Spacing/dividers**: Shared rhythm between grouped controls
- **Label/icon**: Optional item content that communicates the action or option

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Button group · Toggle group | Action cluster vs. selectable segment group |
| Selection | Single · None | Toggle groups are typically single-select |
| Size | sm · md · lg | Match surrounding controls |
| State | Default · Hover · Focus · Disabled · Selected | `Selected` applies to toggle groups |
| Icon | On · Off | Use when icons improve recognition |

## States
Default · Hover · Focus · Disabled · Selected

## Usage
**Use when**: Users need a compact set of closely related actions or a visible set of short peer options.
**Avoid when**: There are too many options to scan comfortably — use Dropdown. If the options represent page-level navigation, use Tabs instead.

## Selection Rules
- Use **Button group** when each item triggers an action.
- Use **Toggle group** when the controls represent a current selected mode, filter, or view.
- Keep toggle groups to short labels and a small number of visible options.
- Use exactly one selected item in single-select toggle groups unless an explicit empty state is supported.

## Best Practices
**Do**: Keep all items in a group consistent in size and hierarchy.
**Do**: Use toggle groups for mode or filter switches that should remain visible.
**Do**: Use button groups for tightly related actions in toolbars, editors, and dense surfaces.
**Don't**: Mix action buttons and selected-state toggles in the same group.
**Don't**: Use a button group when the controls are actually navigation tabs.

## Agent Contract
**Default choice**: Use Button group for clustered actions and Toggle group for visible segmented selection.
**Action rule**: If clicking an item performs an action immediately, use Button group.
**Selection rule**: If clicking an item changes the active option or view, use Toggle group.
**Scale rule**: If the option count grows beyond a compact visible group, switch to Dropdown or Tabs based on intent.
**Do not invent**: Do not create custom segmented controls when Button group or Toggle group covers the need.

## Related
- [Buttons](./button.md)
- [Toggles](./toggles.md)
- [Tabs](./tabs.md)
- [Dropdowns](./dropdowns.md)
