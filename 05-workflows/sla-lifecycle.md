# SLA Lifecycle

This document explains the complete lifecycle of SLA timers—from when they start, what affects them, to how they're recorded in metrics.

---

## SLA Timer Types

### Response SLA

**Purpose:** Ensure clients receive timely acknowledgment

**Starts:** When the request is submitted  
**Stops:** When an agent sends the first message via Messenger  
**Measures:** Time to first communication

### Resolution SLA

**Purpose:** Ensure requests are completed within committed time

**Starts:** When the request is submitted  
**Stops:** When request status changes to "Completed"  
**Measures:** Total time from submission to resolution

---

## Timer Lifecycle Diagram

```
REQUEST SUBMITTED
       │
       ▼
┌──────────────────┐     ┌──────────────────┐
│  RESPONSE TIMER  │     │  RESOLUTION TIMER │
│    RUNNING       │     │     RUNNING       │
└────────┬─────────┘     └────────┬──────────┘
         │                        │
    Agent sends                   │
    first message                 │
         │                        │
         ▼                        │
┌──────────────────┐              │
│  RESPONSE TIMER  │              │
│    STOPPED       │              │
│  (Met or Breach) │              │
└──────────────────┘              │
                                  │
                            Request marked
                              complete
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ RESOLUTION TIMER │
                         │     STOPPED      │
                         │  (Met or Breach) │
                         └──────────────────┘
```

---

## Phase 1: Timer Activation

### What Triggers Timer Start

| Trigger | Response Timer | Resolution Timer |
|---------|:--------------:|:----------------:|
| Client submits via Portal | ✅ Starts | ✅ Starts |
| Agent creates request manually | ✅ Starts | ✅ Starts |

Both timers start simultaneously at request creation.

### SLA Configuration Applied

At timer start:
1. System checks for client-specific SLA override
2. If none, uses cloud-level defaults
3. Calculates deadline based on configured hours
4. Business hours considered if configured

### Initial State

```
Response Timer: [Configured Hours] remaining → Deadline: [Calculated Time]
Resolution Timer: [Configured Hours] remaining → Deadline: [Calculated Time]
```

---

## Phase 2: Timers Running

### Visual States

| Remaining Time | Color | Indicator |
|----------------|-------|-----------|
| > 25% remaining | 🟢 Green | On Track |
| 10-25% remaining | 🟡 Yellow | Warning |
| < 10% remaining | 🟡 Yellow | Critical Warning |
| 0% (deadline passed) | 🔴 Red | Breached |

### What Affects Running Timers

**Does NOT Pause Timer:**
- Assigning the request
- Changing status (except to Complete)
- Adding internal notes
- Waiting on client response

**Stops Response Timer:**
- First message sent via Messenger

**Stops Resolution Timer:**
- Marking request as Completed

### Timer Countdown

Timers count down continuously:
- Based on wall-clock time (or business hours if configured)
- Updates displayed in real-time
- Server calculates, client displays

---

## Phase 3: Response Timer Completion

### Triggering Stop

The response timer stops when **any agent sends the first message** through Messenger.

**Counts as response:**
- Message via Milestone Messenger
- Any agent (doesn't have to be assignee)

**Does NOT count:**
- Jira comments
- Email replies
- Status changes
- Assignments

### Result Recording

| Condition | Result |
|-----------|--------|
| Responded before deadline | Met ✅ |
| Responded after deadline | Breached ❌ |

### After Response Timer Stops

- Timer shows "Responded" with timestamp
- Green checkmark indicates completion
- Resolution timer continues independently
- Metrics record the response time

---

## Phase 4: Resolution Timer Completion

### Triggering Stop

The resolution timer stops when the **request status changes to "Completed"**.

This typically happens when:
- Agent marks the request complete in Milestone
- Underlying Jira issue is resolved (if configured to sync)

### Result Recording

| Condition | Result |
|-----------|--------|
| Completed before deadline | Met ✅ |
| Completed after deadline | Breached ❌ |

### After Resolution Timer Stops

- Timer shows "Resolved" with timestamp
- Request moves to closed state
- Both SLA results are final
- Metrics updated

---

## SLA Breach Handling

### What Happens at Breach

1. **Visual Change:**
   - Timer shows red
   - "Expired" or "Breached" label
   - Continues showing time past deadline

2. **Recording:**
   - Breach is permanently recorded
   - Cannot be undone
   - Affects SLA compliance metrics

3. **Work Continues:**
   - Request still needs resolution
   - Breached doesn't mean abandoned

### After Breach

| Scenario | Response Timer | Resolution Timer |
|----------|----------------|------------------|
| Response breached, resolved on time | ❌ Breached | ✅ Met |
| Response on time, resolution breached | ✅ Met | ❌ Breached |
| Both breached | ❌ Breached | ❌ Breached |
| Both met | ✅ Met | ✅ Met |

---

## Business Hours Considerations

### If Business Hours Configured

Timers only count during operating hours:
- Pauses at end of business day
- Resumes at start of next business day
- Weekends may not count
- Holidays may not count (if configured)

### Example

```
SLA: 4 business hours
Business Hours: 9 AM - 5 PM, Mon-Fri

Request submitted: Friday 4 PM
Time counted Friday: 1 hour (4 PM - 5 PM)
Time counted Monday: 3 hours (9 AM - 12 PM)
Deadline: Monday 12 PM
```

### If 24/7 Configured

Timers count continuously:
- No pausing
- Weekends count
- All hours equal

---

## Metrics and Reporting

### What Gets Recorded

For each request:
- Response time (actual)
- Response deadline (committed)
- Response met (true/false)
- Resolution time (actual)
- Resolution deadline (committed)
- Resolution met (true/false)

### Aggregated Metrics

In Insights and Delivery App:

| Metric | Calculation |
|--------|-------------|
| Response SLA % | (Responded on time / Total responded) × 100 |
| Resolution SLA % | (Resolved on time / Total resolved) × 100 |
| Avg Response Time | Sum of response times / Count |
| Avg Resolution Time | Sum of resolution times / Count |

### Historical Accuracy

SLA results are immutable:
- Can't retroactively change breach to met
- Provides accurate historical record
- Supports honest client reporting

---

## Edge Cases

### Request Completed Without Response

If agent resolves without ever messaging:
- Response timer continues until completion
- At completion, response is recorded (met or breached)
- Resolution timer stops normally

**Best practice:** Always respond before resolving.

### Request Reopened

If a completed request is reopened:
- SLA timers for original completion remain
- New work may or may not start new SLAs (depends on configuration)
- Typically tracked as new request activity

### Multiple Response Attempts

Only the **first** message counts for response SLA:
- First message stops timer
- Subsequent messages don't affect response SLA
- All messages affect resolution work

---

## Best Practices

### Maximizing Response SLA

1. **Acknowledge quickly** — even brief messages count
2. **Monitor Warning status** — act before breach
3. **Use templates** — speed up acknowledgments

### Maximizing Resolution SLA

1. **Set realistic SLAs** — don't overpromise
2. **Work urgently on Warning items**
3. **Complete and close promptly** — don't leave finished work open
4. **Communicate delays** — clients appreciate proactive notice

### When Breach Is Inevitable

1. **Communicate to client before breach**
2. **Document the reason**
3. **Still work to resolve ASAP**
4. **Review for process improvement**

---

## Troubleshooting

### Timer not starting

- Verify SLA is configured (cloud default or client override)
- Check request was properly submitted
- Refresh page

### Response timer didn't stop

- Verify message was sent via Messenger (not Jira)
- Check message actually sent (not draft)
- Refresh page

### Resolution timer didn't stop

- Verify status changed to "Completed"
- Check if there's a status sync issue
- Manually update if needed

### Wrong deadline showing

- Check SLA configuration
- Verify correct client is associated
- Check business hours settings

---

## Related Documentation

- **[SLA Tracking](../02-features/sla-tracking.md)** — Feature overview
- **[Client Directory](../02-features/client-directory.md)** — Configuring SLAs
- **[Insights](../02-features/insights.md)** — Viewing SLA metrics

---

*Next: [Hours Consumption →](hours-consumption.md)*
