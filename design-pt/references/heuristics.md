# References: Heurísticas de Nielsen

> **Instrução para agentes:** Consulte este arquivo sempre que a demanda envolver avaliação de interfaces, identificação de problemas de usabilidade, revisão de fluxos ou construção de telas. As heurísticas são o critério de qualidade de UX desta skill — toda decisão de interface deve ser justificada por ao menos uma delas.

---

## O que são as Heurísticas de Nielsen

As 10 Heurísticas de Usabilidade de Jakob Nielsen são princípios gerais de design de interface, estabelecidos em 1994 e amplamente adotados como padrão da indústria. Não são regras rígidas, mas diretrizes para identificar problemas de usabilidade e guiar decisões de design.

**Quando aplicar:**
- Avaliação heurística de interfaces existentes
- Revisão de protótipos antes de testes com usuários
- Justificativa de decisões de design para stakeholders
- Identificação de problemas sem necessidade de pesquisa com usuários

---

## As 10 Heurísticas

---

### H1 — Visibilidade do status do sistema

**Princípio**
O sistema deve sempre manter o usuário informado sobre o que está acontecendo, por meio de feedback adequado em tempo razoável.

**Regra**
O usuário nunca deve se perguntar: *"O sistema recebeu minha ação? O que está acontecendo agora?"*

**Como aplicar**
- Mostre estados de carregamento (spinners, skeletons, barras de progresso)
- Confirme ações concluídas (mensagens de sucesso, mudanças visuais de estado)
- Indique etapas em processos longos (ex: "Passo 2 de 4")
- Use cores e ícones para comunicar estados (ativo, inativo, erro, sucesso)

**Problemas comuns quando violada**
- Botões que não dão feedback ao ser clicados
- Formulários que não confirmam o envio
- Upload de arquivos sem indicador de progresso
- Navegação sem indicação de página atual

---

### H2 — Correspondência entre o sistema e o mundo real

**Princípio**
O sistema deve falar a linguagem do usuário — palavras, frases e conceitos familiares ao usuário, não jargões técnicos. Seguir convenções do mundo real, fazendo informações aparecerem em ordem natural e lógica.

**Regra**
O usuário nunca deve precisar aprender uma nova linguagem para usar o produto.

**Como aplicar**
- Use terminologia do domínio do usuário, não da tecnologia
- Utilize metáforas do mundo real quando apropriado (lixeira, pasta, carrinho)
- Organize informações na ordem em que o usuário as processa mentalmente
- Evite abreviações, siglas ou termos técnicos sem explicação

**Problemas comuns quando violada**
- Mensagens de erro técnicas ("Error 404", "Null pointer exception")
- Labels que fazem sentido para o dev mas não para o usuário
- Fluxos organizados pela lógica do sistema, não do usuário

---

### H3 — Controle e liberdade do usuário

**Princípio**
Usuários frequentemente escolhem funções por engano e precisam de uma "saída de emergência" clara para deixar o estado indesejado sem passar por um processo longo.

**Regra**
O usuário deve sempre poder desfazer, cancelar ou voltar facilmente.

**Como aplicar**
- Ofereça opções de desfazer e refazer
- Confirme ações destrutivas (exclusão, cancelamento) antes de executar
- Permita cancelar processos em andamento
- Garanta que o botão "voltar" funcione de forma previsível

**Problemas comuns quando violada**
- Exclusão sem confirmação e sem possibilidade de recuperação
- Fluxos sem botão de cancelar
- Modais que prendem o usuário sem saída clara
- Formulários longos que perdem dados ao tentar sair

---

### H4 — Consistência e padrões

**Princípio**
Usuários não deveriam se perguntar se palavras, situações ou ações diferentes significam a mesma coisa. Siga as convenções da plataforma.

**Regra**
O mesmo elemento deve se comportar da mesma forma em todo o sistema.

**Como aplicar**
- Use o mesmo componente para a mesma função em todas as telas
- Mantenha terminologia consistente (não misture "salvar" e "confirmar" para a mesma ação)
- Siga as convenções da plataforma (iOS, Android, Web)
- Documente padrões no design system e siga-os rigorosamente

**Problemas comuns quando violada**
- Botões primários com cores diferentes em telas distintas
- Ações com nomes diferentes fazendo a mesma coisa
- Componentes que se comportam de formas inesperadas em contextos diferentes

---

### H5 — Prevenção de erros

**Princípio**
Melhor do que boas mensagens de erro é um design cuidadoso que previne problemas antes que ocorram.

**Regra**
O sistema deve ser projetado para tornar o erro difícil ou impossível de acontecer.

**Como aplicar**
- Desabilite ações impossíveis ou inadequadas no contexto atual
- Use validação em tempo real em formulários (não só ao submeter)
- Confirme ações irreversíveis antes de executar
- Limite opções de entrada quando possível (selects, toggles, calendários)
- Use defaults inteligentes que reduzem chance de erro

**Problemas comuns quando violada**
- Formulários que só validam ao submeter
- Campos de data em formato livre sem máscara
- Ações destrutivas facilmente acessíveis e sem confirmação

---

### H6 — Reconhecimento em vez de memorização

**Princípio**
Minimize a carga de memória do usuário tornando objetos, ações e opções visíveis. O usuário não deve precisar lembrar informações de uma parte da interação para usar em outra.

**Regra**
O usuário nunca deve precisar memorizar informações para completar uma tarefa.

**Como aplicar**
- Mostre opções disponíveis em vez de exigir que o usuário as lembre
- Mantenha contexto visível durante tarefas longas (ex: resumo do pedido durante checkout)
- Use histórico, sugestões e autocompletar
- Mostre exemplos do formato esperado em campos de entrada

**Problemas comuns quando violada**
- Campos sem placeholder ou exemplo de formato
- Processos multi-etapa sem resumo do que foi preenchido
- Menus sem indicação de onde o usuário está

---

### H7 — Flexibilidade e eficiência de uso

**Princípio**
Aceleradores — invisíveis para usuários novatos — podem aumentar a velocidade de interação para usuários experientes. Permita que usuários adaptem ações frequentes.

**Regra**
O sistema deve servir bem tanto ao usuário iniciante quanto ao avançado.

**Como aplicar**
- Ofereça atalhos de teclado para ações frequentes
- Permita personalização de fluxos para usuários avançados
- Crie shortcuts para tarefas repetitivas
- Não force usuários experientes a seguir fluxos guiados desnecessariamente

**Problemas comuns quando violada**
- Sistemas que forçam wizards passo-a-passo para usuários experientes
- Ausência de atalhos em ferramentas de uso intenso
- Impossibilidade de pular etapas já conhecidas

---

### H8 — Design estético e minimalista

**Princípio**
Diálogos não devem conter informações irrelevantes ou raramente necessárias. Cada unidade extra de informação compete com as unidades relevantes e diminui sua visibilidade relativa.

**Regra**
Cada elemento na tela deve ter um propósito. Se não tem, remove.

**Como aplicar**
- Remova informações, campos e elementos que não contribuem para a tarefa atual
- Priorize hierarquia visual clara: o que é mais importante deve ser mais visível
- Evite decoração sem função
- Use espaço em branco intencionalmente para dar respiração ao conteúdo

**Problemas comuns quando violada**
- Dashboards com dezenas de métricas sem hierarquia
- Formulários com campos opcionais desnecessários
- Telas poluídas que dificultam identificar a ação principal

---

### H9 — Ajuda ao usuário para reconhecer, diagnosticar e recuperar erros

**Princípio**
Mensagens de erro devem ser expressas em linguagem clara (sem códigos), indicar precisamente o problema e sugerir uma solução construtivamente.

**Regra**
Quando um erro ocorre, o usuário deve entender o que aconteceu e saber o que fazer.

**Como aplicar**
- Escreva mensagens de erro em linguagem humana, não técnica
- Seja específico: "Email inválido" é melhor que "Erro no campo"
- Sempre ofereça um próximo passo ("Tente novamente", "Entre em contato")
- Use cor e ícone para reforçar visualmente o estado de erro
- Posicione a mensagem próxima ao elemento com problema

**Problemas comuns quando violada**
- "Ocorreu um erro inesperado. Código: 500"
- Mensagens genéricas que não indicam qual campo tem problema
- Erros sem orientação de como corrigir

---

### H10 — Ajuda e documentação

**Princípio**
Mesmo que seja melhor que o sistema possa ser usado sem documentação, pode ser necessário fornecer ajuda. Tal informação deve ser fácil de encontrar, focada na tarefa do usuário, listar passos concretos e não ser muito extensa.

**Regra**
Quando o usuário precisar de ajuda, ela deve estar ao alcance, ser contextual e ser acionável.

**Como aplicar**
- Ofereça tooltips e hints contextuais nos momentos de dúvida
- Crie uma central de ajuda pesquisável
- Use onboarding progressivo em vez de tutoriais longos iniciais
- Documente casos de uso reais, não funcionalidades isoladas

**Problemas comuns quando violada**
- Ajuda genérica que não resolve o problema específico do usuário
- Documentação desatualizada ou difícil de encontrar
- Ausência de contexto: ajuda só disponível fora do fluxo onde o problema ocorre

---

## Como conduzir uma Avaliação Heurística

**Processo recomendado**

1. **Defina o escopo** — quais telas ou fluxos serão avaliados?
2. **Execute a avaliação** — percorra o fluxo como usuário, identificando violações
3. **Documente cada problema** com:
   - Heurística violada (H1 a H10)
   - Descrição do problema
   - Severidade (1 = cosmético, 2 = menor, 3 = maior, 4 = catastrófico)
   - Sugestão de correção
4. **Priorize por severidade** para o plano de correção

**Escala de severidade (Nielsen)**

| Nível | Descrição |
|---|---|
| **0** | Não é um problema de usabilidade |
| **1** | Cosmético — corrigir apenas se houver tempo extra |
| **2** | Menor — baixa prioridade de correção |
| **3** | Maior — importante corrigir, afeta a experiência |
| **4** | Catastrófico — deve ser corrigido antes do lançamento |
