# CockroachDB

> Distributed SQL database built for cloud-native applications — survives any failure, scales without limits, PostgreSQL compatible.

| Metric | Data |
|--------|------|
| GitHub | [cockroachdb/cockroach](https://github.com/cockroachdb/cockroach) |
| Stars | ~30,000 |
| License | BSL-1.1 (core) / Apache-2.0 (some components) |
| Language | Go |
| Last Updated | 2026-04 (very active, daily commits) |
| Contributors | 600+ |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Technology | 90 | Google Spanner-inspired architecture. Serializable isolation (strongest consistency). Geo-partitioning for data locality. Automatic rebalancing. Online schema changes. PostgreSQL wire protocol compatible. |
| E Ecosystem | 78 | 30k⭐, Cockroach Labs raised $600M+. Used by major enterprises (DoorDash, Netflix, Bose). CockroachDB Serverless available. PG compatibility means existing PG tools work. |
| M Market | 70 | Enterprise-focused distributed database. CockroachDB Serverless makes it accessible but competes directly with Neon/Supabase for developer mindshare. Not the default choice for new projects. |
| C Combinability | 58 | PG-compatible so Drizzle/Prisma technically work. But distributed nature adds complexity (no foreign keys across partitions, different performance characteristics). Serverless tier has generous free quota. |
| **Composite** | **74** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value

CockroachDB answers: "What if PostgreSQL could survive any failure and scale to any size without manual sharding?" It's the database you graduate to when single-node PostgreSQL can't meet your availability or scale requirements — and you want to keep using SQL.

## Architecture Highlights

- **Raft consensus** — every piece of data replicated across 3+ nodes automatically
- **Range-based sharding** — data automatically split and distributed as it grows
- **Serializable isolation** — strongest transaction isolation level, no anomalies
- **Geo-partitioning** — pin data to specific regions for compliance (GDPR, data sovereignty)
- **Online schema changes** — zero-downtime DDL operations
- **Multi-active availability** — every node can serve reads AND writes (no primary/replica split)
- **PostgreSQL wire protocol** — connect with `psql`, PG drivers, existing ORMs

## Key Extractable Patterns

1. **Multi-region architecture** — geo-partitioned tables for data sovereignty compliance
2. **Serializable transactions** — strongest consistency without performance collapse
3. **Zero-downtime migrations** — online DDL patterns for production deployments
4. **Survivability testing** — chaos engineering patterns (kill nodes, verify availability)

## Competitive Comparison

| | CockroachDB | TiDB | Neon | Supabase | PlanetScale |
|---|------------|------|------|----------|-------------|
| Protocol | PostgreSQL | MySQL | PostgreSQL | PostgreSQL | MySQL |
| Distribution | Multi-region | Multi-region | Single-region | Single-region | Single-region |
| Consistency | Serializable | Snapshot | Serializable | Serializable | Eventual (Vitess) |
| Serverless | ✅ | ✅ | ✅ | ✅ | ✅ |
| Free Tier | 10 GiB | 25 GiB | 0.5 GiB | 500 MB | 5 GiB |
| License | BSL-1.1 | Apache-2.0 | Apache-2.0 | Apache-2.0 | ❌ |
| Best For | Global scale | MySQL scale | Dev-friendly PG | Full-stack BaaS | MySQL serverless |

## ⚠️ License Warning

**BSL-1.1**: Free to use for your own applications. You cannot offer CockroachDB as a competing database-as-a-service. For building SaaS products ON CockroachDB, the license is fine. The BSL converts to Apache-2.0 after 3 years for each version.

## Solo Dev Verdict

**Impressive engineering but overkill for 99% of solo dev projects.** The Serverless free tier (10 GiB, 50M request units/month) is generous enough to experiment. The real learning value is understanding distributed systems concepts: consensus, partitioning, serializable isolation. **For production solo dev work, Supabase or Neon are better fits** — they give you PostgreSQL with less operational complexity. Consider CockroachDB when you need multi-region deployment or regulatory compliance (GDPR data residency).

⭐ **Extractable to code-base**: Multi-region deployment patterns, geo-partitioning strategies, zero-downtime migration scripts.
