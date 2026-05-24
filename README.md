# Design Skill — Claude Skill

> Uma skill orquestradora de design para Claude, com agentes especializados em estratégia, pesquisa e design engineering.

---

## O que é esta skill?

Esta skill centraliza todo o processo de design dentro do Claude — do estratégico ao visual. Ao ser acionada, ela analisa a solicitação, identifica em qual etapa do processo de design a demanda se encaixa e delega automaticamente para o agente especialista mais adequado.

A skill foi construída para funcionar como um time de design completo dentro do Claude: um **Strategist** para decisões de produto, um **Researcher** para pesquisas e descobertas, e um **Designer Engineer** para construção e entrega visual.

> **Nota:** a skill é acionada automaticamente mesmo quando o usuário não menciona "design" explicitamente — qualquer demanda que envolva produto, experiência do usuário, estratégia digital ou construção de interfaces aciona este fluxo.

---

## Agentes

| Agente | Arquivo | Responsabilidade |
|---|---|---|
| **Strategist** | `agents/strategist.md` | Estratégia de produto, OKRs, priorização, MVPs, arquitetura de informação, user flows, personas, regras de negócio |
| **Researcher** | `agents/researcher.md` | Pesquisas qualitativas e quantitativas, benchmarking, desk research, síntese de insights |
| **Designer Engineer** | `agents/designer-engineer.md` | Princípios de design, heurísticas de Nielsen, construção de telas, protótipos, handoff para dev |

---

## Estrutura de arquivos

```
design/
├── SKILL.md                        ← Orquestrador principal
├── agents/
│   ├── strategist.md               ← Agente de estratégia de produto
│   ├── researcher.md               ← Agente de pesquisa com usuários
│   └── designer-engineer.md        ← Agente de design e engenharia
└── references/
    ├── frameworks.md               ← Biblioteca de frameworks (consultada pelos agentes)
    ├── heuristics.md               ← 10 Heurísticas de Nielsen com exemplos de aplicação
    └── patterns.md                 ← Design system e padrões do produto (em construção)
```

---

## Frameworks disponíveis

### Estratégia — Agente Strategist
Matriz CSD, MoSCoW, Service Blueprint, Fluxogramas, Double Diamond, Opportunity Solution Tree (OST), Jobs to Be Done (JTBD)

### Research — Agente Researcher
Pesquisa Qualitativa, Pesquisa Quantitativa, Teste de Usabilidade (moderado e não moderado), Desk Research, Benchmarking, Teste A/B, Fakedoor Test

### Design Engineering — Agente Designer Engineer
Figma, Storybook, Radix UI / Headless UI, Tailwind CSS, Framer Motion, React / Next.js, Svelte, Git / GitHub

---

## Como usar no Claude

1. Adicione os arquivos desta skill ao seu projeto Claude em **Configurações → Projetos**
2. O Claude detecta automaticamente qual agente acionar com base no contexto da sua solicitação
3. Para forçar um agente específico, mencione explicitamente: *"usando o agente Researcher..."* ou *"acione o Strategist para..."*
4. Quando a demanda cruzar mais de uma área (ex: estratégia + pesquisa), a skill informa quais agentes serão acionados e em qual ordem

---

## Comportamento padrão da skill

- **Nunca** desvia do assunto solicitado
- **Sempre** apresenta no mínimo 2 opções quando há ambiguidade de caminho ou abordagem
- **Sempre** deixa claro qual agente foi acionado e por quê
- Faz **no máximo 1 pergunta** quando a demanda for ambígua — nunca um interrogatório
- Toda entrega é apresentada em **Português (BR)** e **Inglês (EN)**

---

## Licença

MIT — sinta-se livre para usar, adaptar e contribuir.

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
