---
component: Headers
category: application-components
figma_page: 15:37845
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 55:7012
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=55-7008"
figma_in_page_doc_node_id: "55:7008"
---

# Headers
Structural header patterns for pages, cards, filters, builders, and sections. Use the header family to establish context and place high-priority actions consistently.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Header | Header | Generic title/action header block |
| Section label | Section label | Compact section title or label |
| Page Header | Page Header | Page-level title, metadata, and actions |
| Card Header | Card Header | Header area inside cards or panels |
| Filter Bar | Filter Bar | Filter/action row above data views |
| Automation Builder Sub Header Bar | Automation Builder Sub Header Bar | Builder sub-header controls |
| LC Builder Header + Preview Bar | LC Builder Header + Preview Bar | Builder header paired with preview controls |
| Builder header | Builder header | Builder/editor header region |

## Anatomy
- **Title**: Primary heading for the page, card, or section
- **Description/metadata**: Optional supporting context
- **Primary action**: Main action for the current scope
- **Secondary actions**: Supporting controls, filters, or menus
- **Breadcrumb/context**: Optional navigation context above or beside the title
- **Divider/bar**: Optional separator from content below

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Page · Card · Filter · Builder · Section | Choose by structural context |
| Actions | None · Single · Multiple | Keep action hierarchy clear |
| Metadata | On · Off | Use when additional context is needed |
| Density | Default · Compact | Compact for panels and dense app surfaces |

## States
Headers are structural. Interactive child controls carry their own states.

## Usage
**Use when**: A page, panel, card, or builder region needs a stable title and action area.
**Avoid when**: The content block is too small to need a header — use inline text or a section label instead.

## Best Practices
**Do**: Keep one primary action per header scope.
**Do**: Use Page Header for top-level page context and Card Header for contained surfaces.
**Do**: Pair Filter Bar with data-heavy tables or lists.
**Don't**: Stack multiple header patterns for the same scope.
**Don't**: Put low-priority actions in the primary action slot.

## Agent Contract
**Default choice**: Use Page Header for page scope, Card Header for contained surfaces, and Filter Bar above tables/lists.
**Scope rule**: A header owns the title and primary action for its immediate region only.
**Action rule**: Keep one primary action per header scope; move overflow actions into Dropdowns.
**Builder rule**: Use builder-specific headers for builder/editor contexts instead of generic page headers.
**Do not invent**: Do not stack multiple header patterns for the same content scope.

## Related
- [Buttons](./button.md)
- [Breadcrumbs](./breadcrumbs.md)
- [Tabs](./tabs.md)
- [Navigation](./navigation.md)
