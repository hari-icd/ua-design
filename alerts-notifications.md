---
component: Alerts & Notifications
category: components
figma_page: 21:11576
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 45:35798
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=45-35794"
figma_in_page_doc_node_id: "45:35794"
---

# Alerts & Notifications
A family of feedback components. Each sub-component serves a distinct feedback context — choose based on persistence, trigger, and content richness.

## Sub-components Overview
| Sub-component | Persistence | Trigger | Use for |
|---------------|-------------|---------|---------|
| Alert | Persistent | System/content | Inline warnings, status, blocking info |
| Snackbar | Transient (auto-dismiss) | User action | Brief confirmations |
| Notification (Toast) | Transient | Async event | Richer event updates |
| Information Box | Persistent, collapsible | Contextual | Expandable help/context |
| Global Error | Persistent | System failure | Page-level or slideout errors |
| Notification Panel | Persistent | On demand | Full notification history/inbox |

---

## 1. Alert
Persistent inline message for status, warnings, or information directly related to nearby content.

### Anatomy
- **Icon**: Semantic color icon (left-aligned)
- **Message**: Primary text; second line available when `Double Stack=On`
- **Actions**: Optional inline link or button (right-aligned)
- **Close**: Optional dismiss icon

### Variants
| Property | Values |
|----------|--------|
| Size | sm · md · lg |
| Color | Default · Grey · Brand · Error · Warning · Success |
| Double Stack | On · Off |

---

## 2. Snackbar
Transient bottom-anchored message. Auto-dismisses after a short delay.

### Anatomy
- **Icon**: Semantic indicator
- **Message**: Short confirmation text (1 line)
- **Description**: Optional secondary line (`Description=On`)
- **Close**: Optional manual dismiss

### Variants
| Property | Values |
|----------|--------|
| Color | Brand · Neutral · Grey · Error · Warning · Success |
| Description | On · Off |

---

## 3. Notification (Toast)
Floating overlay notification, richer than Snackbar. Appears at a screen edge for async events.

### Variants
| Property | Values |
|----------|--------|
| Type | Primary icon · Gray icon · Success icon · Warning icon · Error icon · No icon · Avatar · Image · Progress indicator |
| Breakpoint | Desktop |

---

## 4. Information Box
Collapsible contextual block. Shows summary when closed (`Open=Off`), full content when expanded (`Open=On`).

### Variants
| Property | Values |
|----------|--------|
| Color | Brand · Default · Error · Warning · Success |
| Open | On · Off |

---

## 5. Global Error
Full-area error state for critical failures.

### Variants
| Property | Values |
|----------|--------|
| Type | Page · Slideout |

---

## 6. Notification Panel
Full notification center listing recent events. Supports empty state and action menu.

### Variants
| Property | Values |
|----------|--------|
| Platform | Web · Mobile |
| States | Default · 3 dots · Empty |

---

## Color Semantics
| Color | Meaning |
|-------|---------|
| Default | Neutral / informational |
| Grey | Subtle / low-emphasis |
| Brand | Product-initiated / feature callout |
| Error | Failure, destructive, invalid |
| Warning | Caution, potential issue |
| Success | Completed, positive outcome |

---

## Usage Decision Tree
1. **Inline, must-read, tied to content** → Alert
2. **Confirms a user action (save, delete, copy)** → Snackbar
3. **Async event not triggered by user** → Notification (Toast)
4. **Collapsible contextual help** → Information Box
5. **Page or slideout failed to load** → Global Error
6. **Notification history/inbox** → Notification Panel

## Best Practices
**Do**: Match color strictly to semantic meaning.
**Do**: Use Snackbar for success confirmations; Alert for warnings requiring attention before proceeding.
**Do**: Stack max 3 Toasts simultaneously — dismiss oldest when limit is reached.
**Do**: Use `Double Stack=On` for alerts with a short description (max 2 lines).
**Don't**: Auto-dismiss Alerts — only Snackbars and Toasts auto-dismiss.
**Don't**: Use Alert for non-blocking info that doesn't affect the user's task — use Information Box.
**Don't**: Use Error color for warnings or neutral info.

## Agent Contract
**Default choice**: Use Alert for persistent inline feedback and Snackbar for transient confirmations.
**Route by trigger**: User-action confirmation → Snackbar; async event → Notification Toast; page/slideout failure → Global Error.
**State rule**: Alerts are not auto-dismissed; Snackbars and Toasts may auto-dismiss.
**Semantic rule**: Color must match the actual meaning, not the desired visual emphasis.
**Do not invent**: Use the documented Alert/Snackbar/Toast/Information Box/Global Error/Notification Panel family before creating custom feedback UI.

## Related
- [Buttons](./button.md)
- [Loading Indicator](./loading-indicator.md)
- [Modals](./modals.md)
