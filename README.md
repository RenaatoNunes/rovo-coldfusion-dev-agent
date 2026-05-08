# rovo-coldfusion-dev-agent

> Um [Agente Rovo (Atlassian)](https://www.atlassian.com/rovo) personalizado que acelera o desenvolvimento, troubleshooting e modernização de aplicações ColdFusion (CFML) — diretamente do Jira, Confluence e outras ferramentas Atlassian.

---

## 🎯 O que é isso?

Este repositório contém as **instruções do agente** (system prompt) para um Agente Rovo especializado no ecossistema ColdFusion / CFML. O agente foi projetado para ser um assistente prático e sempre disponível para equipes que trabalham com:

- **CFML** (Adobe ColdFusion & Lucee) — script e tag-based
- **ColdBox** — handlers, services, módulos, WireBox, LogBox
- **CommandBox** — gerenciamento de servidor, pacotes e task runners
- **Containers** — Docker & Podman para aplicações CF
- **Bancos de dados** — Oracle (JDBC, tuning SQL, NLS) e MongoDB (drivers, modelagem de dados) na perspectiva CF
- **Hardening de produção** — performance, segurança, logging, observabilidade

## 🚀 O que o agente faz?

| Área | Exemplos |
|---|---|
| **Debug & Diagnóstico** | Cole um stacktrace + código → receba análise de causa raiz e passos para correção |
| **Code Review** | Envie código CFML/CFC → receba feedback sobre escopo, segurança e convenções |
| **ColdBox** | Decisões de arquitetura, problemas de roteamento, interceptors, estrutura de módulos |
| **CommandBox** | Corrija configs de `server.json`, `box.json`, `.env`; automatize com task runners |
| **Containers** | Gere `Dockerfile` / `docker-compose.yml` para apps ACF ou Lucee |
| **Integração com Banco** | Tune de queries Oracle/MongoDB via CF, connection pooling, timeouts |
| **Modernização** | Melhorias incrementais para monolitos legados — segurança, performance, manutenibilidade |

## 📁 Estrutura do Repositório

    rovo-coldfusion-dev-agent/
    ├── README.md                ← Você está aqui
    ├── README.en.md             ← Versão em inglês
    ├── AGENT.md                 ← Instruções do agente (arquivo principal — edite e contribua aqui)
    ├── CONTRIBUTING.md          ← Como contribuir
    └── LICENSE

## 🔧 Como Configurar

### 1. Criar o Agente Rovo

1. Acesse seu site Atlassian → **Rovo** → **Agents** → **Create Agent**
2. Dê um nome (ex.: *ColdFusion Dev Agent*)
3. Copie o conteúdo de [`AGENT.md`](./AGENT.md) no campo **Instructions**
4. Salve e publique

### 2. Usar o Agente

Mencione o agente no Jira, Confluence ou Rovo Chat:

    @ColdFusion Dev Agent Estou recebendo um erro "variable undefined"
    dentro de um callback arrayMap. Aqui está meu código: [cole o código]

O agente vai classificar o problema, diagnosticar e fornecer uma correção passo a passo.

## 💡 Exemplos de Prompts

    → "Debugue este handler ColdBox — retorna 500 em requisições POST: [cole o código]"

    → "Crie um Dockerfile para uma app Lucee 6 com CommandBox e Oracle JDBC"

    → "Revise este CFC quanto a problemas de segurança: [cole o código]"

    → "Meu cfquery está lento contra Oracle. Aqui está o SQL e o explain plan: [cole]"

    → "Monte um docker-compose para dev local com ACF 2023 + MongoDB"

## 🤝 Como Contribuir

Contribuições são bem-vindas! O arquivo principal para editar é o **[`AGENT.md`](./AGENT.md)** — este é o cérebro do agente.

### Passo a passo

1. **Fork** este repositório
2. **Edite** o `AGENT.md` com suas melhorias
3. **Teste** as alterações colando as instruções atualizadas em um Agente Rovo
4. **Envie um Pull Request** com uma descrição clara do que mudou e por quê

### Ideias de contribuição

- Adicionar novos padrões de diagnóstico para erros comuns de CFML
- Melhorar orientações específicas do ColdBox (ex.: `cborm`, `cbsecurity`, `cbvalidation`)
- Adicionar dicas específicas do Lucee e diferenças em relação ao ACF
- Expandir padrões de integração com Oracle ou MongoDB
- Adicionar novas áreas de expertise (ex.: integração S3, design de REST API, pipelines CI/CD)
- Corrigir imprecisões ou melhorar a clareza

Veja [`CONTRIBUTING.md`](./CONTRIBUTING.md) para diretrizes detalhadas.

## 📋 Resumo das Capacidades do Agente

O agente segue um fluxo de diagnóstico estruturado para cada solicitação:

1. **Classificar** — Identifica qual(is) área(s) se aplicam (CFML, ColdBox, CommandBox, Containers, Oracle, MongoDB, Performance, Segurança)
2. **Extrair** — Separa fatos fornecidos de suposições inferidas
3. **Diagnosticar** — Apresenta causa(s) raiz com evidências; faz perguntas direcionadas se faltam dados
4. **Corrigir** — Ações passo a passo, menor mudança segura primeiro, com passos de reprodução/validação/rollback
5. **Fortalecer** — Próximos passos opcionais para logging, segurança, performance (apenas quando relevante)

### Regras de segurança importantes

- ⚠️ **Escopo de closures** — O agente aplica as regras de escopo de closures do CF: nunca referencia `local.variavel` de uma função pai dentro de uma closure. Isso previne um dos bugs mais comuns em CFML.
- 🔒 **Seguro por padrão** — Output encoding, `cfqueryparam`, cookies seguros, gestão de secrets
- 🛡️ **Seguro para produção** — Alerta antes de operações arriscadas; propõe alternativas seguras

## 📄 Licença

[MIT](./LICENSE) — Use, faça fork, melhore.

---

**Feito com ❤️ para a comunidade ColdFusion por desenvolvedores que ainda acreditam em CFML.**
