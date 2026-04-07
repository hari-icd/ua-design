# Figma Dev Mode MCP — Experiment Notes

## Setup
- MCP: `mcp__Figma_Dev_Mode__*`
- Tools: `get_metadata`, `get_design_context`, `get_screenshot`, `get_variable_defs`, `get_figjam`
- **Always call `get_design_context` after `get_metadata` if implementing design**

## Learnings

### Agent-readiness layer
- Added `agent-rules.md` as the global read-first guide for agents creating UnifyApps experiences.
- The guide captures component selection rules, composition recipes, anti-patterns, and output expectations.
- Component docs should include an `Agent Contract` section when they need local constraints beyond the global rules.
- Synced the `Agent Contract` sections into all 17 Figma `markdown-content` text layers in ICD-Test-DS without changing surrounding frames or other nodes.
- Added compiled wiki indexes under `indexes/`: component map, decision map, composition recipes, Figma node map, and open gaps.
- Added reusable experience recipes under `patterns/`: form page, data table page, wizard flow, and upload flow.
- Added `health-checks.md` as the repeatable QA checklist for link integrity, Figma sync, Agent Contract coverage, consistency, and gap filing.
- Organized component docs out of the root: core primitives now live under `components/`, larger product/application components now live under `application-components/`, and the root stays focused on onboarding, agent rules, indexes, health checks, and notes.

### In-page component docs workflow
- Use `figma-use` before any `use_figma` write. Return created/mutated node IDs from the script.
- Current target file: `UglTWbSMldmsVjwl9nZbo6` (`ICD-Test-DS`).
- In-page docs convention: one top-level frame per component page named `📋 In-page docs — {Component}`.
- Each in-page docs frame contains a `markdown-content` text layer generated from the local `.md` source of truth.
- On reruns, find the existing `📋 In-page docs — {Component}` frame, preserve its position, clear its children, and rebuild the docs content instead of creating duplicates.
- For new frames, place the docs to the right of the existing page content using the page content bounds plus a gap.
- Figma node links can be written back to frontmatter with the file key and node ID converted from `45:35794` to `45-35794`: `https://www.figma.com/design/UglTWbSMldmsVjwl9nZbo6/ICD-Test-DS?node-id=45-35794`.
- Correction note: in-page docs were first created in `ckqzPKg0VuzsDXXpMIVWkl` by mistake. They were cross-checked against ICD-Test-DS, the missing docs were recreated in ICD-Test-DS, and the exact known wrong-file doc frames were removed from `ckqzPKg0VuzsDXXpMIVWkl`.

### In-page docs created
| Component | Page ID | Page | Frame node | `markdown-content` node |
|---|---|---|---|---|
| Alerts & Notifications | `21:11576` | `↳ Alerts & notifications` | `45:35794` | `45:35798` |
| Avatar | `8:2589` | `↳ Avatars` | `47:1609` | `47:1613` |
| Breadcrumbs | `21:17358` | `↳ Breadcrumbs` | `45:35782` | `45:35786` |
| Button | `9:6982` | `↳ Buttons` | `47:3819` | `47:3823` |
| Checkbox & Radio | `9:14766` | `↳ Checkboxes` | `47:4099` | `47:4103` |
| Dropdowns | `10:15619` | `↳ Dropdowns` | `55:1628` | `55:1632` |
| Inputs | `12:23378` | `↳ Inputs` | `55:3328` | `55:3332` |
| Headers | `15:37845` | `↳ Headers` | `55:7008` | `55:7012` |
| Modals | `17:43468` | `↳ Modals` | `55:12177` | `55:12181` |
| Navigation | `18:50064` | `↳ Navigation` | `55:19530` | `55:19534` |
| Code Snippet | `21:17585` | `↳ Code snippets` | `45:35724` | `45:35728` |
| Loading Indicator | `22:20377` | `↳ Loading indicators` | `45:35788` | `45:35792` |
| Progress Steps + Timeline | `18:83802` | `↳ Progress steps + Timeline` | `45:35806` | `45:35810` |
| Section Footers | `16:41061` | `↳ Section footers` | `47:4256` | `47:4260` |
| Tabs | `20:3102` | `↳ Tabs` | `45:35800` | `45:35804` |
| Tables | `21:7605` | `↳ Tables` | `55:22828` | `55:22832` |
| File Upload | `21:19128` | `↳ File upload` | `55:24012` | `55:24016` |

### Validation
- Verified all 17 non-foundation in-page doc frames after creation with `use_figma`.
- Each frame has 4 child layers: `doc-source`, `doc-title`, `doc-sync-note`, and `markdown-content`.
- No missing Figma in-page doc frames were reported in the validation pass.
- ICD-Test-DS cross-check found 6 moved docs and 4 missing docs (`Avatar`, `Button`, `Checkbox & Radio`, `Section Footers`). The missing 4 were created in ICD-Test-DS.
- A later non-foundation pass found 7 remaining pages without docs (`Dropdowns`, `Inputs`, `Headers`, `Modals`, `Navigation`, `Tables`, `File Upload`). Those docs were added to ICD-Test-DS and new `.md` source files were created in this repo.
- The wrong file cleanup used exact known node IDs and verified that all 10 wrong-file in-page doc frame IDs are missing afterward.

### Tool Behavior
- `get_metadata` with `nodeId=0:1` → returns document root with all pages listed as canvas nodes
- `get_metadata` with no nodeId → returns currently selected node in Figma
- `get_metadata` returns XML with structure: node IDs, layer types, names, positions, sizes only (no styles/fills)
- `get_design_context` needed for full design details (colors, typography, spacing, etc.)

### Token Efficiency Tips
- Use `get_metadata` first to navigate structure, then `get_design_context` on specific node IDs
- Avoid calling `get_design_context` on large frames — drill down to specific components first

## File: ICD-Test-DS (`UglTWbSMldmsVjwl9nZbo6`)
- Pages listed below are from the ICD-Test-DS file.

## Page Listing Strategy
- `get_metadata(nodeId="0:0")` → returns entire document (~3M chars, saved to file, not streamed)
- Parse with: `python3 -c "import json,re; data=json.load(open('file')); print(re.findall(r'<canvas id=\"([^\"]+)\" name=\"([^\"]+)\"', data[0]['text']))"`
- **Do NOT use Grep on result file** — lines too long, use python3 parsing instead

## File Pages: ICD-Test-DS
| ID | Name |
|---|---|
| 0:1 | ❖ FOUNDATIONS |
| 0:2 | Internal Only Canvas |
| 6:9289 | ↳ Colors |
| 6:15731 | ↳ Typography |
| 6:16179 | ↳ Icons |
| 7:36916 | ↳ Spacing, radius & grids |
| 9:14765 | ❖ COMPONENTS |
| 8:2589 | ↳ Avatars |
| 9:6982 | ↳ Buttons |
| 9:14766 | ↳ Checkboxes |
| 10:15619 | ↳ Dropdowns |
| 12:23378 | ↳ Inputs |
| 13:28940 | ❖ APPLICATION COMPONENTS |
| 15:37845 | ↳ Headers |
| 16:41061 | ↳ Section footers |
| 17:43468 | ↳ Modals |
| 18:50064 | ↳ Navigation |
| 18:83802 | ↳ Progress steps + Timeline |
| 20:3102 | ↳ Tabs |
| 21:7605 | ↳ Tables |
| 21:11576 | ↳ Alerts & notifications |
| 21:17358 | ↳ Breadcrumbs |
| 21:17585 | ↳ Code snippets |
| 22:20377 | ↳ Loading indicators |
| 21:19128 | ↳ File upload |
