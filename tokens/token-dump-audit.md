# Token Dump Audit

Audit of [source/unify-ds.json](./source/unify-ds.json) for future library implementation.

## Format
- JSON array with 7 top-level entries
- Token objects use DTCG-like fields: `$type`, `$value`, and optional `$scopes`

## Top-Level Entries
1. `_Primitives`
2. `1. Colors`
3. `2. Radius`
4. `3. Spacing`
5. `4. Widths`
6. `5. Containers`
7. `Fonts`

## Token Counts
- `color`: 1533
- `float`: 152
- `string`: 4

## Modes
### `_Primitives`
- `Style`

### `1. Colors`
- `Light mode`
- `Dark mode`

### `2. Radius`
- `Default`

### `3. Spacing`
- `Mode 1`

### `4. Widths`
- `Mode 1`

### `5. Containers`
- `Value`

### `Fonts`
- `Geist`
- `Inter`
- `Manrope`
- `Source Serif Pro`

## What This Gives Us Immediately
- Primitive palette colors for base Tailwind theme extension
- Semantic light/dark color tokens for component styling
- Numeric spacing scale for layout, gap, and padding tokens
- Radius scale for rounded surfaces
- Width/container values for layout primitives
- Font family choices for theme setup

## What Is Missing From This Dump
- Typography sizes, weights, line heights, and letter spacing
- Shadow/effect tokens
- Icon definitions
- Motion/transition tokens
- Z-index and opacity scales

## Recommended Use In The Future App
1. Generate Tailwind theme tokens from this dump.
2. Keep primitives and semantic tokens separate in code.
3. Map `1. Colors` into light/dark theme objects first.
4. Use spacing/radius/width/container values directly for Tailwind config generation.
5. Do not infer missing typography or shadow tokens from this file alone.

## Agent Rule
- When generating UI, prefer semantic tokens first.
- When a needed token domain is missing here, mark it as unresolved instead of inventing a fake token scale.
