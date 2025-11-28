# Roles and Permissions

Milestone uses a role-based access system to control what users can see and do. Understanding roles helps you configure appropriate access for your team.

---

## Role Overview

Milestone has two primary roles:

| Role | Description | Who Should Have It |
|------|-------------|-------------------|
| **Admin** | Full access to all features and settings | Team leads, managers, account managers |
| **Member** | Standard agent access without admin functions | Support agents, engineers |

---

## Role Capabilities

### Admin Role

Admins have complete access to Milestone:

**All Member Capabilities Plus:**

| Capability | Description |
|------------|-------------|
| **Admin Console** | Access to user management and system settings |
| **User Management** | Promote/demote users between roles |
| **SLA Configuration** | Set cloud-level and client-level SLAs |
| **Full Client Directory** | All client management features |
| **Portal Link Generation** | Create portal access links |
| **Delivery App Access** | Grant access to leadership dashboard |

### Member Role

Members have access to day-to-day operational features:

| Capability | Description |
|------------|-------------|
| **Unified Queue** | View and work all requests |
| **My Work** | Personal assignment view |
| **Messenger** | Send and receive client messages |
| **Insights** | View analytics (read-only) |
| **Client Directory** | View clients (limited editing) |

### Feature Access Matrix

| Feature | Admin | Member |
|---------|:-----:|:------:|
| Unified Queue | ✅ | ✅ |
| My Work | ✅ | ✅ |
| Messenger | ✅ | ✅ |
| Insights | ✅ | ✅ (read) |
| Client Directory - View | ✅ | ✅ |
| Client Directory - Edit | ✅ | ❌ |
| Admin Console | ✅ | ❌ |
| User Management | ✅ | ❌ |
| SLA Settings | ✅ | ❌ |
| Portal Link Generation | ✅ | ❌ |

---

## Managing User Roles

### Viewing Users

1. Go to **Admin Console** (sidebar)
2. Click the **Users** tab
3. See all users with their current roles

### Promoting a User to Admin

1. Go to **Admin Console** → **Users**
2. Find the user in the list
3. Click the **Promote** button (or arrow up icon)
4. Confirm the promotion

The user immediately gains admin access.

### Demoting an Admin to Member

1. Go to **Admin Console** → **Users**
2. Find the admin in the list
3. Click the **Demote** button (or arrow down icon)
4. Confirm the demotion

The user immediately loses admin privileges.

### Role Change Considerations

Before changing roles:
- Ensure you're not removing the last admin
- Consider impact on user's workflow
- Communicate the change to the affected user

---

## First User Behavior

When Milestone is first installed:
- The first user to access the app becomes an admin
- This is automatic—no configuration needed
- This user should then set up other admins

---

## Best Practices

### Who Should Be Admin

**Make someone admin if they:**
- Manage client relationships
- Need to configure SLAs
- Should manage team access
- Generate portal links
- Need full system oversight

**Keep as member if they:**
- Primarily work requests
- Don't need system configuration
- Focus on operational tasks

### Admin Count Guidelines

| Team Size | Recommended Admins |
|-----------|-------------------|
| 1-5 | 1-2 |
| 6-15 | 2-4 |
| 15+ | 3-5 |

Too many admins creates configuration risk. Too few creates bottlenecks.

### Security Considerations

- Review admin list periodically
- Remove admin access when roles change
- Use admin sparingly—grant only when needed

---

## Role-Based Workflows

### Admin Workflow

Typical admin activities:
- Configure new clients
- Set and adjust SLAs
- Generate portal links
- Manage user access
- Review system health

### Member Workflow

Typical member activities:
- Work the Unified Queue
- Manage personal assignments
- Communicate with clients
- Log time in Jira
- Review personal insights

---

## Troubleshooting

### User can't see Admin menu

- They're not an admin
- Have an admin promote them
- Or use Admin Console to promote

### Can't demote an admin

- You might be trying to demote yourself
- You might be trying to demote the last admin
- Have another admin perform the action

### New user has wrong role

- All new users start as members
- Admins must explicitly promote them
- Check Admin Console → Users

### User left the company

- Demote them from admin (if applicable)
- They lose Milestone access when Jira access is removed
- No separate Milestone deprovisioning needed

---

## Related Documentation

- **[Admin Console](admin-console.md)** — Full admin console guide
- **[First-Time Setup](../01-getting-started/first-time-setup.md)** — Initial configuration
- **[Client Onboarding](client-onboarding.md)** — Adding clients (admin task)

---

*Next: [Client Onboarding →](client-onboarding.md)*
