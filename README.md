![Stars](https://img.shields.io/github/stars/bursh3347-collab/database-stack?style=flat-square)
![License](https://img.shields.io/github/license/bursh3347-collab/database-stack?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/bursh3347-collab/database-stack?style=flat-square)

[English](README.md) | [中文](README_CN.md)

# 🗄️ database-stack

> ⭐ Maturity: **L1 Growing** — 7 projects analyzed, comparison complete, best practices started.

Best database tools and ORMs analyzed, compared, and scored using the **TEMC framework** (Technology · Ecosystem · Market Timing · Combinability). Deep architecture analysis and migration patterns from 7 high-star projects.

Part of the [Open Source Knowledge Restructuring Project](https://github.com/bursh3347-collab).

## 📈 Trending This Week (Updated: 2026-04-15)

| Rank | Project | Stars | Weekly Δ | Trend |
|------|---------|-------|----------|-------|
| 1 | [Supabase](https://github.com/supabase/supabase) | 100.9k | +800 | 🚀 |
| 2 | [Drizzle ORM](https://github.com/drizzle-team/drizzle-orm) | 33.9k | +500 | 🚀 |
| 3 | [Neon](https://github.com/neondatabase/neon) | 21.5k | +300 | ↑ |
| 4 | [Prisma](https://github.com/prisma/prisma) | 45.8k | +200 | → |
| 5 | [TypeORM](https://github.com/typeorm/typeorm) | 36.4k | +50 | → |
| 6 | [Vitess](https://github.com/vitessio/vitess) | 19.5k | +80 | → |
| 7 | [SQLAlchemy](https://github.com/sqlalchemy/sqlalchemy) | 9.8k | +30 | → |

> 🌟 Drizzle ORM is gaining fast — becoming the new TypeScript ORM standard. Neon picking up momentum with official Vercel partnership.

## 📊 Project Rankings (by TEMC Score)

| Rank | Project | Stars | TEMC | Language | Category |
|------|---------|-------|------|----------|----------|
| 1 | [Supabase](projects/supabase.md) | 100.9k | **92** | TypeScript | BaaS Platform |
| 2 | [Drizzle ORM](projects/drizzle-orm.md) | 33.9k | **87** | TypeScript | ORM |
| 3 | [Prisma](projects/prisma.md) | 45.8k | **85** | TypeScript | ORM |
| 4 | [Neon](projects/neon.md) | 21.5k | **84** | Rust | Serverless DB |
| 5 | [SQLAlchemy](projects/sqlalchemy.md) | ~9.8k | **74** | Python | ORM |
| 6 | [TypeORM](projects/typeorm.md) | 36.4k | **68** | TypeScript | ORM |
| 7 | [Vitess](projects/vitess.md) | ~19.5k | **65** | Go | MySQL Scaling |

> **TEMC** = Technology (25%) + Ecosystem (20%) + Market Timing (30%) + Combinability (25%)

## 📋 What's Inside

- [📊 ORM & Platform Comparison](comparison.md) — Side-by-side feature matrix
- [🏗️ Schema Design Patterns](best-practices/schema-design.md) — Patterns distilled from all 7 projects
- [🔄 Migration Strategies](best-practices/migration-patterns.md) — Safe migration workflows
- [🗺️ Technology Roadmap](roadmap.md) — Trends & predictions for database tooling

## 🏆 Solo Dev Verdict

**For a TypeScript Micro SaaS (solo developer):**

| Layer | Pick | Why |
|-------|------|-----|
| Database | **Supabase** | All-in-one BaaS — auth, storage, realtime included |
| Alt DB | **Neon** | If you need Vercel edge or branching workflows |
| ORM | **Drizzle ORM** | Lightweight, type-safe, edge-ready, fastest growing |
| Migrations | **Drizzle Kit** | Generate + push, zero friction |

## 📂 Structure

```
database-stack/
├── projects/              ← Individual project deep-dives (TEMC scored)
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
