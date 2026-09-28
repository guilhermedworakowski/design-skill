---
---

# Design Skill — Claude Skill

> An orchestrating design skill for Claude, with specialized agents for strategy, research, and design engineering.

---

## What is this skill?

This skill centralizes the entire design process within Claude — from strategy to visual delivery. When triggered, it analyzes the request, identifies which stage of the design process the demand fits into, and automatically delegates to the most appropriate specialist agent.

The skill was built to act as a complete design team inside Claude: a **Strategist** for product decisions, a **Researcher** for user research and discovery, and a **Designer Engineer** for interface building and delivery.

> **Note:** the skill is triggered automatically even when the user doesn't explicitly mention "design" — any demand involving product, user experience, digital strategy, or interface building activates this flow.

---

## Agents

| Agent | File | Responsibility |
|---|---|---|
| **Strategist** | `agents/strategist.md` | Product strategy, OKRs, prioritization, MVPs, information architecture, user flows, personas, business rules |
| **Researcher** | `agents/researcher.md` | Qualitative and quantitative research, benchmarking, desk research, insight synthesis |
| **Designer Engineer** | `agents/designer-engineer.md` | Design principles, Nielsen heuristics, screen building, prototypes, dev handoff |

---

## File structure

```
design/
├── SKILL.md                        ← Main orchestrator
├── agents/
│   ├── strategist.md               ← Product strategy agent
│   ├── researcher.md               ← User research agent
│   └── designer-engineer.md        ← Design engineering agent
└── references/
    ├── frameworks.md               ← Framework library (consulted by agents)
    ├── heuristics.md               ← Nielsen's 10 Heuristics with application examples
    └── patterns.md                 ← Design system and product patterns (in progress)
```

---

## Available frameworks

### Strategy — Strategist Agent
CSD Matrix, MoSCoW, Service Blueprint, Flowcharts, Double Diamond, Opportunity Solution Tree (OST), Jobs to Be Done (JTBD)

### Research — Researcher Agent
Qualitative Research, Quantitative Research, Usability Testing (moderated and unmoderated), Desk Research, Benchmarking, A/B Testing, Fakedoor Test

### Design Engineering — Designer Engineer Agent
Figma, Storybook, Radix UI / Headless UI, Tailwind CSS, Framer Motion, React / Next.js, Svelte, Git / GitHub

---

## How to use in Claude

1. Add the skill files to your Claude project under **Settings → Projects**
2. Claude automatically detects which agent to trigger based on the context of your request
3. To force a specific agent, explicitly mention: *"using the Researcher agent..."* or *"activate the Strategist for..."*
4. When the demand crosses more than one area (e.g. strategy + research), the skill informs which agents will be triggered and in which order

---

## Default skill behavior

- **Never** deviates from the requested subject
- **Always** presents at least 2 options when there is ambiguity of path or approach
- **Always** makes clear which agent was triggered and why
- Asks **at most 1 question** when the demand is ambiguous — never an interrogation
- Every deliverable is presented in **Portuguese (BR)** and **English (EN)**

---

## License

MIT — feel free to use, adapt, and contribute.
