# Unified Queue

The Unified Queue is your team's central command center—a single view of all client requests across your entire MSP practice. Instead of jumping between projects, email, and different client folders, you see everything in one place, prioritized by what matters most.

---

## Why the Unified Queue Matters

### Before Milestone
- Requests scattered across Jira projects, email, Slack, and ticketing systems
- No single view of "what needs attention right now"
- SLA tracking done manually or not at all
- Agents pick easy work, urgent items slip through

### With the Unified Queue
- Every client request in one filterable list
- Visual SLA indicators show what's urgent
- Sort by SLA expiry to always work the right thing next
- Search across all requests instantly

---

## Accessing the Unified Queue

1. Open Jira
2. Click **Apps** → **Milestone**
3. The Unified Queue is the default landing page

You'll see it in the sidebar with an inbox icon: **Unified Queue**

---

## Understanding the Interface

### The Request List

Each request in the queue shows:

| Element | Description |
|---------|-------------|
| **Title** | The request title (from the portal submission or Jira issue) |
| **Client** | Which client submitted this request |
| **Status** | Current status: Submitted, In Progress, or Completed |
| **SLA Timer** | Live countdown showing time remaining (response or resolution) |
| **Assignee** | Who's working on this (or "Unassigned") |
| **Created** | When the request was submitted |
| **Tracking ID** | Unique identifier (e.g., REQ-1234) |

### SLA Visual Indicators

The SLA timer uses color coding for instant recognition:

| Color | Meaning | Action |
|-------|---------|--------|
| 🟢 **Green** | On track—plenty of time remaining | Continue normal workflow |
| 🟡 **Yellow** | Warning—75% of time elapsed | Prioritize this request |
| 🔴 **Red** | Breached—SLA has been exceeded | Address immediately |
| ⚪ **Gray** | Completed or paused | No action needed |

### The Detail Panel

Click any request to open the detail panel on the right side, showing:

- Full request description
- Client information
- Complete SLA breakdown (response + resolution)
- Linked Jira issue
- Work items (sub-tasks)
- Message thread
- Hours logged

---

## Filtering Requests

Use filters to focus on specific subsets of requests. Filters work together—you can combine multiple filters for precise results.

### Search

The search box filters by:
- Request title
- Description content
- Tracking ID (e.g., "REQ-1234")
- Jira issue key (e.g., "PROJ-567")

**Tip:** Search is instant—results update as you type.

### Client Filter

Filter to show only requests from a specific client:

1. Click the **Client** dropdown
2. Select a client name
3. View updates to show only that client's requests

Use this when:
- Preparing for a client call
- Reviewing a specific client's workload
- Onboarding a new team member to a client account

### Status Filter

Filter by request status:

| Status | Shows |
|--------|-------|
| **All** | Everything (default) |
| **Submitted** | New requests not yet in progress |
| **In Progress** | Requests actively being worked |
| **Completed** | Resolved requests |

**Best Practice:** Start each day by filtering to "Submitted" to see new incoming work.

### SLA Filter

Filter by SLA health:

| Option | Shows |
|--------|-------|
| **All** | All requests regardless of SLA status |
| **On Track** | Requests within SLA (green) |
| **Warning** | Requests approaching breach (yellow, 75%+ elapsed) |
| **Breached** | Requests that have exceeded SLA (red) |

**Best Practice:** Filter to "Warning" or "Breached" first thing each morning.

### Assignee Filter

Filter by who's assigned:

| Option | Shows |
|--------|-------|
| **All** | All requests |
| **Unassigned** | Requests without an owner |
| **[Agent Name]** | Requests assigned to a specific person |

**Best Practice:** Leads should regularly check "Unassigned" to ensure nothing falls through.

### Category Filter

If you use request categories, filter by type:
- Bug reports
- Feature requests
- Support questions
- etc.

---

## Sorting Options

Change the order of requests using the sort dropdown:

| Sort Option | Best For |
|-------------|----------|
| **SLA Expiring** | Daily triage—work the most urgent first |
| **Oldest First** | FIFO processing—ensure nothing gets stale |
| **Newest First** | Seeing what just came in |
| **Client Name** | Grouping work by client visually |

### Recommended: SLA Expiring Sort

For most agents, sorting by **SLA Expiring** is the optimal default:

1. Requests closest to SLA breach appear at top
2. Breached requests appear first (so you address them)
3. You're always working on what matters most

**To set this:**
1. Click the **Sort** dropdown
2. Select **SLA Expiring**
3. This becomes your view until you change it

---

## Working with Requests

### Selecting a Request

Click any request row to:
- Open the detail panel
- See full information
- Access actions (respond, assign, etc.)

### Quick Actions from the List

Some actions are available directly from the list:
- Click the assignee to quickly reassign
- Status badges are clickable to update status

### Opening in Jira

From the detail panel:
1. Find the **Jira Issue** section
2. Click the issue key (e.g., "PROJ-567")
3. Opens the full Jira issue in a new tab

---

## Best Practices

### Morning Routine

1. **Open Unified Queue**
2. **Sort by SLA Expiring**
3. **Filter to Breached** → Address any breaches immediately
4. **Filter to Warning** → Prioritize these next
5. **Filter to Submitted** → See new incoming work
6. **Clear filters** → Review full queue

### During the Day

- **Keep the queue open** in a browser tab
- **Refresh periodically** (click the refresh icon) to see new requests
- **Use search** when a client calls about a specific request
- **Filter by your name** to focus on your assigned work

### For Team Leads

- **Check "Unassigned" daily** to ensure coverage
- **Review "Breached" filter** to spot systemic issues
- **Use Client filter** when preparing for client meetings

---

## Common Mistakes to Avoid

### ❌ Ignoring the Queue
Some agents work only from Jira. You'll miss SLA context and cross-client visibility.

**Fix:** Make the Unified Queue your starting point, not Jira.

### ❌ Not Using SLA Sort
Working oldest-first sounds fair but ignores urgency.

**Fix:** Sort by SLA Expiring so urgent items surface automatically.

### ❌ Forgetting to Refresh
The queue doesn't auto-refresh (to save bandwidth).

**Fix:** Click refresh before making prioritization decisions.

### ❌ Over-Filtering
Too many filters active can hide important requests.

**Fix:** Clear all filters regularly to see the full picture.

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `/` | Focus search box |
| `Esc` | Clear search / close detail panel |
| `↑` / `↓` | Navigate between requests |
| `Enter` | Open selected request detail |
| `R` | Refresh the queue |

---

## Troubleshooting

### "No requests found"
- Check if filters are too restrictive
- Click "Clear Filters" to reset
- Ensure the request exists and isn't archived

### Requests not showing up
- New requests may take a few seconds to sync
- Click the refresh button
- Check if status filter is hiding the request

### SLA showing wrong time
- SLA timers sync from the server
- Refresh the page for latest data
- Check if the SLA was configured correctly for this client

---

## Related Documentation

- **[My Work](my-work.md)** — Your personal filtered view of assigned requests
- **[SLA Tracking](sla-tracking.md)** — Understanding how SLAs work
- **[Messenger](messenger.md)** — Communicating with clients on requests

---

*Next: [My Work →](my-work.md)*
