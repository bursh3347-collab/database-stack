# ClickHouse

> The fastest open-source columnar database for real-time analytics — processes billions of rows per second.

| Metric | Data |
|--------|------|
| GitHub | [ClickHouse/ClickHouse](https://github.com/ClickHouse/ClickHouse) |
| Stars | ~38,000 |
| License | Apache-2.0 |
| Language | C++ |
| Last Updated | 2026-04 (very active, daily commits) |
| Contributors | 1,800+ |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Technology | 92 | Industry-leading OLAP performance. Vectorized query execution, columnar compression (up to 40x), MergeTree engine family, materialized views, approximate query processing. Handles petabyte-scale datasets. |
| E Ecosystem | 85 | 38k⭐, ClickHouse Inc (raised $300M+), massive enterprise adoption (Cloudflare, Uber, eBay, Spotify). 100+ input/output formats. Native integrations with Kafka, S3, PostgreSQL. |
| M Market | 78 | Analytics is evergreen but ClickHouse is primarily an enterprise/infrastructure tool. Not directly a SaaS builder but essential for analytics-heavy products. Real-time dashboards market growing fast. |
| C Combinability | 65 | Heavy infrastructure footprint. Not ideal for solo dev Micro SaaS unless building analytics product. ClickHouse Cloud simplifies ops. JS/TS client available but ecosystem is smaller than PG. |
| **Composite** | **80** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value

When PostgreSQL can't handle your analytics queries (millions+ rows, aggregations, time-series), ClickHouse is the answer. It's not a replacement for your transactional database — it's the **analytics layer** that sits alongside it.

## Architecture Highlights

- **Columnar storage** — only reads columns needed for query, massive I/O reduction
- **MergeTree engine** — LSM-tree inspired, optimized for append-heavy analytics workloads
- **Vectorized execution** — processes data in batches using SIMD instructions
- **Materialized views** — pre-aggregate data on insert for instant dashboard queries
- **Approximate functions** — `uniqHLL12`, `quantileTDigest` for fast estimates on billions of rows
- **Sharding & replication** — horizontal scaling with ZooKeeper/ClickHouse Keeper coordination

## Key Extractable Patterns

1. **Event analytics pipeline** — Kafka → ClickHouse materialized view → API → dashboard
2. **Time-series aggregation** — pre-computed rollups for fast time-range queries
3. **Funnel analysis** — `windowFunnel` function for conversion tracking
4. **A/B test analysis** — statistical functions built-in for experiment evaluation

## Competitive Comparison

| | ClickHouse | BigQuery | Snowflake | DuckDB | TimescaleDB |
|---|-----------|----------|-----------|--------|-------------|
| Type | Columnar OLAP | Cloud DW | Cloud DW | Embedded OLAP | PG Extension |
| Speed | ⚡ Fastest | Fast | Fast | Fast (local) | Good |
| Cost | Self-host free | Pay-per-query | $$$$ | Free | PG cost |
| Scale | Petabytes | Petabytes | Petabytes | Single-node | Terabytes |
| Best For | Real-time analytics | Ad-hoc analysis | Enterprise BI | Local analytics | Time-series on PG |

## Solo Dev Verdict

**Only if you're building an analytics-heavy product.** For a typical Micro SaaS, PostgreSQL handles analytics fine up to ~10M rows. But if you're building a product where real-time analytics IS the product (dashboards, monitoring, event tracking), ClickHouse is unbeatable. ClickHouse Cloud offers a serverless option starting at ~$50/mo. Consider it when your PG analytics queries start taking seconds instead of milliseconds.

⭐ **Extractable to code-base**: Event ingestion patterns, materialized view designs, analytics API patterns.
