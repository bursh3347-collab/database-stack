# Kysely

> The type-safe SQL query builder for TypeScript — Write SQL, get types

| Metric | Data |
|--------|------|
| GitHub | [kysely-org/kysely](https://github.com/kysely-org/kysely) |
| Stars | ~12,000 |
| License | MIT |
| Language | TypeScript |
| Last Updated | Active (v0.28.16) |
| Contributors | 80+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 90 | Full type safety for raw SQL queries without codegen. Supports Postgres/MySQL/SQLite/MSSQL. Plugin system for custom dialects. Zero runtime overhead — types are compile-time only |
| E (Ecosystem) | 75 | 12k stars, growing steadily. Official plugins for Postgres, MySQL, SQLite. Community dialects for PlanetScale, D1, Turso, SingleStore. Smaller ecosystem than Prisma but deeper SQL control |
| M (Market) | 78 | Sweet spot between raw SQL and heavy ORMs. Developers fleeing Prisma's abstraction love Kysely. Edge/serverless compatible (tiny bundle). Growing as the "serious" alternative |
| C (Combo) | 88 | Perfect complement to Drizzle (different philosophy). Works with Neon, Turso, Supabase. Zero-overhead = ideal for serverless. Multi-DB support means database-agnostic code |
| **Overall** | **83** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Write SQL the way you think, but with full TypeScript autocompletion and type checking. Kysely doesn't abstract away SQL — it makes SQL type-safe. If you know SQL, you know Kysely.

## Architecture Highlights
- **Zero runtime overhead** — All type checking at compile time, no runtime schema
- **SQL-first** — API mirrors SQL syntax: `db.selectFrom('users').where('id', '=', 1)`
- **Plugin system** — Extend with custom dialects, transformers, query hooks
- **Multi-database** — Same API for Postgres, MySQL, SQLite, MSSQL
- **Migration toolkit** — Built-in migration system with TypeScript migrations
- Supports: CJS + ESM, Deno, Bun, Cloudflare Workers, browsers

## Key Modules
1. **Query Builder** — SELECT/INSERT/UPDATE/DELETE with full type inference
2. **Schema Builder** — CREATE TABLE/ALTER TABLE with typed migrations
3. **Dialect System** — Postgres/MySQL/SQLite/MSSQL drivers + community dialects
4. **Plugin System** — Query transformers (camelCase, soft-delete, etc.)
5. **Helpers** — Database-specific helpers (postgres jsonb, mysql spatial, etc.)

## Solo Dev Verdict
🟢 **Best choice for SQL-loving TypeScript devs.** If Prisma feels too magical and Drizzle too opinionated, Kysely is your tool. You write actual SQL patterns with full type safety. Tiny bundle = perfect for edge/serverless. The Turso/D1 community dialects make it edge-database ready.

## Anti-Pattern Warning
- Steeper learning curve than Prisma (you need to know SQL)
- No auto-generated client like Prisma — you define types manually or use codegen tools
- Smaller plugin ecosystem than Prisma/Drizzle
- Still v0.x — API may have breaking changes (though stable in practice)
