---
component: Progress Steps + Timeline
category: application-components
figma_page: 18:83802
figma_file: UglTWbSMldmsVjwl9nZbo6
figma_node_id: 45:35810
figma_in_page_doc_url: "https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=45-35806"
figma_in_page_doc_node_id: "45:35806"
---

# Progress Steps + Timeline
A family of sequential indicator and chronicle components covering wizard progress, timelines, and activity feeds.

## Sub-components Overview
| Sub-component | Use for |
|---------------|---------|
| Progress Steps Horizontal | Left-to-right step indicator for wizards |
| Progress Steps Vertical | Top-to-bottom step list with optional sub-steps |
| Progress Steps Arrow | Compact arrow-chevron stepper |
| Progress Steps Icons Horizontal | Icon-only horizontal indicator |
| Progress Steps Icons Minimal | Minimal icon strip with optional labels |
| Timeline | Chronological event sequence (Dot or Featured icon) |
| Activity | Activity feed with avatar or icon markers |

---

## 1. Progress Steps

### Anatomy
- **Step icon**: Visual status indicator (Incomplete/Current/Complete/Error)
- **Connector**: Line linking consecutive steps
- **Label**: Step name
- **Sub-label**: Optional secondary text below label
- **Sub-steps**: Nested child steps under a parent (`Sub-steps=Yes`)

### Step Status Values
| Status | Meaning |
|--------|---------|
| Incomplete | Not yet reached |
| Current | Active/in-progress |
| Complete | Successfully finished |
| Error | Failed or requires attention |

### Variants (Step Base)
| Property | Values |
|----------|--------|
| Status | Incomplete · Current · Complete · Error |
| Type | Icon left · Icon top L · Icon top C · Featured icon left · Featured icon top · Icon only · Arrow stepper |
| State | Default · Hover · Focus |

### Variants (Composed: Horizontal)
| Property | Values |
|----------|--------|
| Size | sm |
| Type | Icon top L · Icon top C · Featured icon |
| Breakpoint | Desktop |

### Variants (Composed: Vertical)
| Property | Values |
|----------|--------|
| Connector | True · False |
| Type | Icon · Icon featured |
| Sub-steps | Yes · No |

### States
Default · Hover · Focus (on interactive steps)

---

## 2. Timeline

### Anatomy
- **Marker**: Dot or featured icon at each event point
- **Connector**: Line linking markers
- **Content**: Event description alongside the marker

### Variants
| Property | Values |
|----------|--------|
| Type | Dot · Featured icon |
| Orientation | Vertical · Horizontal |
| Start Connector | True · False |

---

## 3. Activity Feed

### Anatomy
- **Marker**: Dot, featured icon, or user avatar
- **Connector**: Line between activity items
- **Content**: Activity text + timestamp

### Variants
| Property | Values |
|----------|--------|
| Type | Dot · Featured icon · Avatar |
| Orientation | Horizontal · Vertical |
| Size | xs · sm · lg |
| Start Connector | True · False |

---

## Usage
**Progress Steps — Use when**: User must complete a multi-step process in a defined order (onboarding, checkout, configuration wizard).
**Timeline — Use when**: Displaying a chronological sequence of events (version history, audit log, order tracking).
**Activity Feed — Use when**: Showing a real-time stream of user/system actions (collaboration feed, change log).

**Avoid when**:
- Steps are parallel/optional → use Tabs.
- Single step → no indicator needed.
- Timeline items are unordered → use a list.

## Best Practices
**Do**: Always show `Status=Current` on exactly one step at a time.
**Do**: Use `Sub-steps=Yes` for complex steps that have meaningful intermediate checkpoints.
**Do**: Use `Connector=False` on the last step in a vertical list.
**Do**: Use `Featured icon` type for steps where the icon category carries meaning (e.g., payment, shipping).
**Don't**: Use Progress Steps for navigation between unrelated views — use Tabs.
**Don't**: Show more than 7 top-level steps — break into phases.
**Don't**: Mix Horizontal and Vertical orientation in the same flow.

## Agent Contract
**Default choice**: Use Progress Steps for ordered workflows, Timeline for chronological events, and Activity Feed for action streams.
**Status rule**: Exactly one top-level progress step should be `Current` at a time.
**Scale rule**: Do not show more than 7 top-level steps; break longer flows into phases.
**Navigation rule**: If the sections are parallel or optional, use Tabs instead.
**Do not invent**: Do not mix horizontal and vertical progress orientations in one flow.

## Related
- [Tabs](./tabs.md)
- [Loading Indicator](./loading-indicator.md)
