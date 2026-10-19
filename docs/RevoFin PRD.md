# RevoFin: Product Requirements Document (Solo Build)

**Version:** 2.0 (solo MVP scope) | **Author:** Samrudh | **Status:** Draft for build

## 1. Overview

RevoFin is a mobile app that delivers daily finance, stock market, and business news as short vertical reels and quick news cards. The goal is to let anyone understand what happened in the markets today in under a minute.

**Vision:** To become India's go-to app for daily finance and business knowledge.

### Project context: a solo build

RevoFin is a personal project built by one person, who is both the product manager and the only engineer, and published on GitHub. It has to work as a real product that real users can test, and as a way to learn and show product and engineering skill.

| Constraint | What it means for the plan |
| --- | --- |
| One engineer, working part-time around studies | Small scope, managed services, one vertical slice at a time |
| Learning is a goal, not a side effect | Each sprint carries a learning objective and short written notes |
| Low or zero budget | Free tiers, compressed video, a monthly cost cap |
| Public GitHub repo | No secrets in the repo; product docs live beside the code |
| The project must prove skill to interviewers | Decisions, research, and metrics are documented, not only the code |

**Builder goals**

| Goal | How this project delivers it |
| --- | --- |
| Build a product end to end | Sprints cover design, build, test, beta, and review |
| Learn the technologies, terms, and the code behind them | Learning notes per sprint; every technology choice explained in the decision log |
| Gain real PM experience | PRD, user research, prioritization, agile sprints, metrics, and retros |
| Build coding and PM expertise together | Every feature has a user story, acceptance criteria, and a success metric |
| Stand out on a resume and in interviews | A finished, user-tested, documented app with a clear story: problem, choices, data, lessons |

## 2. Problem

- Finance news is long, jargon-heavy, and hard to follow for beginners.
- Young Indians are opening demat accounts in large numbers, but their learning happens on Instagram, YouTube, and Telegram. That content is scattered, unstructured, and often unreliable.
- No dedicated app offers finance news in a reels-first, swipeable format.

## 3. Target Users

| Persona | Description | Main need |
| --- | --- | --- |
| **First-time investor** (primary) | 18-25, student or early-career, just started investing | Learn basics and understand daily market news without jargon |
| **Retail trader** | 22-35, trades actively | Fast, scannable updates on stocks, IPOs, and sectors |
| **Business enthusiast** | 18-40, follows startups and companies | Quick business news and explainers |

## 4. Goals and Non-Goals

### Goals (MVP)

1. Prove that people will watch short finance reels daily.
2. Prove that people come back (retention).
3. Learn which content categories perform best.
4. Ship a small, stable, documented MVP that one person can build and maintain.

### Non-Goals (MVP)

- User-uploaded reels, creator monetization, and moderation tooling
- Ads, sponsored reels, affiliate links, premium subscriptions
- Stock alerts, advanced market tools, live prices
- Regional languages and international markets
- Buying, selling, or recommending specific securities
- A custom-built admin dashboard (the MVP uses one minimal admin page)
- Adaptive streaming (HLS), phone OTP login, sharing, and reporting (all moved to Release 2)
- An iOS release (the code stays cross-platform, but the first release is Android)

## 5. Success Metrics

| Metric | Definition | MVP target |
| --- | --- | --- |
| Activation | % of new users who watch 5+ reels in their first session | 60%+ |
| Avg. session length | Average time in feed per session | 4+ min |
| Completion rate | % of reels watched to the end | 50%+ |
| D1 / D7 / D30 retention | % of users who return on day 1, 7, 30 | 35% / 20% / 10% |
| Engagement | Likes + saves + shares per 100 views | 5+ |
| Crash-free sessions | Stability on core flows | 99%+ |

These targets are starting hypotheses. A beta of 30-50 users can only show direction, not proof, so record the actual numbers and what you changed because of them in `/docs/metrics.md`.

## 6. Scope by Release

| Release | Goal | Features |
| --- | --- | --- |
| **R1: MVP** | Prove demand and retention | Google sign-in, onboarding (interests), reels feed with MP4 video, category tabs, like and save, basic profile, minimal admin upload page, analytics events |
| **R2: Habit** | Build daily use | Explore page, news cards, follow creators, push notifications, share, report a reel, HLS streaming, phone OTP login |
| **R3: Supply** | Open to creators | Creator upload, creator profiles and analytics, moderation tools |
| **R4: Monetize** | Revenue | Sponsored reels, affiliates, premium subscription |
| **R5: Scale** | Growth | Regional languages, iOS release, stock alerts, advanced tools |

## 7. MVP User Stories

Priority uses MoSCoW: **M** = Must, **S** = Should, **C** = Could.

### Epic A: Account and Onboarding

| ID | Story | Priority |
| --- | --- | --- |
| A1 | As a new user, I want to sign up with Google so I can start quickly. | M |
| A2 | As a new user, I want to pick my interests (stocks, crypto, IPOs, personal finance, business) so my feed is relevant. | M |
| A3 | As a user, I want to log out and delete my account so I control my data. | M |
| A4 | As a user, I want to sign in with a phone OTP if I don't use Google. | C (R2) |

### Epic B: Reels Feed

| ID | Story | Priority |
| --- | --- | --- |
| B1 | As a user, I want to swipe vertically through full-screen reels so I can consume news quickly. | M |
| B2 | As a user, I want the next reel to load instantly so scrolling feels smooth. | M |
| B3 | As a user, I want to filter by category tabs so I see only what interests me. | M |
| B4 | As a user, I want to see the title, creator, tags, and date on each reel so I know what it covers and how fresh it is. | M |
| B5 | As a user, I want captions or subtitles on reels so I can watch without sound. | C |

### Epic C: Engagement

| ID | Story | Priority |
| --- | --- | --- |
| C1 | As a user, I want to like a reel. | M |
| C2 | As a user, I want to save reels and see them later in my profile. | M |
| C3 | As a user, I want to share a reel through WhatsApp and other apps. | C (R2) |
| C4 | As a user, I want to report a reel that looks misleading. | C (R2) |

### Epic D: Profile

| ID | Story | Priority |
| --- | --- | --- |
| D1 | As a user, I want a profile with my saved reels and interests. | M |
| D2 | As a user, I want to edit my interests and display name. | S |

### Epic E: Admin Panel

| ID | Story | Priority |
| --- | --- | --- |
| E1 | As an admin, I want to upload a reel with title, category, tags, and creator name through a minimal admin page. | M |
| E2 | As an admin, I want to unpublish or delete a reel. | M |
| E3 | As an admin, I want to schedule a reel for a future time. | C (R2) |
| E4 | As an admin, I want to see per-reel metrics in the analytics dashboard (no custom screen). | S |

### Epic F: Analytics

| ID | Story | Priority |
| --- | --- | --- |
| F1 | As the product team, we want to log events (reel\_view, watch\_time, completed, swipe\_away, like, save, share) so we can measure success. | M |

## 8. Functional Requirements

**Feed**

- Full-screen vertical video, one reel at a time, with swipe up for next and down for previous.
- Reels are 15-60 seconds. Autoplay on view, pause on tap, mute toggle.
- Preload the next 2 reels. Paginate in batches of 10.
- Feed order for MVP: reverse chronological, with a simple interest-based boost. No complex recommendation engine yet.
- Already-seen reels are deprioritized.

**Engagement**

- Like and save respond instantly (optimistic UI) and sync in the background.
- Share and report arrive in Release 2.

**Admin page (minimal, web)**

- A minimal page protected by admin login. In the first sprints, the Firebase console can do the job.
- Upload an already-compressed MP4 with a thumbnail, title, category, tags, and creator name.
- Compress videos by hand with FFmpeg before upload. HLS conversion comes in Release 2.

**Analytics**

- Every event includes user id, reel id, timestamp, and category.
- A simple dashboard (Firebase Analytics or equivalent) is enough for MVP.

## 9. Non-Functional Requirements

| Area | Requirement |
| --- | --- |
| Performance | First frame in under 1.5 seconds on a 4G connection; scrolling at 60 fps on mid-range Android |
| Platforms | Android first. iOS later, since an iOS release needs a Mac and a paid Apple developer account |
| Network | Compressed 720p MP4 in the MVP; adaptive HLS in Release 2 |
| Security | Firebase Auth, token checks on the API, no secrets in the repo (it is public) |
| Privacy | Collect only what's needed, clear privacy policy, account deletion supported |
| Scalability | About 1,000 users on free or low-cost tiers; redesign only if traction demands it |
| Cost | Monthly cap on video storage and bandwidth, set before beta |

## 10. Content and Compliance

Finance content in India is regulated. SEBI restricts unregistered individuals from giving investment advice, and it has rules for finfluencers. This must be designed in from day one, not added later.

- Every reel is educational or informational. No "buy this stock" or guaranteed-return claims.
- A persistent disclaimer appears in the app: "For education only. Not investment advice."
- Written content guidelines for the admin team and, later, for creators.
- A way for users to report misleading content.
- A legal review of the policy before public launch.

## 11. Technical Approach

- **Client:** Flutter (Dart), feature-based folders, and one state management approach (Riverpod).
- **Backend:** a small Node.js REST API with tests.
- **Auth, analytics, notifications:** Firebase.
- **Database:** PostgreSQL on a free-tier host, for users, reels, likes, and saves.
- **Video:** cloud storage behind a CDN. Compressed MP4 first, HLS in Release 2.
- **Repo:** one GitHub monorepo with `/app`, `/api`, and `/docs`, plus GitHub Actions for lint and tests.
- Every technology choice gets a short entry in `/docs/decisions/`.

### Core data entities

User, Interest, Reel, Category, Tag, Creator, Like, SavedReel, Report, AnalyticsEvent.

## 12. Delivery Approach (Agile)

- 2-week sprints. Capacity is low until the November exams end, then at least 10 hours a week, so plan each sprint from the hours you can really spend.
- Sprint 0: user interviews, wireframes, architecture, repo and docs setup, GitHub Projects board.
- Sprints 1-2 (exam period): app shell, sign-in, and the backend skeleton. Sprints 3-6: build the rest of the MVP in vertical slices (admin upload, feed, engagement, profile).
- Sprint 7: closed beta with 30-50 users.
- Sprint 8: review the metrics and decide to proceed, pivot, or fix retention first.
- Sprint review: demo to real users, or record a short screen demo.
- **Definition of Done:** acceptance criteria met, tested on a real Android device, analytics events firing, no crashes on core flows, code pushed to GitHub, docs updated.

### Portfolio deliverables (GitHub)

Push the code to GitHub at the end of every sprint, and update these artifacts in the same push.

| Artifact | Where | When |
| --- | --- | --- |
| PRD | `/docs/prd.md` | Sprint 0, updated whenever scope changes |
| User research notes | `/docs/research/` | Sprint 0 and before each release |
| Decision log (why Flutter, why cut uploads, why Postgres) | `/docs/decisions/` | Each time a real choice is made |
| Metrics: targets and actuals | `/docs/metrics.md` | Targets in Sprint 0, actuals from the beta |
| Sprint retro (start, stop, continue) | `/docs/retros/` | End of every sprint |
| Learning notes (what I built and why it works) | `/docs/learning/` | Each sprint, timeboxed |
| Board with sprints, issues, and user stories | GitHub Projects | Throughout |
| README: problem statement, screenshots or demo GIF, "what I'd do next" | `README.md` | First draft in Sprint 0, polished before the beta |

## 13. Risks and Mitigations

| Risk | Mitigation |
| --- | --- |
| Solo burnout or stalled progress | Small sprints, a visible board, and weekly hours set realistically |
| Scope creep | Hold to the non-goals list; new ideas go into the backlog |
| Learning slows delivery | Timebox learning: build first, then spend a fixed time understanding why it works |
| Not enough fresh content (cold start) | Hand-picked creators or your own reels, plus a daily content calendar |
| Regulatory trouble (SEBI) | Education-only policy, disclaimers, legal review before public launch |
| High video costs | Compression, a CDN, and a monthly cost cap |
| Poor retention | Track D1 and D7 early; test onboarding and notifications in Release 2 |
| Slow or buggy feed | Dedicate Sprint 4 to feed performance; test on a low-end phone |
| Secrets leaked in the public repo | Keep keys in ignored `.env` files; never commit them |

## 14. Open Questions

1. Answered: limited time until the November exams end, then at least 10 hours a week.
2. Who will make the first 50-100 reels, and how often can they publish?
3. Is the content original, or curated and re-explained from public news? (This affects copyright.)
4. Which Android phone will you test on, and do you have access to an iPhone or a Mac?
5. What is the monthly budget for video hosting?
6. Is the name "RevoFin" available as a brand and on the app stores?

## 15. Next Steps

1. Review and adjust this PRD.
2. Archive the old code (branch or tag).
3. Create the GitHub repo with the `/docs` structure above and a Projects board.
4. Write the Sprint 0 and Sprint 1 plan.
