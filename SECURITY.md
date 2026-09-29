# 🔒 Segurança · Security

🇧🇷 [Português](#-português) · 🇺🇸 [English](#-english)

---

## 🇧🇷 Português

### Por que isso importa

Uma skill é um conjunto de instruções que roda dentro do Claude de quem a instala. Uma alteração maliciosa, como instruções escondidas para enviar dados do usuário para fora, afetaria todo mundo que usa a skill. Por isso, qualquer suspeita deve ser relatada em privado.

### Como relatar uma vulnerabilidade

1. **Não abra uma issue pública.**
2. Acesse **[Security → Report a vulnerability](https://github.com/guilhermedworakowski/design-skill/security/advisories/new)** e descreva o problema.
3. Informe o arquivo, o trecho e, se possível, como reproduzir.

Você recebe uma resposta assim que possível. Quando a correção sair, o crédito é seu, se quiser.

### O que relatar

- Instruções nos arquivos da skill que tentem fazer o Claude agir contra o usuário (prompt injection, envio de dados, links suspeitos)
- Um pacote `.skill` com conteúdo diferente da pasta correspondente
- Qualquer dado pessoal, senha ou chave que tenha sido publicado por engano

### Como o repositório se protege

- Os pacotes `.skill` são gerados só pelo mantenedor, a partir das pastas `design-pt/` e `design-en/`
- Uma verificação automática confere, em todo PR e push, se cada `.skill` é idêntico à sua pasta
- A branch `main` não aceita force-push nem exclusão
- O secret scanning com push protection está ativado

### Dica para quem instala

Prefira baixar os pacotes deste repositório oficial. Se baixar de um fork ou outro site, abra o `.skill` (é um `.zip`) e confira o conteúdo antes de instalar.

---

## 🇺🇸 English

### Why this matters

A skill is a set of instructions that runs inside the Claude of whoever installs it. A malicious change, such as hidden instructions to send user data elsewhere, would affect everyone using the skill. That's why any suspicion should be reported privately.

### How to report a vulnerability

1. **Don't open a public issue.**
2. Go to **[Security → Report a vulnerability](https://github.com/guilhermedworakowski/design-skill/security/advisories/new)** and describe the problem.
3. Include the file, the passage and, if possible, how to reproduce it.

You'll get a reply as soon as possible. Once the fix ships, you get the credit if you want it.

### What to report

- Instructions in the skill files that try to make Claude act against the user (prompt injection, data exfiltration, suspicious links)
- A `.skill` package whose content differs from its matching folder
- Any personal data, password or key that was published by mistake

### How the repository protects itself

- `.skill` packages are built only by the maintainer, from the `design-pt/` and `design-en/` folders
- An automated check confirms, on every PR and push, that each `.skill` matches its folder exactly
- The `main` branch rejects force-pushes and deletion
- Secret scanning with push protection is turned on

### Tip for anyone installing

Prefer downloading the packages from this official repository. If you get them from a fork or another site, open the `.skill` (it's a `.zip`) and check its content before installing.
