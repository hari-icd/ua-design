# Agent Rules for UnifyApps Experience Creation

Global rules for agents using the UnifyApps component documentation to design or generate new product experiences.

## Read Order
1. Read this file first for global selection and composition rules.
2. Read [indexes/component-map.md](./indexes/component-map.md), [indexes/decision-map.md](./indexes/decision-map.md), or [indexes/composition-recipes.md](./indexes/composition-recipes.md) depending on the task.
3. Read the specific component docs linked from [index.md](./index.md).
4. Use each file's `figma_in_page_doc_url` as the visual reference and `figma_node_id` as the `markdown-content` source node.

## Global Agent Contract
- Prefer existing documented components before inventing custom UI.
- Choose components by semantic intent first, visual appearance second.
- Use the smallest component family that satisfies the task; do not overbuild a pattern.
- Keep one primary action per page, modal, footer, or card scope.
- Do not mix interaction models: Tabs are parallel navigation, Progress Steps are sequential progress, Dropdowns are compact choices/actions.
- Keep destructive actions explicit and visually separated from neutral actions.
- Use component states only when the state is meaningful in the flow.
- Add loading feedback only for async operations expected to take more than 300ms.
- If a component doc says a variant depends on another prop, satisfy the dependency instead of approximating.
- If no documented component fits, record the gap and propose the closest DS-aligned fallback rather than creating a one-off pattern silently.

## Component Selection Map
| Need | Use | Avoid |
|------|-----|-------|
| Trigger an action | [Button](./components/button.md) | Link-style text unless the action is inline |
| Confirm a user action briefly | [Alerts & Notifications](./components/alerts-notifications.md) → Snackbar | Persistent Alert |
| Show blocking inline status | [Alerts & Notifications](./components/alerts-notifications.md) → Alert | Toast/Snackbar |
| Show page or slideout failure | [Alerts & Notifications](./components/alerts-notifications.md) → Global Error | Inline warning |
| Represent a user | [Avatar](./components/avatar.md) | Generic icon when identity exists |
| Show hierarchy path | [Breadcrumbs](./components/breadcrumbs.md) | Primary navigation |
| Collect text input | [Inputs](./components/inputs.md) | Dropdown for freeform values |
| Pick from 2–5 mutually exclusive options | [Checkbox & Radio](./components/checkbox-radio.md) → Radio | Dropdown unless space is constrained |
| Pick multiple visible options | [Checkbox & Radio](./components/checkbox-radio.md) → Checkbox | Radio |
| Expose compact options/actions | [Dropdowns](./components/dropdowns.md) | Tabs for actions |
| Show code or copyable technical text | [Code Snippet](./components/code-snippet.md) | Editable input |
| Show indeterminate async progress | [Loading Indicator](./components/loading-indicator.md) | Progress Steps |
| Show sequential workflow progress | [Progress Steps + Timeline](./application-components/progress-steps-timeline.md) | Tabs |
| Switch parallel content views | [Tabs](./components/tabs.md) | Progress Steps |
| Place page/card/builder titles and actions | [Headers](./application-components/headers.md) | Inline text-only headers for major scopes |
| Anchor form/modal/panel actions | [Section Footers](./application-components/section-footers.md) | Inline buttons when content scrolls |
| Focus a blocking task | [Modals](./application-components/modals.md) | Navigation to a new page for quick decisions |
| Move across product areas/settings | [Navigation](./application-components/navigation.md) | Tabs for global destinations |
| Show structured records | [Tables](./application-components/tables.md) | Cards for dense comparable data |
| Upload/import files | [File Upload](./application-components/file-upload.md) | Plain input when file validation/progress matters |

## Composition Recipes
| Experience | Recommended composition |
|------------|-------------------------|
| Standard form page | Header → Inputs/Checkbox & Radio → Section Footer |
| Data table view | Header → Filter Bar/Header controls → Table → Empty/Loading/Alert state |
| Settings area | Navigation or Tabs → Header → Inputs/Checkbox & Radio → Section Footer |
| Creation wizard | Progress Steps → Inputs/Dropdowns → Section Footer |
| Confirmation modal | Modal header → concise body → Modal actions with Button hierarchy |
| Upload flow | File Upload → Uploaded File rows → Alert/Snackbar for status → Button action |
| Audit/history view | Header → Timeline or Activity Feed → Loading/Empty state |
| Detail page with sections | Breadcrumbs → Header → Tabs if sections are parallel → Cards/Tables/forms |

## Anti-Patterns
- Do not use Alert for success messages that can auto-dismiss; use Snackbar.
- Do not use Snackbar for blocking errors; use Alert or Global Error.
- Do not use Tabs for required ordered steps; use Progress Steps.
- Do not use Progress Steps for unrelated navigation.
- Do not put two Primary buttons side by side in the same scope.
- Do not use icon-only buttons without tooltip/accessibility label.
- Do not use Radio for more than 5–6 options; use Dropdown or another picker.
- Do not use a modal for passive information that can sit inline.
- Do not use a table for small key-value details; use cards or description content.
- Do not create custom upload/status rows when File Upload covers the state.

## Output Expectations for Agents
- Name the components and variants used in proposed UIs.
- Mention any unresolved DS gap explicitly.
- Link to the relevant `.md` files when explaining a design decision.
- Keep generated experiences aligned to the documented hierarchy, state, and composition rules.
