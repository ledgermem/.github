# LedgerMem

> **Long-term memory infrastructure for AI agents.**
> Hybrid retrieval. Event-sourced. Auditable. Reproducible.

[Website](https://proofly.dev) · [Docs](https://proofly.dev/docs) · [Status](https://status.proofly.dev) · [Benchmarks](https://proofly.dev/benchmarks)

---

## Start in 30 seconds

```bash
# TypeScript
npm install @ledgermem/memory

# Python
pip install ledgermem

# MCP (Claude Desktop, Cursor, Windsurf)
npx -y @ledgermem/mcp-server
```

```ts
import { LedgerMem } from "@ledgermem/memory";
const mem = new LedgerMem({ apiKey: process.env.LEDGERMEM_API_KEY! });
await mem.add("Loves Italian food, allergic to shellfish.");
const hits = await mem.search("dinner ideas");
```

## Repos worth bookmarking

| Repo | What it is |
| --- | --- |
| [`ledgermem-mcp`](https://github.com/ledgermem/ledgermem-mcp) | Model Context Protocol server |
| [`ledgermem-python`](https://github.com/ledgermem/ledgermem-python) | Python SDK |
| [`ledgermem-js`](https://github.com/ledgermem/ledgermem-js) | TypeScript / JavaScript SDK |
| [`ledgermem-integrations`](https://github.com/ledgermem/ledgermem-integrations) | LangChain / LlamaIndex / AutoGen / CrewAI / PydanticAI / Vercel AI |
| [`ledgermem-enterprise`](https://github.com/ledgermem/ledgermem-enterprise) | Self-hosting (Docker, Helm, license verifier) |
| [`ledgermem-status`](https://github.com/ledgermem/ledgermem-status) | Cloudflare Worker for status.proofly.dev |
| [`awesome-ledgermem`](https://github.com/ledgermem/awesome-ledgermem) | Curated list of integrations + examples |

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

## Contact

- Founders: founders@proofly.dev
- Security: security@proofly.dev
- Docs: https://proofly.dev/docs
