# Client Portal Overview

The Client Portal is a standalone web application designed for your customers—the end clients you serve as an MSP. It gives them direct visibility into their requests, SLA status, and hours consumption without requiring a Jira license or access to your internal systems.

---

## Why the Portal Matters

### For Your Clients
- **Transparency**: See exactly what's happening with their requests
- **Self-service**: Submit requests and check status without calling/emailing
- **Accountability**: SLA timers show your commitment in real-time
- **Trust**: Hours tracking shows exactly how their investment is being used

### For Your MSP
- **Reduced support load**: Clients self-serve instead of asking for status
- **Differentiation**: Professional portal experience sets you apart
- **Fewer disputes**: Transparent tracking prevents billing disagreements
- **Client retention**: Better experience = happier clients

---

## Portal Features at a Glance

| Feature | Description |
|---------|-------------|
| **Dashboard** | Overview with key metrics and recent activity |
| **Submit Requests** | Simple form to create new service requests |
| **Track Requests** | View open and historical requests |
| **SLA Visibility** | Live countdown timers for response and resolution |
| **Hours Dashboard** | Purchased vs. consumed hours |
| **Messenger** | Two-way communication with your team |
| **Reports** | Activity history and monthly summaries |

---

## The Portal Experience

### Home Dashboard

When clients log in, they see:

**Key Metrics:**
- Open requests count
- Closed requests count
- SLA compliance rate
- Hours remaining

**Recent Activity:**
- Latest updates on their requests
- New messages from your team
- Recent resolutions

**Quick Actions:**
- Submit new request button
- View open requests
- Access messages

### Requests Section

**New Request:**
- Clean form with title, description
- Urgency level selection
- Category selection (if configured)
- Submit and track automatically

**Open Requests:**
- All active requests in one view
- SLA timers on each request
- Status indicators (Submitted, In Progress)
- Click to view details

**Closed Requests:**
- Historical record of completed work
- Resolution details
- Hours logged per request

### Hours Dashboard

Clients see their hour bank status:

```
┌─────────────────────────────────────────────┐
│          Your Hours This Period             │
├─────────────────────────────────────────────┤
│  Purchased:  40 hours                       │
│  Used:       28 hours    ████████████░░░    │
│  Remaining:  12 hours                       │
└─────────────────────────────────────────────┘
```

### Messenger

- View message threads for each request
- Send messages to your team
- Receive real-time replies
- Full conversation history

### Reports

**Activity History:**
- Chronological log of all request activity
- Filter by date range
- See who did what and when

**Monthly Summary:**
- Requests submitted and resolved
- Hours consumed
- SLA performance

---

## How Clients Access the Portal

### Initial Access

1. You generate a portal link in Client Directory
2. Send the link to your client contacts
3. Client clicks the link
4. Client creates an account (or signs in)
5. Client is automatically connected to their company

### Ongoing Access

After initial setup:
1. Client goes to the portal URL
2. Signs in with their account
3. Sees their company's dashboard

### Multiple Users Per Client

- Multiple people from one client company can have portal accounts
- Each user sees the same client data
- All users can submit requests and view status

---

## Security and Scoping

### What Clients CAN See

- ✅ Their own company's requests
- ✅ SLA timers for their requests
- ✅ Hours for their company
- ✅ Messages on their requests
- ✅ Their company's history

### What Clients CANNOT See

- ❌ Other clients' requests
- ❌ Your internal Jira
- ❌ Internal notes or comments
- ❌ Other clients' hours or data
- ❌ Agent information beyond messages

---

## Best Practices for Portal Rollout

### Client Communication

When introducing the portal:

**Email Template:**
```
Subject: Introducing Your New Service Portal

Hi [Name],

We're excited to share your new service portal—a dedicated space to 
submit requests, track progress, and communicate with our team.

Access your portal here: [Portal Link]

With the portal, you can:
• Submit new service requests anytime
• Track real-time status and SLA timers
• View your hours consumption
• Message our team directly

Getting started takes just a minute. Click the link above to set up 
your account.

Questions? Reply to this email and we'll help you get started.

Best,
[Your name]
```

### Training Clients

Key points to communicate:
1. How to submit a request
2. What the SLA timers mean
3. How to send messages
4. Where to see hours

### Setting Expectations

Be clear about:
- Response and resolution times
- How urgency affects prioritization
- When they'll receive updates
- What's included in their hours

---

## Portal vs. Email/Phone

| Aspect | Portal | Email/Phone |
|--------|--------|-------------|
| **Request Tracking** | Automatic | Manual |
| **SLA Visibility** | Real-time | None |
| **Hours Tracking** | Automatic | Manual |
| **History** | Complete | Scattered |
| **24/7 Access** | Yes | No |
| **Status Updates** | Self-serve | Requires asking |

Encourage portal usage for better experience all around.

---

## Common Client Questions

### "Why do I need to create an account?"

The account connects you to your company and keeps your requests secure. It takes just a minute to set up.

### "Can I add colleagues?"

Yes! Share the portal link with colleagues who need access. Each person creates their own account.

### "Where do I see my hours?"

On the home dashboard, you'll see your hours balance. For details, check the Reports section.

### "How do I know you received my request?"

After submitting, you'll see the request immediately in your Open Requests. You'll also see when we respond via the SLA timer.

### "Can I see old requests?"

Yes! The Closed Requests section shows your complete history.

---

## Troubleshooting Portal Issues

### Client can't access portal

1. Verify the link hasn't expired
2. Generate a new link if needed
3. Ensure they're using the correct link

### Client sees wrong company

1. They may have accessed with wrong link
2. Contact support to correct account association

### Requests not showing

1. Ask client to refresh the page
2. Verify request was successfully submitted
3. Check for any error messages

### Messages not appearing

1. Refresh the page
2. Check internet connection
3. Verify message was sent successfully

---

## Portal Administration

### Generating Links

See [Portal Links](portal-links.md) for detailed instructions on:
- Creating invite links
- Setting expiration
- Managing access

### Customization

Current customization options:
- Company name display
- Portal URL (if configured)

### Monitoring Usage

Track portal adoption through:
- Request submission patterns
- Message activity
- Login frequency

---

## Related Documentation

- **[Portal Links](portal-links.md)** — How invite links work
- **[Portal FAQ](portal-faq.md)** — Common questions
- **[Portal User Guide](portal-user-guide.md)** — Guide for end customers
- **[Client Directory](../02-features/client-directory.md)** — Managing clients

---

*Next: [Portal Links →](portal-links.md)*
