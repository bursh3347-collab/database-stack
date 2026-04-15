# SQLAlchemy

> Python's most powerful and flexible ORM — the gold standard for Python database access.

| Metric | Data |
|--------|------|
| GitHub | [sqlalchemy/sqlalchemy](https://github.com/sqlalchemy/sqlalchemy) |
| Stars | ~9,800 |
| Forks | ~1,500 |
| License | MIT |
| Language | Python |
| Last Updated | 2026-04 (active) |
| Contributors | 700+ |

## TEMC Score

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| T Tech | 92 | Most sophisticated ORM design ever, Unit of Work pattern, expression language, async support |
| E Ecosystem | 85 | De facto Python ORM, Alembic migrations, used by Flask/FastAPI/Django(optional) |
| M Market | 75 | Dominant in Python, but Python is secondary priority for天子 |
| C Combo | 55 | Python (secondary stack), not directly composable with TypeScript基准栈 |
| **Overall** | **74** | T×0.25 + E×0.20 + M×0.30 + C×0.25 |

## Core Value
SQLAlchemy is the reference implementation for ORM design. Its dual-layer architecture (Core + ORM) and Unit of Work pattern are studied by every ORM author. Essential for Python backend work.

## Architecture Highlights
- **Dual Layer**: Core (SQL expression language) + ORM (object mapping)
- **Unit of Work**: Automatic change tracking and batch flushing
- **Alembic**: Industrial-grade migration framework
- **Async Support**: Full asyncio integration (v2.0+)
- **Expression Language**: Pythonic SQL construction

## Key Modules
1. **SQLAlchemy Core** (Large) — SQL expression language
2. **SQLAlchemy ORM** (Large) — Object-Relational Mapping
3. **Alembic** (Medium) — Migration framework
4. **Engine/Pool** (Medium) — Connection pooling + management

## Extractable Components
- Unit of Work pattern → code-base/database/patterns/
- Migration best practices (Alembic) → code-base/database/migrations/

## Why It Might NOT Be Worth It
- Python-only, not composable with TypeScript stack
- Steep learning curve
- Verbose for simple operations
- Stars count understates actual usage (pre-GitHub era project)

## 天子点评
Python ORM 天花板，学习 ORM 设计模式的最佳教材。天子 Python 项目可用，但 TypeScript 主栈用 Drizzle。
