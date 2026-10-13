# @core/catalog

[![genpm](https://api.genpm.net/v1/badge/@core/catalog.svg)](https://genpm.net/p/@core/catalog) ![license](https://img.shields.io/badge/license-MIT-blue)

> Product catalog: variants with options, prices in cents, categories, collections, translations and safe stock reservations

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/lib/catalog`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/catalog
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/catalog`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/catalog with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Products for a store: up to 3 options (Size, Color…) and their variants with SKU, price/compare-at/cost in minor
units, stock with backorder rules, weight and image; categories (tree), manual ordered collections, tags, attributes,
per-locale translations, media references (@core/media ids), sitemap/search sources and admin resources.
`reserveStock` locks the variant row so two buyers can't get the last unit. No cart, prices rules or multi-warehouse.

## At a glance

- **GenPM dependencies** (installed with it): [@core/db](https://genpm.net/p/@core/db), [@core/money](https://genpm.net/p/@core/money), [@core/rich-text](https://genpm.net/p/@core/rich-text), [@core/contracts](https://genpm.net/p/@core/contracts)
- **npm dependencies** (proposed, never installed without asking): `zod`
- **Environment variables** (added to `.env.example`): `STORE_CURRENCY`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/lib/catalog`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
