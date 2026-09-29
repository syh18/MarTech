# MarketPulse Intelligence

Modern SaaS MarTech foundation for integrated marketing operations, analytics, CRM, content, campaigns, attribution, competitor intelligence, AI assistance, and reporting.

## Status
Phase 1 foundation: monorepo, React/Vite web shell, NestJS API shell, PostgreSQL/Prisma data model, authentication architecture, shared configuration, and baseline documentation.

## Planned stack
- Web: React + TypeScript + Vite + Tailwind CSS
- API: NestJS + TypeScript + Prisma
- Database: PostgreSQL
- Auth: JWT access/refresh tokens + Argon2 + RBAC
- Tests: Vitest/Jest + Supertest + Playwright
- API docs: OpenAPI/Swagger
- Local orchestration: Docker Compose

## Repository
/apps/web
/apps/api
/packages/types
/packages/config
/packages/ui

See ARCHITECTURE.md, DATABASE.md, API.md, SECURITY.md for the foundation design.

## Quick start
1. Copy `.env.example` to `.env`.
2. Start PostgreSQL with `docker compose up -d postgres`.
3. Install dependencies with `npm install`.
4. Generate Prisma client and run migrations.
5. Seed demo data.
6. Start web and API in development.

The implementation roadmap intentionally delivers capability incrementally; external social APIs are represented by explicit mock-provider boundaries until official credentials and platform approvals are available.
