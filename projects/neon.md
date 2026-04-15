# Neon

> Serverless Postgres with branching, autoscaling, and scale-to-zero — the GitHub of databases.

| Metric | Data |
|--------|------|
| GitHub | [neondatabase/neon](https://github.com/neondatabase/neon) |
| Stars | 21,499 |
| Forks | 926 |
| License | Apache-2.0 |
| Language | Rust |
| Last Updated | 2026-04-15 |
| Contributors | 200+ |
| Funding | $174M+ (Series C) |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Tech | 90 | Storage-compute separation, copy-on-write branching, autoscaling, Rust core |
| E Ecosystem | 78 | 21.5k stars, Vercel partnership, growing fast but smaller than Supabase community |
| M Market | 85 | Serverless DB is hot, Vercel/Cloudflare integration, $174M+ funding |
| C Combo | 80 | Excellent with Vercel + Drizzle/Prisma, but competes with Supabase in天子栈 |
| **Overall** | **84** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Neon reimagines Postgres for the serverless era. Database branching (like git branches) enables preview deployments. Scale-to-zero means you only pay for what you use. Perfect for indie hackers and startups.

## Architecture Highlights
- **Storage-Compute Separation**: Pageserver stores data, Compute nodes run Postgres
- **Copy-on-Write Branching**: Instant DB branches for dev/preview/testing
- **Autoscaling**: Scale compute up/down based on load
- **Scale-to-Zero**: No cost when idle
- **@neondatabase/serverless**: HTTP-based Postgres driver for edge

## Key Modules
1. **Pageserver** (Large) — Distributed storage engine (Rust)
2. **Compute** (Large) — Modified Postgres with Neon extensions
3. **Safekeeper** (Medium) — WAL durability + replication
4. **Serverless Driver** (Small) — HTTP/WebSocket Postgres for edge

## Extractable Components
- Serverless DB connection pattern → code-base/database/serverless/
- Branch-based preview deployment workflow → code-base/deploy/preview-db/

⭐ Universal Code Candidate: Serverless Postgres connection for edge/Vercel

## Why It Might NOT Be Worth It
- Overlaps with Supabase (already in天子基准栈)
- Self-hosting is extremely complex (distributed Rust system)
- Cold start latency for scale-to-zero
- Vendor lock-in risk despite open source
- Storage layer is custom, not standard Postgres

## 天子点评
技术精妙但与 Supabase 重叠。分支功能适合团队协作，一人公司暂不需要。留作 Supabase 的 Plan B。
