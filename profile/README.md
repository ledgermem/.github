# LedgerMem

> **Long-term memory infrastructure for AI agents.**
> Hybrid retrieval. Event-sourced. Auditable. Reproducible.

[Website](https://proofly.dev) · [Docs](https://proofly.dev/docs) · [Status](https://status.proofly.dev) · [Benchmarks](https://proofly.dev/benchmarks) · [Awesome list](https://github.com/ledgermem/awesome-ledgermem)

---

## Start in 30 seconds

```bash
# TypeScript                              # Python
npm install @ledgermem/memory             pip install ledgermem

# MCP (Claude Desktop, Cursor, Windsurf)
npx -y @ledgermem/mcp-server
```

```ts
import { LedgerMem } from "@ledgermem/memory";
const mem = new LedgerMem({ apiKey: process.env.LEDGERMEM_API_KEY! });
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

Methodology + raw outputs in [`ledgermem-eval`](https://github.com/ledgermem/ledgermem-eval).

---

## The ecosystem

**10 SDKs · 10 framework adapters · 16 connectors · 6 IDE plugins · 5 automation platforms · 8 IaC packages.** All open source unless noted.

### SDKs (10)

| Language | Repo | Install |
| --- | --- | --- |
| TypeScript / JavaScript | [`ledgermem-js`](https://github.com/ledgermem/ledgermem-js) | `npm i @ledgermem/memory` |
| Python | [`ledgermem-python`](https://github.com/ledgermem/ledgermem-python) | `pip install ledgermem` |
| Go | [`ledgermem-go`](https://github.com/ledgermem/ledgermem-go) | `go get github.com/ledgermem/ledgermem-go` |
| Rust | [`ledgermem-rust`](https://github.com/ledgermem/ledgermem-rust) | `cargo add ledgermem` |
| Ruby | [`ledgermem-ruby`](https://github.com/ledgermem/ledgermem-ruby) | `gem install ledgermem` |
| Java | [`ledgermem-java`](https://github.com/ledgermem/ledgermem-java) | Maven Central: `dev.proofly:ledgermem` |
| C# / .NET | [`ledgermem-csharp`](https://github.com/ledgermem/ledgermem-csharp) | NuGet: `LedgerMem` |
| PHP | [`ledgermem-php`](https://github.com/ledgermem/ledgermem-php) | `composer require ledgermem/ledgermem` |
| Elixir | [`ledgermem-elixir`](https://github.com/ledgermem/ledgermem-elixir) | Hex: `{:ledgermem, "~> 0.1"}` |
| Swift | [`ledgermem-swift`](https://github.com/ledgermem/ledgermem-swift) | Swift Package Manager |

Mobile-first SDKs: [`ledgermem-ios-sdk`](https://github.com/ledgermem/ledgermem-ios-sdk) · [`ledgermem-android-sdk`](https://github.com/ledgermem/ledgermem-android-sdk)

### Framework adapters (10)

| Framework | Repo |
| --- | --- |
| LangChain | [`ledgermem-langchain`](https://github.com/ledgermem/ledgermem-langchain) |
| LangGraph | [`ledgermem-langgraph`](https://github.com/ledgermem/ledgermem-langgraph) |
| LlamaIndex | [`ledgermem-llamaindex`](https://github.com/ledgermem/ledgermem-llamaindex) |
| CrewAI | [`ledgermem-crewai`](https://github.com/ledgermem/ledgermem-crewai) |
| AutoGen | [`ledgermem-autogen`](https://github.com/ledgermem/ledgermem-autogen) |
| Vercel AI SDK | [`ledgermem-vercel-ai`](https://github.com/ledgermem/ledgermem-vercel-ai) |
| Mastra | [`ledgermem-mastra`](https://github.com/ledgermem/ledgermem-mastra) |
| PydanticAI | [`ledgermem-pydantic-ai`](https://github.com/ledgermem/ledgermem-pydantic-ai) |
| OpenAI Assistants (compat shim) | [`ledgermem-openai-assistants`](https://github.com/ledgermem/ledgermem-openai-assistants) |
| Anthropic helper | [`ledgermem-anthropic`](https://github.com/ledgermem/ledgermem-anthropic) |

### Connectors (16)

**Chat & messaging:** [slack-bot](https://github.com/ledgermem/ledgermem-slack-bot) · [discord-bot](https://github.com/ledgermem/ledgermem-discord-bot) · [telegram-bot](https://github.com/ledgermem/ledgermem-telegram-bot) · [whatsapp](https://github.com/ledgermem/ledgermem-whatsapp)

**Knowledge bases:** [notion](https://github.com/ledgermem/ledgermem-notion) · [obsidian](https://github.com/ledgermem/ledgermem-obsidian) · [roam](https://github.com/ledgermem/ledgermem-roam) · [logseq](https://github.com/ledgermem/ledgermem-logseq)

**Email & files:** [email-ingest](https://github.com/ledgermem/ledgermem-email-ingest) · [gdrive-sync](https://github.com/ledgermem/ledgermem-gdrive-sync)

**Read-it-later:** [readwise](https://github.com/ledgermem/ledgermem-readwise) · [pocket](https://github.com/ledgermem/ledgermem-pocket) · [instapaper](https://github.com/ledgermem/ledgermem-instapaper)

**Engineering:** [github-sync](https://github.com/ledgermem/ledgermem-github-sync) · [linear](https://github.com/ledgermem/ledgermem-linear)

**Browsers:** [chrome-extension](https://github.com/ledgermem/ledgermem-chrome-extension) · [arc](https://github.com/ledgermem/ledgermem-arc)

### IDE / dev surfaces (6)

| IDE | Repo |
| --- | --- |
| VS Code (also Cursor / Windsurf / code-server) | [`ledgermem-vscode`](https://github.com/ledgermem/ledgermem-vscode) |
| JetBrains family (IDEA / WebStorm / PyCharm / GoLand) | [`ledgermem-jetbrains`](https://github.com/ledgermem/ledgermem-jetbrains) |
| Zed | [`ledgermem-zed`](https://github.com/ledgermem/ledgermem-zed) |
| Neovim | [`ledgermem-neovim`](https://github.com/ledgermem/ledgermem-neovim) |
| Cursor (rules + MCP preset) | [`ledgermem-cursor-rules`](https://github.com/ledgermem/ledgermem-cursor-rules) |
| GitHub Action | [`ledgermem-github-action`](https://github.com/ledgermem/ledgermem-github-action) |

### Automation platforms (5)

[zapier](https://github.com/ledgermem/ledgermem-zapier) · [make](https://github.com/ledgermem/ledgermem-make) · [n8n](https://github.com/ledgermem/ledgermem-n8n) · [pipedream](https://github.com/ledgermem/ledgermem-pipedream) · [activepieces](https://github.com/ledgermem/ledgermem-activepieces)

### Self-hosting & IaC (8)

| Tool | Repo |
| --- | --- |
| Docker Compose + license verifier | [`ledgermem-enterprise`](https://github.com/ledgermem/ledgermem-enterprise) |
| Helm chart (Artifact Hub) | [`ledgermem-helm-charts`](https://github.com/ledgermem/ledgermem-helm-charts) |
| Kubernetes operator (CRDs) | [`ledgermem-k8s-operator`](https://github.com/ledgermem/ledgermem-k8s-operator) |
| Terraform provider | [`ledgermem-terraform-provider`](https://github.com/ledgermem/ledgermem-terraform-provider) |
| Pulumi provider | [`ledgermem-pulumi`](https://github.com/ledgermem/ledgermem-pulumi) |
| AWS CDK constructs | [`ledgermem-cdk-constructs`](https://github.com/ledgermem/ledgermem-cdk-constructs) |
| Backup / restore CLI | [`ledgermem-backup`](https://github.com/ledgermem/ledgermem-backup) |
| OpenTelemetry + Grafana dashboards | [`ledgermem-otel`](https://github.com/ledgermem/ledgermem-otel) |

### Tooling & developer experience

- [`ledgermem-mcp`](https://github.com/ledgermem/ledgermem-mcp) — Model Context Protocol server (Claude Desktop, Cursor, Windsurf, Cline)
- [`ledgermem-cli`](https://github.com/ledgermem/ledgermem-cli) — official CLI: `ledgermem add`, `search`, `mcp`, `doctor`
- [`ledgermem-migrate`](https://github.com/ledgermem/ledgermem-migrate) — one-command importer from Mem0 / Zep / Supermemory / Letta
- [`ledgermem-examples`](https://github.com/ledgermem/ledgermem-examples) — runnable cookbook
- [`ledgermem-agents`](https://github.com/ledgermem/ledgermem-agents) — reference agents (research, customer support, coding)
- [`ledgermem-eval`](https://github.com/ledgermem/ledgermem-eval) — public benchmark harness + leaderboard
- [`ledgermem-docs`](https://github.com/ledgermem/ledgermem-docs) — docs.proofly.dev source
- [`ledgermem-status`](https://github.com/ledgermem/ledgermem-status) — Cloudflare Worker for status.proofly.dev

### Mobile

- [`ledgermem-mobile`](https://github.com/ledgermem/ledgermem-mobile) — iOS + Android end-user app (Expo, private)
- [`ledgermem-watch`](https://github.com/ledgermem/ledgermem-watch) — Apple Watch quick-capture companion (private)

### Meta

- [`.github`](https://github.com/ledgermem/.github) — reusable workflows + community templates consumed across the org
- [`ledgermem-ui`](https://github.com/ledgermem/ledgermem-ui) — shared design tokens + Tailwind preset (private)
- [`ledgermem-meta`](https://github.com/ledgermem/ledgermem-meta) — clone-all / test-all orchestration (private)
- [`awesome-ledgermem`](https://github.com/ledgermem/awesome-ledgermem) — curated list

---

## Contact

- Founders: founders@proofly.dev
- Security: see [SECURITY.md](https://github.com/ledgermem/.github/blob/main/SECURITY.md)
- Docs: https://proofly.dev/docs
