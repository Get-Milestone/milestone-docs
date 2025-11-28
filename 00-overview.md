# Milestone Platform Overview

Milestone is a professional services management platform purpose-built for Managed Service Providers (MSPs). It transforms how your team manages client requests, tracks service level agreements (SLAs), logs billable hours, and communicates with customers—all while keeping Jira as your central work management hub.

---

## The Problems Milestone Solves

### For MSP Teams
- **Scattered request intake**: Requests come from email, Slack, phone calls, and portals—leading to missed items and duplicate work
- **Manual SLA tracking**: Spreadsheets and mental math to track response and resolution commitments
- **Hours reconciliation headaches**: Matching worklogs to client hour banks requires manual effort
- **Context switching**: Jumping between Jira, email, and client communication tools wastes time
- **Inconsistent client updates**: Customers don't know what's happening with their requests

### For Your Clients
- **No visibility**: They submit requests into a black hole and wait for updates
- **Unclear SLA status**: They don't know if their request is on track or delayed
- **Hours confusion**: They can't see how their purchased hours are being consumed
- **Communication friction**: They have to email or call to get status updates

### For Leadership
- **Metrics are manual**: Building QBR reports requires pulling data from multiple systems
- **No real-time visibility**: Understanding team performance requires asking individuals
- **Client health is opaque**: Hard to spot at-risk accounts before they escalate

---

## How Milestone Works: The Three Apps

Milestone consists of three interconnected applications, each designed for a specific user type:

```
┌─────────────────────────────────────────────────────────────────────┐
│                        YOUR JIRA INSTANCE                          │
│  ┌───────────────────────────────────────────────────────────────┐ │
│  │                    MILESTONE FORGE APP                        │ │
│  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────────────────┐ │ │
│  │  │ Unified     │ │ My Work     │ │ Messenger               │ │ │
│  │  │ Queue       │ │             │ │                         │ │ │
│  │  └─────────────┘ └─────────────┘ └─────────────────────────┘ │ │
│  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────────────────┐ │ │
│  │  │ Client      │ │ Insights    │ │ Admin Console           │ │ │
│  │  │ Directory   │ │             │ │                         │ │ │
│  │  └─────────────┘ └─────────────┘ └─────────────────────────┘ │ │
│  └───────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────────┘
              │                                    │
              │ Real-time sync                     │ Worklog sync
              ▼                                    ▼
┌─────────────────────────┐          ┌─────────────────────────────┐
│     CLIENT PORTAL       │          │       DELIVERY APP          │
│  ┌───────────────────┐  │          │  ┌───────────────────────┐  │
│  │ Submit Requests   │  │          │  │ Executive Dashboard   │  │
│  │ Track Status      │  │          │  │ SLA Compliance        │  │
│  │ View SLA Timers   │  │          │  │ Client Analytics      │  │
│  │ See Hours Used    │  │          │  │ Team Performance      │  │
│  │ Message Your Team │  │          │  │ QBR Reports           │  │
│  └───────────────────┘  │          │  └───────────────────────┘  │
│                         │          │                             │
│  Used by: Your Clients  │          │  Used by: Your Leadership   │
│  No Jira license needed │          │  No Jira license needed     │
└─────────────────────────┘          └─────────────────────────────┘
```

### 1. Milestone Forge App (For Your Agents)

**Where:** Installed directly in your Jira instance  
**Who uses it:** Your delivery team—the agents who handle client requests  
**Access:** Anyone with Jira access to your instance

The Forge app is your team's command center. It provides:

| Feature | Description |
|---------|-------------|
| **Unified Queue** | See all client requests in one view, filterable by client, status, SLA urgency, and assignee |
| **My Work** | Personal view of your assigned requests with SLA timers and quick actions |
| **Messenger** | Real-time communication with clients that syncs to the portal |
| **Client Directory** | Manage clients, their hour banks, and SLA configurations |
| **Insights** | Performance metrics, SLA compliance, and trend analysis |
| **Admin Console** | User management, delivery app access, and system configuration |

### 2. Client Portal (For Your Customers)

**Where:** Standalone web application at a unique URL per client  
**Who uses it:** Your end customers  
**Access:** Via invite link—no Jira license required

The Client Portal gives your customers transparency without overwhelming them:

| Feature | Description |
|---------|-------------|
| **Submit Requests** | Clean form to submit new service requests |
| **Track Open Requests** | See all active requests with real-time status |
| **SLA Visibility** | Live countdown timers showing response and resolution targets |
| **Hours Dashboard** | See purchased vs. consumed hours at a glance |
| **Messenger** | Two-way communication that syncs with your team's Messenger |
| **Request History** | Complete archive of past requests and resolutions |

### 3. Delivery App (For Your Leadership)

**Where:** Standalone web application  
**Who uses it:** Executives, managers, and team leads  
**Access:** Via signup link from the Admin Console—no Jira license required

The Delivery App provides the metrics leadership needs:

| Feature | Description |
|---------|-------------|
| **Executive Dashboard** | High-level KPIs across all clients |
| **SLA Compliance** | Track response and resolution performance over time |
| **Client Analytics** | Per-client breakdown of volume, hours, and health |
| **Team Performance** | Individual agent metrics and workload distribution |
| **Reports** | Export-ready data for QBRs and internal reviews |

---

## How Data Flows Through Milestone

Understanding how data moves between the apps helps you work more effectively:

### Request Lifecycle

```
1. CLIENT SUBMITS REQUEST
   └── Via Client Portal form
       └── Creates Jira issue automatically
           └── Appears in Unified Queue
               └── SLA timers start

2. AGENT WORKS REQUEST
   └── Assigns from Unified Queue or picks up in My Work
       └── Logs time in Jira (worklogs)
           └── Hours sync to client's consumption
               └── Updates visible in Portal

3. COMMUNICATION
   └── Agent sends message in Messenger
       └── Client sees it instantly in Portal
           └── Client replies
               └── Agent sees reply in Messenger

4. RESOLUTION
   └── Agent resolves Jira issue
       └── SLA resolution timer stops
           └── Portal shows "Completed"
               └── Metrics update in Insights & Delivery App
```

### Real-Time Synchronization

- **Jira → Milestone**: Issue updates, status changes, and worklogs sync within seconds
- **Messenger → Portal**: Messages appear instantly on both sides
- **Hours**: Worklogs in Jira automatically deduct from client hour banks
- **SLAs**: Timer states sync across all three apps in real-time

---

## Who Should Use What

| Role | Primary App | Also Uses |
|------|-------------|-----------|
| **Support Agent** | Forge App (Unified Queue, My Work, Messenger) | — |
| **Team Lead** | Forge App + Delivery App | Client Directory for oversight |
| **Account Manager** | Delivery App + Forge App (Client Directory) | Portal (to see client view) |
| **Executive** | Delivery App | — |
| **Client Contact** | Client Portal | — |
| **System Admin** | Forge App (Admin Console) | All apps for testing |

---

## Key Concepts

### Clients vs. Users
- **Client**: A company you provide services to (e.g., "Acme Corp")
- **User**: An individual person (either your team member or a client contact)
- Each client can have multiple portal users
- Your team members can access all clients (filtered by permissions)

### SLA Types
- **Response SLA**: Time from request submission to first agent response
- **Resolution SLA**: Time from request submission to issue completion
- Both can be configured at the cloud level (default) or per-client (override)

### Hours
- **Purchased Hours**: The hour bank allocated to a client (e.g., 40 hours/month)
- **Consumed Hours**: Hours used, calculated from Jira worklogs
- **Remaining Hours**: Purchased minus consumed

### Request vs. Issue vs. Work Item
- **Request**: What the client submits via the Portal
- **Jira Issue**: The ticket created in your Jira project
- **Work Item**: Child tasks created under a request (for complex requests)

---

## Getting Started

Ready to set up Milestone? Here's your path:

1. **[Install from Marketplace](01-getting-started/install-from-marketplace.md)** — Get the Forge app in your Jira
2. **[First-Time Setup](01-getting-started/first-time-setup.md)** — Configure your first client and SLAs
3. **[Generate Portal Links](03-client-portal/portal-links.md)** — Invite your first client
4. **[Daily Operations](05-workflows/daily-operations.md)** — Learn the recommended workflow

---

## Getting Help

- **Documentation**: You're reading it! Use the navigation to explore features.
- **Support**: support@getmilestone.io
- **Security Issues**: security@getmilestone.io

---

*Next: [Install from Marketplace →](01-getting-started/install-from-marketplace.md)*
