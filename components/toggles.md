---
component: Toggles
category: components
figma_page: 1102:4631
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58179:1256
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58179-1226"
figma_in_page_doc_node_id: "58179:1226"
---

# Toggles
Binary switch controls for turning a setting on or off with immediate or saved effect.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Toggle | Toggle | Standalone on/off switch |
| Toggle Row | Toggle Row | Labeled setting row with description |

## Anatomy
- **Track**: Background surface indicating on/off state
- **Thumb**: Movable indicator showing the current state
- **Label**: Setting name or boolean option
- **Description**: Optional helper text explaining the effect
- **State indicator**: Checked/on or unchecked/off visual state

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Checked | True · False | On/off value |
| State | Default · Hover · Focus · Disabled | Standard interaction states |
| Label | On · Off | Prefer labels for settings |
| Description | On · Off | Use for non-obvious consequences |
| Size | sm · md | Use `md` by default |

## States
Default · Hover · Focus · Disabled · Checked

## Usage
**Use when**: A setting can be turned on or off and the meaning of each state is clear.
**Avoid when**: The user must choose one option from a named set — use Radio, Dropdown, Tabs, or Selection Pill.

## Best Practices
**Do**: Use positive labels that describe the enabled behavior.
**Do**: Explain consequences in description text when the setting affects data, permissions, or billing.
**Do**: Preserve focus visibility for keyboard interaction.
**Don't**: Use a toggle for one-time confirmation; use Checkbox or Button flow.
**Don't**: Pair a toggle with ambiguous labels like "Enabled" without context.

## Agent Contract
**Default choice**: Use Toggle for binary settings and Toggle Row when a label/description is needed.
**Label rule**: Label the setting, not the current state.
**Persistence rule**: If changes require Save/Cancel, place toggles in a form with Section Footer.
**Choice rule**: Use Radio or Selection Pill when the options are named alternatives rather than on/off.
**Do not invent**: Do not substitute Checkbox for a switch-style setting when Toggle is available.

## Related
- [Checkbox & Radio](./checkbox-radio.md)
- [Section Footers](../application-components/section-footers.md)
- [Inputs](./inputs.md)
