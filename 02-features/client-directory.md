# Client Directory

The Client Directory is your central hub for managing all client relationships in Milestone. From here, you add new clients, configure their SLA settings, manage hour banks, and generate portal access links—everything needed to set up and maintain client accounts.

---

## Why Client Directory Matters

### Before Milestone
- Client information scattered across spreadsheets, CRM, and tribal knowledge
- SLA configurations buried in contracts nobody reads
- Hour tracking done manually in separate systems
- Portal links generated through complex processes

### With Client Directory
- Single source of truth for all client configurations
- Visual SLA and hours status at a glance
- One-click portal link generation
- Bulk import for efficient onboarding

---

## Accessing Client Directory

1. Open the Milestone app in Jira
2. Click **Client Directory** in the sidebar (folder icon)
3. You'll see the client list with tabs for different functions

---

## Interface Overview

### Tabs

| Tab | Purpose |
|-----|---------|
| **Client List** | View and manage all clients |
| **Bulk Import** | Import multiple clients via CSV |
| **Portal Access** | Generate portal invitation links |
| **Settings** | Configure selected client (appears when client selected) |

### Client Cards

Each client in the list shows:

| Element | Description |
|---------|-------------|
| **Name** | Client company name |
| **Project Key** | Linked Jira project |
| **Issue Type** | Default issue type for requests |
| **SLA Status** | Indicator showing SLA configuration |
| **Hours** | Purchased/consumed/remaining |

---

## Managing Clients

### Adding a New Client

1. Click **+ Add Client** button
2. Fill in the required fields:
   - **Client ID**: Unique identifier (auto-generated or custom)
   - **Name**: Client company name
   - **Project Key**: Jira project to link requests to
   - **Default Issue Type**: What type of issue to create (Task, Bug, etc.)
   - **Default Assignee**: Optional—auto-assign new requests
3. Click **Save**

The client is now ready to receive requests.

### Editing a Client

1. Find the client in the list
2. Click the **Edit** icon (pencil) or three-dot menu
3. Modify the fields as needed
4. Click **Save**

### Deleting a Client

⚠️ **Warning:** Deleting a client removes their configuration. Historical requests remain but lose client association.

1. Find the client in the list
2. Click the three-dot menu
3. Select **Delete**
4. Confirm the deletion

### Searching Clients

Use the search box to filter the client list:
- Search by name
- Search by project key
- Results update as you type

### Sorting Clients

Click column headers to sort:
- **Name**: Alphabetical
- **Project Key**: By Jira project
- **SLA**: By SLA configuration status

Click again to reverse sort direction.

---

## SLA Configuration

### Cloud-Level Defaults

Set SLAs that apply to all clients unless overridden:

1. Go to **Settings** in the Client Directory (without a client selected)
2. Find **SLA Settings**
3. Configure:
   - **Response Time**: Hours to first response (e.g., 4)
   - **Resolution Time**: Hours to completion (e.g., 24)
   - **Operating Hours**: When SLAs count (24/7 or business hours)
4. Save

### Per-Client SLA Overrides

Give VIP clients tighter SLAs:

1. Select a client from the list
2. Go to the **Settings** tab
3. Find **SLA Override**
4. Enter custom response and resolution times
5. Save

**Priority:** Client override > Cloud default

### SLA Indicators

In the client list, SLA status shows:

| Indicator | Meaning |
|-----------|---------|
| ✓ **Configured** | Client has specific SLA settings |
| **Default** | Using cloud-level defaults |
| ⚠️ **Not Set** | No SLA configured (needs attention) |

---

## Hour Banks

### Understanding Hours

| Term | Definition |
|------|------------|
| **Purchased** | Total hours allocated to the client |
| **Consumed** | Hours used (from Jira worklogs) |
| **Remaining** | Purchased minus consumed |

### Setting Purchased Hours

1. Select a client
2. Go to **Settings** tab
3. Find **Hours Purchased** field
4. Enter the total hours (e.g., 40)
5. Save

### Adjusting Hours

When a client buys more hours:
1. Go to their settings
2. Increase the **Hours Purchased** value
3. Save

The remaining balance updates automatically.

### Hours Display in Client List

Each client card shows hours at a glance:
```
40h purchased | 25h consumed | 15h remaining
```

Color coding indicates status:
- 🟢 **Green**: Plenty remaining (>25%)
- 🟡 **Yellow**: Running low (10-25%)
- 🔴 **Red**: Very low or negative (<10%)

---

## Portal Link Generation

### What Portal Links Do

Portal links allow your clients' employees to:
- Access the Client Portal
- Submit and track requests
- View SLA timers and hours
- Communicate via Messenger

No Jira license required—just the link.

### Generating a Portal Link

1. Go to the **Portal Access** tab
2. Select the client
3. Configure options:
   - **Expiration**: How long the link is valid (default: 90 days)
   - **Company Name**: Display name in the portal
4. Click **Generate Link**
5. Copy the generated link

### Link Formats

The generator provides multiple formats:

| Format | Use Case |
|--------|----------|
| **Direct Link** | Share via email or message |
| **HTML Link** | Embed in a webpage |
| **iFrame** | Embed portal in another site |

### Sharing Portal Links

Send the link to your client contacts:
- Email with brief instructions
- Include in welcome documentation
- Add to client onboarding checklist

### Link Security

- Links are scoped to a specific client
- Users can only see their own client's requests
- Links expire after the configured period
- Generate new links as needed

---

## Bulk Import

### When to Use Bulk Import

- Onboarding many clients at once
- Migrating from another system
- Setting up a new Milestone instance

### CSV Format

Prepare a CSV file with these columns:

```csv
client_id,name,project_key,default_issue_type,default_assignee
acme-001,Acme Corporation,ACME,Task,john@example.com
globex-001,Globex Inc,GLOB,Support,
initech-001,Initech LLC,INIT,Bug,jane@example.com
```

**Required columns:**
- `client_id`: Unique identifier
- `name`: Client name
- `project_key`: Jira project key

**Optional columns:**
- `default_issue_type`: Issue type (defaults to Task)
- `default_assignee`: Auto-assignee email (optional)

### Import Process

1. Go to the **Bulk Import** tab
2. Click **Choose File** or drag and drop CSV
3. Review the preview showing what will be imported
4. Click **Import**
5. Review results for any errors

### Handling Import Errors

Common issues:
- **Duplicate client_id**: Client already exists
- **Invalid project_key**: Jira project doesn't exist
- **Missing required field**: Add the missing data

Fix errors in your CSV and re-import the failed rows.

---

## Best Practices

### Client Setup Checklist

For each new client:

- [ ] Add client with correct Jira project
- [ ] Configure SLA override (if needed)
- [ ] Set purchased hours
- [ ] Generate portal link
- [ ] Send welcome communication

### Naming Conventions

Use consistent client naming:
- ✅ "Acme Corporation" (formal name)
- ❌ "acme" (too informal)
- ❌ "ACME CORP" (inconsistent caps)

### Project Key Strategy

Consider how Jira projects map to clients:
- **1:1**: One project per client (cleanest)
- **1:many**: Multiple clients share a project (use with caution)

### Regular Maintenance

| Frequency | Task |
|-----------|------|
| Weekly | Review hour balances |
| Monthly | Audit SLA configurations |
| Quarterly | Clean up inactive clients |
| As needed | Regenerate expiring portal links |

---

## Common Scenarios

### Scenario 1: New Client Onboarding

1. Create Jira project for the client
2. Add client to Client Directory
3. Set SLA override if VIP
4. Set purchased hours
5. Generate portal link
6. Send welcome email with link

### Scenario 2: Client Needs More Hours

1. Client contacts you about running low
2. Go to Client Directory
3. Select the client → Settings
4. Increase Hours Purchased
5. Confirm with client

### Scenario 3: VIP Client Needs Faster SLAs

1. Go to Client Directory
2. Select the VIP client
3. Settings → SLA Override
4. Set tighter times (e.g., 1h response, 4h resolution)
5. Save
6. Inform team of VIP expectations

### Scenario 4: Portal Link Expired

1. Client reports they can't access portal
2. Go to Client Directory → Portal Access
3. Select the client
4. Generate new link
5. Send updated link to client

---

## Common Mistakes to Avoid

### ❌ Wrong Jira Project

Linking to wrong project = requests go to wrong place.

**Fix:** Double-check project key before saving.

### ❌ Forgetting SLA Setup

Client requests have no SLA tracking.

**Fix:** Always configure at least cloud defaults.

### ❌ Not Setting Hours

Hours balance shows negative unexpectedly.

**Fix:** Set hours purchased during onboarding.

### ❌ Short Portal Link Expiration

Links expire, clients locked out.

**Fix:** Use 90+ day expiration; track renewal.

### ❌ Inconsistent Naming

Hard to find clients in searches.

**Fix:** Establish and follow naming conventions.

---

## Troubleshooting

### Can't find a client

1. Clear search filters
2. Check spelling
3. Verify client was added

### SLA not applying

1. Check client has SLA override or cloud default set
2. Verify the request is linked to this client
3. Refresh and check SLA tracking

### Hours not updating

1. Verify worklogs are on correct Jira issue
2. Check issue is linked to client request
3. Allow a few seconds for sync

### Portal link not working

1. Check if link expired
2. Generate a new link
3. Verify client ID is correct

---

## Related Documentation

- **[SLA Tracking](sla-tracking.md)** — How SLAs work in detail
- **[Hours Tracking](hours-tracking.md)** — Worklog to hours flow
- **[Portal Overview](../03-client-portal/portal-overview.md)** — Client portal features

---

*Next: [Portal Overview →](../03-client-portal/portal-overview.md)*
