# Database Migration Best Practices

> Patterns extracted from Prisma Migrate, Drizzle Kit, Alembic, and TypeORM migrations.

## 1. Migration Principles

1. **Every schema change = a migration file** (never modify database directly)
2. **Migrations are immutable** (once committed, never edit)
3. **Migrations are sequential** (ordered by timestamp)
4. **Always test migrations** on a copy before production
5. **Separate data migrations from schema migrations**

## 2. Migration Workflow Comparison

### Prisma Migrate
```bash
# Generate migration from schema changes
prisma migrate dev --name add_user_avatar

# Apply to production
prisma migrate deploy
```

### Drizzle Kit
```bash
# Generate migration
drizzle-kit generate

# Apply migration
drizzle-kit migrate

# Push directly (dev only)
drizzle-kit push
```

### Alembic (SQLAlchemy)
```bash
# Auto-generate from model changes
alembic revision --autogenerate -m "add user avatar"

# Apply
alembic upgrade head
```

## 3. Safe Migration Patterns

### Adding a Column (Safe)
```sql
ALTER TABLE users ADD COLUMN avatar_url TEXT;
```
Always add as nullable first, then backfill, then add NOT NULL constraint.

### Renaming a Column (Dangerous!)
```sql
-- Step 1: Add new column
ALTER TABLE users ADD COLUMN full_name TEXT;
-- Step 2: Backfill data
UPDATE users SET full_name = name;
-- Step 3: Deploy code that reads both columns
-- Step 4: Drop old column (next migration)
ALTER TABLE users DROP COLUMN name;
```

### Adding an Index (Safe, but slow on large tables)
```sql
CREATE INDEX CONCURRENTLY idx_users_email ON users(email);
```
Always use `CONCURRENTLY` in Postgres to avoid table locks.

## 4. Zero-Downtime Migration Checklist

- [ ] New columns are nullable or have defaults
- [ ] No column renames (use add/backfill/drop pattern)
- [ ] No table renames in single step
- [ ] Indexes created CONCURRENTLY
- [ ] Data backfill in separate step
- [ ] Backward-compatible with current application code
- [ ] Tested on staging with production-size data

## 5. Branch-Based Development (Neon)

Neon's database branching enables:
```
main branch (production DB)
  ├── feature/auth-refactor (branched copy)
  ├── preview/pr-42 (auto-created for PR)
  └── staging (persistent branch)
```
Each branch is a full copy-on-write Postgres instance.

## Sources
- Prisma Migrate documentation
- Drizzle Kit documentation
- Alembic tutorial
- Neon branching guide
- PlanetScale Online DDL documentation
