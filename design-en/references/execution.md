# execution — Designer Engineer execution patterns

## What it's for

This file is the Designer Engineer's **execution** layer. It complements `references/cognitive-biases.md`:

- **cognitive-biases.md** answers *why* a decision works (user behavior)
- **execution.md** answers *how* to build it in the interface (patterns, values, states, checklists)

Both are consulted **always, together**, in every Designer Engineer deliverable. Neither replaces the other: a bias without a pattern produces justification without construction; a pattern without a bias produces construction without justification.

Basic principles of spacing, typography, color and accessibility live in the agent itself (`agents/designer-engineer.md`). Hick's, Miller's, Fitts's, Von Restorff and Serial Position laws live in `cognitive-biases.md`. This file doesn't repeat that content, it only points to it.

---

## How to use it together with the biases

1. **Map the relevant biases** in `references/cognitive-biases.md`
2. **Locate the corresponding patterns** in this file (use the table below as a bridge)
3. **Build** by applying the pattern's rules and values
4. **Document as a set**: for each decision, cite the bias (*why*) + the execution pattern (*how*) + the Nielsen heuristic
5. **Close** with the checklist in section 14 (Handoff and QA) when the deliverable is high fidelity, handoff or code

### Bias → pattern bridge

| Bias / law (cognitive-biases.md) | Sections in this file |
|---|---|
| Anchoring Bias | 10 Visual hierarchy · 12 UX writing |
| Social Proof | 3 Feedback · 12 UX writing |
| Loss Aversion · Framing Effect | 4 Errors · 12 UX writing |
| Decoy Effect | 10 Visual hierarchy |
| Hick's Law | 5 Forms · 6 Navigation · 7 Search |
| Miller's Law | 5 Forms · 11 Layout |
| Zeigarnik · Goal Gradient | 5 Forms (multi-step) · 8 Onboarding · 9 Motion |
| Habit Loop · VRR | 3 Feedback · 9 Micro-interactions |
| Scarcity & FOMO | 3 Feedback · 12 UX writing (always with the ethical Designer Checklist) |
| Peak-End Rule | 3 Feedback (confirmation) · 9 Micro-interactions |
| Von Restorff · Serial Position | 6 Navigation · 10 Visual hierarchy |
| Jakob's Law | 6 Navigation · 7 Search · 9 Gestures |
| Confirmation Bias | 12 UX writing (post-conversion) |
| Fitts's Law | 9 Gestures · 11 Responsive · 14 QA (touch targets) |
| Cognitive Load | 1 States · 2 Response time · 10 Hierarchy |

---

## 1. Interface states

Model every component or flow as a **state machine**: states, events that cause transitions, rules (guards) and actions. This eliminates impossible states (e.g. loading and error at the same time) and becomes a shared language with developers.

**Mandatory states to design** (not just the happy path):
- Component: default · hover · focus · active · disabled · loading · error
- Screen/data: empty (first use and no results) · loading · partial · success · error · no permission

**Standard flows:**
- Form: idle → editing → validating → submitting → success/error → idle
- Data fetching: idle → loading → success/error; error → retrying → success/error
- Wizard: step 1 → step 2 → … → review → submitting → done

Rules: every state has a way out (no dead ends); one machine per concern; each state has a defined visual representation.

---

## 2. Response time and loading

**Doherty Threshold:** below 400ms the user stays in the flow; above it, they notice the wait.

| Duration | What to show |
|---|---|
| < 100ms | Nothing — just the element's state change |
| 100ms–1s | Subtle indicator (opacity, skeleton) |
| 1–10s | Clear loading; determinate bar if progress is measurable |
| > 10s | Detailed progress, time estimate, option to continue in the background or cancel |

**Patterns:**
- **Skeleton** for content with a known structure (preferable to a spinner); shape faithful to the real content
- **Spinner** only for short, unknown durations; small and discreet
- **Optimistic UI**: show the result immediately, reconcile with the server and roll back if it fails
- **Progressive loading**: critical content first, lazy-load below the fold, blur-up images

Rules: visual touch feedback within 100ms, always; never a blank screen; never more than one loading indicator competing; no layout shift while loading; content enters with a fade (doesn't "blink"); don't show a spinner for actions under 400ms (the flash gets in the way).

---

## 3. Feedback and confirmation

Every user action gets a response, with intensity proportional to the importance of the action.

**Hierarchy of where to show it** (prefer the one closest to the action):
1. Inline, on the element itself
2. In the component
3. On the page (toast, banner)
4. In the system (notification outside the current screen)

**Duration:**
- Toast: disappears on its own in 3–5s
- Error: persists until resolved or dismissed
- Confirmation: brief, with an undo window
- Status: persists while it's relevant

Rules: prefer **undo** over "Are you sure?"; don't interrupt the flow for minor confirmations; never use color alone to communicate status; at peak and end-of-journey moments (Peak-End), the confirmation deserves extra care, with a summary of what was done and the next step.

---

## 4. Errors

**Priority order:** prevent → detect → communicate → recover.

- **Prevent:** constrained inputs (date picker, select), smart defaults, auto-save, confirmation only for destructive actions
- **Detect:** per-field validation, validation on submit, network failure, timeout, permission
- **Communicate**, always in this format:
  - **What happened** (human language, no error code)
  - **Why** (if it helps)
  - **What to do now** (specific action)
- **Recover:** never erase what the user typed; offer a retry; an alternative path; undo

| Context | Pattern |
|---|---|
| Form | Inline error on the field + summary at the top if there are several |
| Page | Full-page error with "try again" and "go back" |
| Network | Toast or banner with "try again" |
| No results | Empty state with suggestions |
| Permission | Explains which access is missing and how to get it |

Never blame the user. Never "Something went wrong" without context.

---

## 5. Forms

**Layout:** single column; field width proportional to the expected length of the answer; label above the field; related fields grouped under a section title.

**Labels:** always visible (a placeholder is never a label); sentence case; help text between label and field; mark the **optional** fields, not the required ones; character counter always visible when there's a limit.

**Input type:**

| Data | Input |
|---|---|
| One choice among up to 5 | Radio (all visible) |
| One choice among 6+ | Select / combobox |
| Multiple choices | Checkbox |
| Date | Date picker or segmented fields — never free text |
| Phone, national ID / tax ID, card | Masked field |
| Password | With show/hide button |

**Validation:** on leaving the field (on blur), not on every keystroke; error right below the field; a message that teaches how to fix it ("The email needs an @", not "Invalid email"); success check only where validity isn't obvious (password, username availability).

**Multi-step:** visual progress indicator (Zeigarnik/Goal Gradient); each step is a coherent block; go back without losing data; save progress in long forms; review step before high-risk submissions (payment, money transfer, legal data).

**Accessibility:** programmatic label (`<label for>` or `aria-label`); error linked to the field (`aria-describedby`); focus order matches visual order; focusable error summary with links to each field.

Cut every optional field you can. Fewer fields = more completions.

---

## 6. Navigation

| Situation | Pattern |
|---|---|
| Mobile, 3–5 main destinations | Bottom tab bar (icon + label) |
| Desktop with many destinations or hierarchy | Sidebar |
| Simple site or documentation | Top nav (4–7 items) |
| Deep hierarchy | Breadcrumb + local sidebar |
| Parallel views of the same content | Tabs or segmented control (2–4) |
| Occasional access (account, help, settings) | Utility navigation, visually separated |

**Principles:** the user always knows where they are (active state, title, breadcrumb); the label predicts the destination; main destinations within thumb reach on mobile; structure and position don't change between screens.

Rules: active state differentiated by more than color (weight, indicator, underline); hamburger never as the main navigation on desktop; don't mix global and local levels in the same component; more than 7 top-level items calls for an information architecture review before adding new items; validate labels with first-click testing.

---

## 7. Search

- **Field:** the placeholder says what can be searched ("Search products, brands or categories"); autofocus on open; clear button when there's text; the executed search stays in the field for refinement
- **Autocomplete:** from 2–3 characters; order: recent → popular → predictions; highlight the typed term; 5–8 suggestions at most; keyboard-navigable; include navigation destinations ("my orders", "my profile")
- **Results:** show the count; term highlighted in the title and snippet; metadata that helps decide the click; sorting visible and changeable
- **Filters:** only those relevant to the current result, with counts; applied filters visible and removable one by one; "Clear all"
- **Zero results** (the most neglected state): confirm what was searched, suggest typo corrections and related terms, offer alternative paths. Never an empty page.

Tolerate typos, synonyms, plurals and partial matches.

---

## 8. Onboarding and empty states

**Goals, in order:** reach value fast → guide instead of teaching everything → create small wins → ask only for what's needed now.

| Pattern | When to use it |
|---|---|
| Progressive onboarding (tooltips and tips on first use) | Products with many features |
| Setup wizard | The product doesn't work without setup; minimal steps, optional ones skippable, celebrate the end |
| Sample data | When emptiness prevents understanding the product (dashboards); flag it as sample and let the user clear it |
| Guided tour | Only for 3–5 core concepts; always dismissible |

**An empty state is onboarding:** it explains what the space is for, offers a clear action ("Create your first project"), shows what it looks like when filled. Never an empty table with just a header.

**Reduce friction:** defer non-essential data collection, smart defaults, social login/SSO, "do it later" on non-critical steps.

Define the **"aha" moment** and design the shortest path to it. Metrics: activation rate and time, drop-off per step, D7/D30 retention.

---

## 9. Motion, micro-interactions and gestures

**Micro-interaction**, always specify: trigger → rules → feedback (visual/audio/haptic) → loop/mode (first time vs. repeat) → duration/easing → accessibility.

**Duration:**
- Micro (50–100ms): button state, toggle
- Short (150–250ms): tooltip, fade, small movements
- Medium (250–400ms): screen transition, modal
- Long (400–700ms): complex choreography (rare)

**Easing:** ease-out for entering · ease-in for exiting · ease-in-out for changing position · linear only for continuous loops (progress).

Rules: every animation communicates something; faster is almost always better; interruptible; 30–50ms stagger between list items, total sequence under 700ms; always respect `prefers-reduced-motion`; animate `transform`/`opacity` for performance.

**Gestures:** always with a non-gesture alternative (button/menu); visible affordance and a hint on first use; immediate visual response on start; 10–15px threshold before activating; long press ~500ms; direction lock to separate scroll from swipe; system gestures take priority; undo for destructive gestures; follow platform conventions (Jakob).

---

## 10. Visual hierarchy and composition

**Hierarchy tools:** size (minimum 1.5x difference between levels) · weight · color and contrast · surrounding white space · position (top-left first; F and Z patterns) · isolation.

**Levels:** primary (title, main CTA) → secondary (sections, key content) → tertiary (supporting content, metadata) → quaternary (fine print, timestamps).

**Composition:**
- **Balance:** visual weight distributed intentionally; clear center of gravity
- **White space:** macro between sections, consistent micro between elements
- **Rhythm:** intervals from the spacing scale; repeated items with uniform size and gap
- **Gestalt:** proximity (related things together), similarity (same function, same look), figure/ground, alignment continuity

Rules: **one primary CTA per screen**; the "squint test" (when blurred, the hierarchy is still clear); at most two active type weights per screen; typography only in scale steps (no 1–2px tweaks); line-height 1.1–1.3 for headings and 1.4–1.6 for body; reading line between 45 and 75 characters.

---

## 11. Layout, grid, responsive and dark mode

**Grid:** 4 columns (mobile) · 8 (tablet) · 12 (desktop); gutters of 16/24/32px; margins from 16px (mobile) to 24–48px (desktop); 4 or 8px baseline. Break the grid only on purpose, for emphasis.

**Reference breakpoints:** 375–639px (phone) · 640–1023px (tablet) · 1024–1439px (laptop) · 1440px+ (desktop). Mobile-first; content defines the breakpoint, not the device.

**Responsive patterns:** column drop · reflow (horizontal becomes vertical) · off-canvas for secondary content · priority+ (the most important visible, the rest under "more").

**By input type:** touch requires a minimum 44px target; mouse calls for hover; keyboard calls for visible focus and logical order.

**Dark mode** (it isn't inverting colors):
- Elevation through lighter surfaces, not shadow (background ~#121212 → surfaces 1, 2, 3 progressively lighter)
- Primary colors 10–20% less saturated
- Off-white text (~#E0E0E0), not pure white; white borders at low opacity
- Semantic tokens to switch themes without rework; respect `prefers-color-scheme` and offer a manual toggle

---

## 12. UX writing

- **Buttons/CTAs:** start with a verb, state the outcome ("Confirm payment", not "Submit"); reflect the user's intent, not the business's
- **Labels:** clear, no jargon or internal product names
- **Placeholder:** a format example, not an instruction
- **Errors:** what happened / why / what to do format (section 4); human tone, no blame
- **Empty states:** what will appear here + clear action + encouraging tone
- **Confirmation:** what just happened + next step + undo when reversible
- **Onboarding:** one concept at a time, action-oriented, skippable

**Voice** is constant (brand personality, see `references/patterns.md`); **tone** varies with context (celebration ≠ error ≠ instruction).

Principles: clear > clever · concise > complete · useful > promotional · consistent > original. Write the copy before designing the screen (content-first). Framing, scarcity and social proof in copy always go through the ethical Designer Checklist in `cognitive-biases.md`.

---

## 13. Components and tokens

**Component specification**, in this order:
1. Overview: name, what it's for, when to use it and when **not** to use it
2. Anatomy: required and optional parts
3. Variants: size (sm/md/lg), style (primary/secondary/ghost), layout
4. Props/API: name, type, default, required
5. States: default, hover, focus, active, disabled, loading, error
6. Behavior: interactions, animation, responsive, edge cases
7. Accessibility: ARIA role, keyboard, screen reader, focus management
8. Usage: do/don't, content rules, related components

**Tokens in three layers:**
1. **Global**: raw value (`blue-500: #3B82F6`)
2. **Semantic (alias)**: function (`color-action-primary`)
3. **Component**: specific usage (`button-color-primary`)

Naming: `{category}-{property}-{variant}-{state}`. Categories: color, spacing, typography, elevation, border, motion. A component never references a raw value; themes swap only the semantic layer.

---

## 14. Handoff and QA

**The handoff contains:**
- **Visual:** spacing, colors, typography, radius, shadow, always by token name (not hex)
- **Interaction:** all states, transitions (duration, easing, property), gestures, tab order and shortcuts
- **Content:** character limits and truncation, dynamic content rules (min./max.), text expansion in translations, empty/loading/error copy
- **Edge cases:** minimum and maximum content, each breakpoint, accessibility requirements
- **Implementation notes:** component reuse, API dependencies, performance
- **Assets:** SVG icons named by convention, images with responsive variants

**QA checklist** (design vs. implementation):
- [ ] Colors, typography, spacing, radius and shadow match the tokens
- [ ] Grid and behavior at each breakpoint as specified; no overflow or clipping
- [ ] All states render (including empty, loading and error)
- [ ] Transitions as specified; `prefers-reduced-motion` respected
- [ ] Touch targets ≥ 44px; keyboard navigation in the right order; visible focus
- [ ] WCAG AA contrast (4.5:1 text, 3:1 large text and UI elements)
- [ ] Screen reader announces correctly; ARIA roles and labels correct
- [ ] Real content (no lorem ipsum); truncation works
- [ ] Works with enlarged font in system settings

---

## 15. Screen critique

To evaluate an existing screen, analyze four dimensions: **Hierarchy** (section 10) · **Brand** (voice, tone and tokens from `references/patterns.md`) · **Composition** (section 10) · **Typography** (scale, legibility, consistency, token usage).

For each problem: **observation** (neutral) → **problem** (what breaks and why) → **fix** (specific, with the token name when applicable) → **bias affected** (from `cognitive-biases.md`).

**Prioritize:**
- **P1 — Critical:** breaks usability, accessibility or brand; fix before publishing
- **P2 — Important:** degrades the experience or creates inconsistency; fix in the current cycle
- **P3 — Polish:** visual refinement; when there's capacity

Close with a paragraph pointing out the strongest and the weakest dimension.
