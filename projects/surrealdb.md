# SurrealDB

> Multi-model database combining document, graph, relational, and vector capabilities in one system with its own query language (SurrealQL).

| Metric | Data |
|--------|------|
| GitHub | [surrealdb/surrealdb](https://github.com/surrealdb/surrealdb) |
| Stars | ~28,000 |
| License | BSL-1.1 (Business Source License) |
| Language | Rust |
| Last Updated | 2026-04 (active) |
| Contributors | 200+ |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Technology | 80 | Multi-model (document + graph + relational + vector) in single database. SurrealQL is powerful. Rust performance. Built-in auth, real-time subscriptions, embedded & distributed modes. But still maturing — v2.x era. |
| E Ecosystem | 72 | 28k⭐ strong community interest. SDKs for JS/TS, Python, Rust, Go, Java, .NET. But ecosystem much smaller than PostgreSQL. Limited ORM support. SurrealDB Cloud in beta. |
| M Market | 75 | Multi-model trend rising. Appeals to developers tired of managing multiple databases. But adoption still early-stage — few production case studies at scale. |
| C Combinability | 68 | JS/TS SDK available, can embed in serverless. But BSL-1.1 license limits commercial hosting. No Drizzle/Prisma integration. Learning new query language (SurrealQL) is friction. |
| **Composite** | **74** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value

SurrealDB's bet is that you shouldn't need PostgreSQL + Redis + Neo4j + Pinecone. One database handles documents (like MongoDB), graphs (like Neo4j), relations (like PostgreSQL), and vectors (like pgvector) — all queryable with one language. It's the **Swiss Army knife** approach to databases.

## Architecture Highlights

- **Multi-model engine** — document, graph, relational, and vector in one storage layer
- **SurrealQL** — SQL-like but with graph traversal (`->`, `<-`), record links, and futures
- **Built-in auth** — scope-based authentication, no external auth service needed
- **Real-time subscriptions** — LIVE SELECT for push-based updates
- **Embedded mode** — run in-process (like SQLite) or as distributed cluster
- **Schema flexibility** — schemaless, schemafull, or mixed per-table
- **Change feeds** — built-in CDC for event-driven architectures

## Key Extractable Patterns

1. **Multi-model data design** — when to use documents vs graph edges vs relational tables
2. **Record links** — typed references between records without JOINs
3. **Graph traversal in SQL** — `SELECT ->knows->person FROM user:tobie` pattern
4. **Embedded database** — single-binary deployment for edge/serverless

## Competitive Comparison

| | SurrealDB | PostgreSQL | MongoDB | Neo4j | FaunaDB |
|---|----------|------------|---------|-------|---------|
| Model | Multi-model | Relational (+ext) | Document | Graph | Multi-model |
| Query | SurrealQL | SQL | MQL | Cypher | FQL |
| Graph | ✅ Native | ❌ | ❌ | ✅ Best-in-class | ❌ |
| Vector | ✅ Built-in | ✅ pgvector | ✅ Atlas | ❌ | ❌ |
| License | BSL-1.1 | PostgreSQL | SSPL | GPL | Proprietary |
| Maturity | Early | Decades | Mature | Mature | Mature |

## ⚠️ License Warning

**BSL-1.1 (Business Source License)**: You can use SurrealDB freely for your own applications, but you **cannot offer it as a hosted database service** competing with SurrealDB Cloud. For solo dev building a SaaS product ON TOP of SurrealDB, this is fine. But if your product IS a database hosting service, this license blocks you.

## Solo Dev Verdict

**Fascinating technology but risky for production in 2026.** The multi-model vision is compelling — especially for AI applications that need document storage + vector search + graph relationships. But the ecosystem is thin (no Drizzle/Prisma), the license is restrictive (BSL), and production battle-testing is limited. **Watch closely but build on PostgreSQL/Supabase today.** Revisit when SurrealDB hits v3.0 with more production case studies.

⭐ **Extractable to code-base**: Multi-model schema design patterns, graph traversal query patterns.
