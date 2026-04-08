---
component: Sliders
category: components
figma_page: 1086:1423
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58178:2062
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58178-2038"
figma_in_page_doc_node_id: "58178:2038"
---

# Sliders
Range controls for adjusting numeric values directly along a bounded scale.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Slider | Slider | Single-value range input |
| Range Slider | Range Slider | Min/max interval selection |

## Anatomy
- **Track**: Full available value range
- **Active track**: Selected portion of the range
- **Thumb**: Draggable handle for the current value
- **Value label**: Optional current value or range readout
- **Min/max labels**: Optional scale endpoints
- **Step markers**: Optional tick marks for discrete increments

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Single · Range | Single value vs. min/max interval |
| State | Default · Hover · Focus · Disabled · Error | Error only when value is invalid |
| Label | On · Off | Prefer labels when the scale is ambiguous |
| Value Label | On · Off | Use for precise values |
| Marks | On · Off | Use only for meaningful intervals |
| Size | sm · md | Use `md` by default |

## States
Default · Hover · Focus · Disabled · Error

## Usage
**Use when**: Users adjust a bounded numeric value where relative position matters, such as thresholds, percentages, volume, or ranges.
**Avoid when**: Users need exact numeric entry — use Inputs. For a small fixed set of choices, use Radio, Tabs, or Selection Pill.

## Best Practices
**Do**: Show min/max labels or value labels when users need confidence in the selected value.
**Do**: Use step markers only when the scale has meaningful discrete intervals.
**Do**: Pair sliders with numeric input when precision is required.
**Don't**: Use sliders for unbounded values.
**Don't**: Hide the current value when the setting has meaningful consequences.

## Agent Contract
**Default choice**: Use a single Slider for bounded numeric adjustment and Range Slider for min/max intervals.
**Precision rule**: Add a numeric Input or value label when exact values matter.
**Scale rule**: Always define min, max, and step behavior before using a slider.
**Choice rule**: Use Radio, Tabs, or Selection Pill for small discrete choices instead of a slider.
**Do not invent**: Do not create custom drag handles or scale visuals outside the Slider component.

## Related
- [Inputs](./inputs.md)
- [Checkbox & Radio](./checkbox-radio.md)
- [Selection Pill](./selection-pill.md)
