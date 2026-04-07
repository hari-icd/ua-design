# UnifyApps Design System — Component Documentation

Component rules, anatomy, and usage guidelines for LLMs working with the design system.

**Figma file**: `UglTWbSMldmsVjwl9nZbo6` (`ICD-Test-DS`)
**Figma docs page**: in-page docs on each component page (node IDs in each file's frontmatter)
**Agent guide**: [agent-rules.md](./agent-rules.md)

---

## Agent Knowledge Base

Read these before individual component docs when generating new experiences:

| Artifact | Use for |
|----------|---------|
| [agent-rules.md](./agent-rules.md) | Global component selection, composition, and anti-pattern rules |
| [indexes/component-map.md](./indexes/component-map.md) | Fast component lookup by role |
| [indexes/decision-map.md](./indexes/decision-map.md) | Routing ambiguous UI choices |
| [indexes/composition-recipes.md](./indexes/composition-recipes.md) | Assembling common page/flow patterns |
| [indexes/figma-node-map.md](./indexes/figma-node-map.md) | Mapping Markdown docs to Figma nodes |
| [indexes/open-gaps.md](./indexes/open-gaps.md) | Known missing/under-specified DS areas |
| [health-checks.md](./health-checks.md) | Repeatable wiki integrity checks |

## Repository Layout

| Folder | Contents |
|--------|----------|
| [components/](./components/README.md) | Core reusable component docs and primitives |
| [application-components/](./application-components/README.md) | Larger product/application component docs |
| [indexes/](./indexes/component-map.md) | Compiled lookup maps for agents |
| [patterns/](./patterns/form-page.md) | Reusable experience recipes |

## Components

| Component | File | Category | Status |
|-----------|------|----------|--------|
| Alerts & Notifications | [alerts-notifications.md](./components/alerts-notifications.md) | components | done |
| Avatars | [avatar.md](./components/avatar.md) | components | done |
| Breadcrumbs | [breadcrumbs.md](./components/breadcrumbs.md) | components | done |
| Buttons | [button.md](./components/button.md) | components | done |
| Checkbox & Radio | [checkbox-radio.md](./components/checkbox-radio.md) | components | done |
| Code Snippet | [code-snippet.md](./components/code-snippet.md) | components | done |
| Dropdowns | [dropdowns.md](./components/dropdowns.md) | components | done |
| File Upload | [file-upload.md](./application-components/file-upload.md) | application-components | done |
| Headers | [headers.md](./application-components/headers.md) | application-components | done |
| Inputs | [inputs.md](./components/inputs.md) | components | done |
| Loading Indicator | [loading-indicator.md](./components/loading-indicator.md) | components | done |
| Modals | [modals.md](./application-components/modals.md) | application-components | done |
| Navigation | [navigation.md](./application-components/navigation.md) | application-components | done |
| Progress Steps + Timeline | [progress-steps-timeline.md](./application-components/progress-steps-timeline.md) | application-components | done |
| Section Footers | [section-footers.md](./application-components/section-footers.md) | application-components | done |
| Tables | [tables.md](./application-components/tables.md) | application-components | done |
| Tabs | [tabs.md](./components/tabs.md) | components | done |

---

## Sync
- `.md` files are the source of truth.
- Each file's `figma_node_id` points to the in-page `markdown-content` text layer.
- Each file's `figma_in_page_doc_node_id` points to the top-level in-page docs frame.
- To update Figma: edit `.md` → run `use_figma` to overwrite the `markdown-content` text layer.
- To derive `.md` from Figma: read the `markdown-content` text layer in the component's frame.
