# Prisma

> Next-generation TypeScript ORM with auto-generated type-safe client, visual data browser, and seamless migrations.

| Metric | Data |
|--------|------|
| GitHub | [prisma/prisma](https://github.com/prisma/prisma) |
| Stars | 45,763 |
| Forks | 2,175 |
| License | Apache-2.0 |
| Language | TypeScript |
| Last Updated | 2026-04-15 |
| Contributors | 600+ |
| Open Issues | 2,557 |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Tech | 88 | Auto-generated type-safe client, Prisma Schema Language, excellent DX, supports 7+ databases |
| E Ecosystem | 92 | 45k+ stars, massive adoption (Next.js default ORM), rich plugin ecosystem, Prisma Data Platform |
| M Market | 80 | Dominant in TypeScript ecosystem, but heavy abstraction may not suit all use cases |
| C Combo | 85 | Perfect match with Next.js + Supabase/Postgres stack, direct integration with天子基准栈 |
| **Overall** | **85** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Prisma eliminates the impedance mismatch between application code and database. Its Schema-first approach with auto-generated client provides the best TypeScript DX for database access. Prisma Studio offers visual data browsing.

## Architecture Highlights
- **Prisma Schema Language (PSL)**: Declarative data modeling
- **Prisma Client**: Auto-generated, type-safe query builder
- **Prisma Migrate**: Declarative migration system
- **Prisma Studio**: Visual database browser
- **Query Engine**: Rust-based query engine for performance

## Key Modules
1. **@prisma/client** (Large) — Auto-generated type-safe DB client
2. **prisma migrate** (Medium) — Schema migration engine
3. **prisma studio** (Medium) — Visual data browser GUI
4. **Query Engine** (Large) — Rust-based SQL generation + execution
5. **Schema Parser** (Medium) — PSL parser and validator

## Extractable Components
- Schema-first design pattern → code-base/database/schema-first/
- Migration workflow → code-base/database/migrations/
- Type-safe query builder pattern → reference architecture

⭐ Universal Code Candidate: Schema-first migration pattern

## Why It Might NOT Be Worth It
- Heavy abstraction layer adds overhead (~15-30% slower than raw SQL)
- Schema language is proprietary (not standard SQL)
- Large bundle size for serverless/edge deployments
- Complex queries often require raw SQL escape hatches
- Vendor lock-in risk with Prisma Cloud/Accelerate

## 天子点评
生态最强但渐重。如果不需要 Edge 部署，仍是稳妥之选。但 Drizzle 正在全面超越，新项目建议直接用 Drizzle。
