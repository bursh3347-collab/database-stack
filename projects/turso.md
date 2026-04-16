# Turso / libSQL

> The Edge SQLite Platform — SQLite fork with server mode, replication, and edge deployment

| Metric | Data |
|--------|------|
| GitHub | [tursodatabase/libsql](https://github.com/tursodatabase/libsql) |
| Stars | ~12,000 |
| License | MIT |
| Language | Rust + C (SQLite core) |
| Last Updated | Active (daily commits) |
| Contributors | 200+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 90 | SQLite fork with: HTTP server mode, embedded replicas (local-first), vector search (vector columns), ALTER TABLE extensions, WebAssembly UDFs. Rust server (libsql-server) wrapping battle-tested SQLite |
| E (Ecosystem) | 80 | 12k stars, $30M+ funding (ChiefAI/Felicis). Growing adoption with Drizzle ORM + Next.js. Multi-language SDKs (JS/Python/Rust/Go/Java) |
| M (Market) | 85 | Edge database is the hottest category. Turso = SQLite + edge + sync. Competes with Cloudflare D1, PlanetScale (shut down free tier). Perfect timing for local-first movement |
| C (Combo) | 88 | Works with Drizzle ORM (native driver). Vercel/Fly.io/Cloudflare deployment. Embedded replicas = ultra-low latency reads. Free tier: 9GB storage, 500 databases |
| **Overall** | **86** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
SQLite's simplicity + cloud database features. Turso gives you edge-deployed SQLite with replication, so your database is as close to your users as your CDN. Embedded replicas mean sub-millisecond reads.

## Architecture Highlights
- **libSQL** — Open fork of SQLite with extensions (vector, WASM UDFs, ALTER TABLE)
- **libsql-server** — Rust-based server with HTTP API and WebSocket replication
- **Embedded replicas** — Sync a local SQLite copy for instant reads, async writes to primary
- **Multi-DB** — One account can have 500+ databases (database-per-tenant pattern)
- **Bottomless storage** — S3-backed infinite storage beyond local disk

## Key Modules
1. **libsql-server** — HTTP/WebSocket server, replication coordinator
2. **libsql** (Rust crate) — Core database engine (SQLite fork)
3. **libsql-ffi** — C FFI bindings for SQLite compatibility
4. **Embedded replicas** — Local-first sync protocol
5. **Vector search** — Built-in vector columns for AI/embedding use cases

## Solo Dev Verdict
🟢 **Top pick for edge-first SaaS.** Database-per-tenant with 500 free databases + embedded replicas = dream architecture for Micro SaaS. Drizzle ORM integration is seamless. The local-first sync model means your app works offline. Better than Neon for SQLite-loving solo devs.

## Anti-Pattern Warning
- SQLite limitations (no concurrent writes from multiple processes)
- Turso Cloud is the primary deployment target (self-hosting is complex)
- Smaller query feature set than PostgreSQL
- Vendor lock-in risk (though libSQL is MIT, Turso Cloud is proprietary)
