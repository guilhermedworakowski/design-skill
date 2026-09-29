# References: Frameworks

> **Instrução para agentes:** Consulte este arquivo sempre que precisar selecionar um framework para uma demanda. Escolha com base no contexto do problema — nunca por padrão. Justifique a escolha na sua resposta.

> **Instrução para manutenção:** Sempre que um novo agente for criado e possuir conhecimento de frameworks, os frameworks devem ser documentados aqui. Isso garante que toda a equipe de design compartilhe o mesmo repertório e qualquer agente possa consumir qualquer framework quando necessário.

---

## Índice

### Frameworks de Estratégia — Agente: Strategist
1. [Matriz CSD](#1-matriz-csd)
2. [MoSCoW](#2-moscow)
3. [Service Blueprint](#3-service-blueprint)
4. [Fluxogramas](#4-fluxogramas)
5. [Double Diamond](#5-double-diamond)
6. [Opportunity Solution Tree (OST)](#6-opportunity-solution-tree-ost)
7. [Jobs to Be Done (JTBD)](#7-jobs-to-be-done-jtbd)

### Frameworks de Research — Agente: Researcher
8. [Pesquisa Qualitativa](#8-pesquisa-qualitativa)
9. [Pesquisa Quantitativa](#9-pesquisa-quantitativa)
10. [Teste de Usabilidade](#10-teste-de-usabilidade)
11. [Desk Research](#11-desk-research)
12. [Benchmarking](#12-benchmarking)
13. [Teste A/B](#13-teste-ab)
14. [Fakedoor Test](#14-fakedoor-test)

### Ferramentas e Tecnologias — Agente: Designer Engineer
15. [Figma](#15-figma)
16. [Storybook](#16-storybook)
17. [Radix UI / Headless UI](#17-radix-ui--headless-ui)
18. [Tailwind CSS](#18-tailwind-css)
19. [Framer Motion](#19-framer-motion)
20. [React e Next.js](#20-react-e-nextjs)
21. [Svelte](#21-svelte)
22. [Git e GitHub](#22-git-e-github)

---

## 1. Matriz CSD

**O que é**
Framework de alinhamento de time que organiza o conhecimento em três categorias: o que já sabemos, o que assumimos ser verdade e o que ainda não sabemos.

**Quando usar**
- Início de projeto ou fase de discovery
- Quando o time tem percepções diferentes sobre o problema
- Antes de planejar pesquisas, para identificar o que precisa ser investigado

**Estrutura**

| Certezas | Suposições | Dúvidas |
|---|---|---|
| Fatos confirmados, dados validados, consensos do time | Hipóteses que acreditamos ser verdade mas ainda não validamos | Perguntas abertas que precisam de investigação |

**Como aplicar**
1. Reúna o time (ou estruture individualmente)
2. Para cada coluna, liste os itens relacionados ao problema em questão
3. Use as Dúvidas como insumo direto para o plano de pesquisa
4. Use as Suposições como hipóteses a validar ou refutar

**Resultado esperado**
Um mapa claro do estado do conhecimento do time, com prioridades de investigação identificadas.

---

## 2. MoSCoW

**O que é**
Framework de priorização que classifica itens em quatro categorias de acordo com sua obrigatoriedade e impacto.

**Quando usar**
- Priorização de funcionalidades para MVP
- Decisões de escopo em sprints
- Quando há mais demandas do que capacidade de entrega

**Estrutura**

| Categoria | Significado | Critério |
|---|---|---|
| **Must have** | Obrigatório | Sem isso, o produto não funciona ou não tem valor |
| **Should have** | Importante | Agrega valor significativo, mas não é bloqueante |
| **Could have** | Desejável | Nice to have — entra se houver tempo/recurso |
| **Won't have** | Fora de escopo agora | Reconhecido, mas conscientemente deixado para depois |

**Como aplicar**
1. Liste todas as funcionalidades ou demandas em aberto
2. Para cada item, questione: "O produto funciona sem isso?" e "Qual o impacto de não ter isso agora?"
3. Classifique colaborativamente com stakeholders
4. Use o Must have como escopo do MVP

**Resultado esperado**
Escopo priorizado com critérios explícitos, reduzindo negociações subjetivas.

---

## 3. Service Blueprint

**O que é**
Mapa detalhado de um serviço que visualiza todos os pontos de contato do usuário, as ações visíveis da empresa (frontstage) e os processos internos (backstage) que sustentam o serviço.

**Quando usar**
- Mapeamento de serviços complexos com múltiplos atores
- Identificação de gargalos operacionais que impactam a experiência
- Redesign de serviços existentes
- Quando a experiência do usuário depende de processos internos não visíveis

**Estrutura (camadas)**

| Camada | Descrição |
|---|---|
| **Evidências físicas** | Tudo que o usuário vê e toca (telas, emails, ambientes) |
| **Ações do usuário** | O que o usuário faz em cada etapa da jornada |
| **Frontstage** | Interações visíveis entre usuário e empresa (atendentes, chatbots, interfaces) |
| **Backstage** | Ações internas que suportam o frontstage mas não são visíveis ao usuário |
| **Processos de suporte** | Sistemas, ferramentas e processos internos que sustentam tudo |

**Como aplicar**
1. Defina o serviço e o cenário a mapear
2. Mapeie as ações do usuário em ordem cronológica
3. Para cada ação, identifique o que acontece nas camadas abaixo
4. Identifique pontos de falha, gargalos e oportunidades de melhoria

**Resultado esperado**
Visão sistêmica do serviço, revelando problemas que não aparecem na jornada do usuário isolada.

---

## 4. Fluxogramas

**O que é**
Representação visual de um processo, fluxo lógico ou sequência de decisões usando formas padronizadas.

**Quando usar**
- Mapeamento de user flows e navegação
- Documentação de fluxos de decisão e regras de negócio
- Comunicação de processos para times de desenvolvimento
- Identificação de caminhos alternativos e estados de erro

**Formas padrão**

| Forma | Representa |
|---|---|
| Retângulo | Ação ou etapa do processo |
| Losango | Decisão (sim/não, condição) |
| Oval/Elipse | Início ou fim do fluxo |
| Seta | Direção e sequência |
| Paralelogramo | Entrada ou saída de dados |

**Como aplicar**
1. Defina o ponto de início e fim do fluxo
2. Mapeie cada etapa como uma ação ou decisão
3. Para cada decisão, mapeie todos os caminhos possíveis (incluindo erros e estados alternativos)
4. Revise com o time técnico para validar regras de negócio

**Resultado esperado**
Fluxo completo e validado, sem etapas ambíguas ou caminhos não mapeados.

---

## 5. Double Diamond

**O que é**
Framework de processo de design que estrutura a resolução de problemas em quatro fases distribuídas em dois diamantes: o primeiro para encontrar o problema certo, o segundo para encontrar a solução certa.

**Quando usar**
- Estruturação de projetos de design do início ao fim
- Quando o problema ainda não está bem definido
- Quando há risco de resolver o problema errado

**Estrutura**

```
Diamante 1: Problema           Diamante 2: Solução
─────────────────────          ─────────────────────
DISCOVER  →  DEFINE            DEVELOP   →  DELIVER
(Divergir)   (Convergir)       (Divergir)   (Convergir)
Explorar     Definir o         Gerar        Testar e
o espaço     problema          soluções     entregar
do problema  certo             possíveis    a melhor
```

**Fases em detalhe**

| Fase | Objetivo | Atividades típicas |
|---|---|---|
| **Discover** | Entender o problema e o contexto | Pesquisa com usuários, desk research, entrevistas, observação |
| **Define** | Sintetizar aprendizados e definir o problema real | Análise de dados, insight synthesis, HMW, definição do problema |
| **Develop** | Explorar soluções possíveis | Brainstorming, sketches, conceitos, prototipagem rápida |
| **Deliver** | Refinar e validar a melhor solução | Testes de usabilidade, iteração, entrega |

**Como aplicar**
1. Identifique em qual fase o projeto está atualmente
2. Não pule fases — cada diamante tem um papel específico
3. Garanta que a fase Define produza um problem statement claro antes de avançar para o segundo diamante

**Resultado esperado**
Projeto estruturado com problema validado antes de investir em solução.

---

## 6. Opportunity Solution Tree (OST)

**O que é**
Framework visual que conecta um outcome desejado (resultado de negócio) às oportunidades identificadas e às soluções possíveis para cada oportunidade, evitando o salto direto de problema para solução.

**Quando usar**
- Quando há múltiplas soluções possíveis e é preciso priorizá-las
- Para conectar iniciativas de produto a outcomes de negócio
- Quando o time está resolvendo sintomas em vez de causas

**Estrutura**

```
OUTCOME (resultado desejado)
└── Oportunidade 1
│   ├── Solução A
│   └── Solução B
└── Oportunidade 2
    ├── Solução C
    └── Solução D
```

**Como aplicar**
1. Defina o outcome: qual resultado de negócio ou comportamento do usuário queremos alcançar?
2. Mapeie as oportunidades: quais necessidades, desejos ou pontos de dor dos usuários, se atendidos, contribuem para o outcome?
3. Para cada oportunidade, liste soluções possíveis
4. Priorize oportunidades pelo impacto potencial no outcome

**Resultado esperado**
Visão clara da conexão entre iniciativas do produto e resultados esperados, com priorização baseada em impacto.

---

## 7. Jobs to Be Done (JTBD)

**O que é**
Framework que parte do princípio de que usuários não compram produtos — eles "contratam" soluções para realizar um trabalho específico em suas vidas. O foco está na motivação por trás do comportamento, não no comportamento em si.

**Quando usar**
- Quando personas não estão explicando o comportamento do usuário
- Para identificar oportunidades de inovação não óbvias
- Quando o produto precisa ser reposicionado ou redefinido
- Na fase de discovery para entender motivações profundas

**Estrutura do Job Statement**

```
Quando [situação/contexto],
eu quero [motivação/job],
para que eu possa [resultado esperado].
```

**Tipos de jobs**

| Tipo | Descrição | Exemplo |
|---|---|---|
| **Functional** | O trabalho prático que precisa ser feito | "Preciso transferir dinheiro rapidamente" |
| **Emotional** | Como o usuário quer se sentir | "Quero me sentir no controle das minhas finanças" |
| **Social** | Como o usuário quer ser visto pelos outros | "Quero parecer organizado para minha família" |

**Como aplicar**
1. Conduza entrevistas focadas em situações reais, não em opiniões sobre o produto
2. Identifique o job principal (functional) e os jobs secundários (emotional e social)
3. Use os jobs para avaliar se as funcionalidades planejadas realmente atendem ao que o usuário está tentando realizar
4. Compare com soluções alternativas que o usuário usa hoje para o mesmo job

**Resultado esperado**
Entendimento profundo da motivação do usuário, independente de tecnologia ou interface, permitindo soluções mais precisas e inovadoras.

---

## 8. Pesquisa Qualitativa

**O que é**
Metodologia que busca entender o *porquê* por trás de comportamentos, atitudes e motivações dos usuários. Produz dados ricos em contexto — não estatisticamente representativos, mas profundamente explicativos.

**Quando usar**
- Quando o problema ainda não está bem definido e é preciso explorar
- Quando dados quantitativos mostram *o que* acontece, mas não explicam *por que*
- Para mapear a jornada emocional do usuário
- Nas fases de discovery e definição do Double Diamond

**Por que escolher qualitativa e não quantitativa**
Escolha qualitativa quando o objetivo é gerar hipóteses e entender contexto. Escolha quantitativa quando o objetivo é validar hipóteses com representatividade estatística. As duas se complementam — qualitativa primeiro, quantitativa para confirmar escala.

**Formatos principais**

| Formato | Quando usar |
|---|---|
| **Entrevista em profundidade** | Explorar motivações, crenças e experiências individuais em detalhe |
| **Pesquisa de guerrilha** | Validação rápida de hipóteses com baixo custo e tempo reduzido |
| **Grupo focal** | Explorar dinâmicas de grupo e percepções coletivas sobre um tema |
| **Diário de uso** | Capturar comportamento no contexto real, ao longo do tempo |
| **Observação etnográfica** | Entender o usuário no ambiente natural de uso, sem interferência |

**Como aplicar (entrevista em profundidade)**
1. Defina o objetivo da pesquisa: o que você quer entender ao final?
2. Recrute participantes que representem o perfil do usuário-alvo (5–8 para saturação de insights)
3. Monte um roteiro de perguntas abertas — foque em comportamentos passados, não em opiniões sobre o futuro
4. Conduza sem sugestionar; use silêncio e perguntas de follow-up ("me conta mais sobre isso")
5. Registre e transcreva; identifique padrões, repetições e divergências

**Resultado esperado**
Insights ricos sobre motivações, dores e comportamentos dos usuários, com contexto suficiente para gerar hipóteses sólidas para validação.

---

## 9. Pesquisa Quantitativa

**O que é**
Metodologia que busca medir e quantificar comportamentos, atitudes e padrões com representatividade estatística. Responde às perguntas *quantos*, *com que frequência* e *qual a proporção*.

**Quando usar**
- Para validar hipóteses geradas na pesquisa qualitativa
- Quando é preciso escala e representatividade para tomada de decisão
- Para medir impacto de mudanças no produto
- Para segmentar usuários por comportamento ou perfil

**Por que escolher quantitativa e não qualitativa**
Escolha quantitativa quando você já sabe *o que* perguntar e precisa de dados representativos para decidir com confiança. Se ainda não sabe o que perguntar, faça qualitativa primeiro.

**Formatos principais**

| Formato | Quando usar |
|---|---|
| **Survey (questionário)** | Coletar opiniões, preferências e comportamentos em escala |
| **Análise de métricas e analytics** | Entender padrões de uso, funis de conversão, retenção |
| **Dados comportamentais (heatmaps, gravações)** | Observar onde os usuários clicam, travam ou abandonam |
| **NPS / CSAT** | Medir satisfação e propensão a recomendar de forma padronizada |

**Como aplicar (survey)**
1. Defina o objetivo: qual decisão esse dado vai apoiar?
2. Escreva perguntas fechadas, neutras e específicas — evite dupla negação e jargão
3. Defina o tamanho amostral necessário para confiabilidade estatística
4. Distribua pelo canal onde o usuário está — não force o contexto
5. Analise com cruzamento de variáveis, não apenas médias isoladas

**Resultado esperado**
Dados representativos que validam ou refutam hipóteses, com confiança estatística suficiente para embasar decisões de produto.

---

## 10. Teste de Usabilidade

**O que é**
Método de avaliação que observa usuários reais executando tarefas em um produto (protótipo ou versão live), com o objetivo de identificar problemas de usabilidade, pontos de confusão e oportunidades de melhoria.

**Quando usar**
- Antes de lançar uma nova feature ou redesign
- Quando analytics mostram abandono em uma etapa específica
- Para validar se um fluxo faz sentido para o usuário real
- Como complemento a uma avaliação heurística (H1–H10)

**Tipos**

| Tipo | Descrição | Quando preferir |
|---|---|---|
| **Moderado** | Pesquisador conduz a sessão ao vivo, com possibilidade de aprofundamento | Quando é preciso entender o *porquê* do comportamento observado |
| **Não moderado** | Usuário executa as tarefas sozinho, em ferramenta assíncrona | Quando o objetivo é volume e velocidade, com tarefas autoexplicativas |
| **Guerrilha** | Teste rápido e informal com usuários disponíveis no momento | Para validações rápidas com baixo custo e menor rigor metodológico |

**Como aplicar**
1. Defina as tarefas: o que o usuário precisa conseguir fazer? (ex: "complete o cadastro")
2. Recrute 5–8 participantes que representem o perfil real do usuário
3. Prepare o ambiente: roteiro de tarefas, protótipo ou ambiente de teste, gravação
4. Observe sem interferir — não corrija, não sugira, não explique
5. Documente: onde travou, o que disse, onde clicou de forma inesperada
6. Identifique padrões: problemas que aparecem em 3+ usuários são prioritários

**Resultado esperado**
Lista priorizada de problemas de usabilidade com severidade (escala Nielsen: 1–4) e recomendações de correção contextualizadas.

---

## 11. Desk Research

**O que é**
Pesquisa secundária que consolida dados, estudos, relatórios e informações já existentes sobre um tema, mercado ou problema — sem necessidade de coleta de dados primários com usuários.

**Quando usar**
- No início de um projeto, para construir base de conhecimento rapidamente
- Quando há restrição de tempo ou acesso a usuários
- Para contextualizar dados primários com referências de mercado
- Como insumo para a Matriz CSD (preenche Certezas e reduz Dúvidas)

**Por que escolher desk research e não pesquisa primária**
Desk research é o primeiro passo — evita reinventar o que já existe. Sempre faça desk research antes de pesquisa primária para não gastar esforço respondendo perguntas que já têm resposta.

**Fontes prioritárias por categoria**

| Categoria | Fontes |
|---|---|
| **Comportamento do usuário** | Nielsen Norman Group, Baymard Institute, Think with Google |
| **Dados de mercado** | Statista, institutos oficiais de estatística, relatórios de consultorias (McKinsey, Gartner) |
| **Tendências de produto** | Product Hunt, a16z, First Round Review |
| **Regulatório e legal** | Sites oficiais de órgãos reguladores, publicações jurídicas especializadas |
| **Concorrência** | Sites dos concorrentes, reviews de usuários (App Store, Google Play), relatórios públicos |

**Como aplicar**
1. Defina as perguntas que a pesquisa precisa responder
2. Mapeie as fontes mais confiáveis para cada pergunta
3. Consolide os dados com citação de fonte e data (dados de mercado envelhecem)
4. Identifique lacunas que exigirão pesquisa primária
5. Organize os achados em formato que alimente a Matriz CSD ou o OST

**Resultado esperado**
Base de conhecimento estruturada sobre o tema, com fontes confiáveis, lacunas identificadas e insumos para as próximas etapas de pesquisa.

---

## 12. Benchmarking

**O que é**
Análise comparativa de como outros produtos, empresas ou setores resolvem problemas semelhantes ao seu — com o objetivo de identificar padrões, boas práticas, gaps e oportunidades de diferenciação.

**Quando usar**
- Quando se quer entender o estado da arte em uma determinada funcionalidade ou experiência
- Para identificar onde a concorrência está à frente e onde há espaço para inovar
- Como referência antes de iniciar um novo projeto ou feature
- Para fundamentar decisões de design com evidência de mercado

**Tipos de benchmarking**

| Tipo | Descrição | Quando usar |
|---|---|---|
| **Competitivo** | Analisa concorrentes diretos do mesmo mercado | Entender o padrão do setor e identificar diferenciais |
| **Funcional** | Analisa empresas de outros setores que resolvem o mesmo tipo de problema | Buscar inovação fora da caixa do próprio mercado |
| **UX/UI** | Foca especificamente em fluxos, padrões de interface e experiência | Avaliar soluções de design para um problema específico |

**Como aplicar**
1. Defina o que está sendo analisado: qual funcionalidade, fluxo ou experiência?
2. Selecione os benchmarks: mínimo 3, misturando competitivo e funcional
3. Defina critérios de análise consistentes para todos os benchmarks
4. Documente com capturas, fluxos e anotações — não apenas impressões
5. Identifique padrões (o que todos fazem), boas práticas (o que funciona bem) e gaps (o que nenhum resolve bem)
6. Derive oportunidades para o seu produto com base nos achados

**Resultado esperado**
Mapa comparativo estruturado com padrões identificados, boas práticas referenciadas, gaps de mercado e oportunidades de diferenciação para o produto.

---

## 13. Teste A/B

**O que é**
Experimento controlado que compara duas versões de um elemento (A e B) para determinar qual performa melhor em relação a uma métrica específica, com base em comportamento real de usuários.

**Quando usar**
- Quando há duas hipóteses de solução e dados reais para decidir entre elas
- Para otimizar elementos já existentes (CTAs, copy, layout, fluxos)
- Quando há volume de tráfego suficiente para significância estatística
- Na fase de entrega do Double Diamond, para validar a solução escolhida

**Por que escolher A/B e não teste de usabilidade**
Teste A/B mede *qual performa melhor* em escala — mas não explica *por quê*. Use A/B para confirmar; use teste de usabilidade para entender. Idealmente, use os dois em sequência.

**Requisitos para um teste A/B válido**
- Uma única variável alterada por vez (não teste múltiplas mudanças simultaneamente)
- Tamanho amostral calculado para significância estatística (mínimo 95% de confiança)
- Duração suficiente para capturar variação de comportamento semanal
- Métrica primária definida antes do teste (não mude o critério de sucesso após iniciar)

**Como aplicar**
1. Defina a hipótese: "Acreditamos que [mudança X] vai [aumentar/reduzir] [métrica Y] porque [razão Z]"
2. Calcule o tamanho amostral necessário
3. Divida o tráfego aleatoriamente entre versão A (controle) e versão B (variante)
4. Monitore apenas a métrica primária durante o teste
5. Ao atingir significância, analise os resultados e documente o aprendizado — inclusive se B perdeu

**Resultado esperado**
Decisão baseada em dados com confiança estatística, acompanhada do aprendizado documentado independentemente do resultado.

---

## 14. Fakedoor Test

**O que é**
Técnica de validação de demanda que expõe uma funcionalidade ainda não existente para usuários reais — geralmente como um botão, link ou banner — e mede o interesse real pelo nível de interação, antes de qualquer investimento em desenvolvimento.

**Quando usar**
- Para validar se uma funcionalidade tem demanda real antes de construí-la
- Quando o custo de desenvolver para depois descobrir que ninguém quer é alto
- Na fase de Develop do Double Diamond, antes de prototipar com fidelidade
- Como alternativa mais rápida ao MVP quando o objetivo é apenas validar intenção

**Como funciona**
O usuário vê a "porta" (botão, card, link) da funcionalidade. Ao clicar, em vez de acessar a feature, vê uma mensagem explicando que ela está em desenvolvimento — e pode ser convidado a deixar contato para ser notificado. A taxa de clique mede o interesse real.

**Como aplicar**
1. Defina a funcionalidade a ser validada e a hipótese de interesse
2. Crie o elemento de interface (botão, banner, card) como se a feature existisse
3. Ao clicar, exiba mensagem honesta: "Esta funcionalidade está sendo desenvolvida. Deixe seu email para ser o primeiro a saber."
4. Defina a métrica de sucesso antes do teste: qual taxa de clique valida a hipótese?
5. Analise os dados e, se validado, priorize o desenvolvimento; se não, descarte ou reformule

**Atenção ética**
O fakedoor deve sempre ter uma saída honesta — nunca simular que a funcionalidade existe de verdade. Usuários que clicam e recebem uma mensagem transparente tendem a reagir positivamente.

**Resultado esperado**
Dado de intenção real de uso, com custo mínimo de implementação, que fundamenta (ou descarta) a priorização de uma funcionalidade.

---

## 15. Figma

**O que é**
Ferramenta de design colaborativo baseada em browser, usada para criação de interfaces, componentes, protótipos navegáveis e design systems.

**Quando usar**
- Wireframes de baixa e alta fidelidade
- Prototipação navegável para testes de usabilidade
- Construção e manutenção de design system (componentes, tokens, estilos)
- Handoff para desenvolvedores (especificações, medidas, assets)

**Boas práticas obrigatórias**
- Organizar frames com nomenclatura clara e hierarquia de páginas lógica
- Usar componentes e variantes — nunca duplicar elementos manualmente
- Definir e usar tokens de design (cores, tipografia, espaçamento) como estilos locais ou variáveis
- Manter auto-layout em todos os componentes para garantir responsividade
- Documentar estados dos componentes: default, hover, focus, active, disabled, error

**No contexto desta skill**
- Consulte `references/patterns.md` antes de criar qualquer componente para verificar padrões existentes
- Consulte `references/heuristics.md` para garantir que fluxos e interfaces respeitem as heurísticas de Nielsen

---

## 16. Storybook

**O que é**
Ferramenta de desenvolvimento e documentação de componentes de UI de forma isolada, independente da aplicação principal.

**Quando usar**
- Desenvolvimento e teste de componentes do design system isoladamente
- Documentação visual e interativa dos componentes para o time de design e desenvolvimento
- Garantia de que componentes funcionam corretamente em todos os seus estados e variações

**Boas práticas obrigatórias**
- Criar uma story para cada estado do componente (default, hover, focus, disabled, error, loading)
- Documentar props com descrições claras e exemplos de uso
- Manter stories sincronizadas com as definições do Figma
- Usar Controls para permitir que stakeholders testem variações dos componentes

---

## 17. Radix UI / Headless UI

**O que é**
Bibliotecas de componentes de UI sem estilo (headless) que fornecem comportamento, acessibilidade e semântica corretos, deixando toda a estilização para o time de design.

**Quando usar**
- Como base para componentes de design system que exigem comportamento complexo (dropdowns, modais, accordions, tooltips, dialogs)
- Quando acessibilidade é requisito não negociável (ARIA, navegação por teclado, screen readers)
- Para evitar reinventar comportamentos já resolvidos e testados

**Por que preferir headless e não componentes pré-estilizados**
Headless components separam comportamento de estilo — o design system mantém controle visual total sem abrir mão de acessibilidade e comportamento correto. Componentes pré-estilizados (ex: MUI, Chakra) impõem decisões visuais que conflitam com o design system do produto.

**Boas práticas**
- Sempre combine com Tailwind CSS para estilização
- Valide acessibilidade com screen reader após implementação
- Documente no Storybook com todos os estados de interação

---

## 18. Tailwind CSS

**O que é**
Framework CSS utilitário que aplica estilos diretamente no HTML/JSX através de classes pré-definidas, seguindo uma escala consistente de valores.

**Quando usar**
- Estilização de interfaces React, Next.js ou Svelte
- Quando velocidade e consistência de implementação são prioritárias
- Para garantir que os tokens de design (espaçamento, cores, tipografia) sejam respeitados no código

**Boas práticas obrigatórias**
- Configurar o `tailwind.config` com os tokens de design do produto (cores, tipografia, espaçamento) — nunca use valores arbitrários sem necessidade
- Usar `@apply` com moderação — apenas para abstrações reutilizáveis
- Manter classes organizadas por categoria (layout, tipografia, cor, estado)
- Combinar com Radix UI para componentes acessíveis com estilo controlado

---

## 19. Framer Motion

**O que é**
Biblioteca de animação para React que permite criar microinterações, transições e animações de layout com API declarativa e performática.

**Quando usar**
- Microinterações que comunicam estado (feedback de ação, carregamento, sucesso)
- Transições entre páginas ou estados que melhoram a orientação do usuário
- Animações de layout que reduzem a percepção de mudança abrupta

**Princípio de uso**
Animação serve à usabilidade — não à decoração. Toda animação deve ter um propósito funcional: comunicar mudança de estado, guiar o olhar, confirmar uma ação ou criar senso de progressão.

**Boas práticas**
- Respeite `prefers-reduced-motion` — ofereça sempre uma versão sem animação
- Duração máxima de 300ms para microinterações; 500ms para transições de página
- Nunca anime elementos que o usuário está tentando interagir no momento
- Use `layout` prop para animações de reordenação — evita cálculos manuais de posição

---

## 20. React e Next.js

**O que é**
React é a biblioteca JavaScript para construção de interfaces baseadas em componentes. Next.js é o framework full-stack construído sobre React, com suporte nativo a SSR, SSG, rotas de API e otimizações de performance.

**Quando usar**
- React: construção de interfaces interativas e SPAs
- Next.js: quando SEO, performance, rotas de API ou server-side rendering são requisitos

**Boas práticas obrigatórias**
- Componentes pequenos e com responsabilidade única
- Separar lógica de negócio de lógica de apresentação (hooks customizados para lógica)
- Tipar componentes e props com TypeScript
- Usar Server Components no Next.js por padrão — Client Components apenas quando necessário (interatividade, hooks de estado)
- Nunca colocar dados sensíveis em Client Components

---

## 21. Svelte

**O que é**
Framework JavaScript reativo que compila componentes para JavaScript puro no build — sem virtual DOM, resultando em bundles menores e melhor performance em runtime.

**Quando usar**
- Quando performance e tamanho de bundle são críticos
- Para interfaces com animações e reatividade complexa
- Como alternativa ao React quando o projeto não exige o ecossistema React

**Diferença-chave em relação ao React**
Svelte não usa virtual DOM — a reatividade é compilada. Isso resulta em código mais simples e performance superior em interfaces com muitas atualizações de estado.

---

## 22. Git e GitHub

**O que é**
Git é o sistema de controle de versão distribuído. GitHub é a plataforma de hospedagem e colaboração de código construída sobre Git.

**Quando usar**
- Em todo projeto que envolva entrega de código — sem exceção
- Para colaboração entre design e desenvolvimento (branch por feature, pull requests com contexto)
- Para rastreabilidade de decisões técnicas ao longo do projeto

**Boas práticas obrigatórias**
- Commits atômicos com mensagens claras no padrão Conventional Commits (`feat:`, `fix:`, `chore:`, `docs:`)
- Uma branch por feature ou correção — nunca trabalhar diretamente na `main`
- Pull requests com descrição do contexto, o que foi feito e como testar
- Code review antes de qualquer merge em branch principal
- `.gitignore` configurado corretamente — nunca commitar variáveis de ambiente, chaves de API ou dependências
