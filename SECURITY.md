# Security Policy

- Do not commit secrets. Use `.env` files locally and GitHub environment secrets for staging/production.
- Validate and sanitize all inputs at API boundaries.
- Report vulnerabilities privately via GitHub Security Advisories or email (replace with your contact).
- We use JWT access tokens (short TTL) and rotated, hashed, device-bound refresh tokens.

During development we rely on free/local services only. Production hardening will add stricter controls (WAF, webhook signing, audit logs).