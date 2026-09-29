# Security Baseline

- Argon2 password hashing; no plaintext password persistence.
- Short-lived access JWT plus rotated refresh tokens.
- Secrets only through environment variables.
- ValidationPipe with whitelist/forbidNonWhitelisted.
- Helmet/security headers.
- Rate limiting on authentication endpoints.
- CORS restricted by configured origin.
- Prisma parameterization for SQL-injection resistance.
- Workspace-scoped authorization on tenant data.
- Audit logging for security-sensitive mutations.
- Never expose provider secrets to the browser.
- Official APIs only for production social integrations; no prohibited scraping.
