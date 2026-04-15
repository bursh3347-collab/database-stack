# 🗺️ Database & ORM Technology Roadmap

> Last updated: 2026-04-15

## 🟢 当前主流

| 技术 | 地位 | 一人公司适用度 |
|------|------|----------------|
| **Supabase** | BaaS 开源王者，100k⭐ | ⭐⭐⭐⭐⭐ 首选 |
| **Drizzle ORM** | TypeScript ORM 新标准 | ⭐⭐⭐⭐⭐ 首选 |
| **Prisma** | TypeScript ORM 老牌王者 | ⭐⭐⭐⭐ 稳妥 |
| **PostgreSQL** | 关系型数据库事实标准 | ⭐⭐⭐⭐⭐ 基础 |

## 🚀 崛起方向

### 1. Edge/Serverless 数据库
- **Neon**（21.5k⭐）：Serverless Postgres + 分支 + Scale-to-Zero
- **Turso**（libSQL）：SQLite 的分布式版本，延迟极低
- **PlanetScale**：Serverless MySQL（Vitess），但已移除免费层
- **趋势**：数据库计算分离 + 按需缩放成为标配

### 2. AI-Native 数据库特性
- **pgvector**：Postgres 原生向量搜索（Supabase 已集成）
- **pgai**：Postgres 内直接调用 LLM
- **Lantern / pgembedding**：向量索引优化
- **趋势**：AI 特性从独立向量数据库回归传统数据库

### 3. ORM 轻量化 + Edge-Ready
- **Drizzle** 增速超越 Prisma（周增 +500 vs +200）
- **Kysely**：纯 TypeScript 查询构建器（更轻量）
- **趋势**：从重抽象 ORM → SQL-like 轻量查询构建器

## ↓ 衰退方向

| 技术 | 衰退原因 |
|------|----------|
| **TypeORM** | 维护放缓，类型安全不如 Prisma/Drizzle |
| **Sequelize** | Node.js 老一代 ORM，社区萎缩 |
| **MongoDB/Mongoose** | 新项目回归 SQL，NoSQL 热潮消退 |
| **PlanetScale** | 移除免费层，开发者流失 |

## 🔮 6-12 月预测

1. **Drizzle 将超越 Prisma 成为 Next.js 生态默认 ORM**（置信度 75%）
2. **pgvector 将成为中小型 RAG 应用的默认向量存储**（置信度 80%）
3. **至少 1 家 Edge Database 公司获得 $50M+ 融资**（置信度 70%）
4. **Prisma 将推出 Edge-compatible 版本追赶 Drizzle**（置信度 65%）

## 💡 对一人公司的影响

**核心建议**：
- **坚持 Supabase + Drizzle 组合**，这是目前一人公司数据层的最优解
- **关注 pgvector**，AI 应用直接在 Supabase 内做向量搜索，无需额外服务
- **不要追新**，Turso/PlanetScale 等有趣但 Supabase 已经够用
- **学习 SQL**，ORM 在变轻，SQL 知识越来越重要

> 天子判断：数据层已经稳定，不需要频繁切换。把精力放在产品层而不是基建层。
