---
component: Date Pickers
category: application-components
figma_page: 1143:85678
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58182:4048
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58182-4024"
figma_in_page_doc_node_id: "58182:4024"
---

# Date Pickers
Calendar and date-entry controls for selecting dates, date ranges, and date-related filters.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Date Picker | Date Picker | Single date selection |
| Date Range Picker | Date Range Picker | Start and end date selection |
| Calendar | Calendar | Calendar grid inside a picker or popover |
| Date Input | Date Input | Typed date entry with picker affordance |

## Anatomy
- **Trigger/input**: Field or button that opens the calendar
- **Calendar surface**: Popover or panel containing the date grid
- **Month navigation**: Previous/next controls and current month label
- **Day cells**: Selectable date options
- **Range highlight**: Visual span between start and end dates
- **Footer actions**: Optional Apply, Cancel, Clear, or Today actions

## Variants
| Property | Values | Notes |
|----------|--------|-------|
| Type | Single Date · Date Range | Match the value being collected |
| State | Default · Hover · Focus · Disabled · Error | Input and day cells carry states |
| Range | Start · In Range · End · None | Range picker only |
| Footer | On · Off | Use when selection should be confirmed |
| Size | sm · md | Use `md` by default |

## States
Default · Hover · Focus · Selected · In Range · Disabled · Error

## Usage
**Use when**: Users need to choose calendar dates, deadlines, schedules, or date filters.
**Avoid when**: Users enter freeform text unrelated to dates — use Inputs. For preset-only filters such as "Last 7 days", use Selection Pill or Dropdown.

## Best Practices
**Do**: Support typed entry when exact dates are common.
**Do**: Show validation errors close to the date input.
**Do**: Use footer actions for range selection when accidental changes are costly.
**Don't**: Use a date picker for relative presets only.
**Don't**: Allow impossible ranges without clear error messaging.

## Agent Contract
**Default choice**: Use Date Picker for one date and Date Range Picker for start/end filters.
**Validation rule**: Use Error state and helper text for invalid, unavailable, or impossible dates.
**Preset rule**: Use Selection Pill or Dropdown for relative presets when no calendar selection is needed.
**Confirmation rule**: Use Apply/Cancel footer for range filters that update data-heavy views.
**Do not invent**: Do not build custom calendar grids when Date Picker components cover the need.

## Related
- [Inputs](../components/inputs.md)
- [Selection Pill](../components/selection-pill.md)
- [Dropdowns](../components/dropdowns.md)
