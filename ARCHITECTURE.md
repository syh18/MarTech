# System Architecture

## Context
MarketPulse Intelligence is a multi-tenant SaaS. Workspace is the tenant boundary; users may belong to one or more workspaces through memberships.

## Logical flow
Browser -> React Web -> REST API -> Application Services -> Prisma -> PostgreSQL

External platforms -> Provider adapters -> Normalization -> persistence -> analytics engine -> API -> dashboard

## Architectural decisions
- Monorepo with independently deployable web and api applications.
- NestJS modular architecture for explicit domain boundaries.
- Prisma for relational modeling and migrations.
- PostgreSQL for transactional data and analytics source-of-truth.
- Provider adapter interfaces prevent platform-specific logic leaking into domain services.
- Backend owns KPI calculations; frontend only renders API results.
- UUID primary keys for business entities.
- Audit log is append-oriented and tied to workspace/user context.
- Soft deletion is used only where restoration has meaningful business value.

## Domains
auth, users, workspaces, dashboard, social, content, campaigns, leads, customers, analytics, attribution, competitors, reports, notifications, ai.

## MVP scope
1. Authentication + RBAC
2. Workspace and user membership
3. Campaign CRUD
4. Lead CRUD + pipeline
5. Content ideas/calendar
6. Social accounts + manual/mock posts
7. Analytics engine
8. Executive dashboard
9. Audit logs
10. Basic reports/export

Phase 2 adds official social connectors, richer attribution, segmentation, competitor intelligence, AI assistant, advanced reporting, and production observability.
