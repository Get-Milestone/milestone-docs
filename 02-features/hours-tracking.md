# Hours Tracking

Hours tracking automatically syncs time logged in Jira worklogs to client hour banks in Milestone. When your team logs time on a Jira issue linked to a client request, those hours are deducted from the client's purchased hour balance—visible to both your team and the client in real-time.

---

## How It Works

### The Flow

```
1. AGENT LOGS TIME IN JIRA
   └── Creates a worklog entry on the Jira issue
       └── Milestone detects the worklog
           └── Maps to the linked request
               └── Deducts from client hour bank
                   └── Updates visible in Portal & Directory
```

### Automatic Sync

- **Worklogs sync within seconds** of being logged in Jira
- **Edits are detected**: If you change a worklog from 2h to 3h, 1h additional is consumed
- **Deletes are detected**: If you delete a worklog, those hours are credited back
- **No manual entry**: Everything flows from Jira worklogs

---

## Where Hours Are Visible

### Client Directory (Your Team)

In the Client Directory, each client card shows:
- **Purchased Hours**: Total hours allocated to this client
- **Consumed Hours**: Hours used so far
- **Remaining Hours**: Balance available

### Client Portal (Your Customers)

Clients see their hours in the Portal:
- Hours used vs. purchased
- Per-request hour breakdown
- Consumption history

### Insights & Delivery App

Leadership views show:
- Hours consumed across all clients
- Utilization rates
- Trend analysis

---

## Logging Time in Jira

### How to Log Time

1. Open the Jira issue linked to the request
2. Click **Log Work** (or use keyboard shortcut `w`)
3. Enter time spent (e.g., "2h 30m" or "2.5h")
4. Add work description (optional but recommended)
5. Save

### Time Format

Jira accepts various formats:
- `2h` = 2 hours
- `30m` = 30 minutes
- `2h 30m` = 2 hours 30 minutes
- `1d` = 1 day (typically 8 hours)
- `2.5h` = 2 hours 30 minutes

### Editing Logged Time

If you need to correct a worklog:
1. Open the Jira issue
2. Find the worklog in the activity section
3. Click the edit icon
4. Change the time
5. Save

Milestone automatically adjusts the hours:
- Original: 2h → Edited: 3h = +1h consumed
- Original: 3h → Edited: 2h = -1h consumed (credited back)

### Deleting Logged Time

If a worklog was logged incorrectly:
1. Open the Jira issue
2. Find the worklog
3. Click delete
4. Confirm

The hours are credited back to the client's balance.

---

## Hour Banks

### What Is an Hour Bank?

An hour bank is the allocated hours a client has purchased or been allotted:

| Term | Meaning |
|------|---------|
| **Purchased Hours** | Total hours allocated to the client |
| **Consumed Hours** | Hours used (sum of worklogs) |
| **Remaining Hours** | Purchased minus consumed |

### Setting Up Hour Banks

In the Client Directory:
1. Select a client
2. Find **Hours Purchased** field
3. Enter the total hours (e.g., 40)
4. Save

### Adjusting Hour Banks

When a client purchases more hours:
1. Go to Client Directory
2. Select the client
3. Update the **Hours Purchased** value
4. Save

The remaining balance updates automatically.

---

## Best Practices

### Log Time as You Work

- Don't wait until end of day or week
- Log in small increments as you complete tasks
- More accurate billing, less reconciliation

### Use Descriptive Work Logs

Include what you worked on:
- ✅ "Troubleshooting SSO integration, identified cert issue"
- ❌ "Work"

This helps with:
- Client billing transparency
- Your own time tracking
- Dispute resolution

### Log to the Correct Issue

Make sure you're logging to the right Jira issue:
- Worklogs on the wrong issue won't sync to the correct client
- Double-check the issue before logging

### Review Weekly

- Check client hour balances weekly
- Identify clients running low
- Flag any consumption anomalies

---

## Client Hour Warnings

### Low Hours Alert

When a client's remaining hours get low:
- Milestone can highlight at-risk clients
- Use this to proactively discuss with clients
- Prevents surprise "out of hours" situations

### Negative Balance

What happens if consumed > purchased?
- Balance shows negative
- Work can continue (Milestone doesn't block)
- Use this as a trigger for client conversation

---

## Common Scenarios

### Scenario 1: Normal Time Logging

**Action:** Agent logs 2 hours on Jira issue PROJ-123

**Result:**
- Client's consumed hours: +2h
- Client's remaining hours: -2h
- Visible in Portal within seconds

### Scenario 2: Correcting Over-Logged Time

**Situation:** Agent logged 8h but should have been 4h

**Action:** Edit the worklog from 8h to 4h

**Result:**
- Client's consumed hours: -4h (correction)
- Client's remaining hours: +4h (credited back)

### Scenario 3: Internal Work (Non-Billable)

**Situation:** Work done that shouldn't consume client hours

**Options:**
1. Don't log time in Jira (if not tracking internally)
2. Log to a non-client-linked issue
3. Use Jira's work log types if configured

### Scenario 4: Multiple Agents on Same Request

**Situation:** Three agents each log 2h on the same request

**Result:**
- Total consumed: 6h
- Each worklog tracked separately
- All visible in consumption history

---

## Consumption Reports

### Viewing Consumption History

For a specific request:
1. Open the request detail panel
2. Find the **Hours** section
3. See breakdown of time logged

For a specific client:
1. Open Client Directory
2. Select the client
3. View hours summary and history

### Exporting Hours Data

From the Delivery App:
- Export consumption data for billing
- Generate reports for client invoicing
- Produce QBR-ready summaries

---

## Common Mistakes to Avoid

### ❌ Forgetting to Log Time

Work completed but not logged = inaccurate billing.

**Fix:** Build logging into your workflow. Log before closing a request.

### ❌ Logging to Wrong Issue

Time logged on unlinked issue doesn't sync.

**Fix:** Verify the Jira issue key matches the Milestone request.

### ❌ Bulk Logging at End of Week

Can't remember exact time per task.

**Fix:** Log as you go, or at minimum daily.

### ❌ Not Reviewing Balances

Client runs out of hours unexpectedly.

**Fix:** Weekly review of client hour balances.

### ❌ Logging Personal Time

Breaks, meetings, non-client work logged to client issues.

**Fix:** Log only client-related work to client-linked issues.

---

## Troubleshooting

### Hours not syncing

1. Verify the worklog was saved in Jira
2. Check that the Jira issue is linked to a Milestone request
3. Wait a few seconds and refresh
4. Check Jira issue has the correct project

### Wrong client showing hours

1. Verify the request is associated with the correct client
2. Check the Jira issue linkage
3. A request can only belong to one client

### Hours showing but client says they didn't see update

1. Ask client to refresh their Portal
2. Verify they're looking at the correct request
3. Check if there's browser caching

### Negative hours balance

This is valid—client has used more than purchased. Use this as a prompt to discuss additional hour purchases.

---

## Integration with Jira Time Tracking

Milestone works with Jira's native time tracking:
- **Original Estimate**: Not used by Milestone (informational only)
- **Time Spent**: This is what syncs as consumption
- **Time Remaining**: Not used by Milestone

Milestone reads only the worklog entries—the sum of actual time logged.

---

## Related Documentation

- **[Client Directory](client-directory.md)** — Managing client hour banks
- **[Insights](insights.md)** — Hours consumption reporting
- **[SLA Tracking](sla-tracking.md)** — Time-based commitments

---

*Next: [Messenger →](messenger.md)*
