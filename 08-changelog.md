# Changelog

All notable changes to Milestone are documented here. This changelog follows [Keep a Changelog](https://keepachangelog.com/) principles.

---

## How to Read This Changelog

- **Added** — New features
- **Changed** — Changes to existing functionality
- **Fixed** — Bug fixes
- **Removed** — Removed features
- **Security** — Security-related changes
- **Deprecated** — Features marked for future removal

---

## [Unreleased]

Features in development or testing, not yet generally available.

### Coming Soon
- EU data residency option
- Enhanced reporting exports
- Custom SLA schedules

---

## [1.0.0] - 2024-11-28

### Added

#### Forge App (Jira Integration)
- **Unified Queue** — Centralized view of all client requests with filtering, sorting, and SLA indicators
- **My Work** — Personal dashboard showing assigned requests and individual KPIs
- **Messenger** — Real-time communication with clients, synced to Client Portal
- **Insights** — Analytics dashboard with SLA metrics, volume analysis, and trend reporting
- **Client Directory** — Complete client management including:
  - Client creation and configuration
  - SLA override settings per client
  - Hours purchased tracking
  - Portal link generation
  - Bulk CSV import
- **Admin Console** — Administrative functions including:
  - User role management (Admin/Member)
  - Delivery App access control
  - System settings
- **SLA Tracking** — Automatic response and resolution SLA timers with:
  - Visual countdown indicators
  - Warning states at 75% elapsed
  - Breach detection and recording
  - Cloud-level defaults and per-client overrides

#### Client Portal
- **Request Submission** — Clean form for clients to submit service requests
- **Request Tracking** — View open and closed requests with real-time status
- **SLA Visibility** — Live SLA timers visible to clients
- **Hours Dashboard** — Purchased vs. consumed hours display
- **Messenger** — Two-way communication with MSP team
- **Reports** — Activity history and monthly summaries
- **Profile Management** — User profile settings

#### Delivery App
- **Executive Dashboard** — High-level KPIs and metrics
- **Client Analytics** — Per-client breakdown and health indicators
- **Team Performance** — Agent-level metrics and workload
- **Reports** — Exportable data for QBRs and reviews

#### Core Features
- **Hours Tracking** — Automatic sync from Jira worklogs to client hour banks
- **Firebase Authentication** — Secure auth for Portal and Delivery App
- **HMAC Authentication** — Secure Forge-to-API communication
- **Role-Based Access Control** — Admin and Member roles with appropriate permissions
- **Client Data Isolation** — Complete separation between clients and tenants

### Security
- TLS 1.3 encryption for all data in transit
- AES-256 encryption for data at rest
- HMAC signature verification for Forge API calls
- JWT token authentication for Portal/Delivery
- Multi-tenant data isolation

---

## [0.9.0] - 2024-11-23

### Added
- Early beta release for testing partners
- Core Unified Queue functionality
- Basic Client Directory
- Initial SLA tracking implementation
- Messenger MVP
- Portal link generation
- Hours tracking foundation

### Known Issues (Beta)
- Some edge cases in SLA calculation
- Portal link expiration not enforced
- Limited error messaging

---

## Version History Summary

| Version | Date | Highlights |
|---------|------|------------|
| 1.0.0 | 2024-11-28 | General availability, full feature set |
| 0.9.0 | 2024-11-23 | Early beta release |

---

## Upgrade Notes

### From 0.9.0 to 1.0.0

No action required. All beta configurations are preserved.

**Recommendations:**
- Review SLA settings for accuracy
- Regenerate any expired portal links
- Review user roles in Admin Console

---

## Deprecation Notices

No features are currently deprecated.

---

## Reporting Issues

Found a bug or have a feature request?

- **Bugs:** support@getmilestone.io
- **Feature Requests:** feedback@getmilestone.io
- **Security Issues:** security@getmilestone.io

---

## Roadmap Preview

Features under consideration (not committed):

| Feature | Status |
|---------|--------|
| EU Data Residency | Planned |
| Advanced Reporting | In Development |
| Custom Workflows | Under Consideration |
| Mobile App | Under Consideration |
| API Access | Planned |
| Integrations (Slack, Teams) | Under Consideration |

*Roadmap items are subject to change based on customer feedback and priorities.*

---

## Related Documentation

- **[Overview](00-overview.md)** — Platform introduction
- **[Getting Started](01-getting-started/install-from-marketplace.md)** — Installation guide
- **[Features](02-features/unified-queue.md)** — Feature documentation

---

*Subscribe to product updates at https://getmilestone.io/updates*
