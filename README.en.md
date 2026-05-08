# rovo-coldfusion-dev-agent

> A custom [Atlassian Rovo Agent](https://www.atlassian.com/rovo) that accelerates development, troubleshooting, and modernization of ColdFusion (CFML) applications — directly from Jira, Confluence, and other Atlassian tools.

---

## 🎯 What is this?

This repository contains the **agent instructions** (system prompt) for a Rovo Agent specialized in the ColdFusion / CFML ecosystem. The agent is designed to be a practical, always-available assistant for teams working with:

- **CFML** (Adobe ColdFusion & Lucee) — script and tag-based
- **ColdBox** framework — handlers, services, modules, WireBox, LogBox
- **CommandBox** — server management, package management, task runners
- **Containers** — Docker & Podman setups for CF applications
- **Databases** — Oracle (JDBC, SQL tuning, NLS) and MongoDB (drivers, data modeling) from a CF perspective
- **Production hardening** — performance, security, logging, observability

## 🚀 What can the agent do?

| Area | Examples |
|---|---|
| **Debug & Diagnose** | Paste a stacktrace + code snippet → get root cause analysis and fix steps |
| **Code Review** | Submit CFML/CFC code → receive feedback on scoping, security, conventions |
| **ColdBox Guidance** | Architecture decisions, routing issues, interceptor patterns, module structure |
| **CommandBox Recipes** | Fix `server.json`, `box.json`, `.env` configs; automate with task runners |
| **Container Setups** | Generate `Dockerfile` / `docker-compose.yml` for ACF or Lucee apps |
| **Database Integration** | Tune Oracle/MongoDB queries from CF, connection pooling, timeout configs |
| **Modernization** | Incremental improvements for legacy monoliths — security, performance, maintainability |

## 📁 Repository Structure

    rovo-coldfusion-dev-agent/
    ├── README.md                ← Portuguese version (pt-BR)
    ├── README.en.md             ← You are here
    ├── AGENT.md                 ← Agent instructions (the main file — edit and contribute here)
    ├── CONTRIBUTING.md          ← How to contribute
    └── LICENSE

## 🔧 Setup

### 1. Create the Rovo Agent

1. Go to your Atlassian site → **Rovo** → **Agents** → **Create Agent**
2. Give it a name (e.g., *ColdFusion Dev Agent*)
3. Copy the contents of [`AGENT.md`](./AGENT.md) into the **Instructions** field
4. Save and publish

### 2. Use the Agent

Mention the agent in Jira, Confluence, or Rovo Chat:

    @ColdFusion Dev Agent I'm getting a "variable undefined" error
    inside an arrayMap callback. Here's my code: [paste code]

The agent will classify the issue, diagnose, and provide a step-by-step fix.

## 💡 Example Prompts

    → "Debug this ColdBox handler — it returns 500 on POST requests: [paste code]"

    → "Create a Dockerfile for a Lucee 6 app with CommandBox and Oracle JDBC"

    → "Review this CFC for security issues: [paste code]"

    → "My cfquery is slow against Oracle. Here's the SQL and explain plan: [paste]"

    → "Set up a docker-compose for local dev with ACF 2023 + MongoDB"

## 🤝 Contributing

We welcome contributions! The main file to edit is **[`AGENT.md`](./AGENT.md)** — this is the agent's brain.

### How to contribute

1. **Fork** this repository
2. **Edit** `AGENT.md` with your improvements
3. **Test** the changes by pasting the updated instructions into a Rovo Agent
4. **Submit a Pull Request** with a clear description of what you changed and why

### Contribution ideas

- Add new diagnostic patterns for common CFML errors
- Improve ColdBox-specific guidance (e.g., `cborm`, `cbsecurity`, `cbvalidation`)
- Add Lucee-specific tips and differences from ACF
- Expand Oracle or MongoDB integration patterns
- Add new areas of expertise (e.g., S3 integration, REST API design, CI/CD pipelines)
- Fix inaccuracies or improve clarity

See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for detailed guidelines.

## 📋 Agent Capabilities Summary

The agent follows a structured diagnostic flow for every request:

1. **Classify** — Identifies which area(s) apply (CFML, ColdBox, CommandBox, Containers, Oracle, MongoDB, Performance, Security)
2. **Extract** — Separates provided facts from inferred assumptions
3. **Diagnose** — States root cause(s) with evidence; asks targeted questions if data is missing
4. **Fix** — Step-by-step actions, smallest safe change first, with reproduce/validate/rollback steps
5. **Harden** — Optional next steps for logging, security, performance (only when valuable)

### Key safety rules

- ⚠️ **Closure scoping** — The agent enforces CF's closure scope rules: never references `local.variable` from a parent function inside a closure. This prevents one of the most common CFML bugs.
- 🔒 **Secure by default** — Output encoding, `cfqueryparam`, secure cookies, secrets management
- 🛡️ **Production-safe** — Warns before risky operations; proposes safe alternatives

## 📄 License

[MIT](./LICENSE) — Use it, fork it, improve it.

---

**Built with ❤️ for the ColdFusion community by developers who still believe in CFML.**
