# Architecture Decisions (ADRs)

Status codes:
- Accepted: decision is active
- Pending: needs confirmation
- Proposed: suggested but not yet decided
- Superseded: replaced by a newer ADR

---

## ADR-0001: Monorepo + Bare React Native
- Status: Accepted
- Decision: Single monorepo with `apps/mobile` and `apps/server`. TypeScript strict everywhere.

## ADR-0002: Free-for-dev Principle
- Status: Accepted
- Decision: Prefer local/self-hosted or free tiers during development only.

## ADR-0003: Database — MongoDB Atlas Free (M0)
- Status: Accepted
- Decision: Use Atlas M0 for dev/staging.

## ADR-0004: Object Storage — MinIO (dev) → R2/S3 (staging/prod)
- Status: Proposed
- Decision: S3-compatible pre-signed URL flow across providers.

## ADR-0005: Notifications — FCM
- Status: Accepted
- Decision: Use Firebase Cloud Messaging for push. Notifee for local.

## ADR-0006: Payments — Adapter Interface; Start with Stripe (BDT)
- Status: Accepted
- Decision: Provider-agnostic payment layer. Stripe test first; add Bangladesh gateway before prod.

## ADR-0007: Realtime — Socket.IO
- Status: Accepted
- Decision: Namespaces/rooms; horizontal scale ready.

## ADR-0008: Validation, Security, and Auth
- Status: Accepted
- Decision: Zod DTOs; JWT access (short TTL) + rotated, hashed, device-bound refresh tokens; Helmet/CORS/rate limiting.

## ADR-0009: Logging & Observability
- Status: Accepted
- Decision: Structured logs (pino/winston), correlation IDs, Sentry (free tier) later.

## ADR-0010: CI/CD and Deploy
- Status: Pending
- Decision: Choose staging host (Render/Fly/Railway/Koyeb). Dockerized deploy via GitHub Actions.

## ADR-0011: Package & Workspace Manager
- Status: Proposed
- Decision: Use npm workspaces initially; revisit pnpm if beneficial.

Open questions:
- Staging host choice?
- Staging object storage (R2 vs S3)?
- Target platforms: iOS + Android (assumed both; confirm).