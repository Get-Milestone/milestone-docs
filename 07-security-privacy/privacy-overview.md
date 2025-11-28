# Privacy Overview

Milestone is committed to protecting the privacy of your data and your clients' data. This document explains what data we collect, how we use it, and your rights regarding that data.

---

## Our Privacy Principles

1. **Data Minimization** — We collect only what's necessary to provide the service
2. **Purpose Limitation** — Data is used only for its intended purpose
3. **Transparency** — Clear communication about data practices
4. **User Control** — You control your data and can request changes
5. **Security First** — All data protected with strong security measures

---

## Data We Collect

### From MSP Users (Forge App)

| Data Type | Purpose | Source |
|-----------|---------|--------|
| **Atlassian Account ID** | User identification | Atlassian |
| **Display Name** | Show who's working requests | Atlassian |
| **Email Address** | User identification, notifications | Atlassian |
| **Role Assignment** | Permission management | Milestone configuration |
| **Activity Logs** | Audit trail, debugging | User actions |

### From Portal Users (End Clients)

| Data Type | Purpose | Source |
|-----------|---------|--------|
| **Email Address** | Authentication, notifications | User-provided |
| **Name** | Display in communications | User-provided |
| **Company Association** | Link to correct client | Portal link |
| **Request Content** | Service delivery | User-submitted |
| **Messages** | Communication with MSP | User-submitted |

### From Delivery App Users

| Data Type | Purpose | Source |
|-----------|---------|--------|
| **Email Address** | Authentication | User-provided |
| **Name** | Display purposes | User-provided |
| **Organization Link** | Access control | Admin configuration |

### System-Generated Data

| Data Type | Purpose |
|-----------|---------|
| **Request Metadata** | SLA tracking, reporting |
| **Timestamps** | Audit trail, SLA calculation |
| **Hours Logged** | Synced from Jira worklogs |
| **SLA Metrics** | Performance reporting |

---

## How We Use Data

### Service Delivery

- Processing and tracking service requests
- SLA monitoring and alerting
- Hours consumption tracking
- Real-time messaging between parties
- Performance reporting and insights

### Communication

- System notifications (if enabled)
- Service updates
- Security alerts

### Service Improvement

- Aggregated, anonymized analytics
- Performance optimization
- Feature development prioritization

### We Do NOT

- ❌ Sell your data to third parties
- ❌ Use data for advertising
- ❌ Share individual data across tenants
- ❌ Access your data without legitimate purpose
- ❌ Retain data longer than necessary

---

## Data Sharing

### With Your Organization

Within your Atlassian cloud instance:
- Team members see requests based on permissions
- Admins have broader access for management
- Clients see only their own data

### With Third-Party Services

We use the following services to provide Milestone:

| Service | Purpose | Data Shared |
|---------|---------|-------------|
| **Google Cloud Platform** | Infrastructure hosting | All service data (encrypted) |
| **Firebase** | Authentication, hosting | User credentials, session data |
| **Atlassian** | Forge app platform | Jira integration data |

These providers are bound by their privacy policies and our data processing agreements.

### We Do Not Share

- Individual user data with unrelated third parties
- Data across different MSP tenants
- Data for marketing or advertising purposes

---

## Data Retention

### Active Data

| Data Type | Retention |
|-----------|-----------|
| **User Accounts** | While account is active |
| **Requests** | While tenant is active |
| **Messages** | While associated request exists |
| **Hours Data** | While tenant is active |
| **Audit Logs** | 12 months rolling |

### After Account/Tenant Deletion

| Timeline | Action |
|----------|--------|
| **Immediate** | Access disabled |
| **30 days** | Data marked for deletion |
| **90 days** | Data permanently removed from primary systems |
| **Backups** | Cycled out per backup retention schedule |

### Backup Retention

- Daily backups: 7 days
- Weekly backups: 4 weeks
- Monthly backups: 3 months

---

## Your Rights

### For All Users

You have the right to:

| Right | Description |
|-------|-------------|
| **Access** | Request a copy of your personal data |
| **Correction** | Request correction of inaccurate data |
| **Deletion** | Request deletion of your personal data |
| **Portability** | Receive your data in a standard format |
| **Objection** | Object to certain data processing |

### How to Exercise Your Rights

1. **Contact your MSP administrator** for most requests
2. **Email privacy@getmilestone.io** for direct requests
3. **Include** your email address and specific request
4. **Verification** may be required to protect your data

### Response Timeline

- Acknowledge request: Within 3 business days
- Complete request: Within 30 days (may extend for complex requests)

---

## Data Subject Types

### MSP Team Members

Your data is primarily managed through your Atlassian account:
- Profile changes: Update in Atlassian
- Role changes: Request from your admin
- Account deletion: Contact your Jira admin

### Portal Users (End Clients)

Your data is managed through the portal:
- Profile changes: Update in portal settings
- Account deletion: Request from your MSP
- Data export: Request from your MSP

### Delivery App Users

Your data is managed through the app:
- Profile changes: Update in app settings
- Account deletion: Request from your MSP admin
- Data export: Contact privacy@getmilestone.io

---

## Client Data Isolation

### Multi-Tenant Architecture

Each MSP operates in an isolated environment:

```
MSP Tenant A ──┬── Client 1 data
               ├── Client 2 data
               └── Client 3 data

MSP Tenant B ──┬── Client X data    (completely separate)
               └── Client Y data
```

### Guarantees

- No data leakage between MSP tenants
- No data leakage between clients within a tenant
- Access controls enforced at every layer
- Regular security audits verify isolation

---

## Children's Privacy

Milestone is a business service not intended for children:

- We do not knowingly collect data from children under 16
- If we discover such data, we will delete it promptly
- Parents/guardians can contact us about any concerns

---

## International Data Transfers

### Current Practices

- Primary data storage: United States
- See [Data Residency](data-residency.md) for details

### Transfer Mechanisms

For data transferred internationally:
- Standard Contractual Clauses where applicable
- Privacy Shield principles (where applicable)
- Adequate safeguards per applicable law

---

## Cookies and Tracking

### Portal and Delivery App

| Cookie Type | Purpose | Duration |
|-------------|---------|----------|
| **Session** | Authentication state | Session |
| **Preferences** | User settings | Persistent |

### What We Don't Do

- ❌ Third-party advertising cookies
- ❌ Cross-site tracking
- ❌ Behavioral profiling for ads

### Forge App

The Forge app runs within Atlassian's environment:
- Cookies managed by Atlassian
- Subject to Atlassian's cookie policy

---

## Updates to This Policy

### How We Notify

When privacy practices change:
- Update this documentation
- Notify administrators via email (for material changes)
- Post notice in the application (for significant changes)

### Your Continued Use

Continued use after changes constitutes acceptance. For material changes, we may request explicit acknowledgment.

---

## Contact Information

### Privacy Inquiries

**Email:** privacy@getmilestone.io

Include:
- Your name and email
- Nature of your request
- Relevant details

### Data Protection Officer

For GDPR-related inquiries:
**Email:** dpo@getmilestone.io

### General Support

**Email:** support@getmilestone.io

---

## Regulatory Compliance

### GDPR (European Union)

If you're in the EU or processing EU residents' data:
- Milestone acts as a data processor
- Your MSP is the data controller
- Standard Contractual Clauses available
- DPA available upon request

### CCPA (California)

If you're a California resident:
- Right to know what data is collected
- Right to delete personal information
- Right to opt-out of sale (we don't sell data)
- No discrimination for exercising rights

### Other Regulations

We strive to comply with applicable privacy regulations. Contact us for specific compliance questions.

---

## Related Documentation

- **[Security Overview](security-overview.md)** — How we protect your data
- **[Data Residency](data-residency.md)** — Where data is stored
- **[Roles](../04-admin/roles.md)** — Access control within Milestone

---

*For the most current privacy information, visit https://getmilestone.io/privacy*
