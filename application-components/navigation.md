---
component: Navigation
category: application-components
figma_page: 82:1862
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58153:33921
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58153-33917"
figma_in_page_doc_node_id: "58153:33917"
---

# Navigation
Application navigation patterns for moving across product areas, nested settings, breadcrumbs, and builder-specific nav structures.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| New_Platform Navigation | New_Platform Navigation | Primary platform navigation shell |
| Base_Platform Nav Menu Unit | Base_Platform Nav Menu Unit | Top-level nav item |
| Base_Platform Nav Sub-Menu Unit | Base_Platform Nav Sub-Menu Unit | Nested nav item |
| Base_Platform Nav Project Unit | Base_Platform Nav Project Unit | Project/workspace nav item |
| Base_Platform Nav User Avatar Unit | Base_Platform Nav User Avatar Unit | User/account nav area |
| Tentant Switcher | Tentant Switcher | Tenant/workspace switching |
| Settings_Nav item base | Settings_Nav item base | Settings sidebar item |
| Settings_Nav item dropdown base | Settings_Nav item dropdown base | Expandable settings item |
| Secondary navigation | Secondary navigation | Secondary nav group |
| Tertiary navigation | Tertiary navigation | Third-level nav group |
| Automation nav | Automation nav | Automation-specific navigation |
| New UI - Breadcrumb Bar | New UI - Breadcrumb Bar | Page hierarchy breadcrumb bar |

## Anatomy
- **Navigation container**: Sidebar, rail, or top-level shell
- **Nav item**: Icon, label, active state, and optional badge/count
- **Sub-menu**: Nested navigation under a parent item
- **Project/tenant switcher**: Context selector for workspace-like scopes
- **User area**: Account/avatar section and related actions
- **Breadcrumb bar**: Hierarchical page context

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Level | Primary · Secondary · Tertiary | Match information architecture depth |
| State | Default · Hover · Focus · Active · Disabled | Active marks current location |
| Expanded | True · False | For nested or collapsible nav |
| Icon | On · Off | Use icons for primary product areas |
| Badge | On · Off | Counts, alerts, or status |

## States
Default · Hover · Focus · Active · Disabled · Expanded

## Usage
**Use when**: Users need persistent movement across product areas, settings, nested app sections, or builder workflows.
**Avoid when**: Content switching is local to one page section — use Tabs instead.

## Best Practices
**Do**: Show exactly one active item per navigation level.
**Do**: Keep labels short and stable.
**Do**: Use secondary/tertiary navigation only when hierarchy is meaningful.
**Don't**: Use navigation items as action buttons.
**Don't**: Hide critical destinations behind unclear icons.

## Agent Contract
**Default choice**: Use New_Platform Navigation for global product navigation and Settings navigation patterns for settings areas.
**Active rule**: Show exactly one active item per navigation level.
**Hierarchy rule**: Use secondary/tertiary navigation only when the IA requires depth.
**Action rule**: Navigation items move users to locations; use Buttons or Dropdowns for actions.
**Do not invent**: Do not create custom nav rails, breadcrumbs, or tenant switchers outside this family.

## Related
- [Breadcrumbs](../components/breadcrumbs.md)
- [Tabs](../components/tabs.md)
- [Headers](./headers.md)
