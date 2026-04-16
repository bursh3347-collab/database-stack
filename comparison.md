# Database & ORM Comparison

> Horizontal comparison of all database tools analyzed in this repository.
> Last updated: 2026-04-16

## ORM / Query Builder Comparison

| Feature | Prisma | Drizzle ORM | Kysely | TypeORM | SQLAlchemy |
|---------|--------|-------------|--------|---------|------------|
| **Stars** | 45.8k | 33.9k | 12k | 36.4k | ~9.8k |
| **Language** | TypeScript | TypeScript | TypeScript | TypeScript | Python |
| **License** | Apache-2.0 | Apache-2.0 | MIT | MIT | MIT |
| **Type Safety** | ⭐⭐⭐⭐⭐ (generated) | ⭐⭐⭐⭐⭐ (inferred) | ⭐⭐⭐⭐⭐ (inferred) | ⭐⭐⭐ (decorators) | ⭐⭐⭐⭐ (2.0+) |
| **SQL Control** | Low (abstracted) | High (SQL-like) | Very High (raw SQL) | Medium | Very High |
| **Bundle Size** | Large (~7MB) | Tiny (~50KB) | Tiny (~30KB) | Medium | N/A |
| **Edge/Serverless** | ⚠️ Accelerate | ✅ Native | ✅ Native | ❌ | ❌ |
| **Multi-DB** | Postgres/MySQL/SQLite/MongoDB | Postgres/MySQL/SQLite | Postgres/MySQL/SQLite/MSSQL | Many | Many |
| **Migration** | Prisma Migrate | Drizzle Kit | Built-in | Built-in | Alembic |
| **Visual Studio** | Prisma Studio | Drizzle Studio | ❌ | ❌ | ❌ |
| **Performance** | Good (Rust engine) | Excellent (zero overhead) | Excellent (zero overhead) | Moderate | Excellent |

### ORM Recommendation
- **New TypeScript project**: Drizzle ORM (lightweight, type-safe, edge-ready)
- **SQL purist**: Kysely (write actual SQL with types)
- **Rapid prototyping**: Prisma (best DX, auto-generated client)
- **NestJS enterprise**: TypeORM (ecosystem default)
- **Python backend**: SQLAlchemy (no competition)

## Database Platform Comparison

| Feature | Supabase | Neon | Turso | PocketBase | Upstash Redis | ElectricSQL | Vitess |
|---------|----------|------|-------|------------|---------------|-------------|--------|
| **Stars** | 100.9k | ~15k | ~12k | ~43k | ~2k (SDK) | ~7k | ~19.5k |
| **Database** | PostgreSQL | PostgreSQL | SQLite (libSQL) | SQLite | Redis | Postgres→SQLite | MySQL |
| **License** | Apache-2.0 | Apache-2.0 | MIT | MIT | MIT (SDK) | Apache-2.0 | Apache-2.0 |
| **Auth** | ✅ Built-in | ❌ | ❌ | ✅ Built-in | ❌ | ❌ | ❌ |
| **Realtime** | ✅ WebSocket | ❌ | ❌ | ✅ SSE | ❌ | ✅ Shape sync | ❌ |
| **File Storage** | ✅ S3 | ❌ | ❌ | ✅ Local/S3 | ❌ | ❌ | ❌ |
| **Edge Deploy** | ⚠️ | ✅ | ✅ Embedded | ❌ | ✅ HTTP | ✅ Local-first | ❌ |
| **Scale-to-Zero** | ❌ | ✅ | ✅ | N/A (self-host) | ✅ | ❌ | ❌ |
| **Vector/AI** | ✅ pgvector | ✅ pgvector | ✅ Built-in | ❌ | ✅ Upstash Vector | ❌ | ❌ |
| **Free Tier** | ✅ Generous | ✅ | ✅ 9GB/500DBs | ✅ Self-host | ✅ 10K/day | ✅ Self-host | ❌ |
| **Self-Hosting** | ⚠️ Complex | ⚠️ Complex | ⚠️ Complex | ✅ 1 file | ❌ (SaaS) | ✅ Docker | ⚠️ Complex |
| **Best For** | Full-stack BaaS | Serverless PG | Edge SQLite | MVP/prototype | Serverless cache | Local-first apps | MySQL scale |

### Database Recommendation
- **Solo dev full-stack**: Supabase (all-in-one BaaS)
- **Vercel + edge**: Neon (serverless PG) or Turso (edge SQLite)
- **5-minute MVP**: PocketBase (single file, done)
- **Serverless caching**: Upstash Redis (pay-per-request)
- **Offline-capable app**: ElectricSQL (Postgres→local sync)
- **MySQL at scale**: Vitess

## TEMC Score Ranking

| Rank | Project | Overall | T | E | M | C |
|------|---------|---------|---|---|---|---|
| 1 | **Supabase** | **92** | 92 | 95 | 88 | 95 |
| 2 | **Drizzle ORM** | **87** | 90 | 82 | 85 | 92 |
| 3 | **Turso/libSQL** | **86** | 90 | 80 | 85 | 88 |
| 4 | **Prisma** | **85** | 88 | 92 | 80 | 85 |
| 5 | **Neon** | **84** | 90 | 78 | 85 | 80 |
| 6 | **Kysely** | **83** | 90 | 75 | 78 | 88 |
| 7 | **Upstash Redis** | **82** | 78 | 72 | 82 | 90 |
| 8 | **PocketBase** | **80** | 82 | 85 | 80 | 72 |
| 9 | **ElectricSQL** | **75** | 85 | 68 | 75 | 70 |
| 10 | **SQLAlchemy** | **74** | 92 | 85 | 75 | 55 |
| 11 | **TypeORM** | **68** | 72 | 78 | 65 | 60 |
| 12 | **Vitess** | **65** | 88 | 80 | 65 | 45 |
