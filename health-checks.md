# Knowledge Base Health Checks

Repeatable checks agents should run to keep this design-system wiki trustworthy.

## Link Integrity
- Verify every relative Markdown link resolves to an existing file.
- Verify every component in [index.md](./index.md) links to an existing `.md` source.
- Verify every `Related` link points to an existing component doc or an explicit open gap.
- Verify root component docs have not drifted back into the root; core docs belong in `components/`, and larger product docs belong in `application-components/`.

## Figma Sync
- Verify every component doc has:
- `figma_file`
- `figma_page`
- `figma_node_id`
- `figma_in_page_doc_url`
- `figma_in_page_doc_node_id`
- Verify `figma_node_id` points to a `markdown-content` text layer.
- Verify `figma_in_page_doc_node_id` points to the top-level `📋 In-page docs — {Component}` frame.
- Verify ICD-Test-DS has exactly one in-page docs frame per non-foundation component/application page.

## Agent Contract Coverage
- Verify every component doc has a `## Agent Contract` section.
- Verify each Agent Contract has:
- Default choice
- One or more routing/semantic/dependency rules
- A `Do not invent` rule

## Consistency
- Detect conflicting component guidance, especially:
- Tabs vs Progress Steps
- Dropdown vs Radio
- Alert vs Snackbar vs Toast
- Navigation vs Tabs
- Modal vs inline content
- Button hierarchy and destructive action rules

## Knowledge Gaps
- Review [indexes/open-gaps.md](./indexes/open-gaps.md).
- Promote repeated gaps into new component docs or pattern docs.
- Keep inferred content labeled in docs or notes until verified against Figma properties.

## Output Filing
- If an agent produces a reusable answer, add it to the closest file under `patterns/` or `indexes/`.
- If an answer identifies missing DS coverage, add it to [indexes/open-gaps.md](./indexes/open-gaps.md).
