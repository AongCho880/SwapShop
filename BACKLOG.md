# Backlog and Milestones

We work in vertical slices. Each slice ends with a working, testable feature.

## Milestone 0 — Bootstrap & Quality Gates
- Repo initialization (monorepo)
- Planning docs: WORKLOG.md, DECISIONS.md, BACKLOG.md
- Choose workspace manager (default npm workspaces)
- Root tooling:
  - ESLint + Prettier base configs
  - Commitlint + husky (conventional commits)
  - EditorConfig
- CI (phase 1): lint + typecheck placeholders
- Docker Compose skeleton (dev): MongoDB, Redis, MinIO
- README with getting started
Deliverable: Repo builds, lints, and runs docker-compose up for infra.

## Milestone 1 — Auth Vertical
- Server:
  - Express + TS scaffold
  - Config management (dotenv, env schema)
  - Mongo connection, base Mongoose models
  - Auth: signup/login/logout, JWT access + refresh rotation (hashed, device-bound)
  - Validation with Zod; error handling; rate limiting; Helmet; CORS
  - OpenAPI (Swagger) basic
  - Tests: Jest + Supertest for auth endpoints
- Mobile:
  - Bare RN app init (TypeScript, strict)
  - Navigation setup; auth screens
  - Secure token storage; React Query for API
  - Form + validation (React Hook Form + Zod)
Deliverable: Login/signup works end-to-end locally.

## Milestone 2 — Listings + Media Uploads
- S3-compatible uploads via pre-signed URLs (MinIO dev)
- Create/edit/delete listing; browse feed with pagination (keyset)
- Image caching; list virtualization
- Server indexes (text indexes), lean reads, projections
Deliverable: Create listing with photos; display in feed.

## Milestone 3 — Geo & Search
- User location permissions (app)
- 2dsphere index; distance filters; map view
- Saved searches, categories
Deliverable: Browse listings near me with filters.

## Milestone 4 — Realtime Chat & Push
- Socket.IO rooms, message acks, read receipts
- Offline queue + optimistic UI
- Push: FCM; Notifee for local
Deliverable: Send/receive messages with push.

## Milestone 5 — Offers, Orders, Payments
- Offer flow; accept/decline; checkout
- Payments via adapter interface:
  - Stripe (test, BDT)
  - Prepare provider interface for Bangladesh gateways (e.g., SSLCommerz)
- Webhooks (idempotent); order state machine; receipts
Deliverable: Pay in test mode; order lifecycle managed.

## Milestone 6 — Reviews, Reporting, Admin
- Post-order reviews; reputation; abuse reports
- Basic Admin (AdminJS or lightweight SPA)
- RBAC policies; analytics aggregates
Deliverable: Moderation and basic KPIs.

## Milestone 7 — Offline & Perf
- React Query persistence; optimistic rollback
- Image cache; code splitting; metrics
Deliverable: Smooth UX under flaky network.

## Milestone 8 — CI/CD & Hardening
- CI: full test matrix; build/publish Docker
- Staging deploy to chosen host
- Load testing (k6), SAST/dep scan
- Observability baseline: logs, Sentry, traces (optional)
Deliverable: One-click deploy to staging.

---

Upcoming tasks (next actionable items):
- Add root workspace scaffolding and baseline tooling (ESLint/Prettier, commitlint/husky).
- Decide staging host and object storage provider for staging.