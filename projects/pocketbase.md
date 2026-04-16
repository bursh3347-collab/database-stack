# PocketBase

> Open Source backend in 1 file — Realtime DB + Auth + File storage + Admin dashboard

| Metric | Data |
|--------|------|
| GitHub | [pocketbase/pocketbase](https://github.com/pocketbase/pocketbase) |
| Stars | ~43,000 |
| License | MIT |
| Language | Go |
| Last Updated | Active |
| Contributors | 100+ |

## TEMC Score

| Dimension | Score | Rationale |
|-----------|-------|-----------|
| T (Tech) | 82 | Single binary with embedded SQLite. Built-in: auth (email/OAuth), realtime subscriptions, file storage, admin UI, REST API auto-gen. Extendable via Go or JS hooks |
| E (Ecosystem) | 85 | 43k stars, massive community. JS/Dart SDKs. Active Reddit/Discord. Used by thousands of indie projects. One of the most loved tools on HN |
| M (Market) | 80 | Perfect for indie hackers and solo devs who want Firebase-like experience without vendor lock-in. Self-hostable on a $5 VPS. Growing as Supabase alternative for simpler use cases |
| C (Combo) | 72 | Great for prototyping and MVPs. But Go backend means TypeScript devs can't deeply customize server logic (JS hooks are limited). Not ideal for complex business logic |
| **Overall** | **80** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
The simplest possible backend. Download one file, run it, get a full backend with database, auth, file storage, admin panel, and REST API. Zero configuration. Deploy anywhere with `./pocketbase serve`.

## Architecture Highlights
- **Single binary** — One Go executable, no external dependencies
- **Embedded SQLite** — Database lives in a single file, easy backup
- **Admin UI** — Built-in web dashboard for data management
- **Realtime** — SSE-based realtime subscriptions for data changes
- **JS Hooks** — Extend server logic with JavaScript (Goja runtime)
- Core packages: apis/ (HTTP handlers), core/ (business logic), forms/ (validation), plugins/

## Key Modules
1. **Core** — Collection/record CRUD, hooks system, auth providers
2. **APIs** — Auto-generated REST endpoints per collection
3. **Realtime** — Server-Sent Events for live data sync
4. **File Storage** — Local or S3-compatible storage
5. **Admin UI** — Svelte-based dashboard (embedded in binary)

## Solo Dev Verdict
🟢 **Best MVP launcher for solo devs.** If you need a backend in 5 minutes, PocketBase is unbeatable. Auth + DB + files + admin = done. Perfect for hackathons, side projects, and MVPs. Graduate to Supabase/custom backend when you outgrow it. The 43k stars community means answers to every question.

## Anti-Pattern Warning
- SQLite = not suitable for high-write concurrent workloads
- Go backend = TypeScript devs limited to JS hooks for customization
- No built-in edge/serverless deployment (it's a long-running process)
- Scaling beyond single server requires manual sharding or migration
- Not ideal for complex multi-tenant SaaS architecture
