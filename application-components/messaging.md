---
component: Messaging
category: application-components
figma_page: 10021:10301
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58182:2688
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58182-2664"
figma_in_page_doc_node_id: "58182:2664"
---

# Messaging
Conversation and message-display patterns for chat, comments, assistant responses, and activity communication.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Message Bubble | Message Bubble | Individual sent or received message |
| Message Thread | Message Thread | Ordered conversation content |
| Message Composer | Message Composer | Text entry and send actions |
| Empty Messaging State | Empty Messaging State | No conversation or no messages |

## Anatomy
- **Avatar/identity**: Optional sender indicator
- **Message container**: Bubble or block holding message content
- **Message text**: Primary content
- **Metadata**: Sender, timestamp, status, or delivery state
- **Actions**: Optional reply, copy, retry, or overflow actions
- **Composer**: Input area with send and attachment controls

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Direction | Incoming · Outgoing · System | Match sender role |
| Content Type | Text · Rich Text · Attachment · Error | Reflect message payload |
| State | Default · Sending · Sent · Failed · Loading | Use for delivery lifecycle |
| Avatar | On · Off | Use when sender identity matters |
| Actions | On · Off | Show on hover or when context requires |

## States
Default · Loading · Sending · Sent · Failed · Empty

## Usage
**Use when**: Users read or send conversational content, comments, assistant responses, or threaded communication.
**Avoid when**: The content is a one-way alert or status update — use Alerts & Notifications. For chronological audit records, use Timeline.

## Best Practices
**Do**: Preserve chronological order and group repeated messages from the same sender when appropriate.
**Do**: Show failed state with retry for messages that can fail.
**Do**: Use avatar or sender label when multiple people or agents are involved.
**Don't**: Use chat bubbles for static documentation or audit logs.
**Don't**: Hide important status messages inside transient toasts when they belong in the thread.

## Agent Contract
**Default choice**: Use Messaging for conversational or threaded communication experiences.
**Identity rule**: Show sender identity when messages can come from multiple sources.
**Delivery rule**: Represent Sending, Sent, and Failed states explicitly when sending is async.
**Routing rule**: Use Alerts & Notifications for feedback and Timeline for audit history instead of Messaging.
**Do not invent**: Do not create ad hoc chat layouts when Messaging components cover the thread/composer pattern.

## Related
- [Avatar](../components/avatar.md)
- [Alerts & Notifications](../components/alerts-notifications.md)
- [Progress Steps + Timeline](./progress-steps-timeline.md)
