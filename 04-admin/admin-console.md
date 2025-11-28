# Admin Console

The Admin Console is the administrative hub for Milestone. From here, administrators manage users, configure system settings, and control access to the Delivery app.

---

## Accessing the Admin Console

1. Open Milestone in Jira
2. Click **Admin** in the sidebar (gear/settings icon)
3. The Admin Console opens with multiple tabs

**Note:** Only users with the Admin role see this menu item.

---

## Console Overview

The Admin Console contains these main sections:

| Tab | Purpose |
|-----|---------|
| **Users** | Manage user roles and permissions |
| **Delivery Access** | Control who can access the Delivery app |
| **Settings** | System-wide configuration |

---

## Users Tab

### What You'll See

A list of all Jira users who have accessed Milestone, showing:

| Column | Description |
|--------|-------------|
| **Name** | User's display name |
| **Email** | User's email address |
| **Role** | Current role (Admin or Member) |
| **Actions** | Promote/demote buttons |

### Managing User Roles

**To Promote a User to Admin:**
1. Find the user in the list
2. Click the **Promote** button (up arrow)
3. User immediately gains admin access

**To Demote an Admin to Member:**
1. Find the admin in the list
2. Click the **Demote** button (down arrow)
3. User immediately loses admin access

### User List Notes

- List shows users who have accessed Milestone
- Jira users who haven't opened Milestone won't appear
- Bot/app accounts are filtered out automatically

---

## Delivery Access Tab

The Delivery app is a separate application for leadership and executives. This tab controls who can access it.

### Granting Delivery App Access

1. Go to the **Delivery Access** tab
2. Enter the user's email address
3. Click **Generate Invite** or similar
4. Share the invite link with the user

### Who Should Have Delivery Access

| Role | Should Have Access |
|------|-------------------|
| Executives | Yes |
| Team Managers | Yes |
| Account Managers | Often |
| Support Agents | Rarely |
| Clients | No |

### Managing Delivery Access

- View who has been granted access
- Revoke access if needed
- Generate new invites for additional users

---

## Settings Tab

System-wide configuration options.

### Available Settings

Settings may include:

| Setting | Description |
|---------|-------------|
| **Default SLA** | Cloud-level SLA defaults |
| **Notifications** | Notification preferences |
| **Integrations** | Connected service configuration |

### Accessing Settings

1. Go to the **Settings** tab
2. Modify desired settings
3. Click **Save** to apply changes

**Note:** Changes affect all users and clients unless overridden at a lower level.

---

## Admin Console Best Practices

### Regular Admin Tasks

| Frequency | Task |
|-----------|------|
| Weekly | Review user list for appropriate roles |
| Monthly | Audit admin users—remove unnecessary admins |
| Quarterly | Review Delivery app access list |
| As needed | Promote new team leads, demote departures |

### Security Practices

- Keep admin count minimal
- Remove admin access when roles change
- Review Delivery access before sharing sensitive data
- Document who has elevated access and why

### Delegation

If you're a senior admin:
- Train backup admins
- Document admin procedures
- Ensure coverage during absences

---

## Common Admin Tasks

### New Employee Joins

1. They access Milestone (automatically becomes Member)
2. Go to Admin Console → Users
3. Promote to Admin if needed
4. Grant Delivery access if appropriate

### Employee Role Changes

**Promoted to Lead:**
1. Promote to Admin in Users tab
2. Consider Delivery access

**Moved to Different Team:**
1. Review if admin access still needed
2. Demote if no longer appropriate

### Employee Leaves

1. Their Jira access is removed (handles Milestone access)
2. If they had admin, their role is preserved in records
3. Revoke any Delivery app access

### New Client Needs Executive Dashboard

1. Generate portal link (for client)—not Delivery access
2. Delivery app is for your internal leadership, not clients

---

## Troubleshooting

### Can't access Admin Console

**Cause:** You're not an Admin

**Fix:** Have an existing admin promote you

### User not appearing in list

**Cause:** They haven't accessed Milestone yet

**Fix:** Have them open Milestone once; they'll appear

### Can't demote the last admin

**Cause:** System prevents removing all admins

**Fix:** Promote someone else first, then demote

### Delivery invite not working

**Causes:**
- Email may be incorrect
- Invite may have expired
- User may be using wrong email to sign up

**Fix:** Generate a new invite with correct email

---

## Related Documentation

- **[Roles](roles.md)** — Understanding roles and permissions
- **[First-Time Setup](../01-getting-started/first-time-setup.md)** — Initial admin configuration
- **[Client Onboarding](client-onboarding.md)** — Adding clients

---

*Next: [Delivery App Setup →](delivery-app-setup.md)*

