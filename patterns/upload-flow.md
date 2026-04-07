# Pattern: Upload Flow

Use this when agents need file import, validation, and review.

## Components
- [File Upload](../application-components/file-upload.md) for dropzone and uploaded file rows.
- [Loading Indicator](../components/loading-indicator.md) for indeterminate upload work.
- [Alerts & Notifications](../components/alerts-notifications.md) for validation errors and confirmations.
- [Button](../components/button.md) for submit, retry, and remove actions.

## Agent Recipe
1. Start with File Upload Unit for the upload surface.
2. Show accepted file type and size limits before upload.
3. Use Uploaded File base for each selected or uploaded file.
4. Represent each file as Empty, Uploading, Uploaded, Error, or Disabled.
5. Provide retry/remove when failure or correction is possible.
6. Use Snackbar for success and Alert for blocking validation.

## Anti-Patterns
- Do not use a plain input if progress, validation, or file rows are required.
- Do not hide file-level errors.
- Do not use upload UI for pasted text or URL entry unless importing files is primary.
