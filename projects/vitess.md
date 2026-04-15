# Vitess (PlanetScale)

> MySQL horizontal scaling system from YouTube, powering PlanetScale's serverless MySQL platform.

| Metric | Data |
|--------|------|
| GitHub | [vitessio/vitess](https://github.com/vitessio/vitess) |
| Stars | ~19,500 |
| Forks | ~2,500 |
| License | Apache-2.0 |
| Language | Go |
| Last Updated | 2026-04 (very active) |
| Contributors | 600+ |
| CNCF | Graduated Project |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Tech | 88 | Battle-tested at YouTube scale, online DDL, horizontal sharding, VReplication |
| E Ecosystem | 80 | CNCF graduated, PlanetScale commercial, but MySQL-focused (Postgres dominant in new projects) |
| M Market | 65 | MySQL sharding niche, new projects prefer Postgres; PlanetScale free tier removed |
| C Combo | 45 | MySQL (not in天子基准栈), Go (not primary language), overkill for one-person company |
| **Overall** | **65** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Vitess solves MySQL horizontal scaling — the exact problem YouTube had. Online DDL (schema changes without downtime) and transparent sharding are its superpowers. PlanetScale commercialized it as serverless MySQL.

## Architecture Highlights
- **VTGate**: Query router + connection pooler
- **VTTablet**: Per-shard MySQL manager
- **VReplication**: Change data capture + resharding
- **Online DDL**: Zero-downtime schema migrations
- **Topology Service**: Cluster metadata (etcd/ZooKeeper)

## Key Modules
1. **VTGate** (Large) — SQL-aware proxy/router
2. **VTTablet** (Large) — Tablet management
3. **VReplication** (Large) — Streaming replication
4. **Online DDL** (Medium) — Schema migration engine

## Extractable Components
- Online DDL pattern → code-base/database/migrations/ (concept reference)
- Connection pooling patterns → code-base/database/pooling/

## Why It Might NOT Be Worth It
- MySQL-only (天子栈 = Postgres)
- Massive complexity for solo developer
- PlanetScale removed free tier
- Go codebase, not TypeScript
- Overkill — designed for YouTube-scale, not Micro SaaS

## 天子点评
YouTube 级基建，学习架构思想（Online DDL、分片）即可。一人公司用 Supabase 就够了，不需要这个级别。
