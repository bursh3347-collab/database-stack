# Database & ORM Comparison

> Horizontal comparison of all database tools analyzed in this repository.
> Last updated: 2026-04-15

## ORM Comparison Matrix

| Feature | Prisma | Drizzle ORM | TypeORM | SQLAlchemy |
|---------|--------|-------------|---------|------------|
| **Stars** | 45.8k | 33.9k | 36.4k | ~9.8k |
| **Language** | TypeScript | TypeScript | TypeScript | Python |
| **License** | Apache-2.0 | Apache-2.0 | MIT | MIT |
| **Type Safety** | ⭐⭐⭐⭐⭐ (auto-generated) | ⭐⭐⭐⭐⭐ (inferred) | ⭐⭐⭐ (decorators) | ⭐⭐⭐⭐ (2.0+) |
| **SQL Control** | Low (abstracted) | High (SQL-like) | Medium | Very High |
| **Bundle Size** | Large (~7MB) | Tiny (~50KB) | Medium | N/A (Python) |
| **Edge/Serverless** | ⚠️ (Accelerate needed) | ✅ Native | ❌ | ❌ |
| **Migration Tool** | Prisma Migrate | Drizzle Kit | Built-in | Alembic |
| **Learning Curve** | Low | Medium | Medium | High |
| **Visual Studio** | Prisma Studio | Drizzle Studio | ❌ | ❌ |
| **Performance** | Good (Rust engine) | Excellent (zero overhead) | Moderate | Excellent |
| **Active Maintenance** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |

### Recommendation
- **New TypeScript project**: Drizzle ORM (lightweight, type-safe, edge-ready)
- **Rapid prototyping**: Prisma (best DX, auto-generated client)
- **NestJS enterprise**: TypeORM (ecosystem default)
- **Python backend**: SQLAlchemy (no competition)

## Database Platform Comparison

| Feature | Supabase | Neon | PlanetScale/Vitess |
|---------|----------|------|--------------------|
| **Stars** | 100.9k | ~15k | ~19.5k |
| **Database** | PostgreSQL | PostgreSQL | MySQL |
| **License** | Apache-2.0 | Apache-2.0 | Apache-2.0 |
| **Auth** | ✅ Built-in | ❌ | ❌ |
| **Realtime** | ✅ WebSocket | ❌ | ❌ |
| **Storage** | ✅ S3-compatible | ❌ | ❌ |
| **Edge Functions** | ✅ Deno | ❌ | ❌ |
| **Branching** | ⚠️ Limited | ✅ Native | ✅ Native |
| **Scale-to-Zero** | ❌ | ✅ | ❌ |
| **Vector/AI** | ✅ pgvector | ✅ pgvector | ❌ |
| **Free Tier** | ✅ Generous | ✅ | ❌ (removed) |
| **Self-Hosting** | ⚠️ Complex | ⚠️ Very Complex | ⚠️ Complex |
| **Best For** | Full-stack BaaS | Serverless Postgres | MySQL at scale |

### Recommendation
- **Solo developer / Micro SaaS**: Supabase (all-in-one BaaS)
- **Vercel + edge**: Neon (serverless Postgres, scale-to-zero)
- **MySQL legacy**: Vitess/PlanetScale

## TEMC Score Ranking

| Rank | Project | Overall | T | E | M | C |
|------|---------|---------|---|---|---|---|
| 1 | **Supabase** | **92** | 92 | 95 | 88 | 95 |
| 2 | **Drizzle ORM** | **87** | 90 | 82 | 85 | 92 |
| 3 | **Prisma** | **85** | 88 | 92 | 80 | 85 |
| 4 | **Neon** | **84** | 90 | 78 | 85 | 80 |
| 5 | **SQLAlchemy** | **74** | 92 | 85 | 75 | 55 |
| 6 | **TypeORM** | **68** | 72 | 78 | 65 | 60 |
| 7 | **Vitess** | **65** | 88 | 80 | 65 | 45 |
