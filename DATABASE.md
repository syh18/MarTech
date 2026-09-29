# Database Design

Tenant boundary: workspace_id on tenant-owned tables.

Core tables:
- users, roles, permissions, workspaces, workspace_members
- social_accounts, social_posts
- content_ideas, content_calendar
- campaigns, campaign_channels
- leads, lead_activities
- customers, customer_segments
- marketing_touchpoints
- competitors
- analytics_daily
- budgets
- notifications
- reports
- audit_logs

Integrity rules:
- Foreign keys are enforced.
- Unique constraints exist for globally unique user email and workspace-scoped unique identifiers where applicable.
- created_at and updated_at are mandatory on mutable entities.
- All analytics formulas use Decimal/Float-safe handling in service code and are never trusted from the browser.
