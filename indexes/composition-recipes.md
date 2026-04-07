# Composition Recipes

Reusable UI patterns assembled from documented UnifyApps components.

## Standard Form Page
Use when creating settings, creation, or edit screens.

Recommended structure:
1. [Breadcrumbs](../components/breadcrumbs.md) if the page is 3+ hierarchy levels deep.
2. [Headers](../application-components/headers.md) → Page Header with one primary action or context.
3. [Inputs](../components/inputs.md), [Checkbox & Radio](../components/checkbox-radio.md), and [Dropdowns](../components/dropdowns.md) for fields.
4. [Alerts & Notifications](../components/alerts-notifications.md) for persistent validation or status.
5. [Section Footers](../application-components/section-footers.md) for anchored Save/Cancel actions.

## Data Table Page
Use when users scan, compare, filter, and act on records.

Recommended structure:
1. [Headers](../application-components/headers.md) → Page Header.
2. Filter Bar or header controls from [Headers](../application-components/headers.md).
3. [Tables](../application-components/tables.md) for structured data.
4. [Dropdowns](../components/dropdowns.md) for row or overflow actions.
5. [Loading Indicator](../components/loading-indicator.md) or empty state during fetch/no data.
6. [Alerts & Notifications](../components/alerts-notifications.md) for blocking table errors.

## Settings Area
Use when editing configuration across multiple sections.

Recommended structure:
1. [Navigation](../application-components/navigation.md) or [Tabs](../components/tabs.md), depending on scope.
2. [Headers](../application-components/headers.md) for the selected settings section.
3. [Inputs](../components/inputs.md), [Checkbox & Radio](../components/checkbox-radio.md), and [Dropdowns](../components/dropdowns.md).
4. [Section Footers](../application-components/section-footers.md) for persistent Save/Cancel.

## Wizard Or Onboarding Flow
Use when the user must complete ordered steps.

Recommended structure:
1. [Progress Steps + Timeline](../application-components/progress-steps-timeline.md) → Progress Steps.
2. Step content with [Inputs](../components/inputs.md), [Dropdowns](../components/dropdowns.md), or [File Upload](../application-components/file-upload.md).
3. [Alerts & Notifications](../components/alerts-notifications.md) for blocking step errors.
4. [Section Footers](../application-components/section-footers.md) for Back/Continue.

## Focused Confirmation
Use when users must confirm or complete a blocking decision.

Recommended structure:
1. [Modals](../application-components/modals.md) → Modal Unit.
2. Modal header with clear title and risk/context.
3. Concise body copy.
4. Modal actions using [Button](../components/button.md) hierarchy.
5. Use Button Error only for destructive confirmation.

## Upload Flow
Use when users import or attach files.

Recommended structure:
1. [File Upload](../application-components/file-upload.md) → File Upload Unit.
2. Uploaded File base for selected files.
3. [Loading Indicator](../components/loading-indicator.md) for upload progress when indeterminate.
4. [Alerts & Notifications](../components/alerts-notifications.md) for validation errors or success confirmation.
5. [Button](../components/button.md) for submit/retry/remove actions.

## Activity Or Audit View
Use when showing chronological events.

Recommended structure:
1. [Headers](../application-components/headers.md) → Page or Card Header.
2. [Progress Steps + Timeline](../application-components/progress-steps-timeline.md) → Timeline or Activity Feed.
3. [Avatar](../components/avatar.md) for user-driven activity.
4. [Loading Indicator](../components/loading-indicator.md) for initial async load.
5. [Alerts & Notifications](../components/alerts-notifications.md) for fetch failures.
