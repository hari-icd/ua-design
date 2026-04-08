---
component: Breadcrumbs
category: components
figma_page: 43:3087
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58153:41908
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58153-41904"
figma_in_page_doc_node_id: "58153:41904"
---

# Breadcrumbs
Secondary navigation showing the user's current location within a hierarchy. Provides a clickable path back to parent pages.

## Anatomy
- **Breadcrumb item**: Individual navigable step — optional leading icon + text label
- **Separator**: Chevron divider between items (not a component prop — handled by layout)
- **Current item**: Last item in trail — non-clickable, visually distinct (`Current=True`)
- **Dropdown variant**: Collapses middle items into an overflow menu (`Size=sm-with dropdown`)
- **Breadcrumb Bar**: Full-width bar variant with optional trailing action button (New UI)

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Size | sm · md | sm = 16px height, md = 24px height |
| Current | True · False | Last item is always Current=True |
| Icon | True · False | Optional leading icon per item |
| Bar Type | Default · With Button | New UI Breadcrumb Bar only |

## States
Default · Hover · Focused

(No Disabled state — items are either Current or navigable)

## Usage
**Use when**: User is 3+ levels deep in a hierarchy and needs location context or a path back.
**Avoid when**: Navigation is flat (1–2 levels); the page title or sidebar already communicates location clearly.

## Best Practices
**Do**: Always set the last item to `Current=True` — it must be non-interactive.
**Do**: Use `sm` in dense toolbars or secondary headers; `md` for primary page-level navigation.
**Do**: Use the dropdown variant when the trail exceeds 4 items.
**Do**: Use `Breadcrumb Bar` (New UI) when breadcrumbs span the full page width with an action (e.g., "Edit").
**Don't**: Use breadcrumbs as primary navigation — they are always supplemental.
**Don't**: Add icons to every item — limit to the root/home item only.

## Agent Contract
**Default choice**: Use `Size=md` for page-level breadcrumbs and `Size=sm` for dense headers/toolbars.
**Depth rule**: Use breadcrumbs when the user is 3+ hierarchy levels deep.
**Current rule**: The last item must be `Current=True` and non-interactive.
**Overflow rule**: Use the dropdown variant when the trail exceeds 4 items.
**Do not invent**: Do not use breadcrumbs as primary/global navigation; use Navigation instead.

## Related
- [Navigation](../application-components/navigation.md)
- [Headers](../application-components/headers.md)
