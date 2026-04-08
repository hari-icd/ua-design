---
component: Inputs
category: components
figma_page: 85:1269
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58148:80193
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58148-80189"
figma_in_page_doc_node_id: "58148:80189"
---

# Inputs
Text-entry fields for collecting short-form user data, search terms, IDs, and configuration values.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Input field outline | Input field_outline | Standard outlined text input |

## Anatomy
- **Label**: Text above the field describing the expected value
- **Input container**: Outlined field surface
- **Value/placeholder**: Entered text or guidance before entry
- **Leading icon**: Optional contextual icon such as search
- **Trailing icon/action**: Optional clear, reveal, status, or action icon
- **Hint/error text**: Helper or validation message below the field

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| State | Default · Hover · Focused · Disabled · Error | Reflects interaction or validation state |
| Size | sm · md | Use `md` by default |
| Label | On · Off | Prefer visible labels for forms |
| Hint Text | On · Off | Use for helper or validation detail |
| Leading Icon | On · Off | Use when the icon improves recognition |
| Trailing Icon | On · Off | Use for clear/reveal/status actions |

## States
Default · Hover · Focused · Disabled · Error

## Usage
**Use when**: The user needs to enter or edit a short text value in a form, filter, search, or settings surface.
**Avoid when**: Users choose from a fixed set of values — use Dropdown, Checkbox, Radio, or Tabs depending on the interaction.

## Best Practices
**Do**: Use labels that describe the data, not the action.
**Do**: Show error text close to the input when validation fails.
**Do**: Keep placeholder text as an example, not the only label.
**Don't**: Hide required context in placeholder text.
**Don't**: Use inputs for read-only values — use text or a copy field.

## Agent Contract
**Default choice**: Use outlined input with visible label for form fields.
**Validation rule**: Use Error state and hint/error text close to the field when validation fails.
**Placeholder rule**: Placeholder text is an example, not a replacement for the label.
**Choice rule**: If the value must come from a fixed set, use Dropdown, Checkbox, Radio, or Tabs instead.
**Do not invent**: Do not create custom field chrome when Input field_outline covers the need.

## Related
- [Dropdowns](./dropdowns.md)
- [Checkbox & Radio](./checkbox-radio.md)
- [Code Snippet](./code-snippet.md)
