# WORK LOG

- Date (UTC): 2025-11-06 05:13:07
- Author: @AongCho880
- Project: SwapShop (Full-stack mobile marketplace)
- Mode: Bare React Native + Express + MongoDB + Mongoose, monorepo
- Constraint: Free-for-dev for all services until deployment

## 2025-11-06 — Kickoff and scope lock
Decisions captured:
- Frontend: Bare React Native + TypeScript, React Navigation, React Query, Zustand/RTK, React Hook Form + Zod, socket.io-client, FCM, Notifee, react-native-maps, SecureStore/Keychain.
- Backend: Express + TypeScript, MongoDB Atlas (free M0), Mongoose, Zod validation, Helmet, CORS, express-rate-limit, pino/winston, Redis (local dev via Docker), BullMQ, Stripe (test mode) with provider abstraction, S3-compatible storage via MinIO (dev).
- Notifications: Firebase Cloud Messaging (free) for dev.
- Payments: Bangladesh region, currency BDT. Start with Stripe test mode; plan a Bangladesh-local gateway adapter before production.
- Object Storage: MinIO locally; later Cloudflare R2 or AWS S3.
- Deploy: Local via Docker Compose. Staging host (Render/Fly.io/Railway/Koyeb) — pending.
- Repo: Monorepo with npm workspaces (default).

Next actions:
1) Confirm staging host and staging object storage (R2 vs S3).
2) Initialize monorepo skeleton (no code yet): root README, planning docs, workspace tool.
3) Set up CI boilerplate (lint/typecheck) — pending.

Notes:
- All tooling/services chosen have free/dev tiers.
- We track decisions in DECISIONS.md and keep this log updated each step.