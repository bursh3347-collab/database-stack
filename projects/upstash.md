# Upstash Redis

> Serverless Redis with HTTP API — Pay per request, scale to zero

| Metric | Data |
|--------|------|
| GitHub | [upstash/redis-js](https://github.com/upstash/redis-js) |
| Stars | ~2,000 (SDK) |
| License | MIT |
| Language | TypeScript |
| Last Updated | Active |
| Contributors | 50+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 78 | HTTP-based Redis client (no TCP needed). Works in edge runtimes (CF Workers, Vercel Edge, Deno). Pipelining, Lua scripts, JSON support. Also offers QStash (messaging) and Vector (embeddings) |
| E (Ecosystem) | 72 | 2k stars for SDK (but Upstash platform widely used). Official Vercel integration partner. Rate limiting, session store, caching SDKs. Growing but smaller than ioredis ecosystem |
| M (Market) | 82 | Serverless Redis is the fastest-growing Redis segment. Pay-per-request eliminates idle costs for solo devs. $0 when not used. Competes with Redis Cloud but 10x cheaper at small scale |
| C (Combo) | 90 | Perfect serverless stack companion. Works in Vercel Edge Functions (where ioredis doesn't). Rate limiting, caching, session management — all serverless-native. Pairs with Next.js, Hono, Remix |
| **Overall** | **82** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Redis that works everywhere — including edge runtimes where TCP connections aren't available. Pay only for what you use, scale to zero. The missing piece for truly serverless architectures.

## Architecture Highlights
- **HTTP-based** — REST API instead of TCP, works in any runtime
- **@upstash/redis** — TypeScript client with auto-pipelining
- **@upstash/ratelimit** — Serverless rate limiting library
- **@upstash/vector** — Vector similarity search for AI/embeddings
- **@upstash/qstash** — Serverless message queue / task scheduler
- Monorepo with multiple packages: redis-js, ratelimit, vector, qstash

## Key Modules
1. **@upstash/redis** — Core Redis client (HTTP-based, edge-compatible)
2. **@upstash/ratelimit** — Sliding window / token bucket rate limiting
3. **@upstash/vector** — Vector database for embeddings (RAG use cases)
4. **@upstash/qstash** — HTTP-based message queue (BullMQ alternative for serverless)
5. **Platform integrations** — Vercel, Next.js, Cloudflare, Deno, Remix

## Solo Dev Verdict
🟢 **Essential for serverless SaaS.** If you deploy on Vercel/Cloudflare, Upstash Redis is your caching + rate limiting + session store layer. $0 idle cost = perfect for side projects that might not get traffic. QStash replaces BullMQ for serverless. The ratelimit SDK is plug-and-play.

## Anti-Pattern Warning
- HTTP overhead vs TCP Redis (2-5ms added latency per request)
- Not suitable for Redis Streams heavy workloads
- Vendor lock-in to Upstash platform (though SDK is MIT)
- More expensive than self-hosted Redis at high volume
- Feature parity with Redis not 100% (some advanced commands missing)
