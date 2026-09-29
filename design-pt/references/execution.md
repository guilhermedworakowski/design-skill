# execution — Padrões de execução do Designer Engineer

## Para que serve

Este arquivo é a camada de **execução** do Designer Engineer. Ele complementa `references/cognitive-biases.md`:

- **cognitive-biases.md** responde *por que* uma decisão funciona (comportamento do usuário)
- **execution.md** responde *como* construir aquilo na interface (padrões, valores, estados, checklists)

Os dois são consultados **sempre, em conjunto**, em toda entrega do Designer Engineer. Nenhum substitui o outro: viés sem padrão gera justificativa sem construção; padrão sem viés gera construção sem justificativa.

Princípios básicos de espaçamento, tipografia, cor e acessibilidade ficam no próprio agente (`agents/designer-engineer.md`). As leis de Hick, Miller, Fitts, Von Restorff e Serial Position ficam em `cognitive-biases.md`. Este arquivo não repete esse conteúdo, só aponta para ele.

---

## Como usar junto com os vieses

1. **Mapeie os vieses** relevantes em `references/cognitive-biases.md`
2. **Localize os padrões** correspondentes neste arquivo (use a tabela abaixo como ponte)
3. **Construa** aplicando as regras e valores do padrão
4. **Documente em par**: para cada decisão, cite o viés (*por que*) + o padrão de execução (*como*) + a heurística de Nielsen
5. **Feche** com a checklist da seção 14 (Handoff e QA) quando a entrega for alta fidelidade, handoff ou código

### Ponte viés → padrão

| Viés / lei (cognitive-biases.md) | Seções deste arquivo |
|---|---|
| Anchoring Bias | 10 Hierarquia visual · 12 UX writing |
| Social Proof | 3 Feedback · 12 UX writing |
| Loss Aversion · Framing Effect | 4 Erros · 12 UX writing |
| Decoy Effect | 10 Hierarquia visual |
| Hick's Law | 5 Formulários · 6 Navegação · 7 Busca |
| Miller's Law | 5 Formulários · 11 Layout |
| Zeigarnik · Goal Gradient | 5 Formulários (multi-step) · 8 Onboarding · 9 Movimento |
| Habit Loop · VRR | 3 Feedback · 9 Microinterações |
| Scarcity & FOMO | 3 Feedback · 12 UX writing (sempre com o Designer Checklist ético) |
| Peak-End Rule | 3 Feedback (confirmação) · 9 Microinterações |
| Von Restorff · Serial Position | 6 Navegação · 10 Hierarquia visual |
| Jakob's Law | 6 Navegação · 7 Busca · 9 Gestos |
| Confirmation Bias | 12 UX writing (pós-conversão) |
| Fitts's Law | 9 Gestos · 11 Responsivo · 14 QA (alvos de toque) |
| Cognitive Load | 1 Estados · 2 Tempo de resposta · 10 Hierarquia |

---

## 1. Estados de interface

Modele todo componente ou fluxo como **máquina de estados**: estados, eventos que causam transição, regras (guards) e ações. Isso elimina estados impossíveis (ex: loading e erro ao mesmo tempo) e vira linguagem comum com dev.

**Estados obrigatórios a desenhar** (não só o caminho feliz):
- Componente: default · hover · focus · active · disabled · loading · error
- Tela/dado: vazio (primeiro uso e sem resultado) · carregando · parcial · sucesso · erro · sem permissão

**Fluxos-padrão:**
- Formulário: idle → editando → validando → enviando → sucesso/erro → idle
- Busca de dados: idle → carregando → sucesso/erro; erro → tentando de novo → sucesso/erro
- Wizard: etapa 1 → etapa 2 → … → revisão → enviando → concluído

Regras: todo estado tem saída (sem becos sem saída); uma máquina por assunto; cada estado tem uma representação visual definida.

---

## 2. Tempo de resposta e loading

**Limiar de Doherty:** abaixo de 400ms o usuário mantém o fluxo; acima, percebe a espera.

| Duração | O que mostrar |
|---|---|
| < 100ms | Nada — só a mudança de estado do elemento |
| 100ms–1s | Indicador sutil (opacidade, skeleton) |
| 1–10s | Loading claro; barra determinada se o progresso for mensurável |
| > 10s | Progresso detalhado, estimativa de tempo, opção de seguir em segundo plano ou cancelar |

**Padrões:**
- **Skeleton** para conteúdo com estrutura conhecida (preferível a spinner); formato fiel ao conteúdo real
- **Spinner** só para duração desconhecida e curta; pequeno e discreto
- **Optimistic UI**: mostra o resultado na hora, reconcilia com o servidor e desfaz se falhar
- **Carregamento progressivo**: conteúdo crítico primeiro, lazy-load abaixo da dobra, imagens blur-up

Regras: feedback visual do toque em até 100ms, sempre; nunca tela em branco; nunca mais de um indicador de loading concorrendo; sem layout shift ao carregar; conteúdo entra com fade (não "pisca"); não exibir spinner para ações abaixo de 400ms (o flash atrapalha).

---

## 3. Feedback e confirmação

Toda ação do usuário recebe resposta, com intensidade proporcional à importância da ação.

**Hierarquia de onde mostrar** (prefira o mais próximo da ação):
1. Inline, no próprio elemento
2. No componente
3. Na página (toast, banner)
4. No sistema (notificação fora da tela atual)

**Duração:**
- Toast: some sozinho em 3–5s
- Erro: persiste até ser resolvido ou dispensado
- Confirmação: breve, com janela de desfazer
- Status: persiste enquanto for relevante

Regras: prefira **desfazer** a "Tem certeza?"; não interrompa o fluxo por confirmações menores; nunca use só cor para comunicar status; em momentos de pico e de fim de jornada (Peak-End), a confirmação merece cuidado extra, com resumo do que foi feito e próximo passo.

---

## 4. Erros

**Ordem de prioridade:** prevenir → detectar → comunicar → recuperar.

- **Prevenir:** inputs com restrição (date picker, select), defaults inteligentes, auto-save, confirmação só para ações destrutivas
- **Detectar:** validação por campo, validação no envio, falha de rede, timeout, permissão
- **Comunicar**, sempre neste formato:
  - **O que aconteceu** (linguagem humana, sem código de erro)
  - **Por que** (se ajudar)
  - **O que fazer agora** (ação específica)
- **Recuperar:** nunca apague o que o usuário digitou; ofereça tentar de novo; caminho alternativo; desfazer

| Contexto | Padrão |
|---|---|
| Formulário | Erro inline no campo + resumo no topo se forem vários |
| Página | Erro de página inteira com "tentar de novo" e "voltar" |
| Rede | Toast ou banner com "tentar de novo" |
| Sem resultado | Empty state com sugestões |
| Permissão | Explica qual acesso falta e como obter |

Nunca culpe o usuário. Nunca "Algo deu errado" sem contexto.

---

## 5. Formulários

**Layout:** uma coluna; largura do campo proporcional ao tamanho esperado da resposta; label acima do campo; campos relacionados agrupados com título de seção.

**Labels:** sempre visíveis (placeholder nunca é label); sentence case; texto de ajuda entre label e campo; marque os **opcionais**, não os obrigatórios; contador de caracteres sempre visível quando houver limite.

**Tipo de input:**

| Dado | Input |
|---|---|
| Uma escolha entre até 5 | Radio (todas visíveis) |
| Uma escolha entre 6+ | Select / combobox |
| Várias escolhas | Checkbox |
| Data | Date picker ou campos segmentados — nunca texto livre |
| Telefone, documento de identificação, cartão | Campo com máscara |
| Senha | Com botão mostrar/ocultar |

**Validação:** ao sair do campo (on blur), não a cada tecla; erro logo abaixo do campo; mensagem que ensina a corrigir ("O e-mail precisa ter @", não "E-mail inválido"); check de sucesso só onde a validade não é óbvia (senha, disponibilidade de usuário).

**Multi-step:** indicador de progresso visual (Zeigarnik/Goal Gradient); cada etapa é um bloco coerente; voltar sem perder dados; salvar progresso em formulários longos; etapa de revisão antes de envios de alto risco (pagamento, transferência de dinheiro, dados legais).

**Acessibilidade:** label programático (`<label for>` ou `aria-label`); erro ligado ao campo (`aria-describedby`); ordem de foco igual à ordem visual; resumo de erros focável com links para cada campo.

Corte todo campo opcional possível. Menos campos = mais conclusão.

---

## 6. Navegação

| Situação | Padrão |
|---|---|
| Mobile, 3–5 destinos principais | Tab bar inferior (ícone + label) |
| Desktop com muitos destinos ou hierarquia | Sidebar |
| Site simples ou documentação | Top nav (4–7 itens) |
| Hierarquia profunda | Breadcrumb + sidebar local |
| Visões paralelas do mesmo conteúdo | Tabs ou segmented control (2–4) |
| Acesso ocasional (conta, ajuda, config.) | Navegação utilitária, separada visualmente |

**Princípios:** o usuário sempre sabe onde está (estado ativo, título, breadcrumb); o rótulo prevê o destino; destinos principais no alcance do polegar no mobile; estrutura e posição não mudam entre telas.

Regras: estado ativo diferenciado por mais que cor (peso, indicador, sublinhado); hamburger nunca como navegação principal no desktop; não misture níveis global e local no mesmo componente; mais de 7 itens no topo pede revisão da arquitetura de informação antes de novos itens; valide rótulos com teste de primeiro clique.

---

## 7. Busca

- **Campo:** placeholder diz o que dá para buscar ("Buscar produtos, marcas ou categorias"); foco automático ao abrir; botão de limpar quando houver texto; a busca feita continua no campo para refinar
- **Autocomplete:** a partir de 2–3 caracteres; ordem: recentes → populares → previsões; destaque do termo digitado; 5–8 sugestões no máximo; navegável por teclado; inclua destinos de navegação ("meus pedidos", "meu perfil")
- **Resultados:** mostre a quantidade; termo destacado no título e no trecho; metadados que ajudam a decidir o clique; ordenação visível e alterável
- **Filtros:** só os relevantes ao resultado atual, com contagem; filtros aplicados visíveis e removíveis um a um; "Limpar todos"
- **Zero resultado** (o estado mais negligenciado): confirme o que foi buscado, sugira correção de digitação e termos relacionados, ofereça caminhos alternativos. Nunca página vazia.

Tolere erros de digitação, sinônimos, plurais e correspondência parcial.

---

## 8. Onboarding e empty states

**Objetivos, em ordem:** chegar ao valor rápido → orientar em vez de ensinar tudo → gerar pequenas vitórias → pedir só o necessário agora.

| Padrão | Quando usar |
|---|---|
| Onboarding progressivo (tooltips e dicas no primeiro uso) | Produtos com muitas funcionalidades |
| Wizard de configuração | O produto não funciona sem setup; etapas mínimas, opcionais puláveis, celebre o fim |
| Dados de exemplo | Quando o vazio impede entender o produto (dashboards); sinalize que é exemplo e deixe limpar |
| Tour guiado | Só para 3–5 conceitos centrais; sempre dispensável |

**Empty state é onboarding:** explica para que serve o espaço, oferece uma ação clara ("Crie seu primeiro projeto"), mostra como fica preenchido. Nunca uma tabela vazia só com cabeçalho.

**Reduzir atrito:** adie coleta de dados não essenciais, defaults inteligentes, login social/SSO, "fazer depois" em etapas não críticas.

Defina o **momento "aha"** e desenhe o caminho mais curto até ele. Métricas: taxa e tempo de ativação, abandono por etapa, retenção D7/D30.

---

## 9. Movimento, microinterações e gestos

**Microinteração**, especifique sempre: gatilho → regras → feedback (visual/sonoro/háptico) → loop/modo (primeira vez vs. repetição) → duração/easing → acessibilidade.

**Duração:**
- Micro (50–100ms): estado de botão, toggle
- Curta (150–250ms): tooltip, fade, pequenos deslocamentos
- Média (250–400ms): transição de tela, modal
- Longa (400–700ms): coreografias complexas (raro)

**Easing:** ease-out para entrada · ease-in para saída · ease-in-out para mudar de posição · linear só para loops contínuos (progresso).

Regras: toda animação comunica algo; mais rápido quase sempre é melhor; interrompível; stagger de 30–50ms entre itens de lista, sequência total abaixo de 700ms; sempre respeite `prefers-reduced-motion`; anime `transform`/`opacity` por performance.

**Gestos:** sempre com alternativa sem gesto (botão/menu); affordance visível e dica no primeiro uso; resposta visual imediata ao iniciar; limiar de 10–15px antes de ativar; long press ~500ms; trava de direção para separar scroll de swipe; gestos do sistema têm prioridade; desfazer para gestos destrutivos; siga as convenções da plataforma (Jakob).

---

## 10. Hierarquia visual e composição

**Ferramentas de hierarquia:** tamanho (diferença mínima de 1,5x entre níveis) · peso · cor e contraste · espaço em branco ao redor · posição (topo-esquerda primeiro; padrões F e Z) · isolamento.

**Níveis:** primário (título, CTA principal) → secundário (seções, conteúdo-chave) → terciário (apoio, metadados) → quaternário (letras miúdas, timestamps).

**Composição:**
- **Equilíbrio:** peso visual distribuído com intenção; centro de gravidade claro
- **Espaço em branco:** macro entre seções, micro consistente entre elementos
- **Ritmo:** intervalos da escala de espaçamento; itens repetidos com tamanho e gap uniformes
- **Gestalt:** proximidade (relacionado junto), similaridade (mesma função, mesmo visual), figura/fundo, continuidade de alinhamento

Regras: **um CTA primário por tela**; teste do "olho semicerrado" (desfocando, a hierarquia continua clara); no máximo dois pesos tipográficos ativos por tela; tipografia só com passos da escala (sem ajustes de 1–2px); line-height 1.1–1.3 em títulos e 1.4–1.6 em corpo; linha de leitura entre 45 e 75 caracteres.

---

## 11. Layout, grid, responsivo e dark mode

**Grid:** 4 colunas (mobile) · 8 (tablet) · 12 (desktop); gutters de 16/24/32px; margens de 16px (mobile) a 24–48px (desktop); baseline de 4 ou 8px. Quebrar o grid só de propósito, para ênfase.

**Breakpoints de referência:** 375–639px (celular) · 640–1023px (tablet) · 1024–1439px (notebook) · 1440px+ (desktop). Mobile-first; o conteúdo define o breakpoint, não o dispositivo.

**Padrões responsivos:** column drop · reflow (horizontal vira vertical) · off-canvas para conteúdo secundário · priority+ (o mais importante visível, o resto em "mais").

**Por tipo de entrada:** toque exige alvo mínimo de 44px; mouse pede hover; teclado pede foco visível e ordem lógica.

**Dark mode** (não é inverter cores):
- Elevação por superfícies mais claras, não por sombra (fundo ~#121212 → superfícies 1, 2, 3 progressivamente mais claras)
- Cores primárias 10–20% menos saturadas
- Texto off-white (~#E0E0E0), não branco puro; bordas brancas com baixa opacidade
- Tokens semânticos para alternar temas sem retrabalho; respeite `prefers-color-scheme` e ofereça toggle manual

---

## 12. UX writing

- **Botões/CTAs:** começam com verbo, dizem o resultado ("Confirmar pagamento", não "Enviar"); refletem a intenção do usuário, não a do negócio
- **Labels:** claras, sem jargão nem nome interno de produto
- **Placeholder:** exemplo de formato, não instrução
- **Erros:** formato o que aconteceu / por que / o que fazer (seção 4); tom humano, sem culpa
- **Empty states:** o que vai aparecer aqui + ação clara + tom encorajador
- **Confirmação:** o que acabou de acontecer + próximo passo + desfazer quando reversível
- **Onboarding:** um conceito por vez, orientado a ação, pulável

**Voz** é constante (personalidade da marca, ver `references/patterns.md`); **tom** varia com o contexto (celebração ≠ erro ≠ instrução).

Princípios: claro > criativo · conciso > completo · útil > promocional · consistente > original. Escreva o texto antes de desenhar a tela (content-first). Framing, escassez e prova social no texto passam sempre pelo Designer Checklist ético de `cognitive-biases.md`.

---

## 13. Componentes e tokens

**Especificação de componente**, nesta ordem:
1. Visão geral: nome, para que serve, quando usar e quando **não** usar
2. Anatomia: partes obrigatórias e opcionais
3. Variantes: tamanho (sm/md/lg), estilo (primary/secondary/ghost), layout
4. Props/API: nome, tipo, default, obrigatório
5. Estados: default, hover, focus, active, disabled, loading, error
6. Comportamento: interações, animação, responsivo, casos-limite
7. Acessibilidade: role ARIA, teclado, leitor de tela, gestão de foco
8. Uso: do/don't, regras de conteúdo, componentes relacionados

**Tokens em três camadas:**
1. **Globais**: valor bruto (`blue-500: #3B82F6`)
2. **Semânticos (alias)**: função (`color-action-primary`)
3. **De componente**: uso específico (`button-color-primary`)

Nomenclatura: `{categoria}-{propriedade}-{variante}-{estado}`. Categorias: cor, espaçamento, tipografia, elevação, borda, movimento. Componente nunca referencia valor bruto; temas trocam só a camada semântica.

---

## 14. Handoff e QA

**Handoff contém:**
- **Visual:** espaçamentos, cores, tipografia, raio, sombra, sempre por nome de token (não hex)
- **Interação:** todos os estados, transições (duração, easing, propriedade), gestos, ordem de tab e atalhos
- **Conteúdo:** limites de caracteres e truncamento, regras de conteúdo dinâmico (mín./máx.), expansão de texto em traduções, textos de vazio/loading/erro
- **Casos-limite:** conteúdo mínimo e máximo, cada breakpoint, requisitos de acessibilidade
- **Notas de implementação:** reuso de componentes, dependências de API, performance
- **Assets:** ícones em SVG nomeados por convenção, imagens com variantes responsivas

**Checklist de QA** (design vs. implementação):
- [ ] Cores, tipografia, espaçamento, raio e sombra batem com os tokens
- [ ] Grid e comportamento em cada breakpoint conforme spec; sem overflow ou corte
- [ ] Todos os estados renderizam (incluindo vazio, loading e erro)
- [ ] Transições conforme spec; `prefers-reduced-motion` respeitado
- [ ] Alvos de toque ≥ 44px; navegação por teclado na ordem certa; foco visível
- [ ] Contraste WCAG AA (4.5:1 texto, 3:1 texto grande e elementos de UI)
- [ ] Leitor de tela anuncia corretamente; roles e labels ARIA corretos
- [ ] Conteúdo real (sem lorem ipsum); truncamento funciona
- [ ] Funciona com fonte aumentada nas configurações do sistema

---

## 15. Crítica de tela

Para avaliar uma tela existente, analise quatro dimensões: **Hierarquia** (seção 10) · **Marca** (voz, tom e tokens de `references/patterns.md`) · **Composição** (seção 10) · **Tipografia** (escala, legibilidade, consistência, uso de tokens).

Para cada problema: **observação** (neutra) → **problema** (o que quebra e por quê) → **correção** (específica, com nome do token quando couber) → **viés afetado** (de `cognitive-biases.md`).

**Priorize:**
- **P1 — Crítico:** quebra usabilidade, acessibilidade ou marca; corrigir antes de publicar
- **P2 — Importante:** degrada a experiência ou gera inconsistência; corrigir no ciclo atual
- **P3 — Polimento:** refinamento visual; quando houver capacidade

Feche com um parágrafo apontando a dimensão mais forte e a mais fraca.
