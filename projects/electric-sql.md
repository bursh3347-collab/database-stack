# ElectricSQL

> Sync engine for local-first apps — Postgres to local SQLite, real-time

| Metric | Data |
|--------|------|
| GitHub | [electric-sql/electric](https://github.com/electric-sql/electric) |
| Stars | ~7,000 |
| License | Apache-2.0 |
| Language | Elixir (server) + TypeScript (client) |
| Last Updated | Active (daily commits) |
| Contributors | 50+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 85 | Postgres logical replication → Shape-based sync → Local SQLite. Sub-ms local reads, automatic conflict resolution (CRDTs). Elixir server handles millions of concurrent sync streams |
| E (Ecosystem) | 68 | 7k stars, $7M+ funding. Active but early community. Integrations with React, Expo, Capacitor. Local-first movement backing. Still finding product-market fit |
| M (Market) | 75 | Local-first is a growing architectural pattern. Google Docs-like collaboration for any app. Competes with Replicache, PowerSync, CRDT libraries. Still early but backed by strong thesis |
| C (Combo) | 70 | Powerful for specific use cases (offline-capable apps, collaborative tools). But adds significant complexity. Requires Postgres + ElectricSQL server + local SQLite. Not needed for simple SaaS |
| **Overall** | **75** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Turn any Postgres database into a real-time sync engine. Your app reads from local SQLite (instant), writes sync to Postgres automatically. Works offline, resolves conflicts, streams changes in real-time.

## Architecture Highlights
- **Shape-based sync** — Define "shapes" (subsets of data) to sync to clients
- **Postgres CDC** — Uses logical replication to capture changes
- **Elixir server** — High-concurrency sync coordinator (handles millions of streams)
- **Local SQLite** — Client-side embedded database for instant reads
- **CRDT conflict resolution** — Automatic merge of concurrent edits
- **HTTP API** — Shape streams via standard HTTP (cacheable by CDN)

## Key Modules
1. **Electric Server** (Elixir) — Postgres CDC + shape routing + sync protocol
2. **@electric-sql/client** — TypeScript client for shape subscriptions
3. **@electric-sql/react** — React hooks for live queries
4. **Shape API** — HTTP-based shape streams (GET /v1/shape/table)
5. **Examples** — React, Expo, Capacitor, Node.js integration examples

## Solo Dev Verdict
🟡 **Powerful but complex. Use for specific use cases only.** If you're building a collaborative tool, offline-capable app, or real-time dashboard, ElectricSQL is the cleanest solution. But for a typical Micro SaaS CRUD app, it's over-engineered. Watch this space — local-first might become standard architecture by 2027.

## Anti-Pattern Warning
- Significant complexity overhead (Postgres + Electric server + local SQLite)
- Elixir server = different tech stack for deployment/debugging
- Still evolving rapidly — API changes between versions
- Overkill for server-rendered or simple SaaS apps
- CRDT conflict resolution has inherent limitations for some data models
