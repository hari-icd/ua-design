# Decision Map

Routing rules for choosing components by user intent.

## Navigation vs Progress vs Tabs
| If the user needs to... | Use | Do not use |
|-------------------------|-----|------------|
| Move across product areas or settings | [Navigation](../navigation.md) | Tabs |
| Switch between peer sections in one context | [Tabs](../tabs.md) | Navigation |
| Complete required ordered steps | [Progress Steps + Timeline](../progress-steps-timeline.md) | Tabs |
| See a chronological history | [Progress Steps + Timeline](../progress-steps-timeline.md) → Timeline | Tabs |
| See live/user activity | [Progress Steps + Timeline](../progress-steps-timeline.md) → Activity Feed | Table unless comparison is needed |

## Feedback
| If the user needs... | Use | Do not use |
|----------------------|-----|------------|
| Persistent inline warning/info | Alert | Snackbar |
| Brief confirmation after user action | Snackbar | Alert |
| Async event notification | Notification Toast | Inline Alert unless tied to content |
| Page/slideout failure | Global Error | Snackbar |
| Expandable contextual help | Information Box | Alert for passive info |

## Forms And Choices
| If the user needs... | Use | Do not use |
|----------------------|-----|------------|
| Free text entry | [Inputs](../inputs.md) | Dropdown |
| 2–5 mutually exclusive visible options | [Checkbox & Radio](../checkbox-radio.md) → Radio | Dropdown by default |
| Multiple visible selections | [Checkbox & Radio](../checkbox-radio.md) → Checkbox | Radio |
| More than 5–6 compact choices | [Dropdowns](../dropdowns.md) | Radio |
| File attachment/import | [File Upload](../file-upload.md) | Plain input |

## Data Display
| If the user needs... | Use | Do not use |
|----------------------|-----|------------|
| Compare many records across columns | [Tables](../tables.md) | Cards |
| Show small key-value detail block | Card/detail content | Table |
| Show code/command/config | [Code Snippet](../code-snippet.md) | Input unless editable |
| Show identity in rows/comments | [Avatar](../avatar.md) | Generic icon |

## Action Placement
| If the action belongs to... | Use |
|-----------------------------|-----|
| Page/card/panel title area | [Headers](../headers.md) |
| Form or modal bottom area | [Section Footers](../section-footers.md) |
| Focused blocking overlay | [Modals](../modals.md) |
| Compact overflow/context menu | [Dropdowns](../dropdowns.md) |
| Standard command trigger | [Button](../button.md) |
