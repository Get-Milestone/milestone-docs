# End-to-End Request Flow

This guide traces a request from the moment a client submits it to final resolution, showing every touchpoint in the Milestone system.

---

## The Complete Journey

```
CLIENT                    YOUR TEAM                  SYSTEMS
──────                    ─────────                  ───────

1. Submits request ──────────────────────────────▶ Portal creates request
        │                                                  │
        │                                                  ▼
        │                                          Jira issue created
        │                                                  │
        │                                                  ▼
        │                                          SLA timers start
        │                                                  │
        ▼                                                  ▼
2. Sees request in ◀───────────────────────────── Request in Unified Queue
   their portal                                           │
        │                                                  ▼
        │                                   3. Agent assigns/acknowledges
        │                                                  │
        ▼                                                  ▼
4. Receives message ◀─────────────────────────────── Response SLA stops
   from agent                                             │
        │                                                  ▼
        │                                   5. Agent works request
        │                                          (logs time in Jira)
        │                                                  │
        ▼                                                  ▼
6. Sees hours ◀─────────────────────────────────── Hours sync to client
   consumed                                               │
        │                                                  ▼
        │                                          7. Agent resolves issue
        │                                                  │
        ▼                                                  ▼
8. Sees completion ◀────────────────────────────── Resolution SLA stops
   in portal                                              │
        │                                                  ▼
        ▼                                          9. Metrics update
9. Views history                                   in Insights
```

---

## Phase 1: Request Submission

### What the Client Does

1. Opens their portal (via portal link)
2. Clicks "New Request"
3. Fills in the form:
   - Title
   - Description
   - Urgency level
   - Category (if configured)
4. Clicks Submit

### What Happens Automatically

1. **Request record created** in Milestone database
2. **Jira issue created** in the client's linked project
3. **SLA timers start**:
   - Response timer begins counting down
   - Resolution timer begins counting down
4. **Request appears** in Unified Queue
5. **Portal updates** to show the new request with "Submitted" status

### Time: Instant (< 1 second)

---

## Phase 2: Agent Triage

### What the Agent Does

1. Opens Unified Queue
2. Sees new request (may sort by oldest or SLA expiring)
3. Clicks to review details
4. Either:
   - Assigns to self and begins work, or
   - Assigns to appropriate team member

### What Happens

- Request updates with assignee
- Still in Unified Queue (now with assignee shown)
- Appears in assigned agent's My Work view
- SLA timers continue running

### Time: Depends on your process (immediate to hours)

---

## Phase 3: Agent Response

### What the Agent Does

1. Opens the request (from Queue or My Work)
2. Sends a message via Messenger:
   > "Hi, I've received your request and am looking into it now."
3. Updates status to "In Progress" (if desired)

### What Happens

1. **Response SLA timer stops** — first response recorded
2. **Message syncs to Portal** — client sees it immediately
3. **Status updates** everywhere (Queue, Portal)
4. **SLA shows "Responded"** instead of countdown

### Time: Instant sync

---

## Phase 4: Client Sees Response

### What the Client Experiences

1. Opens their portal
2. Sees the request is now "In Progress"
3. Sees the message from the agent
4. Response SLA now shows "Responded" with checkmark
5. Resolution timer still counting down

### What the Client Can Do

- Reply to the message
- Add more information
- Wait for resolution

---

## Phase 5: Agent Works the Request

### What the Agent Does

1. Opens the linked Jira issue
2. Performs the actual work
3. **Logs time** in Jira as they work:
   - Click "Log Work"
   - Enter time spent
   - Add work description
4. Communicates with client as needed via Messenger
5. Updates status if workflow requires

### What Happens

- Worklogs sync to Milestone
- **Hours consumed** increase for this client
- **Hours remaining** decrease
- Hours visible in Portal and Client Directory
- Messages continue syncing bidirectionally

### Time: Minutes to days depending on complexity

---

## Phase 6: Hours Sync

### What Syncs

For each worklog:
```
Agent logs 2h → Jira worklog created → Milestone syncs → Client sees update
```

### What the Client Sees

In their portal:
- Dashboard shows updated hours balance
- Request detail shows hours logged on this request
- Total consumed hours increases

### What Your Team Sees

- Client Directory shows updated hours
- Request detail shows hours breakdown
- Insights reflects consumption

---

## Phase 7: Issue Resolution

### What the Agent Does

1. Completes the work
2. Sends final message to client:
   > "This issue is now resolved. [Brief explanation]. Please let me know if you have any questions."
3. Updates the Jira issue status to resolved/done
4. The request status updates to "Completed"

### What Happens

1. **Resolution SLA timer stops** — resolution recorded
2. **Request status changes** to Completed
3. **Metrics update** in Insights
4. **Portal updates** to show completed status

---

## Phase 8: Client Sees Resolution

### What the Client Experiences

1. Opens their portal
2. Sees request is now "Completed"
3. Sees resolution message
4. Resolution SLA shows "Resolved" with checkmark
5. Request moves to Closed Requests history

### Post-Resolution

Client can:
- Review the resolution
- Reply if they have questions (may create follow-up)
- Access request in their history anytime

---

## Phase 9: Metrics and Reporting

### What Gets Recorded

| Metric | Data Captured |
|--------|---------------|
| Response Time | Time from submission to first message |
| Resolution Time | Time from submission to completion |
| SLA Met/Breached | Whether timers were beat |
| Hours Consumed | Total time logged |

### Where Data Appears

- **Insights**: Team-level metrics
- **My Work**: Personal KPIs
- **Delivery App**: Executive dashboards
- **Reports**: Exportable data

---

## Timeline Example

Here's a realistic example timeline:

| Time | Event | SLA Status |
|------|-------|------------|
| 9:00 AM | Client submits request | Response: 4h remaining, Resolution: 24h remaining |
| 9:05 AM | Agent sees in queue | Response: 3h 55m remaining |
| 9:10 AM | Agent sends acknowledgment | **Response: Met ✅** |
| 9:15 AM | Agent starts investigation | Resolution: 23h 45m remaining |
| 10:30 AM | Agent logs 1h 15m | Hours consumed: 1.25h |
| 11:00 AM | Agent updates client with progress | Resolution: 22h remaining |
| 2:00 PM | Agent completes work, resolves | **Resolution: Met ✅** (5h total) |
| 2:05 PM | Client confirms in portal | Complete |

---

## Touchpoints Summary

### Client Touchpoints
1. Portal - Submit request
2. Portal - View status and SLA
3. Portal - Read/send messages
4. Portal - See hours consumed
5. Portal - View resolution
6. Portal - Access history

### Agent Touchpoints
1. Unified Queue - See and triage request
2. My Work - Personal assignments
3. Messenger - Communicate with client
4. Jira - Work issue and log time
5. Milestone - Update status and complete

### System Touchpoints
1. Request created in Milestone
2. Jira issue created
3. SLA timers managed
4. Messages synced
5. Worklogs synced
6. Metrics calculated

---

## When Things Don't Follow the Happy Path

### Request Needs More Information

```
Client submits → Agent responds asking for info → Client provides → Work continues
```

SLA response timer stops at first response, even if it's a question.

### Request Reassigned

```
Agent A assigned → Realizes needs different skill → Reassigns to Agent B
```

Request moves to Agent B's My Work. SLA timers unaffected.

### SLA Breached

```
Timer expires → Shows as breached → Work continues → Eventually resolved
```

Breach is recorded permanently. Resolution still tracked separately.

### Client Unresponsive

```
Agent needs info → Messages client → No response → Follow up → Eventually resolve or close
```

Document attempts. Resolution may be "closed - no response."

---

## Related Documentation

- **[Daily Operations](daily-operations.md)** — Recommended daily workflow
- **[SLA Tracking](../02-features/sla-tracking.md)** — SLA details
- **[Hours Tracking](../02-features/hours-tracking.md)** — Time logging
- **[Messenger](../02-features/messenger.md)** — Communication

---

*Next: [SLA Lifecycle →](sla-lifecycle.md)*
