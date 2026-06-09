# Mnemo

> **Long-term memory infrastructure for AI agents.**
> Hybrid retrieval. Event-sourced. Auditable. Reproducible.

[Website](https://mnemohq.com) · [Docs](https://mnemohq.com/docs) · [npm](https://www.npmjs.com/package/getmnemo) · [PyPI](https://pypi.org/project/getmnemo/)

> **About the name:** the brand is **Mnemo**, but the package is **`getmnemo`** — `mnemo` was already taken on npm and PyPI. So you `pip install getmnemo` / `npm install getmnemo`. In Python the import module is `mnemo` (installed by the `getmnemo` package).

---

## Start in 30 seconds

```bash
# TypeScript / JavaScript            # Python
npm install getmnemo                 pip install getmnemo   # NOT "mnemo" — that's someone else's package
```

```ts
import { Mnemo } from "getmnemo";
const mem = new Mnemo({ apiKey: process.env.GETMNEMO_API_KEY! });
await mem.add("Loves Italian food, allergic to shellfish.");
const hits = await mem.search("dinner ideas");
```

```python
import os
from mnemo import Mnemo            # the module is `mnemo`; you installed it via `pip install getmnemo`
mem = Mnemo(api_key=os.environ["GETMNEMO_API_KEY"])
mem.add("Loves Italian food, allergic to shellfish.")
hits = mem.search("dinner ideas")
```

MCP server (Claude Desktop, Cursor, Windsurf):

```bash
npx -y getmnemo-mcp
```

---

## What's shipped today

Everything below is published and installable right now.

### Core SDKs

| Language | Package | Install |
| --- | --- | --- |
| TypeScript / JavaScript | [`getmnemo`](https://www.npmjs.com/package/getmnemo) | `npm install getmnemo` |
| Python | [`getmnemo`](https://pypi.org/project/getmnemo/) | `pip install getmnemo` (import `mnemo`) |

### Tooling

| Tool | Package | Install |
| --- | --- | --- |
| CLI | [`getmnemo-cli`](https://www.npmjs.com/package/getmnemo-cli) | `npm i -g getmnemo-cli` → run `getmnemo` |
| MCP server | [`getmnemo-mcp`](https://www.npmjs.com/package/getmnemo-mcp) | `npx -y getmnemo-mcp` |

### Framework adapters

| Framework | Package | Install |
| --- | --- | --- |
| Anthropic SDK | [`getmnemo-anthropic`](https://www.npmjs.com/package/getmnemo-anthropic) | `npm install getmnemo-anthropic` |
| Vercel AI SDK | [`getmnemo-vercel-ai`](https://www.npmjs.com/package/getmnemo-vercel-ai) | `npm install getmnemo-vercel-ai` |
| Mastra | [`getmnemo-mastra`](https://www.npmjs.com/package/getmnemo-mastra) | `npm install getmnemo-mastra` |

More SDKs, connectors, and framework integrations are in progress — they'll be listed here as each one ships and is installable. We'd rather list seven things that work than seventy that don't.

---

## Links

- Website & docs — [mnemohq.com](https://mnemohq.com)
- API — `https://api.mnemohq.com`
- npm — [npmjs.com/~shhahhussain](https://www.npmjs.com/~shhahhussain)
