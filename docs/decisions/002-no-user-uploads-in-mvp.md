
# Decision 002: Exclude User Uploads from the MVP

- Status: Accepted
- Date: 2026-10-19
- Sprint: 0

## Context

RevoFin is being built by one engineer with limited time and budget. User-generated finance content adds video storage and bandwidth costs, moderation responsibilities, and risks from misleading investment-related claims. The MVP should validate whether users engage with short finance reels before adding creator infrastructure.

## Options considered

1. **Build user uploads now:** Pros — creators can contribute content and expand supply. Cons — increases engineering work, hosting costs, moderation needs, and compliance risks.
2. **Admin-only uploads:** Pros — keeps content controlled, limits moderation complexity, and supports a small MVP. Cons — content supply depends on the admin and requires a manual publishing workflow.
3. **No-video app:** Pros — avoids video hosting costs and simplifies the initial build. Cons — does not test the core reels-first product hypothesis.

## Decision

Exclude user uploads from the MVP and use admin-only reel publishing, with video content reviewed before publication.

## Consequences

The initial product is easier to control and cheaper to operate, but content supply depends on the admin. User uploads will be reconsidered after the beta if user feedback and retention indicate meaningful demand for more diverse or frequent content, and if moderation, compliance, and hosting costs can be managed.
