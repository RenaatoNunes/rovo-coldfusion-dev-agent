# Contribuindo / Contributing

> 🇧🇷 [Português](#-português) | 🇺🇸 [English](#-english)

---

## 🇧🇷 Português

Obrigado pelo interesse em contribuir com o **rovo-coldfusion-dev-agent**! Este projeto é mantido pela comunidade e toda contribuição é bem-vinda.

### O que pode ser contribuído?

O arquivo principal do projeto é o **[AGENT.md](./AGENT.md)** — ele contém todas as instruções que definem o comportamento do agente Rovo. A maioria das contribuições será neste arquivo.

#### Tipos de contribuição

| Tipo | Descrição |
|---|---|
| 🐛 **Correção** | Corrigir instruções incorretas, imprecisas ou que geram respostas ruins |
| ✨ **Nova capacidade** | Adicionar suporte a novas áreas (ex.: integração S3, CI/CD, REST API design) |
| 📝 **Melhoria de clareza** | Reescrever instruções para que o agente responda de forma mais precisa |
| 🔒 **Regra de segurança** | Adicionar padrões de segurança ou prevenção de erros comuns |
| 📚 **Documentação** | Melhorar README, exemplos de prompts ou este próprio arquivo |

### Como contribuir

#### 1. Fork e clone

    git clone https://github.com/SEU_USUARIO/rovo-coldfusion-dev-agent.git
    cd rovo-coldfusion-dev-agent

#### 2. Crie uma branch

Use um nome descritivo:

    git checkout -b feat/suporte-cbsecurity
    git checkout -b fix/corrige-escopo-closure
    git checkout -b docs/melhora-exemplos

#### 3. Faça suas alterações

Edite o `AGENT.md` (ou outros arquivos conforme necessário).

#### 4. Teste suas alterações

Antes de enviar o PR, **teste o prompt atualizado**:

1. Acesse seu site Atlassian → **Rovo** → **Agents**
2. Crie um agente de teste ou edite um existente
3. Cole o conteúdo atualizado do `AGENT.md` no campo **Instructions**
4. Faça perguntas ao agente que exercitem a área que você alterou
5. Verifique se as respostas estão corretas, seguras e seguem o fluxo esperado

#### 5. Commit e Push

    git add .
    git commit -m "feat: adiciona suporte a cbsecurity no diagnóstico"
    git push origin feat/suporte-cbsecurity

#### 6. Abra um Pull Request

- Descreva **o que** você mudou e **por quê**
- Inclua **exemplos de prompts** que testou e os resultados obtidos
- Se possível, inclua um **antes/depois** mostrando a melhoria na resposta do agente

### Diretrizes para edição do AGENT.md

#### ✅ Faça

- Mantenha instruções **objetivas e acionáveis** — o agente precisa de clareza
- Use a estrutura existente (seções por tópico: CFML, ColdBox, CommandBox, etc.)
- Adicione **exemplos concretos** quando possível
- Considere edge cases e erros comuns
- Teste com prompts reais antes de submeter

#### ❌ Evite

- Instruções vagas ou genéricas demais (ex.: "seja bom em ColdFusion")
- Contradições com regras existentes (especialmente as de segurança)
- Remover regras de segurança sem justificativa clara
- Instruções que dependam de contexto externo que o agente não terá acesso

### Convenções de commit

Usamos [Conventional Commits](https://www.conventionalcommits.org/):

| Prefixo | Uso |
|---|---|
| `feat:` | Nova capacidade ou instrução |
| `fix:` | Correção de instrução incorreta |
| `docs:` | Alteração em documentação (README, CONTRIBUTING) |
| `refactor:` | Reorganização sem mudança de comportamento |
| `test:` | Adição de exemplos de teste/prompts |

### Código de conduta

- Seja respeitoso e construtivo
- Foque em melhorar o agente para toda a equipe
- Aceite feedback nos PRs com mente aberta
- Lembre-se: o objetivo é ajudar desenvolvedores ColdFusion a serem mais produtivos

---

## 🇺🇸 English

Thank you for your interest in contributing to **rovo-coldfusion-dev-agent**! This is a community-maintained project and all contributions are welcome.

### What can be contributed?

The main project file is **[AGENT.md](./AGENT.md)** — it contains all the instructions that define the Rovo agent's behavior. Most contributions will be to this file.

#### Contribution types

| Type | Description |
|---|---|
| 🐛 **Fix** | Correct inaccurate instructions or ones that produce poor responses |
| ✨ **New capability** | Add support for new areas (e.g., S3 integration, CI/CD, REST API design) |
| 📝 **Clarity improvement** | Rewrite instructions so the agent responds more precisely |
| 🔒 **Security rule** | Add security patterns or common error prevention |
| 📚 **Documentation** | Improve README, prompt examples, or this file |

### How to contribute

#### 1. Fork and clone

    git clone https://github.com/YOUR_USERNAME/rovo-coldfusion-dev-agent.git
    cd rovo-coldfusion-dev-agent

#### 2. Create a branch

Use a descriptive name:

    git checkout -b feat/cbsecurity-support
    git checkout -b fix/closure-scope-rule
    git checkout -b docs/improve-examples

#### 3. Make your changes

Edit `AGENT.md` (or other files as needed).

#### 4. Test your changes

Before submitting a PR, **test the updated prompt**:

1. Go to your Atlassian site → **Rovo** → **Agents**
2. Create a test agent or edit an existing one
3. Paste the updated `AGENT.md` content into the **Instructions** field
4. Ask the agent questions that exercise the area you changed
5. Verify that responses are correct, safe, and follow the expected flow

#### 5. Commit and Push

    git add .
    git commit -m "feat: add cbsecurity support to diagnostics"
    git push origin feat/cbsecurity-support

#### 6. Open a Pull Request

- Describe **what** you changed and **why**
- Include **example prompts** you tested and the results
- If possible, include a **before/after** showing the improvement in agent responses

### Guidelines for editing AGENT.md

#### ✅ Do

- Keep instructions **objective and actionable** — the agent needs clarity
- Follow the existing structure (sections by topic: CFML, ColdBox, CommandBox, etc.)
- Add **concrete examples** when possible
- Consider edge cases and common errors
- Test with real prompts before submitting

#### ❌ Don't

- Write vague or overly generic instructions (e.g., "be good at ColdFusion")
- Contradict existing rules (especially security rules)
- Remove security rules without clear justification
- Add instructions that depend on external context the agent won't have access to

### Commit conventions

We use [Conventional Commits](https://www.conventionalcommits.org/):

| Prefix | Usage |
|---|---|
| `feat:` | New capability or instruction |
| `fix:` | Fix for incorrect instruction |
| `docs:` | Documentation changes (README, CONTRIBUTING) |
| `refactor:` | Reorganization without behavior change |
| `test:` | Addition of test examples/prompts |

### Code of conduct

- Be respectful and constructive
- Focus on improving the agent for the entire team
- Accept PR feedback with an open mind
- Remember: the goal is to help ColdFusion developers be more productive

---

## 📬 Dúvidas / Questions

Abra uma [issue](../../issues) se tiver dúvidas ou sugestões que não se encaixam em um PR.

Open an [issue](../../issues) if you have questions or suggestions that don't fit into a PR.
