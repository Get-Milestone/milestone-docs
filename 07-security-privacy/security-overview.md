# Security Overview

Milestone is built with security as a foundational principle. This document outlines the security measures protecting your data and your clients' data across all Milestone applications.

---

## Architecture Overview

Milestone consists of multiple components, each with appropriate security controls:

```
┌─────────────────────────────────────────────────────────────────┐
│                     ATLASSIAN CLOUD                             │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │              MILESTONE FORGE APP                         │   │
│  │         (Runs in Atlassian's secure environment)         │   │
│  │                                                          │   │
│  │  • Atlassian-managed infrastructure                      │   │
│  │  • Forge sandbox isolation                               │   │
│  │  • HMAC-authenticated API calls                          │   │
│  └─────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────┘
                              │
                    HMAC-Signed Requests
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                      GOOGLE CLOUD                               │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                    CORE API                              │   │
│  │              (Cloud Run + Cloud SQL)                     │   │
│  │                                                          │   │
│  │  • TLS 1.3 encryption                                    │   │
│  │  • Firebase Authentication                               │   │
│  │  • Role-based access control                             │   │
│  │  • Encrypted database                                    │   │
│  └─────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────┘
                              │
                      Firebase Auth
                              │
              ┌───────────────┴───────────────┐
              ▼                               ▼
┌─────────────────────────┐     ┌─────────────────────────┐
│     CLIENT PORTAL       │     │      DELIVERY APP       │
│   (Firebase Hosting)    │     │   (Firebase Hosting)    │
│                         │     │                         │
│  • JWT authentication   │     │  • JWT authentication   │
│  • Client-scoped data   │     │  • Role-scoped data     │
└─────────────────────────┘     └─────────────────────────┘
```

---

## Authentication

### Forge App (Jira Users)

The Forge app authenticates users through Atlassian's built-in mechanisms:

| Method | Description |
|--------|-------------|
| **Atlassian Identity** | Users authenticate via their Atlassian account |
| **Session Management** | Handled by Atlassian—no separate login |
| **Permission Inheritance** | Access based on Jira site permissions |

When the Forge app communicates with our Core API, it uses **HMAC authentication**:
- Each request is signed with a shared secret
- Timestamp prevents replay attacks
- Cloud ID verification ensures tenant isolation

### Client Portal

Portal users authenticate via Firebase Authentication:

| Method | Description |
|--------|-------------|
| **Email/Password** | Standard credential-based authentication |
| **Secure Sessions** | Firebase-managed session tokens |
| **Portal Links** | JWT tokens for initial account association |

Portal link tokens:
- Time-limited (configurable expiration)
- Single-purpose (account association only)
- Client-scoped (links to specific client)

### Delivery App

Leadership users authenticate via Firebase Authentication:

| Method | Description |
|--------|-------------|
| **Email/Password** | Standard credential-based authentication |
| **Invite Links** | Controlled access via admin-generated invites |
| **Role Verification** | Access level validated on each request |

---

## Authorization

### Role-Based Access Control (RBAC)

Milestone implements role-based access at multiple levels:

**Forge App Roles:**

| Role | Access Level |
|------|--------------|
| **Admin** | Full access—user management, configuration, all features |
| **Member** | Operational access—queue, assignments, messaging, insights |

**Portal Access:**

| Scope | Access |
|-------|--------|
| **Client-Scoped** | Users see only their company's data |
| **Request-Scoped** | Can only view/interact with own client's requests |

**Delivery App Access:**

| Level | Access |
|-------|--------|
| **Granted Users** | Access to executive dashboards for their organization |
| **Cloud-Scoped** | Data limited to their Atlassian cloud instance |

### Permission Enforcement

Permissions are enforced at multiple layers:
1. **API Layer** — Every request validated against user's role
2. **Database Layer** — Queries scoped to authorized data
3. **UI Layer** — Features hidden/disabled based on permissions

---

## Data Encryption

### Encryption in Transit

All data transmission uses strong encryption:

| Connection | Encryption |
|------------|------------|
| Browser ↔ Portal/Delivery | TLS 1.3 |
| Browser ↔ Forge App | TLS (Atlassian-managed) |
| Forge App ↔ Core API | TLS 1.3 + HMAC signatures |
| Core API ↔ Database | TLS 1.3 (Google-managed) |

### Encryption at Rest

Stored data is encrypted:

| Storage | Encryption |
|---------|------------|
| **Cloud SQL (PostgreSQL)** | AES-256 encryption (Google-managed keys) |
| **Firebase Storage** | AES-256 encryption (Google-managed keys) |
| **Backups** | Encrypted with same standards |

---

## Client Data Isolation

### Tenant Isolation

Each Atlassian Cloud instance (tenant) is isolated:

- **Cloud ID Scoping** — All queries include cloud_id filter
- **No Cross-Tenant Access** — Users cannot access other tenants' data
- **API Validation** — Every request verified against authenticated tenant

### Client Isolation Within Tenant

Within a tenant, client data is isolated:

- **Client UUID Scoping** — Requests filtered by client association
- **Portal Isolation** — Portal users see only their client's data
- **No Client Crossover** — One client cannot see another's requests

### Database-Level Isolation

```sql
-- Example: All queries are scoped
SELECT * FROM requests 
WHERE cloud_id = [authenticated_cloud_id]
  AND client_uuid = [authorized_client_id]
```

---

## Atlassian Forge Security

The Forge app runs within Atlassian's secure environment:

### Forge Sandbox

- **Isolated Execution** — App code runs in isolated containers
- **No Direct Server Access** — Cannot access Atlassian infrastructure
- **Scoped Permissions** — Only granted permissions are available
- **Atlassian Reviewed** — Apps reviewed for security compliance

### Forge Permissions

Milestone requests only necessary permissions:

| Permission | Purpose |
|------------|---------|
| Read issues | View request data |
| Write issues | Create/update requests |
| Read worklogs | Sync hours tracking |
| Read users | User identification |

### External Communication

Forge apps can only communicate with declared external services:
- All external URLs declared in manifest
- Connections use secure protocols
- No unauthorized external access

---

## API Security

### HMAC Authentication (Forge ↔ Core API)

```
Request Flow:
1. Forge app creates request payload
2. Generates HMAC signature using shared secret
3. Includes timestamp in request
4. Core API verifies signature and timestamp
5. Rejects if signature invalid or timestamp stale
```

### JWT Authentication (Portal/Delivery ↔ Core API)

```
Request Flow:
1. User authenticates via Firebase
2. Receives JWT token
3. Token included in API requests
4. Core API validates token with Firebase
5. Extracts user identity and permissions
```

### Rate Limiting

API endpoints are protected against abuse:
- Request rate limits per user/tenant
- Automatic throttling for excessive requests
- Protection against denial-of-service

---

## Security Best Practices for Users

### For Administrators

1. **Limit Admin Access** — Only grant admin role when necessary
2. **Review Users Regularly** — Audit who has access
3. **Use Strong Passwords** — Enforce password policies
4. **Monitor Access** — Watch for unusual patterns

### For Portal Link Management

1. **Set Appropriate Expiration** — Don't use overly long expiration
2. **Share Securely** — Send links via secure channels
3. **Regenerate If Compromised** — Create new links if security concern
4. **Track Distribution** — Know who received which links

### For All Users

1. **Protect Credentials** — Never share passwords
2. **Sign Out When Done** — Especially on shared devices
3. **Report Suspicious Activity** — Contact admin if something seems wrong

---

## Incident Response

### Reporting Security Issues

If you discover a security vulnerability:

**Email:** security@getmilestone.io

Include:
- Description of the vulnerability
- Steps to reproduce (if applicable)
- Your contact information

### Our Commitment

- Acknowledge receipt within 24 hours
- Investigate promptly
- Keep you informed of progress
- Credit reporters (if desired) when issues are resolved

---

## Compliance

### Infrastructure Compliance

Milestone leverages compliant infrastructure:

| Provider | Certifications |
|----------|---------------|
| **Google Cloud** | SOC 1/2/3, ISO 27001, HIPAA, FedRAMP |
| **Atlassian Cloud** | SOC 2, ISO 27001, GDPR compliant |
| **Firebase** | SOC 1/2/3, ISO 27001 |

### Data Handling

- GDPR considerations addressed
- Data minimization practiced
- User rights supported
- See [Privacy Overview](privacy-overview.md) for details

---

## Security Updates

We continuously improve security:

- Regular dependency updates
- Security patch prioritization
- Ongoing security reviews
- Industry best practice adoption

---

## Questions

For security questions or concerns:

- **General Security:** security@getmilestone.io
- **Privacy Concerns:** privacy@getmilestone.io
- **Support:** support@getmilestone.io

---

## Related Documentation

- **[Privacy Overview](privacy-overview.md)** — Data collection and privacy
- **[Data Residency](data-residency.md)** — Where data is stored
- **[Roles](../04-admin/roles.md)** — Permission management

---

*For the most current security information, visit https://getmilestone.io/security*
