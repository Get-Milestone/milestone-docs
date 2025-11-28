# My Work

My Work is your personal dashboard—a focused view of requests assigned to you, along with your performance metrics. While the Unified Queue shows everything across all clients and agents, My Work shows only what's on your plate.

---

## Why My Work Matters

### The Problem with Unified Queue Alone
The Unified Queue shows all requests, which is great for triage and team visibility. But during your workday, you need to focus on *your* assignments without visual clutter from other agents' work.

### My Work Provides
- **Personal focus**: Only your assigned requests
- **Performance visibility**: Your KPIs at a glance
- **Quick filters**: Find requests needing your attention
- **Accountability**: Clear ownership of your workload

---

## Accessing My Work

1. Open the Milestone app in Jira
2. Click **My Work** in the sidebar (briefcase icon)

The page loads showing:
- Your personal KPIs at the top
- Your assigned requests below
- A detail panel when you select a request

---

## Personal KPIs Dashboard

At the top of My Work, you'll see your performance metrics:

| Metric | What It Measures | Target |
|--------|------------------|--------|
| **Avg Response Time** | Time from assignment to first response | Lower is better |
| **SLA On-Time %** | Percentage of your requests that meet SLA | Aim for 95%+ |
| **Messages Handled** | Number of client messages you've responded to | Activity indicator |
| **Resolved Requests** | Requests you've completed | Productivity indicator |
| **Current Load** | Active requests assigned to you | Workload visibility |

### Understanding Your KPIs

**Avg Response Time**
- Measures how quickly you respond after being assigned
- Calculated across your recent requests
- Tip: Even a quick acknowledgment counts as a response

**SLA On-Time %**
- Shows what percentage of your requests met their SLA
- Both response and resolution SLAs are factored in
- If you inherit requests close to breach, your percentage may suffer

**Messages Handled**
- Counts your replies in the Messenger
- Higher numbers indicate active client engagement
- Quality matters more than quantity

**Resolved Requests**
- Total requests you've closed
- Rolling count over a time period
- Shows your throughput

**Current Load**
- Number of open requests assigned to you
- Helps identify if you're over or under capacity
- Leads can use this to balance team workload

---

## The Request List

Below your KPIs, you'll see all requests assigned to you. Each shows:

| Element | Description |
|---------|-------------|
| **Title** | Request title |
| **Client** | Which client this is for |
| **Status** | Current status (Submitted, In Progress, Completed) |
| **SLA Timer** | Time remaining on the SLA |
| **Last Updated** | When the request was last modified |
| **Unread Indicator** | Badge if there are new messages |

### Sorting

My Work sorts by **most recently updated** by default. Requests with recent activity appear at the top so you see what's changed.

---

## Filtering Your Work

Use the filter buttons to focus on specific request types:

### All
Shows all requests assigned to you (default view).

### Waiting for Reply
Requests where the client has sent a message you haven't responded to yet.

**Why it matters:** These clients are waiting on you. Prioritize these to maintain responsiveness.

### SLA Approaching
Requests where SLA is at warning level (75%+ elapsed) or breached.

**Why it matters:** These need immediate attention to prevent or address SLA breaches.

### Pending Approval
Requests that require approval before proceeding (if your workflow uses approvals).

---

## Working with Requests

### Selecting a Request

Click any request to open the detail panel showing:

- **Full description** of the request
- **Client information** with context
- **SLA breakdown** for both response and resolution
- **Jira issue link** to open in Jira
- **Work items** (sub-tasks) if any
- **Message thread** for client communication
- **Hours logged** against this request

### Taking Action

From the detail panel, you can:

1. **Send a message** to the client
2. **Log time** via Jira worklog
3. **Update status** when work progresses
4. **Open in Jira** for full issue editing

### Assignment Changes

If a request is reassigned away from you:
- It disappears from My Work
- It remains visible in Unified Queue
- The new assignee sees it in their My Work

---

## Best Practices

### Start Your Day Here

1. Open My Work
2. Review your KPIs
3. Check "Waiting for Reply" filter—respond to waiting clients
4. Check "SLA Approaching" filter—address urgent items
5. Then work through remaining items

### Keep Your Load Manageable

- Monitor your "Current Load" metric
- If consistently over capacity, discuss with your lead
- If under capacity, check Unified Queue for unassigned work

### Respond Quickly, Even If Briefly

- A quick "I'm looking into this" response is better than silence
- It stops the response SLA timer
- It sets client expectations

### Close Completed Work Promptly

- Don't leave resolved requests sitting "in progress"
- Closing them improves your resolved count
- It gives accurate workload visibility

---

## Common Mistakes to Avoid

### ❌ Only Working from Jira
Some agents work requests in Jira and never check My Work.

**Problem:** You miss SLA context and client messages.

**Fix:** Use My Work as your starting point, then jump to Jira for detailed work.

### ❌ Ignoring "Waiting for Reply"
Client messages can go unnoticed if you're deep in technical work.

**Problem:** Clients feel ignored; satisfaction drops.

**Fix:** Check "Waiting for Reply" several times daily.

### ❌ Hoarding Requests
Taking assignment of requests you can't get to.

**Problem:** SLAs breach; work sits stale.

**Fix:** Only assign yourself what you can actively work. Use Unified Queue for backlog visibility.

### ❌ Not Logging Time
Forgetting to log Jira worklogs against requests.

**Problem:** Hours don't sync; client reports are inaccurate.

**Fix:** Log time as you work, not at end of day.

---

## My Work vs. Unified Queue

| Aspect | My Work | Unified Queue |
|--------|---------|---------------|
| **Scope** | Only your assigned requests | All requests across all agents |
| **Purpose** | Personal productivity | Team triage and oversight |
| **KPIs** | Your personal metrics | Team/overall metrics (in Insights) |
| **Best for** | Daily work focus | Morning triage, lead oversight |

**Use both:** Start in Unified Queue for triage, then work from My Work for focus.

---

## For Team Leads

My Work isn't just for individual contributors. As a lead:

- Check team members' loads via Client Directory or ask them
- If someone's load is high, help reassign work
- Use KPIs in 1:1s to discuss performance
- Note: You can't see others' My Work views directly

---

## Troubleshooting

### "No requests found"
- You may have no assigned requests
- Check Unified Queue for unassigned work
- Verify filters aren't hiding requests

### KPIs showing zero
- Metrics need request history to calculate
- New users start with zero
- KPIs update as you work requests

### Missing request that should be assigned to me
- Refresh the page
- Check if it was reassigned
- Verify in Unified Queue that your account is the assignee

---

## Related Documentation

- **[Unified Queue](unified-queue.md)** — The team-wide request view
- **[SLA Tracking](sla-tracking.md)** — Understanding SLA timers
- **[Messenger](messenger.md)** — Responding to client messages

---

*Next: [SLA Tracking →](sla-tracking.md)*
