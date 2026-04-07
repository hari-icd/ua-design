# Pattern: Form Page

Use this when agents need to create a standard create/edit/settings form.

## Components
- [Headers](../headers.md) for page or section title.
- [Inputs](../inputs.md) for free text values.
- [Checkbox & Radio](../checkbox-radio.md) for visible choices.
- [Dropdowns](../dropdowns.md) for compact choice sets.
- [Alerts & Notifications](../alerts-notifications.md) for blocking validation or inline status.
- [Section Footers](../section-footers.md) for anchored Save/Cancel.

## Agent Recipe
1. Start with a Page Header.
2. Group fields by meaning, not by component type.
3. Use visible labels for all fields.
4. Use Radio for 2–5 mutually exclusive options and Dropdown for larger compact lists.
5. Put persistent save/cancel actions in Section Footer when content may scroll.
6. Use Alert for blocking validation and Snackbar after successful save.

## Anti-Patterns
- Do not rely on placeholders as labels.
- Do not use a modal for a full multi-section form unless the task is truly blocking.
- Do not put two primary actions in the footer.
