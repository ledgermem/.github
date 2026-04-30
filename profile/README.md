# Mnemo

> **Long-term memory infrastructure for AI agents.**
> Hybrid retrieval. Event-sourced. Auditable. Reproducible.

[Website](https://getmnemo.xyz) · [Docs](https://getmnemo.xyz/docs) · [Status](https://status.getmnemo.xyz) · [Benchmarks](https://getmnemo.xyz/benchmarks) · [Awesome list](https://github.com/ledgermem/awesome-getmnemo)

---

## Start in 30 seconds

```bash
# TypeScript                   # Python
npm install mnemo              pip install mnemo

# MCP (Claude Desktop, Cursor, Windsurf)
npx -y mnemo-mcp
```

```ts
import { Mnemo } from "mnemo";
const mem = new Mnemo({ apiKey: process.env.MNEMO_API_KEY! });
await mem.add("Loves Italian food, allergic to shellfish.");
const hits = await mem.search("dinner ideas");
```

## Benchmark

Phase 14 final on **LongMemEval (500 questions)**:

| Metric | Score |
| --- | --- |
| Strict | **375 / 500 (75.0%)** |
| Average | **85.09%** |
| Single-session-user | 91.4% |
| Knowledge update | 89.7% |
| Single-session-assistant | 82.1% |
| Temporal reasoning | 76.7% |
| Multi-session | 69.9% |

Methodology + raw outputs in [`getmnemo-eval`](https://github.com/ledgermem/getmnemo-eval).

---

## The ecosystem

**10 SDKs · 10 framework adapters · 16 connectors · 6 IDE plugins · 5 automation platforms · 8 IaC packages.** All open source unless noted.

### SDKs (10)

| Language | Repo | Install |
| --- | --- | --- |
| TypeScript / JavaScript | [`getmnemo-js`](https://github.com/ledgermem/getmnemo-js) | `npm i mnemo` |
| Python | [`getmnemo-python`](https://github.com/ledgermem/getmnemo-python) | `pip install mnemo` |
| Go | [`getmnemo-go`](https://github.com/ledgermem/getmnemo-go) | `go get github.com/ledgermem/getmnemo-go` |
| Rust | [`getmnemo-rust`](https://github.com/ledgermem/getmnemo-rust) | `cargo add mnemo` |
| Ruby | [`getmnemo-ruby`](https://github.com/ledgermem/getmnemo-ruby) | `gem install mnemo` |
| Java | [`getmnemo-java`](https://github.com/ledgermem/getmnemo-java) | Maven Central: `xyz.getmnemo:mnemo` |
| C# / .NET | [`getmnemo-csharp`](https://github.com/ledgermem/getmnemo-csharp) | NuGet: `Mnemo` |
| PHP | [`getmnemo-php`](https://github.com/ledgermem/getmnemo-php) | `composer require mnemo/mnemo` |
| Elixir | [`getmnemo-elixir`](https://github.com/ledgermem/getmnemo-elixir) | Hex: `{:mnemo, "~> 0.1"}` |
| Swift | [`getmnemo-swift`](https://github.com/ledgermem/getmnemo-swift) | Swift Package Manager |

Mobile-first SDKs: [`getmnemo-ios-sdk`](https://github.com/ledgermem/getmnemo-ios-sdk) · [`getmnemo-android-sdk`](https://github.com/ledgermem/getmnemo-android-sdk)

### Framework adapters (10)

| Framework | Repo |
| --- | --- |
| LangChain | [`getmnemo-langchain`](https://github.com/ledgermem/getmnemo-langchain) |
| LangGraph | [`getmnemo-langgraph`](https://github.com/ledgermem/getmnemo-langgraph) |
| LlamaIndex | [`getmnemo-llamaindex`](https://github.com/ledgermem/getmnemo-llamaindex) |
| CrewAI | [`getmnemo-crewai`](https://github.com/ledgermem/getmnemo-crewai) |
| AutoGen | [`getmnemo-autogen`](https://github.com/ledgermem/getmnemo-autogen) |
| Vercel AI SDK | [`getmnemo-vercel-ai`](https://github.com/ledgermem/getmnemo-vercel-ai) |
| Mastra | [`getmnemo-mastra`](https://github.com/ledgermem/getmnemo-mastra) |
| PydanticAI | [`getmnemo-pydantic-ai`](https://github.com/ledgermem/getmnemo-pydantic-ai) |
| OpenAI Assistants (compat shim) | [`getmnemo-openai-assistants`](https://github.com/ledgermem/getmnemo-openai-assistants) |
| Anthropic helper | [`getmnemo-anthropic`](https://github.com/ledgermem/getmnemo-anthropic) |

### Connectors (16)

**Chat & messaging:** [slack-bot](https://github.com/ledgermem/getmnemo-slack-bot) · [discord-bot](https://github.com/ledgermem/getmnemo-discord-bot) · [telegram-bot](https://github.com/ledgermem/getmnemo-telegram-bot) · [whatsapp](https://github.com/ledgermem/getmnemo-whatsapp)

**Knowledge bases:** [notion](https://github.com/ledgermem/getmnemo-notion) · [obsidian](https://github.com/ledgermem/getmnemo-obsidian) · [roam](https://github.com/ledgermem/getmnemo-roam) · [logseq](https://github.com/ledgermem/getmnemo-logseq)

**Email & files:** [email-ingest](https://github.com/ledgermem/getmnemo-email-ingest) · [gdrive-sync](https://github.com/ledgermem/getmnemo-gdrive-sync)

**Read-it-later:** [readwise](https://github.com/ledgermem/getmnemo-readwise) · [pocket](https://github.com/ledgermem/getmnemo-pocket) · [instapaper](https://github.com/ledgermem/getmnemo-instapaper)

**Engineering:** [github-sync](https://github.com/ledgermem/getmnemo-github-sync) · [linear](https://github.com/ledgermem/getmnemo-linear)

**Browsers:** [chrome-extension](https://github.com/ledgermem/getmnemo-chrome-extension) · [arc](https://github.com/ledgermem/getmnemo-arc)

### IDE / dev surfaces (6)

| IDE | Repo |
| --- | --- |
| VS Code (also Cursor / Windsurf / code-server) | [`getmnemo-vscode`](https://github.com/ledgermem/getmnemo-vscode) |
| JetBrains family (IDEA / WebStorm / PyCharm / GoLand) | [`getmnemo-jetbrains`](https://github.com/ledgermem/getmnemo-jetbrains) |
| Zed | [`getmnemo-zed`](https://github.com/ledgermem/getmnemo-zed) |
| Neovim | [`getmnemo-neovim`](https://github.com/ledgermem/getmnemo-neovim) |
| Cursor (rules + MCP preset) | [`getmnemo-cursor-rules`](https://github.com/ledgermem/getmnemo-cursor-rules) |
| GitHub Action | [`getmnemo-github-action`](https://github.com/ledgermem/getmnemo-github-action) |

### Automation platforms (5)

[zapier](https://github.com/ledgermem/getmnemo-zapier) · [make](https://github.com/ledgermem/getmnemo-make) · [n8n](https://github.com/ledgermem/getmnemo-n8n) · [pipedream](https://github.com/ledgermem/getmnemo-pipedream) · [activepieces](https://github.com/ledgermem/getmnemo-activepieces)

### Self-hosting & IaC (8)

| Tool | Repo |
| --- | --- |
| Docker Compose + license verifier | [`getmnemo-enterprise`](https://github.com/ledgermem/getmnemo-enterprise) |
| Helm chart (Artifact Hub) | [`getmnemo-helm-charts`](https://github.com/ledgermem/getmnemo-helm-charts) |
| Kubernetes operator (CRDs) | [`getmnemo-k8s-operator`](https://github.com/ledgermem/getmnemo-k8s-operator) |
| Terraform provider | [`getmnemo-terraform-provider`](https://github.com/ledgermem/getmnemo-terraform-provider) |
| Pulumi provider | [`getmnemo-pulumi`](https://github.com/ledgermem/getmnemo-pulumi) |
| AWS CDK constructs | [`getmnemo-cdk-constructs`](https://github.com/ledgermem/getmnemo-cdk-constructs) |
| Backup / restore CLI | [`getmnemo-backup`](https://github.com/ledgermem/getmnemo-backup) |
| OpenTelemetry + Grafana dashboards | [`getmnemo-otel`](https://github.com/ledgermem/getmnemo-otel) |

### Tooling & developer experience

- [`getmnemo-mcp`](https://github.com/ledgermem/getmnemo-mcp) — Model Context Protocol server (Claude Desktop, Cursor, Windsurf, Cline)
- [`getmnemo-cli`](https://github.com/ledgermem/getmnemo-cli) — official CLI: `mnemo add`, `search`, `mcp`, `doctor`
- [`getmnemo-migrate`](https://github.com/ledgermem/getmnemo-migrate) — one-command importer from Mem0 / Zep / Supermemory / Letta
- [`getmnemo-examples`](https://github.com/ledgermem/getmnemo-examples) — runnable cookbook
- [`getmnemo-agents`](https://github.com/ledgermem/getmnemo-agents) — reference agents (research, customer support, coding)
- [`getmnemo-eval`](https://github.com/ledgermem/getmnemo-eval) — public benchmark harness + leaderboard
- [`getmnemo-docs`](https://github.com/ledgermem/getmnemo-docs) — docs.getmnemo.xyz source
- [`getmnemo-status`](https://github.com/ledgermem/getmnemo-status) — Cloudflare Worker for status.getmnemo.xyz

### Mobile

- [`getmnemo-mobile`](https://github.com/ledgermem/getmnemo-mobile) — iOS + Android end-user app (Expo, private)
- [`getmnemo-watch`](https://github.com/ledgermem/getmnemo-watch) — Apple Watch quick-capture companion (private)

### Meta

- [`.github`](https://github.com/ledgermem/.github) — reusable workflows + community templates consumed across the org
- [`getmnemo-ui`](https://github.com/ledgermem/getmnemo-ui) — shared design tokens + Tailwind preset (private)
- [`getmnemo-meta`](https://github.com/ledgermem/getmnemo-meta) — clone-all / test-all orchestration (private)
- [`awesome-getmnemo`](https://github.com/ledgermem/awesome-getmnemo) — curated list

---

## Contact

- Founders: founders@getmnemo.xyz
- Security: see [SECURITY.md](https://github.com/ledgermem/.github/blob/main/SECURITY.md)
- Docs: https://getmnemo.xyz/docs
