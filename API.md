# API Architecture

Base path: /api

Auth
- POST /api/auth/register
- POST /api/auth/login
- POST /api/auth/refresh
- POST /api/auth/logout

Health
- GET /api/health

Planned modules
- GET/POST /api/campaigns
- GET/POST /api/leads
- GET/POST /api/social/accounts
- GET/POST /api/social/posts
- GET/POST /api/content
- GET /api/dashboard
- GET /api/analytics
- GET /api/reports

Cross-cutting behavior:
- DTO validation
- standardized errors
- request correlation ids
- authenticated workspace context
- role/permission guards
- audit events for mutations
