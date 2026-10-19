
# Decision 003: Use PostgreSQL as the Primary Database

- Status: Accepted
- Date: 2026-10-19
- Sprint: 0

## Context

RevoFin needs to store users, interests, reels, categories, likes, and saved reels. These entities have relationships that need consistent handling. The project is also intended to build practical SQL and backend development skills.

## Options considered

1. **PostgreSQL:** Pros — relational data modeling, foreign keys, transactions, and SQL practice. Cons — requires database schema design and backend integration.
2. **MongoDB:** Pros — flexible document structures and a natural fit for some nested data. Cons — relationships and consistency may require additional application-level decisions.
3. **Firestore:** Pros — managed infrastructure and convenient integration with Firebase services. Cons — requires learning its document-oriented data model and query constraints.

## Decision

Use PostgreSQL as the primary database for RevoFin because its relational model suits the application's data, supports data integrity, and aligns with the goal of developing practical SQL skills.

## Consequences

Relationships between users, reels, likes, and saves can be represented with relational tables and constraints, while the project develops practical SQL skills. The application now needs a small backend API to handle database access and enforce application rules securely. Revisit the choice if real usage, cost, or operational requirements make the current approach unsuitable.
