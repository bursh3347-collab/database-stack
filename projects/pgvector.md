# pgvector

> Open-source vector similarity search extension for PostgreSQL — the AI/RAG infrastructure layer every app needs.

| Metric | Data |
|--------|------|
| GitHub | [pgvector/pgvector](https://github.com/pgvector/pgvector) |
| Stars | ~13,000 |
| License | PostgreSQL License (permissive) |
| Language | C |
| Last Updated | 2026-04 (active) |
| Contributors | 30+ |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Technology | 82 | Production-grade HNSW + IVFFlat indexes, binary/scalar quantization, exact & approximate search. Native PG extension = zero new infra. Supports L2, inner product, cosine, L1, Hamming, Jaccard distances. Up to 16,000 dimensions. |
| E Ecosystem | 88 | Pre-installed on Supabase, Neon, AWS RDS, Azure, GCP. Bindings for Python, Node.js, Ruby, Go, Rust, Java, C#, PHP. Massive PostgreSQL ecosystem leverage. |
| M Market | 92 | AI/RAG explosion = every application needs vector search. pgvector is the default choice for teams already on PostgreSQL. No vendor lock-in vs Pinecone/Weaviate. |
| C Combinability | 90 | Direct integration with Supabase (already in database-stack). Works with Drizzle ORM & Prisma. Zero new infrastructure — just `CREATE EXTENSION vector`. Perfect for solo dev adding AI to existing PG app. |
| **Composite** | **88** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value

pgvector eliminates the need for a separate vector database. If you're already on PostgreSQL (and you should be), you get vector search for free — same backups, same migrations, same tooling. This is the **zero-overhead AI infrastructure** play.

## Architecture Highlights

- **Pure C extension** — compiles against any PG 13+ installation
- **HNSW indexing** — logarithmic query time, the gold standard for ANN search
- **IVFFlat indexing** — faster build times, good for batch workflows
- **Quantization** — binary & scalar quantization reduce storage 8-32x with minimal recall loss
- **Streaming disk ANN** — iterative index scans for filtered queries
- **Full SQL integration** — `ORDER BY embedding <=> query_vector LIMIT 10` — it's just SQL

## Key Extractable Patterns

1. **Vector column type** — `vector(1536)` as a native PG column, not a separate store
2. **Hybrid search** — combine vector similarity with traditional WHERE clauses in one query
3. **Quantization pattern** — store full vectors but index quantized versions for speed
4. **Multi-index strategy** — HNSW for low-latency queries, IVFFlat for batch processing

## Competitive Comparison

| | pgvector | Pinecone | Weaviate | Qdrant |
|---|---------|----------|----------|--------|
| Type | PG Extension | Managed SaaS | Standalone DB | Standalone DB |
| Cost | Free (PG cost) | $70+/mo | Self-host free | Self-host free |
| Lock-in | None | High | Medium | Medium |
| SQL | Full PostgreSQL | Proprietary API | GraphQL | REST/gRPC |
| Hybrid Search | Native PG WHERE | Metadata filters | BM25+Vector | Payload filters |
| Best For | PG users adding AI | Serverless scale | Multi-modal | High-performance |

## Solo Dev Verdict

**Must-have for any AI/RAG application on PostgreSQL.** If you're using Supabase or Neon (both already in this stack), pgvector is pre-installed — just enable the extension and you have production vector search in 5 minutes. No new infrastructure, no new billing, no new SDK to learn. This is the highest-ROI addition to any TypeScript + Supabase stack.

⭐ **Extractable to code-base**: Vector search setup patterns, hybrid search queries, quantization configuration.
