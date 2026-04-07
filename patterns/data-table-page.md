# Pattern: Data Table Page

Use this when agents need to create record browsing, filtering, and row-action experiences.

## Components
- [Headers](../headers.md) for title, filters, and page actions.
- [Tables](../tables.md) for structured row/column data.
- [Dropdowns](../dropdowns.md) for row overflow and compact actions.
- [Checkbox & Radio](../checkbox-radio.md) for row selection when bulk actions exist.
- [Loading Indicator](../loading-indicator.md) for blocked async loads.
- [Alerts & Notifications](../alerts-notifications.md) for table-level errors.

## Agent Recipe
1. Use Page Header to identify the record set.
2. Add Filter Bar or header controls when filtering/searching is needed.
3. Use Table for comparable columns.
4. Add row selection only when bulk actions are available.
5. Use overflow Dropdowns for secondary row actions.
6. Include Loading, Empty, and Error states.

## Anti-Patterns
- Do not use cards for dense comparable tabular data.
- Do not put many visible action buttons in every row.
- Do not use table layout for a small key-value summary.
