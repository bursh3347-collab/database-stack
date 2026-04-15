# Database Schema Design Best Practices

> Extracted from analysis of 7 database tools and their documentation patterns.

## 1. Schema-First vs Code-First

### Schema-First (Prisma approach)
```prisma
// schema.prisma — single source of truth
model User {
  id        String   @id @default(cuid())
  email     String   @unique
  name      String?
  posts     Post[]
  createdAt DateTime @default(now())
  updatedAt DateTime @updatedAt
}
```
**Pros**: Clear data model, auto-generated types, easy to review
**Cons**: Custom DSL, limited expressiveness

### Code-First (Drizzle approach)
```typescript
// schema.ts — TypeScript IS the schema
import { pgTable, text, timestamp } from 'drizzle-orm/pg-core';

export const users = pgTable('users', {
  id: text('id').primaryKey().$defaultFn(() => crypto.randomUUID()),
  email: text('email').notNull().unique(),
  name: text('name'),
  createdAt: timestamp('created_at').defaultNow().notNull(),
  updatedAt: timestamp('updated_at').defaultNow().notNull(),
});
```
**Pros**: Full TypeScript, SQL-level control, composable
**Cons**: More verbose, requires SQL knowledge

### Recommendation
For Micro SaaS: **Drizzle Code-First** (lightweight, type-safe, edge-ready)
For Rapid Prototyping: **Prisma Schema-First** (fastest to productive)

## 2. Essential Schema Patterns

### Soft Delete
```typescript
export const posts = pgTable('posts', {
  // ... other columns
  deletedAt: timestamp('deleted_at'), // null = not deleted
});
```

### Audit Timestamps
Always include `createdAt` and `updatedAt` on every table.

### Multi-Tenancy
```typescript
export const resources = pgTable('resources', {
  id: text('id').primaryKey(),
  teamId: text('team_id').notNull().references(() => teams.id),
  // ... always filter by teamId
});
```

### Row Level Security (Supabase)
```sql
CREATE POLICY "Users can only see own data"
ON public.profiles
FOR SELECT
USING (auth.uid() = user_id);
```

## 3. Indexing Strategy

1. **Primary keys**: Always use `text` with CUID/UUID (not auto-increment for distributed systems)
2. **Foreign keys**: Always index FK columns
3. **Unique constraints**: On email, slug, any lookup field
4. **Composite indexes**: For common WHERE clause combinations
5. **Partial indexes**: For filtered queries (e.g., `WHERE deleted_at IS NULL`)

## 4. Naming Conventions

| Element | Convention | Example |
|---------|------------|--------|
| Tables | snake_case, plural | `user_profiles` |
| Columns | snake_case | `created_at` |
| Primary Key | `id` | `id` |
| Foreign Key | `{table}_id` | `user_id` |
| Indexes | `idx_{table}_{columns}` | `idx_users_email` |
| Timestamps | `{action}_at` | `created_at`, `updated_at` |

## Sources
- Prisma schema best practices
- Drizzle ORM documentation
- Supabase Row Level Security guide
- PostgreSQL indexing documentation
