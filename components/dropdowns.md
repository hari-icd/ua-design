---
component: Dropdowns
category: components
figma_page: 10:15619
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 55:1632
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=55-1628"
figma_in_page_doc_node_id: "55:1628"
---

# Dropdowns
Menu and list components for exposing secondary actions, selectable options, and contextual controls from a trigger.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Dropdown list item | Dropdown list item | Individual option/action row |
| Dropdown Menu | Dropdown Menu | Composed dropdown menu surface |
| Dropdown open states | Dropdown open states | Trigger + open menu examples |
| Dropdown list header | Dropdown list header | Static menu section header |
| Dropdown list header search | Dropdown list header search | Searchable menu header |
| Dropdown list footer | Dropdown list footer | Footer action or contextual note |

## Anatomy
- **Trigger**: Button, input, or control that opens the dropdown
- **Menu surface**: Floating container that holds menu items
- **List item**: Row with optional start content, label, supporting text, and end content
- **Start content**: Default, avatar, checkbox, or toggle depending on menu intent
- **End content**: Shortcut, icon, reorder handle, or empty slot
- **Header/footer**: Optional framing content for search, grouping, or secondary action

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Start Type | Default · Avatar · Checkbox · Toggle | Controls leading visual affordance |
| End Type | Shortcut · Icon · Reorder · None | Right-side metadata or action affordance |
| Selected | On · Off | For selectable menu options |
| State | Default · Hover · Focus · Disabled | Standard interactive states |
| Divider | True · False | Adds row separation |
| Supporting Text | On · Off | Adds helper/description text |
| Size | sm · md | Use `sm` for dense menus, `md` by default |

## States
Default · Hover · Focus · Disabled · Selected

## Usage
**Use when**: A control needs to expose a compact list of actions, filters, destinations, or selectable options without taking persistent page space.
**Avoid when**: The choices are few and always visible — use buttons, tabs, or checkboxes instead. For long searchable datasets, use a command palette or dedicated picker.

## Best Practices
**Do**: Keep item labels short and action-oriented.
**Do**: Use supporting text only when the label alone is ambiguous.
**Do**: Use checkbox/toggle start types only for multi-select or stateful menu rows.
**Don't**: Mix unrelated action groups without dividers or headers.
**Don't**: Put destructive actions next to neutral actions without clear visual separation.

## Agent Contract
**Default choice**: Use Dropdown Menu with `Dropdown list item` rows for compact actions or option lists.
**Selection rule**: Use `Selected=On` only when the menu represents current state or a selectable option.
**Grouping rule**: Use headers, dividers, or footers when menu items mix categories or actions.
**Scale rule**: Use Dropdown for compact lists; use a dedicated picker or command palette for large searchable datasets.
**Do not invent**: Do not create custom menu rows when documented start/end types cover the row.

## Related
- [Buttons](./button.md)
- [Checkbox & Radio](./checkbox-radio.md)
- [Inputs](./inputs.md)
