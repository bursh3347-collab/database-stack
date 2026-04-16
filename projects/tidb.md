# TiDB

> MySQL-compatible distributed SQL database with horizontal scalability — HTAP (Hybrid Transactional/Analytical Processing) in one system.

| Metric | Data |
|--------|------|
| GitHub | [pingcap/tidb](https://github.com/pingcap/tidb) |
| Stars | ~38,000 |
| License | Apache-2.0 |
| Language | Go |
| Last Updated | 2026-04 (very active, daily commits) |
| Contributors | 900+ |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Technology | 88 | Raft-based distributed consensus, TiKV storage engine (CNCF graduated), TiFlash columnar engine for analytics, MySQL wire protocol compatible. Online DDL, distributed transactions with snapshot isolation. |
| E Ecosystem | 80 | 38k⭐, PingCAP raised $370M+, CNCF project. Used by 3000+ companies globally. TiDB Cloud managed service available. Strong in Asia-Pacific market. |
| M Market | 72 | Enterprise-focused distributed database. Overkill for most solo dev projects. Market timing good for companies outgrowing single-node MySQL. |
| C Combinability | 55 | Go-based, MySQL compatible (can use existing MySQL ORMs). But heavy infrastructure footprint (TiDB + TiKV + PD minimum). Not in TypeScript ecosystem. TiDB Serverless reduces this barrier. |
| **Composite** | **73** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value

TiDB solves the "I've outgrown MySQL but can't afford downtime for migration" problem. It speaks MySQL wire protocol, so existing apps work unchanged, but scales horizontally like a distributed system. The HTAP capability (TiFlash) means you don't need a separate analytics database.

## Architecture Highlights

- **Three-layer architecture** — TiDB (SQL layer) + TiKV (row storage) + TiFlash (columnar storage)
- **Raft consensus** — every data region replicated across 3+ nodes automatically
- **MySQL compatibility** — connect with any MySQL driver, most MySQL syntax works
- **Online DDL** — `ALTER TABLE` without locking, critical for zero-downtime deployments
- **HTAP** — TiFlash provides columnar replicas for real-time analytics without ETL
- **TiDB Serverless** — fully managed, pay-per-request option (free tier: 25 GiB storage)

## Key Extractable Patterns

1. **HTAP architecture** — transactional + analytical in one database, no ETL pipeline needed
2. **Horizontal sharding** — automatic data distribution across nodes without application changes
3. **Online schema change** — DDL operations that don't block reads or writes
4. **Multi-region deployment** — geo-distributed data placement for compliance and latency

## Competitive Comparison

| | TiDB | CockroachDB | PlanetScale | Aurora | Vitess |
|---|------|-------------|-------------|--------|--------|
| Protocol | MySQL | PostgreSQL | MySQL | MySQL/PG | MySQL |
| HTAP | ✅ TiFlash | ❌ | ❌ | Limited | ❌ |
| Serverless | ✅ | ✅ | ✅ | ✅ | ❌ |
| Open Source | Full (Apache-2.0) | Core (BSL) | ❌ (Vitess only) | ❌ | ✅ |
| Best For | MySQL at scale + analytics | PG at scale | MySQL serverless | AWS-native | MySQL sharding |

## Solo Dev Verdict

**Interesting to study but overkill for most solo projects.** TiDB Serverless with its free tier makes it accessible for experimentation. The real value is understanding HTAP architecture — when to use row stores vs columnar stores. If you're building for the MySQL ecosystem (rare for new TypeScript projects), TiDB is the best scale-out path. For PG-based stacks (Supabase/Neon/Drizzle), stick with the PG ecosystem.

⭐ **Extractable to code-base**: HTAP design patterns, online DDL strategies, Raft consensus concepts.
