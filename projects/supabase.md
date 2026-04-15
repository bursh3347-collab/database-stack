# Supabase

> Open-source Firebase alternative with Postgres, Auth, Storage, Realtime, Edge Functions, and Vector embeddings.

| Metric | Data |
|--------|------|
| GitHub | [supabase/supabase](https://github.com/supabase/supabase) |
| Stars | 100,883 |
| Forks | 12,082 |
| License | Apache-2.0 |
| Language | TypeScript |
| Last Updated | 2026-04-15 |
| Contributors | 1,200+ |
| Open Issues | 972 |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Tech | 92 | Full-stack BaaS on Postgres, pgvector for AI, Edge Functions, Realtime subscriptions |
| E Ecosystem | 95 | 100k+ stars, massive community, official integrations with every major framework |
| M Market | 88 | Dominant open-source BaaS, $116M+ funding, enterprise adoption accelerating |
| C Combo | 95 | Core of天子基准技术栈, already integrated in workflow |
| **Overall** | **92** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
Supabase provides a complete backend-as-a-service built on Postgres. One dashboard gives you database, auth, storage, realtime, edge functions, and vector search. Perfect for solo developers and small teams.

## Architecture Highlights
- **PostgREST**: Auto-generated REST API from Postgres schema
- **GoTrue**: Auth server (email, OAuth, magic links)
- **Realtime**: WebSocket-based change data capture
- **Storage**: S3-compatible file storage with RLS
- **Edge Functions**: Deno-based serverless functions
- **pgvector**: Native vector embeddings for AI apps

## Key Modules
1. **supabase-js** (Medium) — Client SDK for all services
2. **Auth (GoTrue)** (Large) — Authentication + authorization
3. **PostgREST** (Large) — Auto REST API from schema
4. **Realtime** (Large) — WebSocket subscriptions
5. **Storage** (Medium) — File storage with policies
6. **Edge Functions** (Medium) — Serverless compute

## Extractable Components
- Row Level Security patterns → code-base/auth/rls/
- Realtime subscription patterns → code-base/api/realtime/
- pgvector embedding workflows → code-base/ai-integration/embedding/
- Auth patterns (email/OAuth/magic-link) → code-base/auth/

⭐ Universal Code Candidate: Auth patterns, RLS policies, pgvector integration

## Why It Might NOT Be Worth It
- Vendor dependency risk (self-hosting is complex)
- PostgREST limitations for complex queries
- Edge Functions still maturing
- Pricing can escalate with heavy usage
- Some features lag behind Firebase (push notifications, analytics)
