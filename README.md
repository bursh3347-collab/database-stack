# 🗄️ database-stack

> ⭐ Maturity: **L1 Growing** — 7 projects analyzed, comparison complete, best practices started.

Extracted best practices, architecture patterns, and deep analysis from 7 high-star database and ORM projects on GitHub.

## 📈 What's Inside

### Projects Analyzed (7)
| Project | Stars | TEMC | Language | Category |
|---------|-------|------|----------|----------|
| [Supabase](projects/supabase.md) | 100.9k | **92** | TypeScript | BaaS Platform |
| [Drizzle ORM](projects/drizzle-orm.md) | 33.9k | **87** | TypeScript | ORM |
| [Prisma](projects/prisma.md) | 45.8k | **85** | TypeScript | ORM |
| [Neon](projects/neon.md) | ~15k | **84** | Rust | Serverless DB |
| [SQLAlchemy](projects/sqlalchemy.md) | ~9.8k | **74** | Python | ORM |
| [TypeORM](projects/typeorm.md) | 36.4k | **68** | TypeScript | ORM |
| [Vitess](projects/vitess.md) | ~19.5k | **65** | Go | MySQL Scaling |

### Comparison & Best Practices
- [📊 ORM & Platform Comparison](comparison.md) — Side-by-side feature matrix
- [🏗️ Schema Design](best-practices/schema-design.md) — Schema patterns from all 7 projects
- [🔄 Migration Patterns](best-practices/migration-patterns.md) — Safe migration strategies

## 🎯 Quick Recommendation

**For a TypeScript Micro SaaS (solo developer):**
1. **Database**: Supabase (all-in-one BaaS) or Neon (if Vercel edge)
2. **ORM**: Drizzle ORM (lightweight, type-safe, edge-ready)
3. **Migrations**: Drizzle Kit (generate + push)

## 🏗️ Repository Structure
```
database-stack/
├── README.md              ← You are here
├── projects/              ← Individual project analyses (TEMC scored)
├── best-practices/        ← Cross-project patterns
├── code/                  ← Extractable code (coming soon)
├── comparison.md          ← Horizontal comparison tables
└── SOURCES.md             ← All source links + licenses
```

## 📝 How to Use
1. Start with [comparison.md](comparison.md) to understand the landscape
2. Read the project analysis for your chosen tool
3. Apply patterns from best-practices/ in your project

## License
This repository contains analysis and extracted patterns. Each referenced project has its own license — see [SOURCES.md](SOURCES.md).
