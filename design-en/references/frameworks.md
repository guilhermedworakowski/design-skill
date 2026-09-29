# References: Frameworks

> **Instruction for agents:** Consult this file whenever you need to select a framework for a request. Choose based on the context of the problem — never by default. Justify the choice in your response.

> **Maintenance instruction:** Whenever a new agent is created and has framework knowledge, those frameworks must be documented here. This ensures the whole design team shares the same repertoire and any agent can use any framework when needed.

---

## Table of contents

### Strategy Frameworks — Agent: Strategist
1. [CSD Matrix](#1-csd-matrix)
2. [MoSCoW](#2-moscow)
3. [Service Blueprint](#3-service-blueprint)
4. [Flowcharts](#4-flowcharts)
5. [Double Diamond](#5-double-diamond)
6. [Opportunity Solution Tree (OST)](#6-opportunity-solution-tree-ost)
7. [Jobs to Be Done (JTBD)](#7-jobs-to-be-done-jtbd)

### Research Frameworks — Agent: Researcher
8. [Qualitative Research](#8-qualitative-research)
9. [Quantitative Research](#9-quantitative-research)
10. [Usability Testing](#10-usability-testing)
11. [Desk Research](#11-desk-research)
12. [Benchmarking](#12-benchmarking)
13. [A/B Testing](#13-ab-testing)
14. [Fake Door Test](#14-fake-door-test)

### Tools and Technologies — Agent: Designer Engineer
15. [Figma](#15-figma)
16. [Storybook](#16-storybook)
17. [Radix UI / Headless UI](#17-radix-ui--headless-ui)
18. [Tailwind CSS](#18-tailwind-css)
19. [Framer Motion](#19-framer-motion)
20. [React and Next.js](#20-react-and-nextjs)
21. [Svelte](#21-svelte)
22. [Git and GitHub](#22-git-and-github)

---

## 1. CSD Matrix

**What it is**
A team alignment framework that organizes knowledge into three categories: what we already know (Certainties), what we assume to be true (Suppositions) and what we don't know yet (Doubts).

**When to use it**
- At the start of a project or discovery phase
- When the team has different perceptions of the problem
- Before planning research, to identify what needs to be investigated

**Structure**

| Certainties | Suppositions | Doubts |
|---|---|---|
| Confirmed facts, validated data, team consensus | Hypotheses we believe to be true but haven't validated yet | Open questions that need investigation |

**How to apply it**
1. Gather the team (or structure it individually)
2. For each column, list the items related to the problem at hand
3. Use the Doubts as direct input for the research plan
4. Use the Suppositions as hypotheses to validate or refute

**Expected result**
A clear map of the team's state of knowledge, with investigation priorities identified.

---

## 2. MoSCoW

**What it is**
A prioritization framework that classifies items into four categories according to how essential they are and their impact.

**When to use it**
- Prioritizing features for an MVP
- Scope decisions in sprints
- When there are more demands than delivery capacity

**Structure**

| Category | Meaning | Criterion |
|---|---|---|
| **Must have** | Mandatory | Without it, the product doesn't work or has no value |
| **Should have** | Important | Adds significant value, but isn't blocking |
| **Could have** | Desirable | Nice to have — goes in if there's time/resources |
| **Won't have** | Out of scope for now | Acknowledged, but consciously left for later |

**How to apply it**
1. List all open features or demands
2. For each item, ask: "Does the product work without this?" and "What is the impact of not having this now?"
3. Classify collaboratively with stakeholders
4. Use the Must haves as the MVP scope

**Expected result**
A prioritized scope with explicit criteria, reducing subjective negotiations.

---

## 3. Service Blueprint

**What it is**
A detailed map of a service that visualizes all of the user's touchpoints, the company's visible actions (frontstage) and the internal processes (backstage) that support the service.

**When to use it**
- Mapping complex services with multiple actors
- Identifying operational bottlenecks that impact the experience
- Redesigning existing services
- When the user experience depends on internal processes that aren't visible

**Structure (layers)**

| Layer | Description |
|---|---|
| **Physical evidence** | Everything the user sees and touches (screens, emails, environments) |
| **User actions** | What the user does at each stage of the journey |
| **Frontstage** | Visible interactions between user and company (agents, chatbots, interfaces) |
| **Backstage** | Internal actions that support the frontstage but aren't visible to the user |
| **Support processes** | Systems, tools and internal processes that sustain everything |

**How to apply it**
1. Define the service and the scenario to map
2. Map the user's actions in chronological order
3. For each action, identify what happens in the layers below
4. Identify failure points, bottlenecks and improvement opportunities

**Expected result**
A systemic view of the service, revealing problems that don't show up in the user journey on its own.

---

## 4. Flowcharts

**What it is**
A visual representation of a process, logical flow or sequence of decisions using standardized shapes.

**When to use it**
- Mapping user flows and navigation
- Documenting decision flows and business rules
- Communicating processes to development teams
- Identifying alternative paths and error states

**Standard shapes**

| Shape | Represents |
|---|---|
| Rectangle | Action or process step |
| Diamond | Decision (yes/no, condition) |
| Oval/Ellipse | Start or end of the flow |
| Arrow | Direction and sequence |
| Parallelogram | Data input or output |

**How to apply it**
1. Define the start and end points of the flow
2. Map each step as an action or decision
3. For each decision, map every possible path (including errors and alternative states)
4. Review with the technical team to validate business rules

**Expected result**
A complete, validated flow, with no ambiguous steps or unmapped paths.

---

## 5. Double Diamond

**What it is**
A design process framework that structures problem-solving into four phases spread across two diamonds: the first to find the right problem, the second to find the right solution.

**When to use it**
- Structuring design projects from start to finish
- When the problem isn't well defined yet
- When there's a risk of solving the wrong problem

**Structure**

```
Diamond 1: Problem             Diamond 2: Solution
─────────────────────          ─────────────────────
DISCOVER  →  DEFINE            DEVELOP   →  DELIVER
(Diverge)    (Converge)        (Diverge)    (Converge)
Explore      Define the        Generate     Test and
the problem  right             possible     deliver
space        problem           solutions    the best one
```

**Phases in detail**

| Phase | Goal | Typical activities |
|---|---|---|
| **Discover** | Understand the problem and the context | User research, desk research, interviews, observation |
| **Define** | Synthesize learnings and define the real problem | Data analysis, insight synthesis, HMW, problem definition |
| **Develop** | Explore possible solutions | Brainstorming, sketches, concepts, rapid prototyping |
| **Deliver** | Refine and validate the best solution | Usability testing, iteration, delivery |

**How to apply it**
1. Identify which phase the project is currently in
2. Don't skip phases — each diamond has a specific role
3. Make sure the Define phase produces a clear problem statement before moving to the second diamond

**Expected result**
A structured project with a validated problem before investing in a solution.

---

## 6. Opportunity Solution Tree (OST)

**What it is**
A visual framework that connects a desired outcome (business result) to the opportunities identified and the possible solutions for each opportunity, avoiding the direct jump from problem to solution.

**When to use it**
- When there are multiple possible solutions and they need to be prioritized
- To connect product initiatives to business outcomes
- When the team is solving symptoms instead of causes

**Structure**

```
OUTCOME (desired result)
└── Opportunity 1
│   ├── Solution A
│   └── Solution B
└── Opportunity 2
    ├── Solution C
    └── Solution D
```

**How to apply it**
1. Define the outcome: what business result or user behavior do we want to achieve?
2. Map the opportunities: which user needs, desires or pain points, if addressed, contribute to the outcome?
3. For each opportunity, list possible solutions
4. Prioritize opportunities by their potential impact on the outcome

**Expected result**
A clear view of the connection between product initiatives and expected results, with impact-based prioritization.

---

## 7. Jobs to Be Done (JTBD)

**What it is**
A framework based on the principle that users don't buy products — they "hire" solutions to get a specific job done in their lives. The focus is on the motivation behind the behavior, not on the behavior itself.

**When to use it**
- When personas aren't explaining user behavior
- To identify non-obvious innovation opportunities
- When the product needs to be repositioned or redefined
- In the discovery phase, to understand deep motivations

**Job Statement structure**

```
When [situation/context],
I want to [motivation/job],
so I can [expected outcome].
```

**Types of jobs**

| Type | Description | Example |
|---|---|---|
| **Functional** | The practical job that needs to get done | "I need to transfer money quickly" |
| **Emotional** | How the user wants to feel | "I want to feel in control of my finances" |
| **Social** | How the user wants to be seen by others | "I want to look organized to my family" |

**How to apply it**
1. Run interviews focused on real situations, not on opinions about the product
2. Identify the main job (functional) and the secondary jobs (emotional and social)
3. Use the jobs to assess whether the planned features actually serve what the user is trying to accomplish
4. Compare with the alternative solutions the user uses today for the same job

**Expected result**
A deep understanding of the user's motivation, independent of technology or interface, enabling more precise and innovative solutions.

---

## 8. Qualitative Research

**What it is**
A methodology that seeks to understand the *why* behind users' behaviors, attitudes and motivations. It produces context-rich data — not statistically representative, but deeply explanatory.

**When to use it**
- When the problem isn't well defined yet and needs exploring
- When quantitative data shows *what* happens but doesn't explain *why*
- To map the user's emotional journey
- In the Discover and Define phases of the Double Diamond

**Why choose qualitative over quantitative**
Choose qualitative when the goal is to generate hypotheses and understand context. Choose quantitative when the goal is to validate hypotheses with statistical representativeness. The two complement each other — qualitative first, quantitative to confirm scale.

**Main formats**

| Format | When to use it |
|---|---|
| **In-depth interview** | Explore individual motivations, beliefs and experiences in detail |
| **Guerrilla research** | Quick hypothesis validation at low cost and in less time |
| **Focus group** | Explore group dynamics and collective perceptions about a topic |
| **Diary study** | Capture behavior in real context, over time |
| **Ethnographic observation** | Understand users in their natural usage environment, without interference |

**How to apply it (in-depth interview)**
1. Define the research goal: what do you want to understand by the end?
2. Recruit participants who represent the target user profile (5–8 for insight saturation)
3. Build a script of open-ended questions — focus on past behavior, not opinions about the future
4. Conduct without leading; use silence and follow-up questions ("tell me more about that")
5. Record and transcribe; identify patterns, repetitions and divergences

**Expected result**
Rich insights into users' motivations, pain points and behaviors, with enough context to generate solid hypotheses for validation.

---

## 9. Quantitative Research

**What it is**
A methodology that seeks to measure and quantify behaviors, attitudes and patterns with statistical representativeness. It answers the questions *how many*, *how often* and *what proportion*.

**When to use it**
- To validate hypotheses generated in qualitative research
- When scale and representativeness are needed for decision-making
- To measure the impact of product changes
- To segment users by behavior or profile

**Why choose quantitative over qualitative**
Choose quantitative when you already know *what* to ask and need representative data to decide with confidence. If you don't know what to ask yet, do qualitative first.

**Main formats**

| Format | When to use it |
|---|---|
| **Survey (questionnaire)** | Collect opinions, preferences and behaviors at scale |
| **Metrics and analytics analysis** | Understand usage patterns, conversion funnels, retention |
| **Behavioral data (heatmaps, recordings)** | Observe where users click, get stuck or drop off |
| **NPS / CSAT** | Measure user satisfaction and likelihood to recommend in a standardized way |

**How to apply it (survey)**
1. Define the goal: which decision will this data support?
2. Write closed, neutral and specific questions — avoid double negatives and jargon
3. Define the sample size needed for statistical reliability
4. Distribute through the channel where the user is — don't force the context
5. Analyze by cross-referencing variables, not just isolated averages

**Expected result**
Representative data that validates or refutes hypotheses, with enough statistical confidence to support product decisions.

---

## 10. Usability Testing

**What it is**
An evaluation method that observes real users performing tasks in a product (prototype or live version), with the goal of identifying usability problems, points of confusion and improvement opportunities.

**When to use it**
- Before launching a new feature or redesign
- When analytics show drop-off at a specific step
- To validate whether a flow makes sense to the real user
- As a complement to a heuristic evaluation (H1–H10)

**Types**

| Type | Description | When to prefer it |
|---|---|---|
| **Moderated** | The researcher runs the session live, with room to dig deeper | When you need to understand the *why* behind the observed behavior |
| **Unmoderated** | The user performs the tasks alone, in an asynchronous tool | When the goal is volume and speed, with self-explanatory tasks |
| **Guerrilla** | Quick, informal testing with whichever users are available at the moment | For quick, low-cost validations with less methodological rigor |

**How to apply it**
1. Define the tasks: what does the user need to be able to do? (e.g. "complete sign-up")
2. Recruit 5–8 participants who represent the real user profile
3. Prepare the environment: task script, prototype or test environment, recording
4. Observe without interfering — don't correct, don't suggest, don't explain
5. Document: where they got stuck, what they said, where they clicked unexpectedly
6. Identify patterns: problems that show up in 3+ users are a priority

**Expected result**
A prioritized list of usability problems with severity (Nielsen scale: 1–4) and contextualized fix recommendations.

---

## 11. Desk Research

**What it is**
Secondary research that consolidates existing data, studies, reports and information about a topic, market or problem — without the need to collect primary data from users.

**When to use it**
- At the start of a project, to build a knowledge base quickly
- When there are constraints on time or access to users
- To contextualize primary data with market references
- As input for the CSD Matrix (fills in Certainties and reduces Doubts)

**Why choose desk research over primary research**
Desk research is the first step — it avoids reinventing what already exists. Always do desk research before primary research so you don't spend effort answering questions that already have answers.

**Priority sources by category**

| Category | Sources |
|---|---|
| **User behavior** | Nielsen Norman Group, Baymard Institute, Think with Google |
| **Market data** | Statista, official national statistics offices, consulting reports (McKinsey, Gartner) |
| **Product trends** | Product Hunt, a16z, First Round Review |
| **Regulatory and legal** | Official websites of regulatory bodies, specialized legal publications |
| **Competition** | Competitors' websites, user reviews (App Store, Google Play), public reports |

**How to apply it**
1. Define the questions the research needs to answer
2. Map the most reliable sources for each question
3. Consolidate the data citing source and date (market data gets outdated)
4. Identify gaps that will require primary research
5. Organize the findings in a format that feeds the CSD Matrix or the OST

**Expected result**
A structured knowledge base on the topic, with reliable sources, identified gaps and inputs for the next research steps.

---

## 12. Benchmarking

**What it is**
A comparative analysis of how other products, companies or industries solve problems similar to yours — with the goal of identifying patterns, best practices, gaps and differentiation opportunities.

**When to use it**
- When you want to understand the state of the art for a given feature or experience
- To identify where the competition is ahead and where there's room to innovate
- As a reference before starting a new project or feature
- To ground design decisions in market evidence

**Types of benchmarking**

| Type | Description | When to use it |
|---|---|---|
| **Competitive** | Analyzes direct competitors in the same market | Understand the industry standard and identify differentiators |
| **Functional** | Analyzes companies from other industries that solve the same type of problem | Look for innovation outside your own market's box |
| **UX/UI** | Focuses specifically on flows, interface patterns and experience | Evaluate design solutions for a specific problem |

**How to apply it**
1. Define what is being analyzed: which feature, flow or experience?
2. Select the benchmarks: at least 3, mixing competitive and functional
3. Define consistent analysis criteria for all benchmarks
4. Document with screenshots, flows and notes — not just impressions
5. Identify patterns (what everyone does), best practices (what works well) and gaps (what no one solves well)
6. Derive opportunities for your product based on the findings

**Expected result**
A structured comparative map with identified patterns, referenced best practices, market gaps and differentiation opportunities for the product.

---

## 13. A/B Testing

**What it is**
A controlled experiment that compares two versions of an element (A and B) to determine which performs better against a specific metric, based on real user behavior.

**When to use it**
- When there are two solution hypotheses and real data to decide between them
- To optimize existing elements (CTAs, copy, layout, flows)
- When there's enough traffic volume for statistical significance
- In the Deliver phase of the Double Diamond, to validate the chosen solution

**Why choose A/B over usability testing**
A/B testing measures *which performs better* at scale — but doesn't explain *why*. Use A/B to confirm; use usability testing to understand. Ideally, use both in sequence.

**Requirements for a valid A/B test**
- A single variable changed at a time (don't test multiple changes simultaneously)
- Sample size calculated for statistical significance (minimum 95% confidence)
- Enough duration to capture weekly behavior variation
- Primary metric defined before the test (don't change the success criterion after starting)

**How to apply it**
1. Define the hypothesis: "We believe that [change X] will [increase/decrease] [metric Y] because [reason Z]"
2. Calculate the required sample size
3. Split traffic randomly between version A (control) and version B (variant)
4. Monitor only the primary metric during the test
5. Once significance is reached, analyze the results and document the learning — even if B lost

**Expected result**
A data-driven decision with statistical confidence, accompanied by documented learning regardless of the outcome.

---

## 14. Fake Door Test

**What it is**
A demand validation technique that exposes a not-yet-existing feature to real users — usually as a button, link or banner — and measures real interest through the level of interaction, before any investment in development.

**When to use it**
- To validate whether a feature has real demand before building it
- When the cost of building it only to find out nobody wants it is high
- In the Develop phase of the Double Diamond, before prototyping at high fidelity
- As a faster alternative to an MVP when the goal is only to validate intent

**How it works**
The user sees the feature's "door" (button, card, link). When they click, instead of accessing the feature, they see a message explaining it's in development — and may be invited to leave their contact to be notified. The click-through rate measures real interest.

**How to apply it**
1. Define the feature to be validated and the interest hypothesis
2. Create the interface element (button, banner, card) as if the feature existed
3. On click, show an honest message: "This feature is being developed. Leave your email to be the first to know."
4. Define the success metric before the test: which click-through rate validates the hypothesis?
5. Analyze the data and, if validated, prioritize development; if not, discard or reframe

**Ethical note**
The fake door must always have an honest way out — never pretend the feature really exists. Users who click and get a transparent message tend to react positively.

**Expected result**
Real usage-intent data, at minimal implementation cost, that supports (or rules out) prioritizing a feature.

---

## 15. Figma

**What it is**
A browser-based collaborative design tool used to create interfaces, components, clickable prototypes and design systems.

**When to use it**
- Low- and high-fidelity wireframes
- Clickable prototyping for usability tests
- Building and maintaining a design system (components, tokens, styles)
- Developer handoff (specs, measurements, assets)

**Mandatory best practices**
- Organize frames with clear naming and a logical page hierarchy
- Use components and variants — never duplicate elements manually
- Define and use design tokens (colors, typography, spacing) as local styles or variables
- Keep auto-layout on every component to ensure responsiveness
- Document component states: default, hover, focus, active, disabled, error

**In the context of this skill**
- Consult `references/patterns.md` before creating any component to check existing patterns
- Consult `references/heuristics.md` to ensure flows and interfaces respect Nielsen's heuristics

---

## 16. Storybook

**What it is**
A tool for developing and documenting UI components in isolation, independent of the main application.

**When to use it**
- Developing and testing design system components in isolation
- Visual, interactive documentation of components for the design and development team
- Ensuring components work correctly across all their states and variations

**Mandatory best practices**
- Create a story for each component state (default, hover, focus, disabled, error, loading)
- Document props with clear descriptions and usage examples
- Keep stories in sync with the Figma definitions
- Use Controls to let stakeholders test component variations

---

## 17. Radix UI / Headless UI

**What it is**
Unstyled (headless) UI component libraries that provide correct behavior, accessibility and semantics, leaving all styling to the design team.

**When to use it**
- As a foundation for design system components that require complex behavior (dropdowns, modals, accordions, tooltips, dialogs)
- When accessibility is a non-negotiable requirement (ARIA, keyboard navigation, screen readers)
- To avoid reinventing behaviors that are already solved and tested

**Why prefer headless over pre-styled components**
Headless components separate behavior from style — the design system keeps full visual control without giving up accessibility and correct behavior. Pre-styled components (e.g. MUI, Chakra) impose visual decisions that conflict with the product's design system.

**Best practices**
- Always combine with Tailwind CSS for styling
- Validate accessibility with a screen reader after implementation
- Document in Storybook with all interaction states

---

## 18. Tailwind CSS

**What it is**
A utility-first CSS framework that applies styles directly in HTML/JSX through predefined classes, following a consistent scale of values.

**When to use it**
- Styling React, Next.js or Svelte interfaces
- When implementation speed and consistency are priorities
- To ensure design tokens (spacing, colors, typography) are respected in code

**Mandatory best practices**
- Configure `tailwind.config` with the product's design tokens (colors, typography, spacing) — never use arbitrary values without need
- Use `@apply` sparingly — only for reusable abstractions
- Keep classes organized by category (layout, typography, color, state)
- Combine with Radix UI for accessible components with controlled styling

---

## 19. Framer Motion

**What it is**
An animation library for React that enables micro-interactions, transitions and layout animations with a declarative, performant API.

**When to use it**
- Micro-interactions that communicate state (action feedback, loading, success)
- Transitions between pages or states that improve user orientation
- Layout animations that reduce the perception of abrupt change

**Usage principle**
Animation serves usability — not decoration. Every animation must have a functional purpose: communicate a state change, guide the eye, confirm an action or create a sense of progression.

**Best practices**
- Respect `prefers-reduced-motion` — always offer a version without animation
- Maximum duration of 300ms for micro-interactions; 500ms for page transitions
- Never animate elements the user is trying to interact with at that moment
- Use the `layout` prop for reordering animations — avoids manual position calculations

---

## 20. React and Next.js

**What it is**
React is the JavaScript library for building component-based interfaces. Next.js is the full-stack framework built on top of React, with native support for SSR, SSG, API routes and performance optimizations.

**When to use it**
- React: building interactive interfaces and SPAs
- Next.js: when SEO, performance, API routes or server-side rendering are requirements

**Mandatory best practices**
- Small components with a single responsibility
- Separate business logic from presentation logic (custom hooks for logic)
- Type components and props with TypeScript
- Use Server Components in Next.js by default — Client Components only when needed (interactivity, state hooks)
- Never put sensitive data in Client Components

---

## 21. Svelte

**What it is**
A reactive JavaScript framework that compiles components to plain JavaScript at build time — no virtual DOM, resulting in smaller bundles and better runtime performance.

**When to use it**
- When performance and bundle size are critical
- For interfaces with complex animations and reactivity
- As an alternative to React when the project doesn't require the React ecosystem

**Key difference from React**
Svelte doesn't use a virtual DOM — reactivity is compiled. This results in simpler code and superior performance in interfaces with many state updates.

---

## 22. Git and GitHub

**What it is**
Git is the distributed version control system. GitHub is the code hosting and collaboration platform built on Git.

**When to use it**
- In every project that involves delivering code — no exceptions
- For collaboration between design and development (one branch per feature, pull requests with context)
- For traceability of technical decisions throughout the project

**Mandatory best practices**
- Atomic commits with clear messages following Conventional Commits (`feat:`, `fix:`, `chore:`, `docs:`)
- One branch per feature or fix — never work directly on `main`
- Pull requests describing the context, what was done and how to test it
- Code review before any merge into the main branch
- `.gitignore` configured correctly — never commit environment variables, API keys or dependencies
