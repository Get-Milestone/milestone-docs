# Daily Operations Guide

This guide outlines the recommended daily workflow for MSP agents using Milestone. Following a consistent routine helps prevent SLA breaches, keeps clients happy, and maintains team effectiveness.

---

## The Daily Routine

### Morning Startup (10-15 minutes)

When you begin your day:

#### 1. Check Breached Items First
```
Unified Queue → Filter: SLA Status = Breached
```
- Address any breached items immediately
- Send client communication about delays
- Escalate if needed

#### 2. Review Warning Items
```
Unified Queue → Filter: SLA Status = Warning
```
- These are close to breach
- Prioritize for immediate attention
- Quick acknowledgment if you can't work immediately

#### 3. Check Unassigned Requests
```
Unified Queue → Filter: Assignee = Unassigned
```
- Assign to yourself or appropriate team member
- Ensure nothing sits unassigned too long

#### 4. Review Your Work
```
My Work → Overview
```
- See your assigned items
- Check "Waiting for Reply" filter
- Respond to any pending client messages

---

## During the Day

### Working Requests

**For each request you work:**

1. **Acknowledge First**
   - Send a quick message via Messenger
   - Stops the response SLA timer
   - Sets client expectations

2. **Update Status**
   - Move to "In Progress" when starting
   - Keep status current

3. **Log Time**
   - Log worklogs in Jira as you work
   - Don't wait until end of day
   - Accurate time improves billing

4. **Communicate Progress**
   - Message clients with updates
   - Don't leave them wondering

5. **Complete When Done**
   - Mark request complete
   - Send resolution summary to client
   - Stops resolution SLA timer

### Prioritization Framework

When you have multiple items, work in this order:

| Priority | What to Work |
|----------|--------------|
| 1st | Breached items (damage control) |
| 2nd | Warning items (prevent breach) |
| 3rd | Waiting for Reply (client waiting) |
| 4th | Oldest unworked items |
| 5th | Newly submitted requests |

### Checking Messages

Check Messenger regularly:
- Every 1-2 hours at minimum
- Immediately when you see unread indicators
- After completing any work (client may have questions)

---

## Midday Check (5 minutes)

Around lunchtime:

1. **Refresh Unified Queue**
   - New requests may have arrived
   - SLA statuses may have changed

2. **Check for New Breaches**
   - Items may have breached while working
   - Address any new urgent items

3. **Review Your Messages**
   - Respond to any pending client messages

---

## Afternoon Routine

### End of Day (10 minutes)

Before finishing your day:

#### 1. Clear Waiting Items
- Respond to any "Waiting for Reply" items
- Don't leave clients waiting overnight

#### 2. Update Statuses
- Ensure in-progress items reflect accurate status
- Set expectations for next day if needed

#### 3. Log Any Outstanding Time
- Ensure all worklogs are captured
- Accurate hours tracking

#### 4. Review Tomorrow's Queue
- Check what's upcoming
- Note any items that will need early attention

#### 5. Handoff If Needed
- If items need attention after hours, communicate to on-call
- Document status clearly

---

## Weekly Rhythm

### Monday Morning
- Catch up on weekend submissions
- Review any breaches from over weekend
- Plan the week's priorities

### Friday Afternoon
- Clear as much as possible
- Set expectations with clients for weekend
- Ensure nothing critical waits until Monday

### Weekly Review (30 minutes)
- Check personal KPIs in My Work
- Review Insights for trends
- Identify improvement areas

---

## Communication Best Practices

### When to Message Clients

| Situation | Message? |
|-----------|----------|
| New request received | ✅ Yes - acknowledge |
| Starting work | Optional - depends on complexity |
| Need information | ✅ Yes - ask questions |
| Hit a blocker | ✅ Yes - explain delay |
| Work complete | ✅ Yes - confirm resolution |
| Will miss SLA | ✅ Yes - proactive communication |

### Message Templates

**Acknowledgment:**
> Thanks for reaching out! I've received your request and am looking into it now. I expect to have an update within [timeframe].

**Need Information:**
> To resolve this, I need a bit more information:
> 1. [Question 1]
> 2. [Question 2]
> Once I have this, I can proceed.

**In Progress Update:**
> Quick update: I'm actively working on this. I've [progress made]. Next steps are [what's coming]. Expected completion: [timeframe].

**Resolution:**
> Good news! This issue is resolved. [Brief explanation of what was done]. Please let me know if you have any questions or if the issue recurs.

**Delay Notice:**
> I wanted to update you: this is taking longer than expected due to [reason]. Our new expected completion is [timeframe]. I apologize for the delay and appreciate your patience.

---

## Handling Common Situations

### Multiple Urgent Requests

1. Quickly acknowledge all of them
2. Triage based on business impact
3. Work most critical first
4. Communicate timeline to others
5. Escalate if you can't handle volume

### Complex Request Spanning Days

1. Acknowledge immediately
2. Break into sub-tasks if helpful
3. Provide daily updates
4. Log time regularly
5. Don't let communication gaps occur

### Client Asks for Status

1. Check their request in Unified Queue
2. Provide current status
3. Give expected next steps and timeline
4. Use this as a prompt to message proactively next time

### Request Requires Escalation

1. Document what you've tried
2. Communicate to client that you're escalating
3. Hand off to appropriate person
4. Follow up to ensure it's being handled

---

## Avoiding Common Mistakes

### ❌ Checking Email Before Milestone
Start in Milestone. Email might have requests that aren't in the system yet.

### ❌ Working Without Acknowledging
Always send a quick message first. Stops SLA and sets expectations.

### ❌ Leaving Items "In Progress" Forever
If work is done, mark it complete. Incomplete items skew metrics.

### ❌ End-of-Week Time Logging
Log time daily. You'll forget details and have inaccurate records.

### ❌ Silent Work
Clients appreciate updates. Even "still working on it" is valuable.

---

## Quick Reference

### Morning Checklist
- [ ] Check breached items
- [ ] Check warning items
- [ ] Check unassigned items
- [ ] Review My Work queue
- [ ] Respond to waiting messages

### Per-Request Checklist
- [ ] Acknowledge (message client)
- [ ] Update status
- [ ] Work the request
- [ ] Log time
- [ ] Communicate progress
- [ ] Mark complete when done
- [ ] Send resolution message

### End of Day Checklist
- [ ] Clear waiting messages
- [ ] Update all statuses
- [ ] Log remaining time
- [ ] Review tomorrow's items
- [ ] Handoff if needed

---

## Related Documentation

- **[Unified Queue](../02-features/unified-queue.md)** — Main working queue
- **[My Work](../02-features/my-work.md)** — Personal assignments
- **[Messenger](../02-features/messenger.md)** — Client communication
- **[SLA Tracking](../02-features/sla-tracking.md)** — Understanding SLAs

---

*Next: [End-to-End Flow →](end-to-end-flow.md)*

