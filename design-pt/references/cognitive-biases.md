# cognitive-biases

## Descrição

Este arquivo documenta **18 vieses cognitivos e leis psicológicas** aplicados ao design de produtos digitais, mapeados diretamente em relação aos agentes e frameworks desta skill de design.

Seu propósito é duplo:

1. **Como referência para os agentes** — cada viés especifica qual agente deve aplicá-lo e em qual etapa do processo de design. Os agentes devem cruzar este arquivo ao tomar decisões sobre persuasão, arquitetura de informação, design de interação ou estratégia de engajamento.

2. **Como guia de estudo para o time de design** — o arquivo documenta a base teórica de cada viés (nome, descrição, melhor momento de aplicação, como usar, um exemplo prático e relações com outros vieses), junto com as conexões exatas com a skill de design que o tornam acionável.

**Fontes bibliográficas:** *Enviesados* (Rian Dutra) · *Laws of UX* (Jon Yablonski) · *O Poder do Hábito* (Charles Duhigg) · *Rápido e Devagar* (Daniel Kahneman) · *As Armas da Persuasão* (Robert Cialdini).

**Escopo:** Este arquivo é uma referência independente. Não deve ser importado automaticamente pela skill — deve ser lido deliberadamente sempre que uma decisão de design fundamentada em vieses for necessária.

---

## Como ler este arquivo

Cada viés segue esta estrutura:

| Campo | Descrição |
|---|---|
| **Descrição** | Base teórica e mecanismo cognitivo |
| **Melhor momento** | Em que ponto do processo de design o viés tem maior impacto |
| **Como usar** | Padrões práticos de aplicação |
| **Exemplo** | Aplicação prática em produtos digitais reais (e-commerce, SaaS, fintech, educação, streaming etc.) |
| **Relações** | Outros vieses que este ativa ou pelos quais é reforçado |
| **Agente** | Qual agente especialista é o principal responsável por aplicá-lo |
| **Framework** | A qual framework de `references/frameworks.md` ele se conecta |

> Os nomes dos vieses são mantidos em inglês (com a tradução entre parênteses), pois é assim que aparecem nos agentes, na literatura de referência e no mercado.

---

## Vieses

---

### 01 · Anchoring Bias (Viés de Ancoragem)

**Descrição**
A âncora é a primeira informação que o cérebro recebe, e ela se torna a referência central para todos os julgamentos seguintes. Kahneman e Tversky demonstraram que as pessoas se apoiam fortemente no primeiro número, preço ou dado apresentado — mesmo que irrelevante — ajustando suas estimativas a partir dele em vez de partir do zero. Em produto, a forma como a primeira opção é apresentada molda como todas as outras são percebidas.

**Melhor momento**
Ideação e UI Design — ao definir hierarquias de preço, ordenação de produtos, exibição de dados em dashboards ou qualquer interface em que a comparação faça parte da decisão.

**Como usar**
- Apresente o preço mais alto primeiro (plano Premium) para que os demais pareçam mais acessíveis por comparação.
- Exiba o preço original riscado ao lado do valor com desconto para ancorar o valor percebido.
- Em tabelas comparativas, posicione a opção desejada como ponto central de referência.
- Em dashboards, a primeira métrica exibida define a linha de base cognitiva para todas as outras.

**Exemplo**
Páginas de preço de SaaS que listam o plano Enterprise primeiro fazem o plano Pro parecer acessível por comparação. O e-commerce mostra o preço original riscado ao lado do preço promocional para ancorar o valor percebido. Em dashboards de analytics, o primeiro número exibido (ex.: a receita do mês anterior) vira a linha de base contra a qual todas as outras métricas são lidas — por isso a escolha dele é uma decisão de design, não uma escolha neutra.

**Relações**
Decoy Effect · Framing Effect · Loss Aversion

**Agente**
Designer Engineer (execução de UI) · Strategist (decisões de preço e de arquitetura de informação)

**Framework**
Double Diamond (fase de Ideação) · MoSCoW (enquadramento de valor na priorização de funcionalidades)

---

### 02 · Social Proof (Prova Social)

**Descrição**
Em situações de incerteza, as pessoas usam o comportamento dos outros como guia. Cialdini formalizou isso em *As Armas da Persuasão* (1984): seguimos o que os outros fazem porque interpretamos isso como evidência do comportamento correto. Em ambientes digitais, a prova social reduz o esforço cognitivo da decisão — se outros já fizeram, deve ser seguro. Quanto mais próximo do perfil do usuário for a pessoa de referência, mais forte o efeito.

**Melhor momento**
UI Design, Prototipação e Produto ativo — em fluxos de cadastro, seleção de produtos, páginas de conversão e pontos de contato de retenção.

**Como usar**
- Exiba o número de usuários ativos, avaliações e reviews perto do ponto de decisão.
- Use depoimentos reais, com foto e nome.
- Segmente a prova social por nicho de usuário ("O mais popular entre designers como você").
- Mostre contadores de atividade que atualizam quase em tempo real para sinalizar vitalidade.

**Exemplo**
Marketplaces mostram "1.200 pessoas compraram isto no último mês" ao lado do botão Adicionar ao carrinho. Plataformas de cursos exibem o número de alunos matriculados e as avaliações ao lado do CTA de matrícula. Landing pages B2B mostram logos de clientes conhecidos logo na primeira dobra. A prova segmentada convence mais do que um número global: "Popular entre times do seu tamanho" funciona melhor que "10.000 usuários".

**Relações**
Framing Effect · FOMO · Confirmation Bias

**Agente**
Designer Engineer (execução de UI) · Researcher (validar em quais sinais sociais os usuários confiam)

**Framework**
Pesquisa Qualitativa — para identificar quais sinais de prova social são críveis para o segmento de usuários · Teste A/B — para validar qual formato (contadores, avaliações ou depoimentos) converte melhor

---

### 03 · Loss Aversion (Aversão à Perda)

**Descrição**
Kahneman e Tversky demonstraram que a dor de perder algo é psicologicamente cerca de 2× mais intensa do que o prazer de ganhar algo equivalente. Mensagens que destacam o que o usuário vai perder se não agir — em vez do que vai ganhar — tendem a converter melhor. A aversão à perda é a base de toda lógica de urgência genuína no design de produto.

**Melhor momento**
UI Design e Produto ativo — especialmente em fluxos de conversão, cancelamento, retenção e sequências de reativação.

**Como usar**
- Escreva CTAs com enquadramento de perda: "Não perca sua oferta exclusiva" em vez de "Resgate sua oferta".
- Em fluxos de cancelamento, mostre o que o usuário vai perder (trabalho salvo, histórico, configurações, crédito restante).
- Em promoções por tempo limitado, destaque o tempo restante — não o benefício em si.
- Em campanhas de reativação, comece pelo que o usuário perdeu desde a última sessão.

**Exemplo**
"Seu teste termina em 3 dias — mantenha seus projetos e configurações" converte mais que "Faça upgrade agora". Num fluxo de cancelamento de assinatura, mostrar as playlists salvas, o histórico ou as preferências torna o custo de sair concreto — de forma honesta e sem dificultar o cancelamento. Em e-mails de reativação, "Veja o que você perdeu esta semana" gera mais reengajamento que "Temos novidades".

**Relações**
Scarcity · FOMO · Framing Effect · Anchoring Bias

**Agente**
Designer Engineer (copy e enquadramento na UI) · Strategist (desenho da estratégia de retenção)

**Framework**
Double Diamond (fase Define — identificar onde existem momentos de aversão à perda na jornada do usuário) · Service Blueprint (mapear gatilhos de backstage que podem levar o enquadramento de perda ao usuário no momento certo)

---

### 04 · Framing Effect (Efeito de Enquadramento)

**Descrição**
A mesma informação, apresentada de formas diferentes, leva a decisões diferentes. Kahneman demonstrou que as pessoas reagem de forma diferente a "taxa de sobrevivência de 90%" e "taxa de mortalidade de 10%" — dados idênticos. Em design, o enquadramento controla como o usuário interpreta um dado, uma ação ou uma oferta. A forma como uma proposta é enquadrada determina seu valor, risco e urgência percebidos.

**Melhor momento**
UX Writing, UI Design e Prototipação — em microcopy de CTAs, descrições de planos, rótulos de status, mensagens de feedback e qualquer conteúdo em que a interpretação determine a ação.

**Como usar**
- Use enquadramentos positivos no onboarding ("Falta só um passo") e de perda na conversão ("Não fique de fora").
- Em preços, enquadre o custo por dia em vez de por mês.
- Enquadramentos de progresso ("85% concluído") motivam mais que enquadramentos de déficit ("faltam 15%").
- Descreva a funcionalidade como benefício para o usuário, não como descrição técnica do sistema.

**Exemplo**
"Só $0,80 por dia" é percebido de forma diferente de "$24 por mês". "Seu perfil está 85% completo" motiva mais que "Seu perfil está 15% incompleto". Num app de aprendizado, "Faltam só 2 aulas para o seu certificado" gera aspiração pela proximidade. Uma funcionalidade de backup descrita como "Nunca mais perca um arquivo" convence mais que "Sincronização automática na nuvem".

**Relações**
Anchoring Bias · Loss Aversion · Scarcity · Social Proof

**Agente**
Designer Engineer (execução da copy) · Strategist (definir quais enquadramentos estão alinhados ao posicionamento do produto)

**Framework**
Double Diamond (fase Define — reenquadrar o espaço do problema) · Jobs to Be Done (enquadrar o produto em torno dos resultados do usuário, não das funcionalidades)

---

### 05 · Decoy Effect (Efeito Chamariz)

**Descrição**
Quando uma terceira opção, assimetricamente dominada, é inserida num conjunto de escolhas, ela empurra o usuário para a opção pretendida pelo designer. O experimento clássico da *The Economist*: com três planos (digital $59 / impresso $125 / digital+impresso $125), 84% escolheram o pacote combinado. Sem o chamariz "só impresso", a maioria escolheu a opção digital, mais barata. O chamariz transforma uma escolha binária difícil numa comparação óbvia.

**Melhor momento**
UI Design — ao estruturar tabelas de planos, versões de produto, opções de complementos ou qualquer interface que apresente 3 ou mais escolhas comparáveis.

**Como usar**
- Crie um plano intermediário com custo-benefício inferior ao do plano que você quer vender.
- Posicione sempre o chamariz ao lado da opção preferida.
- Use rótulos como "Mais popular" ou "Melhor custo-benefício" para sinalizar a direção.
- Garanta que o chamariz seja claramente dominado — a opção preferida precisa ser obviamente superior.

**Exemplo**
Planos de assinatura como Básico $8 / Padrão $14 / Premium $16: o Padrão funciona como chamariz que faz o Premium parecer a escolha óbvia. A pipoca do cinema (pequena $3 / média $6,50 / grande $7) segue a mesma lógica. Em planos de armazenamento ou por número de usuários, um plano intermediário com quase nenhum valor a mais que o de entrada empurra o usuário para o plano mais completo.

**Relações**
Anchoring Bias · Framing Effect · Hick's Law

**Agente**
Designer Engineer (estrutura da UI) · Strategist (arquitetura de planos e preços)

**Framework**
Double Diamond (fase de Ideação — estruturar as opções de solução) · MoSCoW (enquadrar pacotes de funcionalidades por nível de valor)

---

### 06 · Hick's Law (Lei de Hick)

**Descrição**
Formulada por William Edmund Hick e Ray Hyman nos anos 1950, esta lei estabelece que o tempo para tomar uma decisão cresce de forma logarítmica com o número de opções disponíveis. Em contextos com escolhas demais, o usuário entra em paralisia de decisão — e tende a não decidir. Esta lei fundamenta o onboarding progressivo, os menus simplificados e os fluxos de seleção guiada com filtros progressivos.

**Melhor momento**
Arquitetura de Informação, Prototipação e UI Design — em sistemas de navegação, filtros, formulários, fluxos de cadastro e qualquer interface de seleção de produtos.

**Como usar**
- Reduza as opções visíveis por nível. Revele a complexidade progressivamente, conforme a necessidade.
- No onboarding, apresente uma ação por tela.
- Agrupe itens relacionados para reduzir a contagem percebida de escolhas.
- Seleções padrão e pré-filtros reduzem o espaço ativo de decisão sem remover opções.

**Exemplo**
Um catálogo grande de e-commerce precisa de hierarquia clara (departamento > categoria > subcategoria) com filtros inteligentes já aplicados. Serviços de streaming mostram fileiras curadas ("Continuar assistindo", "Top 10", "Novidades") em vez do catálogo inteiro de uma vez. No checkout, mostrar primeiro as 3 formas de pagamento mais usadas, com as demais em "Mais opções", reduz o abandono.

**Relações**
Miller's Law · Status Quo Bias · Decoy Effect

**Agente**
Designer Engineer (execução de navegação e arquitetura de informação) · Strategist (definição da arquitetura de informação)

**Framework**
Double Diamond (fase Define — estruturar o espaço da solução) · Fluxogramas (mapear caminhos de decisão simplificados)

---

### 07 · Miller's Law (Lei de Miller)

**Descrição**
O psicólogo George Miller demonstrou em 1956 que a memória de trabalho humana retém em média 7 (±2) itens ao mesmo tempo. Além disso, o processamento da informação se degrada. Esse limite define como menus, formulários, dashboards e listas devem ser estruturados. O conceito de "chunking" — agrupar informações em blocos — deriva diretamente deste princípio.

**Melhor momento**
Arquitetura de Informação, UI Design e Prototipação — especialmente em formulários, sistemas de navegação e telas com muitos dados.

**Como usar**
- Agrupe itens em blocos de no máximo 7. Em formulários longos, use seções visuais com títulos.
- Na navegação, limite a 5–7 itens principais.
- Aplique chunking em números longos (número do cartão: 4242 4242 4242 4242, e não 4242424242424242).
- Em dashboards, mostre as 5–7 métricas mais críticas, com opção de expandir para ver detalhes.

**Exemplo**
Formulários de cadastro e de verificação de identidade funcionam melhor divididos em etapas claras (dados pessoais > endereço > verificação), com barra de progresso. Dashboards de analytics mostram no máximo 7 KPIs principais, com opção de "expandir" para detalhes. Códigos longos — números de cartão, códigos de rastreio, códigos de verificação — são exibidos em blocos.

**Relações**
Hick's Law · Zeigarnik Effect · Cognitive Load

**Agente**
Designer Engineer (design de formulários e dados) · Strategist (chunking na arquitetura de informação)

**Framework**
Double Diamond (fase de Protótipo) · Fluxogramas (quebrar etapas em nós de decisão fáceis de digerir)

---

### 08 · Zeigarnik Effect (Efeito Zeigarnik)

**Descrição**
A psicóloga Bluma Zeigarnik descobriu nos anos 1920 que tarefas incompletas permanecem mais presentes na memória do que as concluídas. O cérebro mantém uma "tensão cognitiva" em torno do que ficou inacabado, gerando um impulso natural de concluir. Esta é a base das barras de progresso, do onboarding gamificado e dos fluxos de verificação que reforçam a incompletude até a ação final.

**Melhor momento**
UI Design, Onboarding e Produto ativo — em fluxos de cadastro, verificação de conta, cursos e trilhas de aprendizado e mecânicas de engajamento recorrente.

**Como usar**
- Use barras de progresso que já começam parcialmente preenchidas.
- Mostre o que falta para concluir ("Faltam 2 etapas para ativar sua conta").
- Em cursos e trilhas de aprendizado, mostre a distância entre a aula atual e o fim do módulo.
- Em notificações push, faça referência a tarefas incompletas específicas para gerar reengajamento.
- Nunca mostre uma barra de progresso totalmente vazia — comece em no mínimo 20% para criar impulso.

**Exemplo**
Medidores de força do perfil ("Seu perfil está 70% completo") mantêm o usuário preenchendo informações. Fluxos de verificação de conta mostram "3 de 5 etapas concluídas" com uma barra visual. Lembretes de carrinho abandonado citam a tarefa inacabada específica: "Você deixou 2 itens no carrinho". Em apps de aprendizado, uma meta diária com 4 de 5 aulas concluídas gera urgência de conclusão maior do que uma meta recém-iniciada.

**Relações**
Goal Gradient Effect · Habit Loop · FOMO

**Agente**
Designer Engineer (UI de progresso e onboarding) · Strategist (estratégia de engajamento e retenção)

**Framework**
Double Diamond (fase de Ideação — identificar onde a incompletude pode ser desenhada intencionalmente) · Opportunity Solution Tree (mapear fluxos incompletos como oportunidades de produto)

---

### 09 · Goal Gradient Effect (Efeito do Gradiente de Meta)

**Descrição**
Quanto mais perto uma pessoa está de uma meta, maior a intensidade do esforço que ela aplica para alcançá-la. O experimento clássico de Clark Hull com ratos em labirintos mostrou que a velocidade aumentava à medida que se aproximavam da recompensa. Em produtos digitais, isso explica por que barras de progresso perto do fim motivam mais que no início, e por que checklists e cursos que destacam o pouco que falta aumentam a taxa de conclusão.

**Melhor momento**
UI Design e Produto ativo — em onboarding, fluxos de verificação, cursos, metas de arrecadação e desafios gamificados.

**Como usar**
- Exiba o progresso visual com ênfase crescente à medida que a meta se aproxima.
- Ofereça um pequeno incentivo extra (ex.: desbloquear uma funcionalidade, um selo de conclusão) quando o usuário estiver a menos de 20% da meta.
- Use mensagens que ficam mais específicas conforme o usuário se aproxima ("Faltam só 2 etapas!").
- Inclua microcelebrações de "quase lá" nos marcos de 80% e 90% de conclusão.

**Exemplo**
Campanhas de crowdfunding e de arrecadação recebem mais contribuições à medida que se aproximam da meta — mostrar "87% arrecadado" com uma barra de progresso em destaque torna essa proximidade visível. Em apps de aprendizado, "Faltam só 2 aulas" junto com o certificado visível acelera a conclusão do curso. Os anéis de atividade de apps de fitness, que se intensificam perto de 100%, aplicam o Goal Gradient visualmente. Num checklist de configuração, fazer da última etapa a mais simples evita que o esforço final empaque.

**Relações**
Zeigarnik Effect · Habit Loop · Loss Aversion

**Agente**
Designer Engineer (design da UI de progresso) · Strategist (arquitetura de metas e desafios)

**Framework**
Opportunity Solution Tree (identificar oportunidades de goal gradient na jornada do usuário) · Double Diamond (fase de Protótipo — testar mecânicas de goal gradient)

---

### 10 · Habit Loop (Loop do Hábito)

**Descrição**
Charles Duhigg descreve em *O Poder do Hábito* que todo comportamento habitual é composto por três elementos: **Deixa (Gatilho) → Rotina → Recompensa**. A deixa é o estímulo que inicia o comportamento; a rotina é a ação em si; a recompensa é o que reforça o circuito e cria o desejo antecipado. Com a repetição, o loop se automatiza nos gânglios da base e passa a acontecer sem esforço consciente. Produtos que constroem loops de hábito intencionais são mais difíceis de abandonar, porque mudar um hábito exige substituir a rotina — não eliminar o loop.

**Melhor momento**
Estratégia de Produto e UI Design — desde a definição inicial do produto até a construção dos fluxos de engajamento recorrente.

**Como usar**
- Identifique o gatilho natural do usuário (notificação, horário do dia, um evento recorrente).
- Reduza o esforço da rotina (um toque para concluir a ação principal, interface rápida, zero atrito no caminho crítico).
- Entregue recompensas imediatas e variáveis (conteúdo surpresa, uma dica útil, reconhecimento de conquistas).
- Desenhe loops secundários que se estendam para a próxima sessão.

**Exemplo**
Um app de idiomas: Gatilho = lembrete no horário escolhido pelo usuário → Rotina = uma aula de 5 minutos, a um toque da notificação → Recompensa = contador de sequência (streak), XP e uma breve celebração. Um app de fitness: Gatilho = notificação pela manhã → Rotina = registrar o treino → Recompensa = o anel de progresso se fecha. O caso Pepsodent, de Duhigg, mostra que a recompensa sensorial imediata é crítica — o microfeedback visual, sonoro e tátil logo depois da ação principal é a "sensação de formigamento" do produto.

**Relações**
Goal Gradient Effect · Zeigarnik Effect · FOMO · Variable Ratio Reinforcement

**Agente**
Strategist (arquitetura do loop de hábito e estratégia de engajamento) · Designer Engineer (design de notificações e feedback de recompensa)

**Framework**
Jobs to Be Done (mapear o job funcional, emocional e social que o loop de hábito cumpre) · Service Blueprint (mapear o loop completo nos pontos de contato de frontstage e backstage)

---

### 11 · Scarcity Bias & FOMO (Viés da Escassez e FOMO)

**Descrição**
A escassez aumenta o valor percebido de uma oportunidade simplesmente por ela ser limitada. O FOMO (Fear of Missing Out, o medo de ficar de fora) é a dimensão emocional da escassez — o medo de ser excluído de algo que outras pessoas estão vivendo. Juntos, criam uma urgência poderosa. A escassez pode ser de quantidade ("só 3 disponíveis"), de tempo ("oferta termina em 2h") ou de acesso ("exclusivo para beta testers"). A autenticidade é crítica: escassez fabricada destrói a confiança.

**Melhor momento**
UI Design e Produto ativo — em promoções, eventos ao vivo, lançamentos de produto e fluxos de conversão em que o tempo ou a disponibilidade são de fato limitados.

**Como usar**
- Use contadores regressivos visuais em promoções com prazo real.
- Mostre a disponibilidade restante ("só restam 12 vagas para este workshop").
- Crie ofertas exclusivas por segmento (usuários ativos, beta testers, clientes antigos) que reforcem o acesso limitado.
- Em contextos ao vivo, deixe visível a restrição natural de tempo do próprio evento.
- Nunca fabrique escassez — aplique apenas onde a limitação for real.

**Exemplo**
Produtos de viagem e venda de ingressos mostram "Só restam 3 lugares neste preço" quando o estoque é de fato limitado. Eventos ao vivo e webinars têm uma restrição natural de tempo: "Inscrições encerram em 2 horas". Lançamentos de edição limitada exibem o estoque real restante. Ofertas de acesso antecipado ou exclusivas para assinantes criam exclusividade legítima. Em todos os casos, o limite exibido precisa ser o limite que existe.

**Relações**
Loss Aversion · Social Proof · Framing Effect · Habit Loop

**Agente**
Designer Engineer (UI de contagem regressiva e de disponibilidade) · Strategist (arquitetura de promoções e segmentação)

**Framework**
Teste A/B (testar formatos de mensagem de escassez e seu impacto na conversão) · Service Blueprint (mapear onde existem momentos de escassez autêntica ao longo da jornada do usuário)

---

### 12 · Peak-End Rule (Regra do Pico-Fim)

**Descrição**
Kahneman demonstrou que as pessoas não avaliam uma experiência pela média de todos os seus momentos, mas por dois pontos específicos: o pico emocional (o momento mais intenso, positivo ou negativo) e o fim (como ela terminou). Uma experiência pode ter vários momentos medianos — mas, se o pico e o fim forem positivos, ela será lembrada positivamente. Isso tem implicações diretas no design de onboarding, offboarding e momentos de celebração.

**Melhor momento**
UI Design e Testes — ao revisar fluxos completos, identificar momentos de alta carga emocional e desenhar o encerramento das sessões.

**Como usar**
- Desenhe deliberadamente os momentos de maior intensidade emocional (primeira compra, primeira meta concluída, primeiro marco alcançado).
- Garanta que o fim da sessão seja positivo, independentemente do resultado (mensagem de incentivo, próxima meta disponível, enquadramento de "progresso salvo").
- Use animação e feedback visual nos momentos de celebração.
- Em pesquisa, avalie as experiências pelos momentos de pico e de fim — não pela média.

**Exemplo**
No e-commerce, o pico é a confirmação da compra — uma tela de sucesso clara e acolhedora, com resumo do pedido e previsão de entrega, importa mais do que ganhar um segundo no checkout. Um atendimento de suporte deve terminar com um resumo da solução e um encerramento cordial. No onboarding de um SaaS, o "momento aha" (primeiro relatório gerado, primeiro arquivo compartilhado com o time) é o pico a ser acelerado e celebrado. Mesmo quando a sessão termina mal (pagamento recusado, upload com falha), o fim deve oferecer um caminho claro para seguir.

**Relações**
Zeigarnik Effect · Habit Loop · Social Proof

**Agente**
Designer Engineer (UI de celebração e de fim de sessão) · Researcher (identificar momentos de pico e de fim por meio de testes de usabilidade e análise de sessões)

**Framework**
Pesquisa Qualitativa (revelar quais momentos os usuários descrevem como mais marcantes) · Teste de Usabilidade (observar os picos emocionais e como os usuários descrevem o fim de uma sessão)

---

### 13 · Von Restorff Effect (Efeito Von Restorff)

**Descrição**
Também chamado de Efeito de Isolamento: um item que se destaca visualmente do seu contexto é significativamente mais memorável e tem mais chance de ser escolhido. Identificado pela psicóloga Hedwig von Restorff em 1933, este princípio é a base do design de CTAs em destaque, selos de "Mais popular" e qualquer elemento de interface que exija atenção prioritária. Usado com moderação, cria uma hierarquia clara; em excesso, anula a si mesmo.

**Melhor momento**
UI Design — ao desenhar hierarquia visual, CTAs, selos e elementos em destaque em qualquer interface com vários itens competindo por atenção.

**Como usar**
- Use cor, tamanho, peso ou forma para diferenciar o elemento prioritário do seu contexto.
- Em tabelas de preço, destaque o plano recomendado com uma cor de fundo diferente.
- Aplique com moderação — se tudo se destaca, nada se destaca. Um elemento Von Restorff por contexto.
- Combine com a Ancoragem: o elemento visualmente isolado vira a âncora cognitiva.

**Exemplo**
Tabelas de preço destacam o plano recomendado com um fundo diferente e o selo "Mais popular". Preços promocionais se destacam dos preços normais pela cor e pelo tamanho. Numa lista de notificações, os itens não lidos ficam visualmente isolados. Na navegação, um único selo de "Novo" ou indicador "ao vivo" deve ser o elemento mais distinto — nunca vários ao mesmo tempo.

**Relações**
Framing Effect · Scarcity · Anchoring Bias

**Agente**
Designer Engineer (hierarquia visual e design de selos)

**Framework**
Double Diamond (fase de Protótipo — testar se o elemento isolado é corretamente identificado como prioridade)

---

### 14 · Serial Position Effect (Efeito da Posição Serial)

**Descrição**
Hermann Ebbinghaus descreveu que as pessoas lembram melhor dos itens do início (efeito de primazia) e do fim (efeito de recência) de uma lista, esquecendo os do meio. Em listas de navegação, sequências de onboarding ou menus, a posição dos itens não é neutra — as extremidades capturam mais atenção e memória que o centro.

**Melhor momento**
Arquitetura de Informação e UI Design — ao definir a ordem dos itens em sistemas de navegação, listas de produtos, sequências de onboarding e menus.

**Como usar**
- Coloque os itens mais importantes no início e no fim de listas e da navegação.
- Evite enterrar ações críticas no meio de fluxos longos.
- No onboarding, comece com uma vitória rápida (primazia) e termine com a ação de maior valor (recência).
- Em navegações com 5 ou mais itens, revise o que ocupa as posições 2 a 4 — são as posições mais fracas.

**Exemplo**
Na navegação principal, o destino mais importante ocupa a primeira posição, e a última costuma abrigar um destino de alto valor (carrinho, perfil, notificações). Em listagens de produtos e resultados de busca, as posições 1 a 3 e os últimos itens visíveis recebem mais cliques — a curadoria dessas posições tem impacto direto na receita. No onboarding, comece com uma vitória rápida e termine com a ação de maior valor (convidar o time, conectar a primeira integração), em vez de escondê-la no meio.

**Relações**
Miller's Law · Hick's Law · Von Restorff Effect

**Agente**
Designer Engineer (design de navegação e listas) · Strategist (ordenação na arquitetura de informação)

**Framework**
Double Diamond (fase Define — estruturar as prioridades de navegação) · Fluxogramas (mapear quais etapas ancoram o início e o fim de cada fluxo)

---

### 15 · Jakob's Law (Lei de Jakob)

**Descrição**
Formulada por Jakob Nielsen: os usuários passam a maior parte do tempo em outros produtos digitais e, por isso, esperam que o seu produto funcione da mesma forma que eles. Quando um produto se afasta muito dos padrões estabelecidos, a carga cognitiva aumenta e a frustração aparece. A familiaridade reduz o esforço de aprendizado e acelera a adoção. A inovação deve estar na experiência — não nas convenções.

**Melhor momento**
Discovery e Prototipação — ao definir padrões de interação, nomenclatura e localização dos elementos na interface.

**Como usar**
- Siga as convenções de mercado para elementos críticos (carrinho no canto superior direito, logo no canto superior esquerdo, CTA principal na cor de destaque).
- Inove na experiência — não na convenção. Reserve a originalidade para momentos reais de diferenciação.
- Faça benchmarking dos concorrentes antes de desenhar qualquer padrão de navegação ou de interação central.
- Ao se afastar de uma convenção, valide com teste de usabilidade antes de lançar.

**Exemplo**
Usuários de e-commerce esperam o carrinho no canto superior direito, a busca no topo e um checkout no padrão dos grandes marketplaces que já usam. Um app de banco que tira a ação de transferência do lugar onde outros apps de banco a colocam gera erros e chamados de suporte. A inovação deve estar no valor do produto — velocidade, preço, conteúdo, atendimento — e não nas convenções que o usuário já internalizou. O checkout precisa se comportar exatamente como o usuário espera; qualquer surpresa ali custa conversão.

**Relações**
Hick's Law · Status Quo Bias · Cognitive Load

**Agente**
Researcher (benchmarking de padrões existentes) · Designer Engineer (aderência às convenções nos protótipos)

**Framework**
Benchmarking (auditar os padrões de interação dos concorrentes antes de se afastar deles) · Teste de Usabilidade (validar se algum desvio de convenção gera confusão)

---

### 16 · Confirmation Bias (Viés de Confirmação)

**Descrição**
A tendência sistemática de buscar, interpretar e lembrar informações que confirmam crenças prévias, ignorando as evidências contrárias. No processo de design, o viés de confirmação é uma das maiores ameaças à qualidade da pesquisa — o designer tende a interpretar os dados de teste como validação das hipóteses que já tinha. Para o usuário, ele reforça padrões de comportamento e escolhas passadas, gerando consistência com as decisões já tomadas.

**Melhor momento**
Discovery e Pesquisa (mitigar no processo de design). Produto ativo (usar para reforçar a escolha do usuário depois da conversão).

**Como usar**
- No processo de design: use red teams para desafiar hipóteses. Documente as suposições antes de pesquisar.
- Depois da conversão, reforce a decisão do usuário com dados que confirmem a qualidade da escolha ("Você escolheu um dos planos mais bem avaliados da categoria").
- Desenhe telas pós-decisão que validem a ação tomada, em vez de deixar o usuário na incerteza.

**Exemplo**
Depois de uma compra ou assinatura, mensagens como "Ótima escolha — este é o nosso plano mais bem avaliado" reduzem a dissonância pós-decisão (o arrependimento do comprador). Em produtos SaaS, um resumo periódico do que o usuário conquistou (horas economizadas, relatórios gerados, projetos entregues) confirma que continuar valeu a pena, reduzindo o churn. Dentro do time de design, ter alguém que desafie as conclusões da pesquisa antes da apresentação evita que o time enxergue apenas o que esperava ver.

**Relações**
Social Proof · Availability Heuristic · Peak-End Rule

**Agente**
Researcher (mitigar durante o processo de pesquisa) · Designer Engineer (usar na UI pós-conversão)

**Framework**
Pesquisa Qualitativa (técnicas de entrevista estruturada que neutralizam o viés de confirmação na coleta de dados) · Teste A/B (usar dados quantitativos para se sobrepor ao viés de confirmação qualitativo nas decisões de design)

---

### 17 · Variable Ratio Reinforcement — VRR (Reforço em Razão Variável)

**Descrição**
Formulado pelo cientista comportamental B.F. Skinner, este princípio descreve o esquema de recompensa mais poderoso para sustentar um comportamento: recompensar em intervalos imprevisíveis. Diferente das recompensas fixas e previsíveis (que perdem impacto com o tempo), as recompensas variáveis mantêm o engajamento elevado porque o cérebro antecipa uma recompensa a cada interação. Feeds de redes sociais e caixas de e-mail funcionam por essa lógica — cada atualização pode trazer algo novo. Aplicações éticas incluem notificações surpresa, vantagens inesperadas e conteúdo variado.

**Melhor momento**
Estratégia de Produto e UI Design — no design de sistemas de recompensa, notificações push e loops de engajamento recorrente.

**Como usar**
- Introduza recompensas surpresa em momentos inesperados (2ª compra da semana, primeiro login da semana, 10º pedido do mês).
- Varie o tipo de recompensa — às vezes frete grátis, às vezes acesso antecipado, às vezes uma recomendação personalizada.
- Evite a previsibilidade total em sistemas de recompensa — a surpresa faz parte do valor.
- Nunca aplique VRR para manipular usuários vulneráveis — limite-se a reforços genuinamente positivos.

**Exemplo**
Um app de e-commerce pode oferecer uma "surpresa" em momentos imprevisíveis — frete grátis num pedido, acesso antecipado a uma promoção. Apps de aprendizado variam a recompensa (selos, XP em dobro, proteção da sequência) para manter a prática envolvente. Feeds sociais e caixas de entrada funcionam por VRR por natureza — cada atualização pode trazer algo novo —, e é exatamente por isso que este mecanismo exige o maior cuidado ético, especialmente com usuários que mostram sinais de uso compulsivo.

**Relações**
Habit Loop · Goal Gradient Effect · Scarcity

**Agente**
Strategist (arquitetura do sistema de recompensas) · Designer Engineer (timing das notificações e design da UI de recompensa)

**Framework**
Opportunity Solution Tree (mapear momentos de recompensa baseados em VRR como oportunidades de produto) · Teste A/B (testar frequência e tipo de recompensa para otimizar o engajamento sem gerar dependência)

---

### 18 · Fitts's Law (Lei de Fitts)

**Descrição**
Paul Fitts demonstrou em 1954 que o tempo para alcançar um alvo é função da distância até ele e do seu tamanho. Quanto maior e mais próximo o elemento interativo, mais rápido e preciso é o clique ou o toque. Esta lei tem implicações diretas no design de interfaces mobile, em que áreas de toque inadequadas são causa frequente de erros, frustração e abandono de tarefas.

**Melhor momento**
Prototipação e UI Design — ao definir tamanho, espaçamento e posicionamento dos elementos interativos, especialmente em interfaces mobile.

**Como usar**
- Os CTAs principais devem ser grandes (mínimo de 44×44pt no mobile).
- Ações frequentes devem ficar em zonas de alcance confortável (terço inferior da tela no mobile, ao alcance do polegar).
- Aumente o tamanho dos alvos críticos proporcionalmente à sua importância.
- Separe elementos destrutivos (excluir, cancelar) dos construtivos para evitar acionamentos acidentais.

**Exemplo**
O botão "Finalizar pedido" ou "Pagar" no checkout é o alvo mais crítico de um produto de e-commerce — grande, bem posicionado e visualmente distinto. No mobile, os CTAs principais devem ficar no terço inferior da tela, ao alcance do polegar. Manter "Excluir" longe de "Salvar" reduz erros acidentais. Em apps usados em movimento (mobilidade, delivery, navegação), os botões críticos precisam ser grandes o bastante para serem tocados com precisão enquanto a pessoa caminha ou está num veículo.

**Relações**
Miller's Law · Jakob's Law · Cognitive Load

**Agente**
Designer Engineer (dimensionamento de UI mobile e design de áreas de toque)

**Framework**
Double Diamond (fase de Protótipo — validar a precisão das áreas de toque em testes de usabilidade) · Teste de Usabilidade (observar a precisão do toque em alvos críticos)

---

## Relações entre vieses

A tabela abaixo mapeia como os vieses se reforçam mutuamente. Entender essas conexões permite estratégias de engajamento em camadas, em que uma única decisão de design ativa vários mecanismos cognitivos ao mesmo tempo.

| Viés | Ativa / É reforçado por |
|---|---|
| **Anchoring Bias** | Decoy Effect (reforça o ponto de referência) · Framing Effect (define o enquadramento da âncora) · Loss Aversion (uma âncora alta amplia o medo de perder o desconto) |
| **Loss Aversion** | Scarcity (amplia o medo de perder a oportunidade) · FOMO (a versão emocional da perda) · Framing Effect (enquadramentos de perda vs. ganho) |
| **Habit Loop** | Goal Gradient (acelera a aproximação da recompensa) · Zeigarnik Effect (mantém a tensão entre sessões) · VRR (mantém o loop imprevisível e envolvente) |
| **Social Proof** | Framing Effect (a forma de apresentar os sinais sociais muda o impacto) · FOMO (outros estão fazendo = estou perdendo) · Confirmation Bias (reforça uma decisão já tomada) |
| **Hick's Law** | Miller's Law (limite de opções + limite de memória são complementares) · Decoy Effect (3 opções + chamariz é a implementação clássica) |
| **Zeigarnik Effect** | Goal Gradient (a incompletude acelera o esforço final) · Habit Loop (a tensão do inacabado é o gatilho do próximo loop) |
| **Peak-End Rule** | Habit Loop (o pico é a recompensa; o fim é o fechamento do loop) · Social Proof (picos compartilhados geram prova social) |
| **Von Restorff** | Anchoring Bias (o elemento isolado vira a âncora) · Scarcity (o isolamento visual reforça a raridade percebida) |
| **VRR** | Habit Loop (a variabilidade torna o loop imprevisível e mais forte) · Goal Gradient (recompensas variáveis perto da meta aceleram o esforço) |
| **Framing Effect** | Todos os vieses — o enquadramento é a metacamada pela qual todos os outros vieses são entregues |

---

## Mapa de Responsabilidade Agente × Viés

| Agente | Vieses principais | Papel |
|---|---|---|
| **Researcher** | Confirmation Bias · Jakob's Law · Peak-End Rule · Framing Effect | Identifica onde os vieses afetam o comportamento do usuário; mitiga-os no processo de pesquisa; traz descobertas que orientam como os vieses devem ser aplicados no design |
| **Strategist** | Habit Loop · Goal Gradient · VRR · Scarcity · Loss Aversion · Decoy Effect | Define a arquitetura de engajamento, o sistema de recompensas e a estratégia de preços em que esses vieses operam no nível sistêmico |
| **Designer Engineer** | Anchoring · Von Restorff · Zeigarnik · Fitts's Law · Hick's Law · Miller's Law · Serial Position · Framing (copy) | Executa as decisões fundamentadas em vieses no nível da interface — hierarquia visual, copy, áreas de toque, navegação e padrões de feedback |

---

## Nota Ética sobre Design Comportamental

### Persuasão vs. manipulação

Existe uma linha clara entre o **design persuasivo** — que usa vieses cognitivos para ajudar o usuário a tomar decisões alinhadas aos seus próprios objetivos genuínos — e os **dark patterns** — que exploram vieses para manipular o usuário contra os seus próprios interesses.

O design persuasivo constrói confiança e retenção no longo prazo. Os dark patterns geram conversão no curto prazo e destroem a confiança no longo prazo. Em produtos que lidam com dinheiro, saúde ou dados pessoais — ou que alcançam usuários vulneráveis — a responsabilidade ética do designer é ainda maior.

**O teste prático:** pergunte se o viés está facilitando o que o usuário genuinamente quer fazer ou se está induzindo o usuário a fazer o que você quer que ele faça. Se for a segunda opção, é um dark pattern.

---

### Dark patterns a evitar

A seguir estão implementações específicas de dark patterns a partir dos vieses documentados neste arquivo. Elas nunca devem ser usadas em produtos desenhados com esta skill.

| Dark pattern | Viés explorado | Por que é proibido |
|---|---|---|
| **Escassez fabricada** ("Só restam 2!" quando o estoque é ilimitado) | Scarcity · Loss Aversion | Destrói a confiança quando descoberto; viola a expectativa de honestidade do usuário |
| **Contadores regressivos infinitos** (timers que reiniciam quando terminam) | Scarcity · FOMO | Fabrica uma urgência que não é real; corrói a credibilidade da marca |
| **Custos ocultos de cancelamento** (mostrar o enquadramento de perda só depois que o usuário tenta cancelar, e não antes) | Loss Aversion · Framing Effect | Prende o usuário por assimetria de informação, e não por valor genuíno |
| **Roach motel** (fácil de assinar, quase impossível de cancelar) | Habit Loop · Status Quo Bias | Retém o usuário pelo atrito, não pelo valor; gera risco regulatório |
| **Confirmshaming** ("Não, obrigado, não quero economizar") | Framing Effect · Loss Aversion | Manipula emocionalmente a opção secundária para forçar a ação principal |
| **Perguntas capciosas** (dupla negação ou linguagem confusa em checkboxes de opt-out) | Cognitive Load · Framing Effect | Explora a carga cognitiva para obter um consentimento que o usuário não daria de outra forma |
| **Prova social falsa** (reviews falsos, contagens de usuários inventadas, depoimentos inexistentes) | Social Proof | Engano direto; ilegal na maioria dos mercados pelas leis de defesa do consumidor |
| **Quase-acertos artificiais** (feedback desenhado para fazer o usuário sentir que "quase" conseguiu uma recompensa, prêmio ou meta com mais frequência do que a realidade, para que continue tentando) | VRR · Loss Aversion | Manipula psicologicamente usuários vulneráveis; sujeito à regulação de defesa do consumidor |
| **Desvio de atenção** (a atenção é levada para um elemento de distração enquanto uma ação prejudicial é disparada em outro lugar) | Von Restorff · Cognitive Load | Engano deliberado por manipulação visual |
| **Anúncios disfarçados** (conteúdo formatado de forma idêntica ao conteúdo editorial, sem identificação) | Social Proof · Confirmation Bias | Violação regulatória; destrói a confiança do usuário |
| **Continuidade forçada** (cobrar o usuário depois de um teste grátis sem um aviso claro) | Loss Aversion · Status Quo Bias | Dano financeiro por meio de atrito deliberado no caminho do cancelamento |

---

### Designer Checklist antes de publicar qualquer feature com viés aplicado

Antes que qualquer feature que aplique os vieses documentados aqui vá para produção, o Designer Engineer precisa confirmar:

- [ ] O sinal de escassez é real — não é fabricado nem exagerado.
- [ ] A mensagem de urgência reflete um prazo ou uma restrição real.
- [ ] Os dados de prova social são precisos e verificáveis.
- [ ] O enquadramento de perda é usado para ajudar o usuário a agir sobre um valor genuíno — não para gerar ansiedade.
- [ ] O caminho de cancelamento ou opt-out é tão fácil de encontrar e concluir quanto o de cadastro.
- [ ] O sistema de recompensa variável não tem como alvo usuários que mostram sinais de uso compulsivo ou outra vulnerabilidade.
- [ ] A copy foi revisada de acordo com o tom de voz de `references/patterns.md`.
- [ ] A feature foi avaliada pela heurística de controle e liberdade do usuário (`references/heuristics.md`).
