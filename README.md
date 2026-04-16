![Stars](https://img.shields.io/github/stars/bursh3347-collab/database-stack?style=flat-square)
![License](https://img.shields.io/github/license/bursh3347-collab/database-stack?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/bursh3347-collab/database-stack?style=flat-square)

[English](README.md) | [中文](README_CN.md)

# 🗄️ database-stack

> ⭐ Maturity: **L2 Growing** — 17 projects analyzed, 5 new deep-dives added, comparison complete, best practices expanding.

Best database tools, ORMs, and database engines analyzed, compared, and scored using the **TEMC framework** (Technology · Ecosystem · Market Timing · Combinability). Deep architecture analysis covering relational, distributed, columnar, multi-model, and vector databases.

Part of the [Open Source Knowledge Restructuring Project](https://github.com/bursh3347-collab).

## 📈 Trending This Week (Updated: 2026-04-16)

| Rank | Project | Stars | Weekly Δ | Trend |
|------|---------|-------|----------|-------|
| 1 | [Supabase](https://github.com/supabase/supabase) | 100.9k | +800 | 🚀 |
| 2 | [ClickHouse](https://github.com/ClickHouse/ClickHouse) | 38k | +400 | 🚀 |
| 3 | [TiDB](https://github.com/pingcap/tidb) | 38k | +200 | ↑ |
| 4 | [Drizzle ORM](https://github.com/drizzle-team/drizzle-orm) | 33.9k | +500 | 🚀 |
| 5 | [CockroachDB](https://github.com/cockroachdb/cockroach) | 30k | +150 | → |
| 6 | [SurrealDB](https://github.com/surrealdb/surrealdb) | 28k | +200 | ↑ |
| 7 | [Neon](https://github.com/neondatabase/neon) | 15k | +300 | 🚀 |
| 8 | [pgvector](https://github.com/pgvector/pgvector) | 13k | +250 | 🚀 |

> 🌟 pgvector surging with AI/RAG adoption. ClickHouse gaining momentum as analytics layer for AI applications.

## 📊 Project Rankings (by TEMC Score)

### 🏆 Tier 1: Must-Know (TEMC ≥ 85)

| Rank | Project | Stars | TEMC | Language | Category |
|------|---------|-------|------|----------|----------|
| 1 | [Supabase](projects/supabase.md) | 100.9k | **92** | TypeScript | BaaS Platform |
| 2 | [pgvector](projects/pgvector.md) | 13k | **88** | C | Vector Search 🆕 |
| 3 | [Drizzle ORM](projects/drizzle-orm.md) | 33.9k | **87** | TypeScript | ORM |
| 4 | [Prisma](projects/prisma.md) | 45.8k | **85** | TypeScript | ORM |

### 📈 Tier 2: Worth Studying (TEMC 70-84)

| Rank | Project | Stars | TEMC | Language | Category |
|------|---------|-------|------|----------|----------|
| 5 | [Neon](projects/neon.md) | 15k | **84** | Rust | Serverless DB |
| 6 | [ClickHouse](projects/clickhouse.md) | 38k | **80** | C++ | Columnar OLAP 🆕 |
| 7 | [SQLAlchemy](projects/sqlalchemy.md) | ~9.8k | **74** | Python | ORM |
| 8 | [SurrealDB](projects/surrealdb.md) | 28k | **74** | Rust | Multi-model DB 🆕 |
| 9 | [CockroachDB](projects/cockroachdb.md) | 30k | **74** | Go | Distributed SQL 🆕 |
| 10 | [TiDB](projects/tidb.md) | 38k | **73** | Go | Distributed SQL 🆕 |

### 📋 Tier 3: Reference (TEMC < 70)

| Rank | Project | Stars | TEMC | Language | Category |
|------|---------|-------|------|----------|----------|
| 11 | [TypeORM](projects/typeorm.md) | 36.4k | **68** | TypeScript | ORM |
| 12 | [Vitess](projects/vitess.md) | ~19.5k | **65** | Go | MySQL Scaling |

> **TEMC** = Technology (25%) + Ecosystem (20%) + Market Timing (30%) + Combinability (25%)

## 📋 What's Inside

- [📊 ORM & Platform Comparison](comparison.md) — Side-by-side feature matrix
- [🏗️ Schema Design Patterns](best-practices/schema-design.md) — Patterns distilled from all projects
- [🔄 Migration Strategies](best-practices/migration-patterns.md) — Safe migration workflows
- [🗺️ Technology Roadmap](roadmap.md) — Trends & predictions for database tooling

## 🗂️ Database Categories

| Category | Projects | Best Pick |
|----------|----------|-----------|
| **BaaS/Full-Stack** | Supabase, PocketBase | Supabase |
| **ORM/Query Builder** | Drizzle, Prisma, TypeORM, Kysely, SQLAlchemy | Drizzle ORM |
| **Vector Search** | pgvector | pgvector (on Supabase) |
| **Analytics/OLAP** | ClickHouse | ClickHouse Cloud |
| **Distributed SQL** | TiDB, CockroachDB, Vitess | CockroachDB Serverless |
| **Multi-model** | SurrealDB | Watch & wait |
| **Serverless** | Neon, Turso | Neon |
| **Edge/Local-first** | Turso/libSQL, ElectricSQL | Turso |
| **Caching** | Upstash Redis | Upstash |

## 🏆 Solo Dev Verdict

**For a TypeScript Micro SaaS (solo developer):**

| Layer | Pick | Why |
|-------|------|-----|
| Database | **Supabase** | All-in-one BaaS — auth, storage, realtime included |
| Alt DB | **Neon** | If you need Vercel edge or branching workflows |
| ORM | **Drizzle ORM** | Lightweight, type-safe, edge-ready, fastest growing |
| Migrations | **Drizzle Kit** | Generate + push, zero friction |
| Vector Search | **pgvector** | Already on Supabase, just enable the extension |
| Analytics | **ClickHouse Cloud** | When PG analytics queries get slow (10M+ rows) |
| Caching | **Upstash Redis** | Serverless Redis, HTTP-based, edge-ready |

## 📂 Structure

```
database-stack/
├── projects/              ← 17 individual project deep-dives (TEMC scored)
├── best-practices/        ← Cross-project patterns
├── code/                  ← Extractable code (coming soon)
├── comparison.md          ← Horizontal comparison tables
├── roadmap.md             ← Technology trends & predictions
├── CONTRIBUTING.md
├── SOURCES.md
└── README.md
```

## 📝 How to Use

1. **Compare** — Start with [comparison.md](comparison.md) to understand the landscape
2. **Deep-dive** — Read the analysis for your chosen tool in `projects/`
3. **Apply** — Use patterns from `best-practices/` in your project
4. **Stay current** — Check [roadmap.md](roadmap.md) for where the ecosystem is heading

## License

Analysis content: MIT. Each referenced project has its own license — see [SOURCES.md](SOURCES.md).
