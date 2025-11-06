# Contributing

Thanks for your interest in contributing!

## Ground rules
- Follow Conventional Commits (`type(scope): message`), e.g., `feat(mobile): add login screen`.
- Small, focused PRs only. One concern per PR.
- Security-first: validate inputs, avoid leaking secrets, handle errors.

## Setup
- Node 20 LTS (see `.nvmrc`)
- `npm ci`
- We will add workspaces and tooling in Milestone 0.

## Branching
- Base branch: `main` (protected)
- Feature branches: `feat/...`, `fix/...`, `chore/...`, `docs/...`, `infra/...`

## PR checklist
- Lint/typecheck pass (CI)
- Tests for new behavior (as applicable)
- Update docs: README/BACKLOG/WORKLOG/ADRs