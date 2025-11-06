# SwapShop — Full‑stack Mobile Marketplace

A production‑ready learning capstone that builds a complete marketplace app using:
- Mobile: Bare React Native + TypeScript
- Server: Express + TypeScript + MongoDB (Mongoose)
- Realtime: Socket.IO
- Media: S3‑compatible (MinIO in dev)
- Notifications: FCM + Notifee (free for dev)
- Payments: Provider abstraction; start with Stripe test mode (BDT)
- Infra: Docker Compose (MongoDB, Redis, MinIO)
- Monorepo; security‑first; free‑for‑dev services

## Free‑for‑dev principle
All tools and services must be free during development (local or free tier). Paid services will be considered at deployment time only.

## Goals
- Learn professional full‑stack mobile development end‑to‑end
- Ship secure, scalable, observable software
- Practice CI/CD, testing, and production hygiene

## Architecture at a glance
- React Native (TypeScript, React Navigation, React Query, Zustand/RTK, RHF + Zod)
- Express API (Zod validation, Helmet, CORS, rate limiting, pino/winston logs)
- MongoDB Atlas (free M0) + Mongoose (indexes, transactions)
- Redis + BullMQ for background jobs
- S3‑compatible storage (MinIO dev; R2/S3 later)
- Stripe test mode (BDT) behind a payment adapter interface

## Monorepo layout (planned)
```
/apps
  /mobile     # React Native app
  /server     # Express API
/packages     # Shared configs/types (optional)
```

## Start here
- Read BACKLOG.md for milestones and vertical slices
- See decisions in DECISIONS.md
- Follow progress in WORKLOG.md

## Local prerequisites
- Node.js 20 LTS, npm 10+
- Git, Docker Desktop (or docker + docker-compose)
- macOS + Xcode for iOS, Android Studio for Android
- Java 17 (Android Gradle)
- gh (GitHub CLI) optional but recommended

## Next steps
We will proceed in small steps with instructor‑style explanations. First milestones:
1) Bootstrap & quality gates (repo/tooling)
2) Auth vertical (signup/login/logout with secure tokens)
3) Listings + media uploads (pre‑signed URLs to MinIO)

## Contributing
See CONTRIBUTING.md. Conventional commits are used.

## Security
See SECURITY.md. Never commit secrets. Use `.env` files locally and environment secrets in CI/deploy.

## License
MIT — see LICENSE.