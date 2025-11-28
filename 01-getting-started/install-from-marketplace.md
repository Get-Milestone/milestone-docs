# Install from Atlassian Marketplace

This guide walks you through installing Milestone from the Atlassian Marketplace. Installation takes just a few minutes and requires Jira admin permissions.

---

## Prerequisites

Before installing, ensure you have:

- [ ] **Jira Cloud instance** (Milestone is built for Jira Cloud)
- [ ] **Admin access** to your Jira site
- [ ] **Project(s) ready** where you'll track client requests

---

## Installation Steps

### Step 1: Find Milestone in the Marketplace

1. Log into your Jira instance
2. Click **Apps** in the top navigation
3. Select **Find new apps** (or go directly to Atlassian Marketplace)
4. Search for **"Milestone"**
5. Click on the Milestone app listing

### Step 2: Review the App

On the listing page, review:
- App description and features
- Pricing (if applicable)
- User reviews and ratings
- Security and privacy information

### Step 3: Install the App

1. Click **Get it now** (or **Try it free** for trials)
2. Select your Jira site if prompted
3. Review the permissions (see below)
4. Click **Install**

### Step 4: Approve Permissions

Milestone requests the following permissions:

| Permission | Why It's Needed |
|------------|-----------------|
| **Read Jira issues** | View requests linked to Jira issues |
| **Create Jira issues** | Create issues when clients submit requests |
| **Edit Jira issues** | Update status, assignee, and fields |
| **View worklogs** | Sync time logged for hours tracking |
| **Access user profiles** | Identify users for assignment and messaging |

Click **Accept** to grant permissions and complete installation.

### Step 5: Wait for Installation

- Installation typically completes in under a minute
- You'll see a confirmation message
- The app appears in your Apps menu

---

## Verification

### Confirm Installation

1. Click **Apps** in the top navigation
2. Find **Milestone** in your apps list
3. Click to open the app

### First Launch

When you first open Milestone:
- You'll land on the **Unified Queue** (likely empty)
- The navigation sidebar shows all available features
- The first user to access becomes an admin

---

## Post-Installation Setup

After installation, complete these steps:

### 1. Configure Cloud-Level SLAs

Set your default response and resolution times:
1. Go to **Client Directory**
2. Access **Settings**
3. Configure default SLA times
4. Save

### 2. Add Your First Client

Create a client entry:
1. Go to **Client Directory**
2. Click **+ Add Client**
3. Fill in client details
4. Link to a Jira project
5. Save

### 3. Set Up Your Team

Promote other users to admin if needed:
1. Go to **Admin Console**
2. Access **Users** tab
3. Find team members
4. Promote to admin role

### 4. Generate Portal Link

Give your first client access:
1. Go to **Client Directory** → **Portal Access**
2. Select the client
3. Generate a link
4. Share with your client

---

## Understanding Roles

### After Installation

| User | Role | What They Can Do |
|------|------|------------------|
| **First user** | Admin | Everything—full access |
| **Other Jira users** | Member | Unified Queue, My Work, Messenger, Insights |

### Role Differences

**Admins can:**
- Access Admin Console
- Manage users
- Configure SLAs
- Access all Client Directory features

**Members can:**
- Use Unified Queue and My Work
- Send messages
- View Insights
- Access basic Client Directory features

---

## Troubleshooting Installation

### App not appearing after installation

1. Refresh your browser
2. Clear browser cache
3. Log out and back into Jira
4. Check Apps menu again

### Permission errors

1. Verify you're a Jira admin
2. Check organization policies
3. Contact your Jira organization admin

### Installation failed

1. Try again after a few minutes
2. Check Atlassian status page for outages
3. Contact Milestone support if persists

---

## Uninstalling (If Needed)

To remove Milestone:
1. Go to **Apps** → **Manage apps**
2. Find Milestone
3. Click **Uninstall**
4. Confirm removal

**Note:** Uninstalling removes the app but your Jira issues remain. Milestone-specific data may be lost.

---

## Next Steps

Now that Milestone is installed:

1. **[First-Time Setup](first-time-setup.md)** — Configure your instance
2. **[Add Your First Client](../04-admin/client-onboarding.md)** — Set up a client
3. **[Unified Queue](../02-features/unified-queue.md)** — Start using the app

---

## Getting Help

If you encounter issues during installation:
- **Documentation**: Review troubleshooting guides
- **Support**: support@getmilestone.io
- **Atlassian Marketplace**: Check app comments and support links

---

*Next: [First-Time Setup →](first-time-setup.md)*
