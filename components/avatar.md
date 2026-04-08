---
component: Avatar
category: components
figma_page: 13931:29731
figma_file: JkJ2dva8GS70ka8dQOlnML
figma_node_id: 58136:3105
figma_in_page_doc_url: "https://www.figma.com/design/JkJ2dva8GS70ka8dQOlnML/ICD-Test-DS?node-id=58136-3101"
figma_in_page_doc_node_id: "58136:3101"
---

# Avatar
Visual representation of a user, entity, or object. A rich component family covering individual avatars, status overlays, groups, pickers, and profile photos.

## Sub-components
| Sub-component | Frame | Use for |
|---------------|-------|---------|
| Avatar | Avatar | Core individual avatar |
| Avatar label group | Avatar label group | Avatar + name/label + status icon |
| Avatar group | Avatar group | Stacked group of avatars |
| Avatar add button | _Avatar add button | Add-user button (circular) |
| Avatar add button (square) | Avatar add button_square | Add-user button (square) |
| Avatar profile photo | Avatar profile photo | Large profile image with placeholder |
| Avatar Picker | Avatar Picker | Avatar/colour selection UI |
| Colour Picker | Colour Picker | Colour selection for avatar customisation |

## Anatomy (Core Avatar)
- **Container**: Circular or square bounding box sized to the Size token
- **Content**: Letter initials · icon · or image photo
- **Online indicator**: Dot badge overlay (bottom-right) showing online presence
- **Company icon**: Small company logo badge (bottom-right, alternative to online indicator)
- **Verified tick**: Verification badge overlay

## Variants (Core Avatar)
| Property | Values                                      | Notes                                                             |
| -------- | ------------------------------------------- | ----------------------------------------------------------------- |
| Size     | xxs · xs · sm · md · lg · xl · 2xl          | xxs=20px, xs=24px, sm=32px, md=40px, lg=48px, xl=56px, 2xl=64px   |
| Type     | Letter · Icon · Image                       | Letter = initials, Icon = generic placeholder icon, Image = photo |
| Colour   | Gray · Brand Subtle · Brand Solid · Default | Only for Letter and Icon types                                    |
| State    | Default · Hover · Selected · Focused        | —                                                                 |

## Variants (Label Group)
| Property | Values |
|----------|--------|
| Size | xs · sm · md · lg · xl |
| Status icon | False · Online indicator · Company · Verified |
| State | Default |

## Variants (Avatar Group)
| Property | Values |
|----------|--------|
| Size | xs · sm · md |

## Variants (Add Button)
| Property | Values |
|----------|--------|
| Size | xs · sm · md · lg |
| State | Default · Hover · Focus · Disabled |

## Variants (Profile Photo)
| Property | Values |
|----------|--------|
| Placeholder | True · False |
| Text | True · False |
| Size | sm · md · lg |

## States
Default · Hover · Selected · Focused

## Usage
**Use when**: Representing a user identity in comments, assignees, team lists, notification feeds, profile pages.
**Avoid when**: Representing non-user entities without a clear identity — use an icon instead.

## Size Selection Guide
- **xxs/xs**: Dense lists, inline mentions, compact table cells
- **sm/md**: Standard lists, comments, assignee fields
- **lg/xl**: Profile cards, user detail panels
- **2xl**: Profile pages, onboarding flows

## Best Practices
**Do**: Use `Type=Letter` with initials when no photo is available — always prefer over generic icon.
**Do**: Use `Colour=Brand Subtle` for the default letter avatar colour; `Gray` for deactivated users.
**Do**: Use Avatar group for showing 3–5 collaborators; truncate beyond 5 with a `+N` counter.
**Do**: Use Avatar label group when the user's name must be visible alongside the avatar.
**Don't**: Use `Type=Image` without a fallback — always define the Letter variant for when the image fails.
**Don't**: Use `State=Selected` unless the avatar is part of a selectable list or picker.

## Agent Contract
**Default choice**: Use `Type=Letter` with `Colour=Brand Subtle` when no image is available.
**Identity rule**: Use Avatar only when representing a user, team member, company, or entity with a recognizable identity.
**Grouping rule**: Use Avatar group for 3–5 collaborators and truncate beyond 5 with a `+N` counter.
**State rule**: Use `State=Selected` only in selectable lists, pickers, or assignment controls.
**Do not invent**: Do not create custom initials, online dots, or avatar stacks outside this component family.

## Related
- [Buttons](./button.md)
- [Tables](../application-components/tables.md)
