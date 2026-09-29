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
- Um pacote `.skill` de uma Release com conteúdo diferente da pasta correspondente
- Qualquer dado pessoal, senha ou chave que tenha sido publicado por engano

### Como o repositório se protege

- Nenhum pacote `.skill` fica no repositório: eles são gerados por um workflow a partir das pastas `design-pt/` e `design-en/` e publicados nas Releases, com o arquivo `SHA256SUMS.txt`
- Uma verificação automática recusa, em todo PR e push, qualquer `.skill` ou `.zip` commitado
- A branch `main` só aceita mudanças por PR com a verificação aprovada, e não aceita force-push nem exclusão
- As tags de versão (`v*`) não podem ser apagadas nem movidas, então uma Release publicada não muda de conteúdo
- O secret scanning com push protection está ativado

### Dica para quem instala

Baixe os pacotes da página de [Releases](https://github.com/guilhermedworakowski/design-skill/releases) deste repositório oficial. Para conferir se o arquivo não foi alterado, compare o hash com o `SHA256SUMS.txt` da mesma Release (`shasum -a 256 design-pt.skill`). Se baixar de um fork ou outro site, abra o `.skill` (é um `.zip`) e confira o conteúdo antes de instalar.

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
- A `.skill` package from a Release whose content differs from its matching folder
- Any personal data, password or key that was published by mistake

### How the repository protects itself

- No `.skill` package lives in the repository: a workflow builds them from the `design-pt/` and `design-en/` folders and publishes them in Releases, along with a `SHA256SUMS.txt` file
- An automated check rejects, on every PR and push, any committed `.skill` or `.zip`
- The `main` branch only accepts changes through a PR with a passing check, and rejects force-pushes and deletion
- Version tags (`v*`) can't be deleted or moved, so a published Release never changes content
- Secret scanning with push protection is turned on

### Tip for anyone installing

Download the packages from this official repository's [Releases](https://github.com/guilhermedworakowski/design-skill/releases) page. To check the file wasn't altered, compare its hash with the `SHA256SUMS.txt` from the same Release (`shasum -a 256 design-en.skill`). If you get them from a fork or another site, open the `.skill` (it's a `.zip`) and check its content before installing.
