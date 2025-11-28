# First-Time Setup

After installing Milestone, follow this guide to configure your instance for your MSP's needs. This setup process takes about 15-30 minutes and establishes the foundation for everything else.

---

## Setup Checklist

Complete these steps in order:

- [ ] **1. Access Milestone** — Open the app and verify installation
- [ ] **2. Configure SLA Defaults** — Set your standard service levels
- [ ] **3. Add Your First Client** — Create a client entry
- [ ] **4. Set Up Team Access** — Configure admin users
- [ ] **5. Generate Portal Link** — Enable client access
- [ ] **6. Test the Workflow** — Verify everything works

---

## Step 1: Access Milestone

### Open the App

1. Log into your Jira instance
2. Click **Apps** in the top navigation
3. Select **Milestone**

### First Launch

On first launch:
- You become the first admin automatically
- The Unified Queue displays (empty)
- All features are accessible via the sidebar

### Verify Navigation

Confirm you can see:
- **Unified Queue** — Main request list
- **My Work** — Personal assignments
- **Messenger** — Communications
- **Insights** — Analytics
- **Client Directory** — Client management
- **Admin** — Administration (if you're admin)

---

## Step 2: Configure SLA Defaults

Set the default SLA times that apply to all clients unless overridden.

### Access SLA Settings

1. Go to **Client Directory**
2. Click the **Settings** area (or access via Admin Console)
3. Find **SLA Configuration**

### Set Default Values

| Setting | Recommended Starting Point |
|---------|---------------------------|
| **Response Time** | 4 hours |
| **Resolution Time** | 24 hours |
| **Operating Hours** | 24/7 or Business Hours |

### Considerations

**Response Time:**
- How quickly can you acknowledge requests?
- Be realistic—better to exceed than miss

**Resolution Time:**
- Average time to complete typical requests
- Factor in complexity variation

**Operating Hours:**
- 24/7 means SLA timers always run
- Business Hours pauses nights/weekends

### Save Configuration

Click **Save** to apply your defaults. These apply to all new clients unless you set client-specific overrides.

---

## Step 3: Add Your First Client

Create your first client entry to start managing their requests.

### Navigate to Client Directory

1. Click **Client Directory** in the sidebar
2. Click **+ Add Client**

### Fill in Client Details

| Field | Description | Example |
|-------|-------------|---------|
| **Client ID** | Unique identifier | acme-corp |
| **Name** | Company name | Acme Corporation |
| **Project Key** | Jira project to link | ACME |
| **Default Issue Type** | Issue type for requests | Task |
| **Default Assignee** | Auto-assign (optional) | (leave blank initially) |

### Link to Jira Project

The Project Key must match an existing Jira project:
- Requests from this client create issues in this project
- Choose or create a project before adding the client

### Set Hours Purchased (Optional)

If this client has an hour bank:
1. After creating the client, select them
2. Go to **Settings** tab
3. Enter **Hours Purchased** (e.g., 40)

### Configure Client SLA Override (Optional)

If this client needs different SLAs than your defaults:
1. Select the client
2. Go to **Settings** → **SLA Override**
3. Enter custom response/resolution times
4. Save

---

## Step 4: Set Up Team Access

Configure your team members' access levels.

### Understanding Roles

| Role | Access |
|------|--------|
| **Admin** | Everything—clients, settings, user management |
| **Member** | Queue, My Work, Messenger, Insights (read) |

### Promote Team Members to Admin

1. Go to **Admin Console** (Admin menu in sidebar)
2. Click the **Users** tab
3. Find the team member
4. Click **Promote to Admin** (or similar action)

### Who Should Be Admin?

- **Admin**: Team leads, managers, account managers
- **Member**: Support agents, engineers

Start conservative—you can always promote later.

---

## Step 5: Generate Portal Link

Create access for your client to use the portal.

### Generate the Link

1. Go to **Client Directory** → **Portal Access** tab
2. Select your client
3. Configure:
   - **Company Name**: How they appear in portal
   - **Expiration**: 90 days recommended
4. Click **Generate Link**
5. Copy the generated link

### Send to Your Client

Email the link to your client contact:

```
Subject: Your Service Portal Access

Hi [Name],

Here's your access link to our service portal: [Link]

With this portal, you can:
• Submit new requests
• Track status and SLA timers
• View your hours
• Message our team

Click the link to create your account.

Best,
[Your name]
```

---

## Step 6: Test the Workflow

Verify everything works end-to-end.

### Test Request Flow

1. **Create Test Request**:
   - Use the portal link to access as a client (or test internally)
   - Submit a test request

2. **Check Unified Queue**:
   - Open Milestone in Jira
   - Verify the request appears
   - Check SLA timers are running

3. **Test Messaging**:
   - Send a message from the Forge app
   - Verify it appears in the portal
   - Reply from the portal
   - Confirm reply appears in Messenger

4. **Test Hours** (optional):
   - Log time on the Jira issue
   - Verify hours update in Client Directory
   - Check hours visible in portal

### Complete the Test

1. Resolve the test request
2. Verify status updates everywhere
3. Delete or keep for reference

---

## Initial Configuration Checklist

Before going live, verify:

### SLA Configuration
- [ ] Default response time set
- [ ] Default resolution time set
- [ ] Operating hours configured

### Client Setup
- [ ] At least one client created
- [ ] Linked to correct Jira project
- [ ] Hours purchased set (if applicable)
- [ ] SLA override configured (if needed)

### Team Access
- [ ] All team members can access Milestone
- [ ] Admins are promoted
- [ ] Everyone understands their role

### Portal Access
- [ ] Portal link generated
- [ ] Link sent to client
- [ ] Client successfully accessed portal

### Testing
- [ ] Request flow tested
- [ ] Messaging tested
- [ ] SLA timers verified
- [ ] Hours tracking verified (if applicable)

---

## Common Setup Issues

### "No Jira projects available"

- You need Jira projects created before adding clients
- Create a project in Jira first, then return to add client

### "SLA timers not starting"

- Verify SLA defaults are configured and saved
- Check client has SLA settings (default or override)
- Ensure request is properly created

### "Portal link not working"

- Check link hasn't expired
- Verify full URL was copied
- Try generating a new link

### "Team member can't see Admin"

- Only admins see the Admin menu
- Promote them via Admin Console → Users

---

## Next Steps

With setup complete, move on to:

1. **[Unified Queue](../02-features/unified-queue.md)** — Learn daily workflow
2. **[Client Onboarding](../04-admin/client-onboarding.md)** — Add more clients
3. **[Daily Operations](../05-workflows/daily-operations.md)** — Establish routines

---

## Getting Help

If you encounter issues during setup:
- Review specific feature documentation
- Contact support@getmilestone.io
- Check the troubleshooting guides

---

*Next: [Unified Queue →](../02-features/unified-queue.md)*
