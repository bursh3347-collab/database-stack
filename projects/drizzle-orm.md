# Drizzle ORM

> Lightweight TypeScript ORM with SQL-like syntax, zero dependencies, and serverless-ready design.

| Metric | Data |
|--------|------|
| GitHub | [drizzle-team/drizzle-orm](https://github.com/drizzle-team/drizzle-orm) |
| Stars | 33,870 |
| Forks | 1,339 |
| License | Apache-2.0 |
| Language | TypeScript |
| Last Updated | 2026-04-15 |
| Contributors | 400+ |
| Open Issues | 1,705 |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Tech | 90 | SQL-like syntax, zero overhead, edge/serverless ready, excellent type inference |
| E Ecosystem | 82 | 34k stars, fast-growing, Drizzle Kit for migrations, but younger ecosystem than Prisma |
| M Market | 85 | Rising fast as lightweight Prisma alternative, preferred for serverless/edge |
| C Combo | 92 | Already used in天子's saas-starter (Next.js 15), perfect stack match |
| **Overall** | **87** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Drizzle provides SQL-level control with TypeScript type safety. Unlike Prisma's abstraction, Drizzle's queries look like SQL — "If you know SQL, you know Drizzle." Zero runtime overhead, perfect for edge/serverless.

## Architecture Highlights
- **SQL-like API**: Queries map directly to SQL, no magic
- **Zero dependencies**: Tiny bundle, edge-ready
- **Drizzle Kit**: CLI for migrations and schema introspection
- **Drizzle Studio**: Web-based data browser
- **Multi-dialect**: PostgreSQL, MySQL, SQLite with dialect-specific features

## Key Modules
1. **drizzle-orm** (Medium) — Core ORM with type-safe query builder
2. **drizzle-kit** (Medium) — Migration CLI + schema introspection
3. **drizzle-studio** (Small) — Web data browser
4. **Dialect drivers** (Small each) — pg/mysql2/better-sqlite3 adapters

## Extractable Components
- Schema definition pattern (TypeScript-native) → code-base/database/drizzle/
- Migration generation workflow → code-base/database/migrations/
- Edge-ready DB connection pattern → code-base/deploy/edge-db/

⭐ Universal Code Candidate: Edge/serverless database connection pattern

## Why It Might NOT Be Worth It
- Younger ecosystem, fewer third-party tools/plugins
- 1,705 open issues suggest growing pains
- Less mature migration tooling compared to Prisma Migrate
- Documentation gaps for advanced use cases
- Rapid API changes between versions

## 天子点评
已替代 Prisma 成为天子首选 ORM。轻量 + Edge-ready + SQL-like，saas-starter 已集成。增速惊人，未来可期。
