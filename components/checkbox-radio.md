---
component: Checkbox & Radio
category: components
figma_page: 9:14766
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 47:4103
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=47-4099"
figma_in_page_doc_node_id: "47:4099"
---

# Checkbox & Radio
Selection controls for choosing options in forms or lists. The DS combines both types in one page — Checkbox for multi-select, Radio for single-select.

## Anatomy
- **Control**: Visual indicator — square (Checkbox) or circle (Radio); xs=14px, sm=16px
- **Label**: Adjacent text describing the option (`Text=True`)
- **Hint text**: Secondary helper text below the label (`Hint Text=True`; requires `Text=True`)
- **Checkbox List**: Layout wrapper for grouped options — Single Column or Double Column

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Checkbox · Radio | Multi-select vs. single-select |
| Size | xs · sm | xs=14px control, sm=16px control |
| Checked | True · False | Selected state |
| Indeterminate | True · False | Checkbox only — partial group selection |
| Text | True · False | With or without label |
| Hint Text | True · False | Requires Text=True |
| List Type | Single Column · Double Column | Checkbox List wrapper only |

## States
Default · Hover · Focused · Disabled

## Usage
**Use when**:
- Checkbox: user can select multiple items, or toggling a standalone boolean.
- Radio: user must choose exactly one from 2–5 mutually exclusive options.

**Avoid when**:
- More than 5–6 options → use Dropdown instead.
- Binary on/off toggle → use a Toggle/Switch component.
- Single yes/no confirmation → consider a Checkbox with no group.

## Best Practices
**Do**: Always pair with a visible label (`Text=True`) unless context is unambiguous (e.g., table column header).
**Do**: Use `Indeterminate` on a parent Checkbox when only some children in a group are selected.
**Do**: Use Checkbox List wrapper for 3+ stacked options to maintain consistent spacing.
**Don't**: Mix Checkbox and Radio in the same option group.
**Don't**: Pre-select Radio options unless there is a clear, safe default.
**Don't**: Use Radio for more than 5–6 options — switch to Dropdown.

## Agent Contract
**Default choice**: Use Checkbox for multi-select or standalone boolean choices; use Radio for 2–5 mutually exclusive visible options.
**Dependency rule**: `Hint Text=True` requires `Text=True`.
**Indeterminate rule**: Use `Indeterminate=True` only for parent checkboxes with partially selected children.
**Overflow rule**: For more than 5–6 radio options, use Dropdown or another picker.
**Do not invent**: Do not mix Checkbox and Radio in one option group or create custom selection controls.

## Related
- [Dropdowns](./dropdowns.md)
- [Inputs](./inputs.md)
