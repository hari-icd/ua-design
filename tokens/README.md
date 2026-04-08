# Design Tokens

Repo-local source for the UnifyApps token dump that will drive the future Next.js + Tailwind component app.

## Source Files
- [source/unify-ds.json](./source/unify-ds.json): raw token export copied from the shared Figma token dump on April 8, 2026
- [token-dump-audit.md](./token-dump-audit.md): quick audit of what this dump contains and what is still missing for implementation

## Current Coverage
- Primitive palette colors
- Semantic/component color tokens with light and dark modes
- Radius scale
- Spacing scale
- Width scale
- Container values
- Font family tokens

## Important Implementation Note
This dump is a strong base for Tailwind theme generation, but it is not a full design-system contract yet.

It does **not** currently provide a complete:
- typography scale
- shadow/effect token set
- icon asset inventory
- motion token set

Those will need to come from the broader design system sources before the standalone app can be fully token-driven.

## Agent Rule
- Treat this folder as the repo-local token source of truth for code generation work.
- Prefer semantic tokens from `1. Colors` over raw primitives when styling components.
- Use primitive spacing/radius values only when no component-specific semantic token exists.
- Keep light/dark mode support in mind from the start because the color dump already includes both modes.
