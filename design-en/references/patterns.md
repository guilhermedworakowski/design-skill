# References: Patterns

> **Instruction for agents:** Consult this file before any visual or flow deliverable to ensure adherence to the product's defined patterns. Once filled in, the tokens documented here are the source of truth — don't replace them with arbitrary values.
>
> **If a section still has placeholders (`[...]`), don't invent values.** Use generic semantic token names (e.g. `color-action-primary`, `spacing-md`), apply the rules from `references/execution.md` and flag in the deliverable which product patterns still need to be defined.

> **Instruction for whoever uses the skill:** This file is a template. Fill in each section with the patterns of your product or design system, replacing everything inside `[brackets]`. Add or remove table rows as needed. Sections that don't apply can be deleted.

---

## Table of contents

1. [Color Palette](#1-color-palette)
2. [Typography](#2-typography)
3. [Border Radius](#3-border-radius)
4. [Spacing](#4-spacing)
5. [Grid](#5-grid)
6. [Iconography](#6-iconography)
7. [Tone of Voice](#7-tone-of-voice)

---

## 1. Color Palette

Document each color with its token name, value and function. Every color needs a defined use.

### Primary
Main action color — primary buttons, links, CTAs. Include the variations (lighter and darker) used for states.

| Token | Hex | Usage |
|---|---|---|
| `[token-name]` | `[#HEX]` | [Where and when to use it] |

### Secondary
Support color — highlight elements that aren't the main action.

| Token | Hex | Usage |
|---|---|---|
| `[token-name]` | `[#HEX]` | [Where and when to use it] |

### Feedback
State colors: success, error, warning and information.

| Token | Hex | Usage |
|---|---|---|
| `[token-name]` | `[#HEX]` | [Success / error / warning / information] |

> **Mandatory rule:** Never use color as the only indicator of state — always combine it with an icon or text. This guarantees accessibility for users with color blindness.

### Neutrals
Backgrounds, surfaces, borders, dividers and text, from lightest to darkest.

| Token | Hex | Usage |
|---|---|---|
| `[token-name]` | `[#HEX]` | [Background, border, supporting text, primary text, etc.] |

---

## 2. Typography

**Family:** [Font name]
**Fallback:** `[fallback stack, e.g. system-ui, sans-serif]`

For each group, document the styles with weight, size, line-height and usage.

### Headline
Page and section titles, subtitles and labels above titles.

| Style | Weight | Size | Line Height | Usage |
|---|---|---|---|---|
| `[style-name]` | [Weight] | [px] | [%] | [Where to use it] |

### Paragraph
Main body text and supporting text. Create one group per body size, if there is more than one.

| Style | Weight | Size | Line Height | Usage |
|---|---|---|---|---|
| `[style-name]` | [Weight] | [px] | [%] | [Where to use it] |

### Caption
Auxiliary text, helper texts, tooltips, badges, field labels.

| Style | Weight | Size | Line Height | Usage |
|---|---|---|---|---|
| `[style-name]` | [Weight] | [px] | [%] | [Where to use it] |

> **Mandatory rule:** Define the interface's minimum font size and the minimum size for body text. Minimum contrast of 4.5:1 between text and background (WCAG AA).

---

## 3. Border Radius

| Token | Value | Usage |
|---|---|---|
| `[token-name]` | [px] | [Components that use this radius] |

---

## 4. Spacing

Scale based on multiples of [4px / 8px]. All inner spacing (padding) and outer spacing (margin/gap) must use only the tokens below — never arbitrary values.

| Token | Value | Typical usage |
|---|---|---|
| `[token-name]` | [px] | [Where to apply it] |

---

## 5. Grid

Document the grid for each breakpoint the product uses.

### [Breakpoint, e.g. Mobile]

| Property | Value |
|---|---|
| Width | [px] |
| Columns | [number] |
| Margin | [px] |
| Gap / Gutter | [px] |

### [Breakpoint, e.g. Desktop]

| Property | Value |
|---|---|
| Width | [px] |
| Columns | [number] |
| Margin | [px] |
| Gap / Gutter | [px] |

> **Mandatory rule:** Define the build strategy (e.g. mobile-first) and the minimum width at which components must be validated.

---

## 6. Iconography

**Library:** [Library name]
**Source:** [Link]

**Usage rules:**
- Always use icons from the defined library — don't mix with other libraries
- Allowed sizes: [list of sizes and the context in which each one is used]
- Never use an icon as the only indicator of an action or state — always pair it with a label or tooltip
- Keep a consistent style within the same product: [outlined / filled / rounded] — don't mix styles

---

## 7. Tone of Voice

### Brand personality

Describe the pillars that define how the brand communicates and how they balance each other.

| Pillar | Description |
|---|---|
| **[Pillar]** | [How this pillar shows up in communication] |

> **Balance rule:** [Describe when the tone can vary and when it must always be clear and direct — e.g. in errors, confirmations and sensitive data, the tone is always clear and direct.]

---

### Interface writing guidelines

- **Objective and concise** — every word has a purpose. Cut what doesn't add value.
- **Avoid technical jargon** — the user shouldn't need to interpret what the interface says.
- **Always active voice** — prefer "Let's fix this" over "This can be fixed".
- [Add the brand-specific guidelines]

---

### Language examples

**✅ Correct**
> *"[Example of copy in the brand's tone]"*

**❌ Incorrect**
> *"[Example of copy off the brand's tone]"*

**Why the correct version works better:**
[Explain which tone characteristics appear in the correct example and are missing from the incorrect one.]

---

### Rules for specific messages

#### Error messages
- **Say what happened** — never leave the user without context or make them figure out on their own what went wrong
- **Offer the way forward** — every error message must have a clear, actionable next step
- **Don't blame the user** — use neutral language, never "you made a mistake" or "invalid field" without explanation
- **Be specific** — "The email must follow the format name@domain.com" is better than "Invalid email"

| ✅ Correct | ❌ Incorrect |
|---|---|
| "[Error message in the brand's tone]" | "[Generic or technical message]" |

#### Onboarding
- **Give context before asking** — explain why each piece of information is needed before requesting it
- **Celebrate progress** — acknowledge each completed step with positive, encouraging language
- **Anticipate questions** — if a field may cause confusion, explain it before the user needs to ask
- **Don't overload** — present one piece of information at a time; progressive onboarding is always preferable

#### Introductions and empty states
- **Turn emptiness into an invitation** — empty states are an engagement opportunity, not an absence of content
- **Say what the user can do** — not just that there's nothing there

| ✅ Correct | ❌ Incorrect |
|---|---|
| "[Empty state that invites action]" | "[Empty state that only reports the absence]" |

---

*Optional sections to add as the product evolves: Components, Interaction Patterns, Visual Business Rules.*
