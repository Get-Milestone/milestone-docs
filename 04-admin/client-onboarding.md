# Client Onboarding

This guide walks through the complete process of onboarding a new client to Milestone—from initial setup to their first request.

---

## Onboarding Overview

Adding a new client involves:

1. **Prepare Jira Project** — Create or identify the project for this client
2. **Add Client to Milestone** — Create the client record
3. **Configure SLA** — Set appropriate service levels
4. **Set Hours** — Configure their hour bank (if applicable)
5. **Generate Portal Access** — Create invitation link
6. **Welcome the Client** — Send access and instructions

**Time required:** 10-15 minutes per client

---

## Step 1: Prepare Jira Project

Each client needs a Jira project where their requests become issues.

### Option A: One Project Per Client (Recommended)

**Benefits:**
- Clean separation of client work
- Simple permission management
- Clear reporting boundaries

**Setup:**
1. Create a new Jira project
2. Use client name or abbreviation as key (e.g., ACME)
3. Configure issue types as needed
4. Set up any workflows

### Option B: Shared Project

**Benefits:**
- Fewer projects to manage
- Shared workflows

**Considerations:**
- Use labels or custom fields to identify client
- More complex reporting
- Permission complexity

**Recommendation:** Start with one project per client unless you have a specific reason to share.

---

## Step 2: Add Client to Milestone

### Open Client Directory

1. Open Milestone in Jira
2. Click **Client Directory** in the sidebar
3. Click **+ Add Client**

### Fill in Client Information

| Field | What to Enter | Example |
|-------|---------------|---------|
| **Client ID** | Unique identifier (lowercase, no spaces) | acme-corp |
| **Name** | Official company name | Acme Corporation |
| **Project Key** | Jira project key | ACME |
| **Default Issue Type** | Issue type for new requests | Task |
| **Default Assignee** | Auto-assign to someone (optional) | john@yourcompany.com |

### Client ID Best Practices

Choose consistent, meaningful IDs:
- ✅ `acme-corp` — Clear, formatted
- ✅ `globex-inc` — Consistent style
- ❌ `Client1` — Not descriptive
- ❌ `AcMe CoRp` — Inconsistent formatting

### Save the Client

Click **Save** to create the client record.

---

## Step 3: Configure SLA

Decide whether this client uses default SLAs or needs custom ones.

### Using Default SLAs

If this client should use your cloud-level defaults:
- No additional configuration needed
- They automatically inherit default response/resolution times

### Setting Client-Specific SLA

For VIP clients or specific contracts:

1. Select the client in Client Directory
2. Go to the **Settings** tab
3. Find **SLA Override**
4. Enter custom times:
   - **Response Time**: Hours until first response required
   - **Resolution Time**: Hours until completion required
5. Save

### Common SLA Configurations

| Client Type | Response | Resolution | Notes |
|-------------|----------|------------|-------|
| Standard | 4 hours | 24 hours | Default for most |
| Premium | 2 hours | 8 hours | Higher-paying clients |
| Enterprise | 1 hour | 4 hours | Critical accounts |
| Low-touch | 8 hours | 48 hours | Budget-conscious |

---

## Step 4: Set Hours

If this client has a purchased hour bank:

### Configure Hours

1. Select the client in Client Directory
2. Go to **Settings** tab
3. Find **Hours Purchased**
4. Enter total hours (e.g., 40)
5. Save

### Hours Considerations

- Set initial hours based on contract
- Hours can be increased anytime
- Consumed hours track automatically from worklogs
- Set to 0 if not tracking hours for this client

---

## Step 5: Generate Portal Access

Create the link for client portal access.

### Generate the Link

1. Go to **Client Directory** → **Portal Access** tab
2. Select the client from dropdown
3. Configure:
   - **Company Name**: How they appear in portal (usually same as client name)
   - **Expiration**: 90 days recommended for initial setup
4. Click **Generate Link**
5. Copy the link

### Save the Link

Record the link somewhere accessible:
- Your CRM
- Client record in your system
- Secure team document

---

## Step 6: Welcome the Client

Send the client their portal access with clear instructions.

### Welcome Email Template

```
Subject: Welcome to Your Service Portal

Hi [Client Contact Name],

Welcome to [Your Company Name]! We're excited to have you as a client.

We've set up your service portal where you can:
• Submit new service requests
• Track the status of your requests in real-time
• See your SLA timers and commitments
• View your hours usage
• Message our team directly

ACCESS YOUR PORTAL
[Portal Link]

Click the link above to create your account—it only takes a minute.

YOUR SERVICE AGREEMENT
• Response Time: [X] hours
• Resolution Time: [X] hours
• Purchased Hours: [X] hours

WHAT'S NEXT
1. Click the link and create your account
2. Explore your portal dashboard
3. Submit your first request when you're ready
4. We'll be here to help!

Questions? Just reply to this email.

Best,
[Your Name]
[Your Company]
```

### Follow-Up

After sending:
- Track if client accessed portal (first request activity)
- Follow up in 2-3 days if no activity
- Offer a quick walkthrough call if helpful

---

## Onboarding Checklist

Use this checklist for each new client:

### Pre-Setup
- [ ] Contract signed
- [ ] Client contact information gathered
- [ ] Service level agreed upon
- [ ] Hours allocation determined

### Technical Setup
- [ ] Jira project created/identified
- [ ] Project key confirmed
- [ ] Issue types configured

### Milestone Setup
- [ ] Client added to Client Directory
- [ ] Project key linked correctly
- [ ] SLA override configured (if needed)
- [ ] Hours purchased set (if applicable)

### Access Setup
- [ ] Portal link generated
- [ ] Link expiration set appropriately
- [ ] Link recorded in your systems

### Client Communication
- [ ] Welcome email sent with portal link
- [ ] Service levels documented in email
- [ ] Contact information for questions provided
- [ ] Follow-up scheduled

### Verification
- [ ] Client confirmed portal access
- [ ] Test request created and processed
- [ ] Client understands how to use portal

---

## Bulk Onboarding

For multiple clients at once:

### CSV Import

1. Prepare CSV with required columns:
   ```
   client_id,name,project_key,default_issue_type
   ```
2. Go to Client Directory → **Bulk Import** tab
3. Upload CSV
4. Review and confirm import
5. Address any errors

### Then for Each Client

After bulk import, still need to:
- Configure SLA overrides individually
- Set hours purchased individually
- Generate portal links individually
- Send welcome communications

---

## Common Onboarding Issues

### Wrong Jira Project Linked

**Problem:** Requests going to wrong project

**Fix:**
1. Edit the client
2. Update the Project Key
3. Save
4. New requests go to correct project

### Client Not Seeing Portal

**Problem:** Portal link not working

**Fix:**
1. Check link expiration
2. Generate new link
3. Resend to client
4. Verify they're using full URL

### SLA Not Applying

**Problem:** Requests show no SLA

**Fix:**
1. Verify cloud defaults are set
2. Check client SLA override settings
3. Ensure settings were saved

---

## Related Documentation

- **[Client Directory](../02-features/client-directory.md)** — Full client management guide
- **[Portal Links](../03-client-portal/portal-links.md)** — Detailed portal link info
- **[SLA Tracking](../02-features/sla-tracking.md)** — Understanding SLAs
- **[Roles](roles.md)** — User access for onboarding

---

*Next: [SLA Defaults →](sla-defaults.md)*
