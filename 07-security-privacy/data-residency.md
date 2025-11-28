# Data Residency

This document details where Milestone stores your data and the infrastructure supporting our service. Understanding data residency is important for compliance, regulatory requirements, and organizational policies.

---

## Current Data Locations

### Primary Infrastructure

All Milestone data is currently hosted in the **United States**:

| Component | Location | Provider |
|-----------|----------|----------|
| **Core API** | US (Google Cloud) | Cloud Run |
| **Database** | US (Google Cloud) | Cloud SQL (PostgreSQL) |
| **Portal/Delivery App** | US (Global CDN) | Firebase Hosting |
| **Authentication** | US (Global) | Firebase Auth |
| **File Storage** | US (Google Cloud) | Cloud Storage |

### Specific Regions

| Service | Region | Details |
|---------|--------|---------|
| **Cloud SQL** | us-central1 (Iowa) | Primary database |
| **Cloud Run** | us-central1 (Iowa) | API servers |
| **Firebase** | us-central1 | Auth and hosting origin |

---

## Data Flow

### Where Data Travels

```
User Browser (Anywhere)
        │
        │ HTTPS (TLS 1.3)
        ▼
┌─────────────────────────────────┐
│   Firebase CDN / Cloud CDN      │
│   (Global Edge Locations)       │
│   - Static assets cached        │
│   - No persistent data stored   │
└─────────────────────────────────┘
        │
        │ HTTPS (TLS 1.3)
        ▼
┌─────────────────────────────────┐
│   Google Cloud - US Central     │
│   (Iowa, United States)         │
│                                 │
│   - Core API processing         │
│   - Database storage            │
│   - All persistent data         │
└─────────────────────────────────┘
```

### Edge Caching

| What's Cached | Where | Data Type |
|---------------|-------|-----------|
| Static assets (JS, CSS, images) | Global CDN edges | Non-sensitive |
| API responses | Not cached | N/A |
| User data | US only | Sensitive |

**Note:** Actual user data and API responses are not cached at edge locations. Only static application assets are distributed globally for performance.

---

## Atlassian Integration

### Forge App Data

The Milestone Forge app runs within Atlassian's infrastructure:

| Data Type | Location |
|-----------|----------|
| **App Code** | Atlassian Cloud (varies by your Atlassian region) |
| **Jira Data** | Your Atlassian data residency setting |
| **Milestone Data** | US (Google Cloud) |

### Your Atlassian Data

Your Jira issues, worklogs, and user data remain in your Atlassian instance according to your Atlassian data residency configuration. Milestone reads this data but stores its own copy for service functionality.

### Data Synchronization

When the Forge app syncs data:
1. Reads from your Atlassian instance
2. Transmits via secure, encrypted connection
3. Stores in our US-based infrastructure

---

## Backup and Recovery

### Backup Locations

| Backup Type | Location | Encryption |
|-------------|----------|------------|
| **Daily Backups** | US (same region) | AES-256 |
| **Point-in-Time Recovery** | US (same region) | AES-256 |
| **Disaster Recovery** | US (different zone) | AES-256 |

### Geographic Redundancy

Within the US region:
- Multiple availability zones
- Automatic failover
- No cross-region replication currently

---

## Compliance Considerations

### Regulations by Region

| Regulation | Applicability | Milestone Approach |
|------------|---------------|-------------------|
| **GDPR (EU)** | EU data subjects | SCCs available, DPA on request |
| **CCPA (California)** | CA residents | Privacy rights supported |
| **HIPAA (US Healthcare)** | Healthcare data | Not currently HIPAA certified |
| **SOC 2** | General | Infrastructure providers certified |

### For EU-Based Organizations

If your organization is in the EU or processes EU residents' data:

**Current status:**
- Data stored in US
- Standard Contractual Clauses (SCCs) available
- Data Processing Agreement (DPA) available on request

**Considerations:**
- Review with your legal/compliance team
- SCCs provide legal mechanism for EU→US transfer
- Contact us for specific compliance documentation

### For Organizations with Data Residency Requirements

If your organization requires data to stay in a specific region:

1. **Review current architecture** — All data is US-based
2. **Assess requirements** — Determine if US hosting meets your needs
3. **Contact us** — Discuss your specific requirements
4. **Consider timeline** — Regional expansion is planned (see below)

---

## Future Regional Expansion

### Planned Regions

We are planning to expand to additional regions:

| Region | Status | Estimated Timeline |
|--------|--------|-------------------|
| **United States** | ✅ Available | Current |
| **European Union** | 🔜 Planned | TBD |
| **Australia** | 📋 Under consideration | TBD |

### What Regional Expansion Means

When available:
- Data stored entirely within chosen region
- No cross-region data transfer for operations
- Regional compliance requirements addressed

### Request Regional Support

To express interest in a specific region:

**Email:** support@getmilestone.io

Include:
- Your organization
- Required region
- Compliance requirements
- Timeline needs

---

## Data Sovereignty

### What We Guarantee

- All persistent data stored in declared region (currently US)
- Data does not replicate to undeclared regions
- Access controls prevent unauthorized regional access

### What We Cannot Control

- CDN edge caching of static assets (non-sensitive)
- Network routing of requests (transient)
- Your users' browser locations

---

## Infrastructure Providers

### Google Cloud Platform

| Certification | Status |
|---------------|--------|
| SOC 1 | ✅ |
| SOC 2 | ✅ |
| SOC 3 | ✅ |
| ISO 27001 | ✅ |
| ISO 27017 | ✅ |
| ISO 27018 | ✅ |
| FedRAMP | ✅ |
| HIPAA | ✅ (BAA available) |

### Firebase (Google)

| Certification | Status |
|---------------|--------|
| SOC 1 | ✅ |
| SOC 2 | ✅ |
| ISO 27001 | ✅ |

### Atlassian Cloud

| Certification | Status |
|---------------|--------|
| SOC 2 | ✅ |
| ISO 27001 | ✅ |
| GDPR | ✅ Compliant |

---

## Requesting Compliance Documentation

### Available Documents

| Document | How to Obtain |
|----------|---------------|
| **Data Processing Agreement (DPA)** | Request via support@getmilestone.io |
| **Standard Contractual Clauses (SCCs)** | Request via support@getmilestone.io |
| **Security Questionnaire** | Request via security@getmilestone.io |
| **SOC 2 Reports (infrastructure)** | Via provider documentation |

### Custom Requirements

For specific compliance needs:
1. Contact support@getmilestone.io
2. Describe your requirements
3. We'll work with you on documentation

---

## Questions

### General Residency Questions

**Email:** support@getmilestone.io

### Compliance and Legal

**Email:** legal@getmilestone.io

### Security Concerns

**Email:** security@getmilestone.io

---

## Related Documentation

- **[Security Overview](security-overview.md)** — Security measures
- **[Privacy Overview](privacy-overview.md)** — Data handling practices

---

*For the most current data residency information, visit https://getmilestone.io/data-residency*
