---
component: Button
category: components
figma_page: 1:1183
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58136:5500
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58136-5496"
figma_in_page_doc_node_id: "58136:5496"
---

# Button
Primary interactive control for triggering actions. The DS includes several distinct button families; choose by semantic intent and visual weight.

## Button Families
| Family | Frame name | Use for |
|--------|-----------|---------|
| Button Brand | Buttons/Button Brand | Default product actions |
| Button AI | Buttons/Button AI | AI-powered actions |
| Button Error | Buttons/Button Error | Destructive or error-state actions |
| Button Neutral | Buttons/Button Neutral | Secondary/neutral actions |
| Button Success | Buttons/Button Success | Confirmation or success actions |
| Split Button Brand | Buttons/Split Button Brand | Primary + dropdown action |
| Split Button Neutral | Buttons/Split Button Neutral | Neutral + dropdown action |
| Link | Buttons/Link | Inline text-link style action |
| Small Icon Button | Small Icon Button | Compact icon-only action |
| Nest Chevron Button | Nest Chevron Button | Expandable/collapsible trigger |

## Anatomy
- **Label**: Button text
- **Leading icon**: Optional dot or icon before label (`Icon=Dot leading`)
- **Trailing icon**: Optional dot or icon after label (`Icon=Dot trailing`)
- **Dropdown chevron**: Split button only — secondary trigger for a menu
- **Loading indicator**: Spinner replacing label during async action (`State=Loading`)

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Size | sm · md · lg | — |
| Hierarchy | Primary · Secondary · Tertiary | Primary = filled, Secondary = outlined, Tertiary = ghost |
| Icon | Default · Dot leading · Dot trailing · None | — |
| State | Default · Hover · Focused · Disabled · Loading | — |

## States
Default · Hover · Focused · Disabled · Loading

## Usage
**Use when**: User needs to trigger an action — submit a form, save data, open a modal, navigate with intent.
**Avoid when**: Navigation without intent → use a Link. Inline text action in a sentence → use a Link button.

## Hierarchy Rules
- **One Primary** per view/section — it marks the single most important action.
- **Secondary** for supporting actions alongside a Primary.
- **Tertiary** for low-emphasis actions that don't compete visually.
- Never place two Primary buttons side by side.

## Family Selection Rules
- Use **Button Brand** (purple) as the default for all product actions.
- Use **Button Error** only for destructive actions (delete, remove, revoke) — never for general cancel/close.
- Use **Button AI** to distinguish AI-generated or AI-triggered actions.
- Use **Split Button** when an action has a primary path + 2–5 variants (e.g., "Save" + "Save as draft").

## Best Practices
**Do**: Show `State=Loading` while the button's async action is pending — disable interaction.
**Do**: Use `sm` in dense toolbars or table rows; `md` as the default; `lg` for hero/prominent CTAs.
**Don't**: Use icon-only buttons without a tooltip — always provide accessible label.
**Don't**: Mix Button Error with other button families in the same action group.

## Agent Contract
**Default choice**: Use Button Brand, `Size=md`, and hierarchy based on scope.
**Hierarchy rule**: One Primary button per page/section/modal/footer scope.
**Semantic rule**: Use Button Error only for destructive actions and Button AI only for AI-powered actions.
**Async rule**: Use `State=Loading` while an async button action is pending and disable repeat activation.
**Do not invent**: Do not create custom button styles or side-by-side Primary actions; use the documented families and hierarchy.

## Related
- [Inputs](./inputs.md)
- [Dropdowns](./dropdowns.md)
- [Loading Indicator](./loading-indicator.md)
