# TypeORM

> Classic TypeScript/JavaScript ORM supporting Active Record and Data Mapper patterns for 7+ databases.

| Metric | Data |
|--------|------|
| GitHub | [typeorm/typeorm](https://github.com/typeorm/typeorm) |
| Stars | 36,443 |
| Forks | 6,512 |
| License | MIT |
| Language | TypeScript |
| Last Updated | 2026-04-15 |
| Contributors | 700+ |
| Open Issues | 524 |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Tech | 72 | Mature ORM, decorator-based, but falling behind in modern TS features and type safety |
| E Ecosystem | 78 | 36k stars, large adoption base, but community momentum shifting to Prisma/Drizzle |
| M Market | 65 | Legacy projects still use it, but new projects rarely choose TypeORM over Prisma/Drizzle |
| C Combo | 60 | Decorator-heavy approach conflicts with modern React/Next.js patterns |
| **Overall** | **68** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
TypeORM is the NestJS-ecosystem default ORM, supporting both Active Record and Data Mapper patterns. Strong for enterprise Java/C#-style architectures.

## Architecture Highlights
- **Decorator-based models**: @Entity, @Column, @OneToMany
- **Dual patterns**: Active Record + Data Mapper
- **Migration system**: Auto-generate + manual migrations
- **Query Builder**: Fluent query construction
- **Multi-database**: 7+ databases supported

## Key Modules
1. **Entity Manager** (Large) — Core ORM operations
2. **Query Builder** (Large) — Fluent SQL construction
3. **Migration Runner** (Medium) — Schema migration system
4. **Connection Manager** (Medium) — Multi-database connection handling

## Why It Might NOT Be Worth It
- Type safety weaker than Prisma/Drizzle
- Decorator syntax requires experimentalDecorators
- Maintenance pace slowed significantly
- Known memory leak issues in long-running processes
- Community migration away accelerating
