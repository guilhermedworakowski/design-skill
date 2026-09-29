# References: Patterns

> **Instrução para agentes:** Consulte este arquivo antes de qualquer entrega visual ou de fluxo para garantir aderência aos padrões definidos do produto. Quando preenchidos, os tokens aqui documentados são a fonte de verdade — não os substitua por valores arbitrários.
>
> **Se uma seção ainda estiver com placeholders (`[...]`), não invente valores.** Use nomes de tokens semânticos genéricos (ex: `color-action-primary`, `spacing-md`), aplique as regras de `references/execution.md` e sinalize na entrega quais padrões do produto precisam ser definidos.

> **Instrução para quem vai usar a skill:** Este arquivo é um modelo. Preencha cada seção com os padrões do seu produto ou design system, substituindo tudo que estiver entre `[colchetes]`. Adicione ou remova linhas das tabelas conforme necessário. Seções que não se aplicam podem ser apagadas.

---

## Índice

1. [Paleta de Cores](#1-paleta-de-cores)
2. [Tipografia](#2-tipografia)
3. [Border Radius](#3-border-radius)
4. [Espaçamento](#4-espaçamento)
5. [Grid](#5-grid)
6. [Iconografia](#6-iconografia)
7. [Tom de Voz](#7-tom-de-voz)

---

## 1. Paleta de Cores

Documente cada cor com o nome do token, o valor e a função. Toda cor precisa ter um uso definido.

### Primária
Cor principal de ação — botões primários, links, CTAs. Inclua as variações (mais claras e mais escuras) usadas para estados.

| Token | Hex | Uso |
|---|---|---|
| `[nome-do-token]` | `[#HEX]` | [Onde e quando usar] |

### Secundária
Cor de suporte — elementos de destaque que não são a ação principal.

| Token | Hex | Uso |
|---|---|---|
| `[nome-do-token]` | `[#HEX]` | [Onde e quando usar] |

### Feedback
Cores de estado: sucesso, erro, aviso e informação.

| Token | Hex | Uso |
|---|---|---|
| `[nome-do-token]` | `[#HEX]` | [Sucesso / erro / aviso / informação] |

> **Regra obrigatória:** Nunca use cor como único indicador de estado — sempre combine com ícone ou texto. Garantia de acessibilidade para usuários com daltonismo.

### Neutras
Fundos, superfícies, bordas, divisores e textos, do mais claro ao mais escuro.

| Token | Hex | Uso |
|---|---|---|
| `[nome-do-token]` | `[#HEX]` | [Fundo, borda, texto de apoio, texto primário, etc.] |

---

## 2. Tipografia

**Família:** [Nome da fonte]
**Fallback:** `[pilha de fallback, ex: system-ui, sans-serif]`

Para cada grupo, documente os estilos com peso, tamanho, line-height e uso.

### Headline
Títulos de página, seção, subtítulos e rótulos acima de títulos.

| Estilo | Peso | Tamanho | Line Height | Uso |
|---|---|---|---|---|
| `[nome-do-estilo]` | [Peso] | [px] | [%] | [Onde usar] |

### Paragraph
Corpo de texto principal e textos de suporte. Crie um grupo por tamanho de corpo, se houver mais de um.

| Estilo | Peso | Tamanho | Line Height | Uso |
|---|---|---|---|---|
| `[nome-do-estilo]` | [Peso] | [px] | [%] | [Onde usar] |

### Caption
Textos auxiliares, helper texts, tooltips, badges, labels de campo.

| Estilo | Peso | Tamanho | Line Height | Uso |
|---|---|---|---|---|
| `[nome-do-estilo]` | [Peso] | [px] | [%] | [Onde usar] |

> **Regra obrigatória:** Defina o tamanho mínimo de fonte da interface e o tamanho mínimo para corpo de texto. Contraste mínimo de 4.5:1 entre texto e fundo (WCAG AA).

---

## 3. Border Radius

| Token | Valor | Uso |
|---|---|---|
| `[nome-do-token]` | [px] | [Componentes que usam este raio] |

---

## 4. Espaçamento

Escala baseada em múltiplos de [4px / 8px]. Todos os espaçamentos internos (padding) e externos (margin/gap) devem usar exclusivamente os tokens abaixo — nunca valores arbitrários.

| Token | Valor | Uso típico |
|---|---|---|
| `[nome-do-token]` | [px] | [Onde aplicar] |

---

## 5. Grid

Documente o grid de cada breakpoint usado pelo produto.

### [Breakpoint, ex: Mobile]

| Propriedade | Valor |
|---|---|
| Width | [px] |
| Colunas | [número] |
| Margin | [px] |
| Gap / Gutter | [px] |

### [Breakpoint, ex: Desktop]

| Propriedade | Valor |
|---|---|
| Width | [px] |
| Colunas | [número] |
| Margin | [px] |
| Gap / Gutter | [px] |

> **Regra obrigatória:** Defina a estratégia de construção (ex: mobile-first) e a largura mínima em que os componentes devem ser validados.

---

## 6. Iconografia

**Biblioteca:** [Nome da biblioteca]
**Fonte:** [Link]

**Regras de uso:**
- Usar sempre ícones da biblioteca definida — não misturar com outras bibliotecas
- Tamanhos permitidos: [lista de tamanhos e em qual contexto cada um é usado]
- Nunca usar ícone como único indicador de ação ou estado — sempre acompanhar de label ou tooltip
- Manter estilo consistente dentro de um mesmo produto: [outlined / filled / rounded] — não misturar estilos

---

## 7. Tom de Voz

### Personalidade da marca

Descreva os pilares que definem como a marca se comunica e como eles se equilibram.

| Pilar | Descrição |
|---|---|
| **[Pilar]** | [Como esse pilar aparece na comunicação] |

> **Regra de equilíbrio:** [Descreva quando o tom pode variar e quando deve ser sempre claro e direto — ex: em erros, confirmações e dados sensíveis, o tom é sempre claro e direto.]

---

### Diretrizes de escrita para interface

- **Objetivo e conciso** — cada palavra tem um propósito. Corte o que não agrega.
- **Evite jargão técnico** — o usuário não deve precisar interpretar o que a interface diz.
- **Voz ativa sempre** — prefira "Vamos resolver isso" a "Isso pode ser resolvido".
- [Adicione as diretrizes específicas da marca]

---

### Exemplos de linguagem

**✅ Correto**
> *"[Exemplo de texto no tom da marca]"*

**❌ Incorreto**
> *"[Exemplo de texto fora do tom da marca]"*

**Por que a versão correta funciona melhor:**
[Explique quais características do tom aparecem no exemplo correto e faltam no incorreto.]

---

### Regras para mensagens específicas

#### Mensagens de erro
- **Informe o que aconteceu** — nunca deixe o usuário sem contexto ou que ele mesmo descubra o que deu errado
- **Ofereça o caminho** — toda mensagem de erro deve ter um próximo passo claro e acionável
- **Não culpe o usuário** — use linguagem neutra, nunca "você errou" ou "campo inválido" sem explicação
- **Seja específico** — "O email precisa ter o formato nome@dominio.com" é melhor que "Email inválido"

| ✅ Correto | ❌ Incorreto |
|---|---|
| "[Mensagem de erro no tom da marca]" | "[Mensagem genérica ou técnica]" |

#### Onboarding
- **Contextualize antes de pedir** — explique o porquê de cada informação solicitada antes de pedir
- **Celebre o progresso** — reconheça cada etapa concluída com linguagem positiva e encorajadora
- **Antecipe dúvidas** — se um campo pode gerar confusão, explique antes que o usuário precise perguntar
- **Não sobrecarregue** — apresente uma informação de cada vez; onboarding progressivo é sempre preferível

#### Introduções e empty states
- **Transforme o vazio em convite** — empty states são oportunidade de engajamento, não ausência de conteúdo
- **Diga o que o usuário pode fazer** — não apenas que não há nada ali

| ✅ Correto | ❌ Incorreto |
|---|---|
| "[Empty state que convida à ação]" | "[Empty state que só informa a ausência]" |

---

*Seções opcionais para adicionar conforme o produto evoluir: Componentes, Padrões de Interação, Regras de Negócio Visuais.*
