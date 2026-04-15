[English](README.md) | [中文](README_CN.md)

# 🗄️ database-stack

> ⭐ 成熟度: **L1 成长期** — 已分析 7 个项目，对比表完成，最佳实践进行中。

对 GitHub 上顶级数据库工具与 ORM 的深度拆解、横向对比与 **TEMC 评分**（技术 · 生态 · 时机 · 组合）。涵盖架构分析与数据库迁移模式。

属于 [GitHub 开源知识重组工程](https://github.com/bursh3347-collab) 的一部分。

## 📈 本分类飙升榜（最近更新：2026-04-15）

| 排名 | 项目 | 总Stars | 周增 | 趋势 |
|------|------|---------|------|------|
| 1 | [Supabase](https://github.com/supabase/supabase) | 100.9k | +800 | 🚀 |
| 2 | [Drizzle ORM](https://github.com/drizzle-team/drizzle-orm) | 33.9k | +500 | 🚀 |
| 3 | [Neon](https://github.com/neondatabase/neon) | 21.5k | +300 | ↑ |
| 4 | [Prisma](https://github.com/prisma/prisma) | 45.8k | +200 | → |
| 5 | [TypeORM](https://github.com/typeorm/typeorm) | 36.4k | +50 | → |
| 6 | [Vitess](https://github.com/vitessio/vitess) | 19.5k | +80 | → |
| 7 | [SQLAlchemy](https://github.com/sqlalchemy/sqlalchemy) | 9.8k | +30 | → |

> 🌟 Drizzle ORM 增速最快，正在成为 TypeScript ORM 新标准。Neon 势头强劲，Vercel 官方合作加速。

## 📊 项目排名（按 TEMC 评分）

| 排名 | 项目 | Stars | TEMC | 语言 | 分类 |
|------|------|-------|------|------|------|
| 1 | [Supabase](projects/supabase.md) | 100.9k | **92** | TypeScript | BaaS 平台 |
| 2 | [Drizzle ORM](projects/drizzle-orm.md) | 33.9k | **87** | TypeScript | ORM |
| 3 | [Prisma](projects/prisma.md) | 45.8k | **85** | TypeScript | ORM |
| 4 | [Neon](projects/neon.md) | 21.5k | **84** | Rust | Serverless 数据库 |
| 5 | [SQLAlchemy](projects/sqlalchemy.md) | ~9.8k | **74** | Python | ORM |
| 6 | [TypeORM](projects/typeorm.md) | 36.4k | **68** | TypeScript | ORM |
| 7 | [Vitess](projects/vitess.md) | ~19.5k | **65** | Go | MySQL 扩展 |

> **TEMC** = 技术分(25%) + 生态分(20%) + 时机分(30%) + 组合分(25%)

## 📋 仓库内容

- [📊 ORM 与平台横向对比](comparison.md) — 功能矩阵一览
- [🏗️ Schema 设计模式](best-practices/schema-design.md) — 从 7 个项目中提炼的模式
- [🔄 迁移策略](best-practices/migration-patterns.md) — 安全的数据库迁移工作流
- [🗺️ 技术路线图](roadmap.md) — 数据库工具的趋势与预测

## 🏆 天子点评（一人公司推荐）

**TypeScript Micro SaaS 独立开发者推荐方案：**

| 层次 | 推荐 | 理由 |
|------|------|------|
| 数据库 | **Supabase** | 一站式 BaaS — 认证、存储、实时推送全包 |
| 备选数据库 | **Neon** | 需要 Vercel Edge 或分支工作流时使用 |
| ORM | **Drizzle ORM** | 轻量、类型安全、Edge 就绪、增速最快 |
| 迁移工具 | **Drizzle Kit** | 生成 + 推送，零摩擦 |

## 📂 仓库结构

```
database-stack/
├── projects/              ← 单个项目深度分析（含 TEMC 评分）
├── best-practices/        ← 跨项目最佳实践
├── code/                  ← 可提取代码（即将上线）
├── comparison.md          ← 横向对比表
├── roadmap.md             ← 技术趋势与预测
├── CONTRIBUTING.md
├── SOURCES.md
└── README.md
```

## 📝 使用指南

1. **对比** — 从 [comparison.md](comparison.md) 开始了解全景
2. **深入** — 阅读 `projects/` 中你选择的工具分析
3. **实践** — 将 `best-practices/` 中的模式应用到你的项目
4. **跟进** — 查看 [roadmap.md](roadmap.md) 了解生态发展方向

## License

分析内容采用 MIT 协议。各项目保留其原始开源协议 — 详见 [SOURCES.md](SOURCES.md)。
