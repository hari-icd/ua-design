# Pattern: Wizard Flow

Use this when agents need to create ordered multi-step experiences.

## Components
- [Progress Steps + Timeline](../application-components/progress-steps-timeline.md) for current step and completion state.
- [Inputs](../components/inputs.md), [Dropdowns](../components/dropdowns.md), and [File Upload](../application-components/file-upload.md) for step content.
- [Alerts & Notifications](../components/alerts-notifications.md) for blocking step-level errors.
- [Section Footers](../application-components/section-footers.md) for Back/Continue actions.
- [Loading Indicator](../components/loading-indicator.md) for async step transitions.

## Agent Recipe
1. Use Progress Steps when the flow is ordered and required.
2. Keep exactly one step in `Current` state.
3. Keep top-level steps to 7 or fewer.
4. Use Section Footer for Back/Continue.
5. Use Alert for blocking step issues and Snackbar for successful step save.

## Anti-Patterns
- Do not use Tabs for required sequential flows.
- Do not mix horizontal and vertical progress orientation in one flow.
- Do not show more than 7 top-level steps without grouping into phases.
