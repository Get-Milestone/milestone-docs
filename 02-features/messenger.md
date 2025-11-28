# Messenger

The Messenger is Milestone's built-in communication hub for client conversations. Messages sent here appear instantly in the Client Portal, and client replies appear instantly for your team—creating a seamless, real-time communication channel that lives alongside your work.

---

## Why Use Messenger?

### Before Milestone Messenger
- Client updates scattered across email, Slack, and ticket comments
- No central record of communications
- Agents miss messages; clients miss updates
- Response SLA tracking requires manual effort

### With Messenger
- All client communication in one place
- Real-time sync with Client Portal
- Messages automatically stop response SLA timers
- Complete audit trail on every request

---

## Accessing Messenger

### Standalone View
1. Click **Messenger** in the sidebar (speech bubble icon)
2. See all conversations across all requests
3. Full conversation list with search and filters

### From Request Detail
1. Open any request (in Unified Queue or My Work)
2. Scroll to the Messages section in the detail panel
3. Send messages directly from there

Both methods access the same messages—they're just different entry points.

---

## The Messenger Interface

### Conversation List (Left Panel)

Shows all requests that have messages:

| Element | Description |
|---------|-------------|
| **Request Title** | What the conversation is about |
| **Client Name** | Which client this is for |
| **Last Message Preview** | Snippet of most recent message |
| **Timestamp** | When the last message was sent |
| **Unread Indicator** | Badge if you have unread messages |

### Message Thread (Right Panel)

When you select a conversation:

- **Full message history** in chronological order
- **Sender identification** (your team vs. client)
- **Timestamps** on each message
- **Compose box** at the bottom to reply

---

## Sending Messages

### Composing a Message

1. Select or open a conversation
2. Type your message in the compose box
3. Click **Send** (or press Enter/Return)

### What Gets Sent

- Your message text
- Your name as the sender
- Timestamp

### What the Client Sees

In their Portal, the client sees:
- Your message content
- "Your Team" or your name as sender
- The timestamp
- The message linked to their request

---

## Message Sync

### Real-Time Updates

- **Your message → Portal**: Instant (< 1 second)
- **Client message → Messenger**: Instant (< 1 second)
- No refresh needed—messages appear automatically

### Offline Behavior

If you're offline when a client sends a message:
- Message is stored
- Appears when you reconnect/refresh
- No messages are lost

---

## SLA Integration

### First Response

When you send a message on a request:
- The **response SLA timer stops**
- This counts as your "first response"
- Even a brief acknowledgment works

### Example Flow

```
09:00 - Client submits request (response SLA starts: 4 hours)
09:15 - You send: "Thanks, I'm looking into this"
        └── Response SLA STOPS (met with 3h 45m remaining ✅)
```

### What Counts as a Response

- ✅ Any message sent via Messenger
- ❌ Jira comments (not synced to Messenger)
- ❌ Email replies (not tracked)
- ❌ Assignment changes

---

## Best Practices

### Acknowledge Quickly

Even if you can't solve the issue immediately:
> "Hi [Name], thanks for reaching out. I've received your request and am looking into it. I'll have an update within [timeframe]."

This:
- Stops the response SLA ✅
- Sets client expectations ✅
- Shows you're engaged ✅

### Be Specific About Next Steps

Instead of: "I'll look into this"

Try: "I'll investigate the database connection issue and will have an update by 3pm today."

### Keep Clients Informed on Delays

If work is taking longer than expected:
> "Hi [Name], wanted to update you—this is more complex than initially assessed. We're still on track for resolution by [date], but I'll keep you posted if that changes."

### Use the Right Channel

| Situation | Use Messenger | Use Something Else |
|-----------|---------------|-------------------|
| Status updates | ✅ | |
| Questions for client | ✅ | |
| Detailed technical discussion | | Jira comments (internal) |
| Sensitive information | Consider | Secure channel |
| Quick acknowledgment | ✅ | |

### Check for Unread Messages

Start and end your day by checking for unread messages:
1. Open Messenger
2. Look for unread indicators
3. Respond to waiting clients

---

## Common Scenarios

### Scenario 1: New Request Acknowledgment

**Situation:** New request arrives, you're the assignee.

**Action:**
```
Hi Sarah, thanks for submitting this request. I've assigned it to myself and 
will start investigating the login issue right away. I expect to have an 
initial diagnosis within the next hour.

Best,
[Your name]
```

### Scenario 2: Requesting Information

**Situation:** You need more details to proceed.

**Action:**
```
Hi Tom, to troubleshoot the report issue, I need a few more details:

1. Which report are you trying to run?
2. What error message do you see (if any)?
3. When did this issue start?

Once I have this information, I can investigate further.
```

### Scenario 3: Providing Resolution

**Situation:** Issue is resolved.

**Action:**
```
Hi Lisa, good news! I've identified and fixed the issue. The problem was 
[brief explanation].

Please try [action] and let me know if everything works as expected. 
I'll close this request once you confirm.
```

### Scenario 4: Escalation Notice

**Situation:** Issue needs escalation.

**Action:**
```
Hi Alex, this issue requires specialized expertise, so I'm bringing in 
our senior engineer, [Name]. They'll be in touch shortly with next steps.

In the meantime, if you have any questions, feel free to reply here.
```

---

## Conversation History

### All Messages Are Saved

- Complete history is preserved
- Available even after request is closed
- Useful for future reference

### Finding Past Conversations

1. Open Messenger
2. Use the search box
3. Search by:
   - Request title
   - Client name
   - Message content (if implemented)

---

## Common Mistakes to Avoid

### ❌ Using Jira Comments Instead of Messenger

Jira comments don't sync to the Portal—clients won't see them.

**Fix:** Use Messenger for all client-facing communication.

### ❌ Delayed Responses Without Acknowledgment

Waiting hours to respond, even when investigating.

**Fix:** Send a quick acknowledgment immediately, detailed response later.

### ❌ One-Word Responses

Sending just "OK" or "Thanks" without context.

**Fix:** Include what you're doing next and when they can expect updates.

### ❌ Assuming Clients Read Jira Tickets

Clients use the Portal, not Jira.

**Fix:** Communicate everything client-relevant via Messenger.

### ❌ Internal Discussions in Messenger

Team coordination visible to clients is unprofessional.

**Fix:** Use Jira comments or other internal tools for team discussion.

---

## Notifications

### Agent Notifications

When a client sends a message:
- Unread indicator appears in Messenger
- Request shows unread badge in queue views
- Browser notification (if enabled)

### Client Notifications

When you send a message:
- Appears in their Portal instantly
- Email notification (if configured)
- Portal shows unread indicator

---

## Troubleshooting

### Messages not appearing

1. Check your internet connection
2. Refresh the page
3. Verify the message was sent (check for confirmation)

### Client says they didn't receive message

1. Confirm message appears in Messenger history
2. Ask client to refresh their Portal
3. Check they're looking at the correct request

### Can't send messages

1. Check internet connection
2. Verify the request isn't closed/archived
3. Ensure you have permission to message

### Old messages missing

- All messages should be preserved
- Try refreshing or clearing browser cache
- Contact support if messages are genuinely missing

---

## Privacy Considerations

### What Clients See

- Messages marked as from your team
- Your name (if configured)
- Message timestamps
- Only messages on their own requests

### What Clients Don't See

- Messages on other clients' requests
- Internal Jira comments
- System logs or technical data
- Other clients' information

---

## Related Documentation

- **[Unified Queue](unified-queue.md)** — Messaging from request views
- **[My Work](my-work.md)** — Quick messaging on your assignments
- **[SLA Tracking](sla-tracking.md)** — How messages affect SLA timers
- **[Client Portal](../03-client-portal/portal-overview.md)** — The client's view

---

*Next: [Insights →](insights.md)*
