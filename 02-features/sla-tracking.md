# SLA Tracking

Service Level Agreement (SLA) tracking is at the heart of Milestone. Every request has automatic timers that count down to your committed response and resolution deadlines, giving you and your clients real-time visibility into service delivery.

---

## What Are SLAs?

SLAs are your promises to clients about how quickly you'll respond to and resolve their requests. Milestone tracks two types:

### Response SLA
**Definition:** Maximum time from request submission to your first reply

**Example:** "We'll respond within 4 hours"

**Timer starts:** When the client submits the request  
**Timer stops:** When any agent sends the first message

### Resolution SLA
**Definition:** Maximum time from request submission to issue completion

**Example:** "We'll resolve issues within 24 hours"

**Timer starts:** When the client submits the request  
**Timer stops:** When the request status is changed to "Completed"

---

## How SLA Timers Work

### Timer States

| State | Color | Meaning |
|-------|-------|---------|
| **On Track** | 🟢 Green | Plenty of time remaining |
| **Warning** | 🟡 Yellow | Less than 25% of time remaining |
| **Breached** | 🔴 Red | Deadline has passed |
| **Completed** | 🟢 Green | Timer stopped (met or missed) |

### Timer Display Format

Timers show time remaining in a human-readable format:

| Time Remaining | Display |
|----------------|---------|
| More than 24 hours | `2d 5h` (days + hours) |
| 1-24 hours | `5h 30m` (hours + minutes) |
| Less than 1 hour | `45m 22s` (minutes + seconds) |
| Deadline passed | `Expired` (in red) |

---

## Where You'll See SLA Timers

### Unified Queue
- Each request row shows its SLA status
- Quick visual scan of what's urgent
- Sort by "SLA Expiring" to prioritize

### My Work
- Your assigned requests show SLA timers
- Filter to "SLA Approaching" for urgent items

### Request Detail Panel
When you click a request, the detail panel shows both timers:

```
┌─────────────────────┐  ┌─────────────────────┐
│   First Response    │  │     Resolution      │
│   ⏱️ 2h 45m        │  │   ⏱️ 1d 5h         │
│   Deadline: 2pm     │  │   Deadline: Tomorrow│
└─────────────────────┘  └─────────────────────┘
```

### Client Portal
Your clients see these same timers, building trust through transparency.

---

## SLA Configuration

### Cloud-Level Defaults

Set default SLAs that apply to all clients unless overridden:

1. Go to **Client Directory**
2. Click **SLA Settings** (or access via Admin Console)
3. Set your standard response and resolution times

**Example defaults:**
- Response: 4 hours
- Resolution: 24 hours

### Per-Client Overrides

VIP clients or specific contracts may require different SLAs:

1. Go to **Client Directory**
2. Select a client
3. Click **SLA Override**
4. Set custom times for this client

**Example override for VIP client:**
- Response: 1 hour
- Resolution: 8 hours

### SLA Inheritance

```
Request SLA = Client Override (if exists) → Cloud Default (fallback)
```

A request always uses the client's SLA settings if configured, otherwise falls back to your cloud defaults.

---

## What Stops the Timers

### Response Timer

The response timer stops when:
- ✅ Any agent sends a message to the client via Messenger
- ✅ The request is marked as "Completed" (implicitly responded)

The response timer does NOT stop when:
- ❌ An agent is assigned (assignment alone isn't a response)
- ❌ Internal notes are added
- ❌ Status changes to "In Progress"

**Key insight:** To stop the response timer, you must communicate with the client.

### Resolution Timer

The resolution timer stops when:
- ✅ The request status changes to "Completed"
- ✅ The underlying Jira issue is resolved

The resolution timer does NOT stop when:
- ❌ Work is in progress
- ❌ Waiting on client response
- ❌ Any status other than "Completed"

---

## SLA Breach Handling

### What Happens When SLA Breaches

1. **Visual indication**: Timer turns red with "Expired" label
2. **Breach recorded**: The breach is logged for reporting
3. **Timer continues**: Shows how far past deadline you are
4. **Metrics affected**: Your SLA compliance percentage drops

### Can You "Un-Breach" an SLA?

No. Once an SLA is breached, it's recorded as breached for historical accuracy. However:

- You can still respond/resolve to minimize impact
- Future reports will show the breach
- Use this data to improve processes

### Breach Prevention Tips

1. **Sort by SLA Expiring** in Unified Queue
2. **Check "Warning" filter** regularly
3. **Send quick acknowledgments** to stop response timers
4. **Escalate early** if resolution will be delayed

---

## Best Practices

### Set Realistic SLAs

- Don't promise what you can't deliver
- Factor in business hours, weekends, holidays
- Consider average resolution times from history

### Respond Early, Even If Briefly

A quick message like:
> "Thanks for reaching out. I'm looking into this and will have more details within the hour."

This:
- Stops the response timer ✅
- Sets client expectations ✅
- Builds trust ✅

### Use SLA Data for Planning

- Review SLA compliance weekly
- Identify patterns (certain clients, request types)
- Adjust staffing or SLAs based on data

### Communicate Proactively on Delays

If you'll miss a resolution deadline:
1. Message the client before breach
2. Explain the situation
3. Provide new expected timeline

Clients understand delays; they don't like surprises.

---

## Common Mistakes to Avoid

### ❌ Ignoring Yellow Warnings

Yellow means you're running out of time. Don't wait for red.

**Fix:** Treat yellow as "needs attention now."

### ❌ Assigning = Responding

Assigning a request to yourself doesn't count as a response.

**Fix:** Always send a client message when you start work.

### ❌ Setting Aggressive SLAs to Impress

Promising 1-hour response when you deliver 4 hours sets you up for failure.

**Fix:** Set achievable SLAs, then beat them.

### ❌ Forgetting to Resolve

Work is done, but you forgot to mark it complete. SLA keeps ticking.

**Fix:** Update status immediately when work is complete.

---

## SLA Reporting

### In Insights

The Insights page shows SLA metrics:
- Overall SLA compliance percentage
- Response time averages
- Resolution time averages
- Breach count and trends

### In Delivery App

Leadership sees:
- SLA compliance across all clients
- Per-client breakdown
- Trend analysis over time
- Data for QBR discussions

### Exporting SLA Data

From Insights or Delivery App, export reports for:
- Client business reviews
- Internal performance reviews
- Contract compliance documentation

---

## SLA Scenarios

### Scenario 1: Quick Response, Long Resolution

**Situation:** Client reports a complex bug at 9am with 4h response / 24h resolution SLA.

**Timeline:**
- 9:00 AM - Request submitted (both timers start)
- 9:15 AM - Agent responds "Looking into it" (response timer stops ✅)
- Next day 8:00 AM - Bug fixed, marked complete (resolution timer stops ✅)

**Result:** Both SLAs met ✅

### Scenario 2: Missed Response

**Situation:** Request submitted Friday 4pm, agent doesn't see it until Monday 9am.

**Timeline:**
- Friday 4pm - Request submitted
- Friday 8pm - Response SLA expires (4h passed)
- Monday 9am - Agent responds

**Result:** Response SLA breached ❌, Resolution may still be achievable

### Scenario 3: Client-Caused Delay

**Situation:** Agent needs information from client to proceed.

**Reality:** SLA timers keep running even while waiting on client.

**Best practice:** 
- Document in messages that you're waiting on client
- Set internal expectations
- Consider SLA pause features (if implemented)

---

## Troubleshooting

### SLA timer not starting
- Verify request was properly submitted
- Check that SLA defaults are configured
- Ensure client has SLA settings

### Response timer didn't stop
- Confirm a message was sent via Messenger (not just Jira comments)
- Internal notes don't count as responses
- Refresh the page

### Wrong SLA times showing
- Check if client has an override configured
- Verify cloud defaults are set correctly
- The displayed time is calculated from deadlines

---

## Related Documentation

- **[Unified Queue](unified-queue.md)** — Where you see and prioritize SLAs
- **[My Work](my-work.md)** — Your personal SLA view
- **[Insights](insights.md)** — SLA reporting and metrics
- **[Client Directory](client-directory.md)** — Setting SLA overrides

---

*Next: [Hours Tracking →](hours-tracking.md)*
