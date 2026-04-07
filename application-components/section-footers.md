---
component: Section Footers
category: application-components
figma_page: 16:41061
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 47:4260
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=47-4256"
figma_in_page_doc_node_id: "47:4256"
---

# Section Footers
Sticky or anchored footer bars that hold primary actions for a section, panel, modal, or builder canvas. Three distinct footer contexts are provided.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Section footer | Section footer | Page-section or modal action bar |
| Side panel footer | Side panel footer | Slideout/side panel action area |
| Builder footer | Builder Footer | Canvas builder confirmation area |

---

## 1. Section Footer
Action bar at the bottom of a page section or modal content area.

### Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Default · 1120 · 800 | Width variants — Default=full, 1120=constrained, 800=narrow |

---

## 2. Side Panel Footer
Action area anchored to the bottom of a slideout side panel.

### Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Double Button · Message | Double Button = primary + secondary action; Message = status text + action |

---

## 3. Builder Footer
Action bar within a canvas-style builder or editor.

### Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Slide Up · Actions | Slide Up = footer that animates in on change; Actions = persistent action strip |

---

## Anatomy
- **Primary action**: Main CTA button (Save, Continue, Apply)
- **Secondary action**: Cancel, Back, or secondary button
- **Message/status**: Optional text for context or validation feedback (Side panel footer)
- **Divider**: Top border separating footer from scrollable content

## States
Footers are structural components — individual buttons inside carry their own states.

## Usage
**Section footer — Use when**: A form, wizard step, or modal needs persistent primary + secondary actions that stay visible while content scrolls.
**Side panel footer — Use when**: A slideout panel requires confirmation actions before close (settings, filters, detail editors).
**Builder footer — Use when**: A canvas/builder has unsaved state — the footer appears to prompt save/discard.

**Avoid when**:
- Actions are inline within the content → place buttons in context.
- No confirm/cancel pattern needed → omit the footer.

## Best Practices
**Do**: Always pair a primary action with a secondary (Cancel/Back) in footers.
**Do**: Use `Type=1120` or `Type=800` Section footer variants to match the content container width — don't let the footer span wider than the form it belongs to.
**Do**: Use `Type=Slide Up` Builder footer to avoid visual noise when there are no unsaved changes.
**Do**: Keep footer action labels consistent across a flow — "Save" not "Save changes" on one step and "Apply" on another.
**Don't**: Stack two footers — if a page section and a modal both need footers, the modal footer takes priority.
**Don't**: Put more than 2 actions in a section footer — escalate to a Button group or move actions inline.

## Agent Contract
**Default choice**: Use Section footer for page/modal sections, Side panel footer for slideouts, and Builder Footer for builder canvases.
**Action rule**: Pair primary and secondary actions in footers, usually Save/Continue plus Cancel/Back.
**Width rule**: Match constrained footer variants to the content width.
**Priority rule**: If a modal and page both have footers, the modal footer takes priority.
**Do not invent**: Do not stack footers or put more than 2 actions in a section footer.

## Related
- [Buttons](../components/button.md)
- [Modals](./modals.md)
- [Headers](./headers.md)
