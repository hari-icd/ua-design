# Open Gaps

Known gaps or follow-up candidates for the UnifyApps design-system knowledge base.

## Missing Or Under-Specified Components
- Toggle/Switch is referenced in [checkbox-radio.md](../components/checkbox-radio.md) and [dropdowns.md](../components/dropdowns.md), but there is no dedicated Toggle/Switch doc in this folder.
- Pagination appears in the Figma file page list but is not currently represented as a component doc.
- Side Panel appears in the broader Figma file but is not currently represented as a component doc.
- Messaging appears in the broader Figma file but is not currently represented as a component doc.
- Empty states are referenced by patterns and Figma page inventory but are not currently represented as a component doc.

## Under-Specified Details
- Exact design tokens for spacing, type styles, and colors are not captured in these Markdown docs yet.
- Some variant values are inferred from visible Figma component names and may need confirmation against component properties.
- Accessibility specifics such as ARIA roles, keyboard behavior, focus order, and tooltip requirements are only partially documented.
- Responsive behavior is mostly high-level and needs more explicit breakpoint rules.

## Suggested Next Articles
- `toggles.md`
- `pagination.md`
- `side-panel.md`
- `empty-states.md`
- `accessibility-rules.md`
- `design-tokens.md`

## Agent Rule
When a requested UX depends on a gap above, use the closest documented component, state the gap, and add a follow-up note here instead of inventing undocumented UI silently.
