---
component: File Upload
category: application-components
figma_page: 1157:90306
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58153:43831
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58153-43827"
figma_in_page_doc_node_id: "58153:43827"
---

# File Upload
Upload patterns for selecting, dropping, validating, and reviewing files before or after upload.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| File Upload empty state | File Upload empty state | Dropzone or empty upload prompt |
| Uploaded File base | Uploaded File base | Row/card for an uploaded file |
| File Upload Unit | File Upload Unit | Composed upload component |

## Anatomy
- **Dropzone/container**: Area that accepts click or drag-and-drop input
- **Prompt text**: Instructional copy for allowed action
- **File constraints**: Optional size/type guidance
- **Uploaded file row**: File name, metadata, progress/status, and actions
- **Remove/retry action**: File-level controls for failed or unwanted files
- **Status indicator**: Uploading, success, error, or validation state

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| State | Empty · Uploading · Uploaded · Error · Disabled | Reflect upload lifecycle |
| File Row | Default · Progress · Error | Use for per-file status |
| Interaction | Click · Drag and drop | Support both when possible |
| Size | Default · Compact | Compact for constrained panels |

## States
Empty · Hover · Focus · Uploading · Uploaded · Error · Disabled

## Usage
**Use when**: Users need to attach, import, or upload one or more files into a workflow.
**Avoid when**: Users are only selecting an existing asset from a library — use a picker instead.

## Best Practices
**Do**: Show accepted file types and size limits before upload.
**Do**: Show file-level progress and error recovery when uploads can fail.
**Do**: Let users remove files before final submission when the flow supports it.
**Don't**: Hide validation errors after a failed upload.
**Don't**: Use upload UI for pasted text or URLs unless file import is the primary action.

## Agent Contract
**Default choice**: Use File Upload Unit for composed upload flows and Uploaded File base for each selected/uploaded file.
**State rule**: Represent lifecycle explicitly: Empty, Uploading, Uploaded, Error, or Disabled.
**Validation rule**: Show file type/size constraints before upload and file-level errors after failure.
**Recovery rule**: Provide remove or retry actions when files can fail or be changed.
**Do not invent**: Do not use a plain input when upload progress, validation, or file rows are needed.

## Related
- [Loading Indicator](../components/loading-indicator.md)
- [Alerts & Notifications](../components/alerts-notifications.md)
- [Buttons](../components/button.md)
