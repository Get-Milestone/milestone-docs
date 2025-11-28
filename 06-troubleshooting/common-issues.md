# Common Issues and Solutions

This guide covers the most frequently encountered issues in Milestone and how to resolve them.

---

## Request Issues

### Request Not Appearing in Queue

**Symptom:** Client submitted request but agent doesn't see it.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Not refreshed | Click refresh button in Unified Queue |
| Filters active | Clear all filters and search |
| Wrong client selected | Check client filter is set to "All" |
| Submission failed | Check client's portal for error message |
| Sync delay | Wait 10-30 seconds, then refresh |

**If still missing:**
- Check Jira project for the issue
- Verify client is properly configured
- Contact support with request details

### Request Created But No Jira Issue

**Symptom:** Request exists in Milestone but no Jira issue created.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Wrong project key | Verify client's project key is correct |
| Jira permissions | Check Milestone has permission to create issues |
| Issue type invalid | Verify default issue type exists in project |

**To fix:**
1. Edit client configuration
2. Correct the project key or issue type
3. May need to manually create Jira issue and link

---

## SLA Issues

### SLA Timer Not Starting

**Symptom:** Request exists but no SLA timer showing.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| SLA not configured | Set cloud default or client SLA |
| Client has no SLA | Configure SLA for this client |
| Display issue | Refresh the page |

**To fix:**
1. Go to Client Directory
2. Check if client has SLA override
3. If not, check cloud defaults
4. Configure missing SLA

### Response Timer Didn't Stop

**Symptom:** Agent sent message but response timer still running.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Message via Jira not Messenger | Send message through Milestone Messenger |
| Message didn't send | Check message actually sent (not draft) |
| Sync delay | Wait a moment, then refresh |

**Key point:** Only Messenger messages stop the response timer. Jira comments don't count.

### Resolution Timer Didn't Stop

**Symptom:** Request resolved but timer still running.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Status not "Completed" | Change status to Completed |
| Jira issue not resolved | Resolve the Jira issue |
| Sync issue | Wait and refresh; manually update if needed |

### Wrong SLA Times

**Symptom:** SLA showing different times than expected.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Client override differs from expected | Check client's SLA override settings |
| Business hours affecting calculation | Review business hours configuration |
| Default different than expected | Check cloud default SLA settings |

---

## Hours Issues

### Hours Not Syncing

**Symptom:** Time logged in Jira but not appearing in Milestone.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Wrong Jira issue | Verify worklog is on request's linked issue |
| Sync delay | Wait 30-60 seconds, refresh |
| Issue not linked to client | Check request is associated with client |

**To verify:**
1. Open the Jira issue
2. Confirm worklog exists
3. Confirm issue is linked to Milestone request
4. Check client directory for hours update

### Client Hours Balance Wrong

**Symptom:** Client's hours don't match expected.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Worklogs on wrong issues | Audit worklogs across client's project |
| Purchased hours incorrect | Update Hours Purchased in client settings |
| Deleted worklogs not reflected | Wait for sync; contact support if persistent |

### Negative Hours Balance

**Symptom:** Client shows negative remaining hours.

**Explanation:** This is valid—client has consumed more than purchased.

**Actions:**
1. Discuss with client about purchasing more hours
2. Update Hours Purchased when they buy more
3. Balance will correct automatically

---

## Messenger Issues

### Messages Not Appearing

**Symptom:** Sent message but recipient doesn't see it.

**For Agent-to-Client:**

| Cause | Solution |
|-------|----------|
| Client hasn't refreshed | Ask client to refresh portal |
| Portal session issue | Have client log out and back in |
| Sync delay | Wait a moment; message should appear |

**For Client-to-Agent:**

| Cause | Solution |
|-------|----------|
| Agent hasn't refreshed | Refresh Messenger or request |
| Looking at wrong request | Verify correct request is open |

### Can't Send Messages

**Symptom:** Send button not working or message fails.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Network issue | Check internet connection |
| Request closed | May not be able to message on closed requests |
| Session expired | Refresh page or re-authenticate |

---

## Portal Issues

### Portal Link Not Working

**Symptom:** Client clicks link and gets error.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Link expired | Generate new link |
| Link copied incorrectly | Send complete URL |
| Browser issue | Try different browser |

**To fix:**
1. Generate new portal link
2. Send via email (avoid messaging apps that may mangle URLs)
3. Verify client can access

### Client Can't Sign In

**Symptom:** Client has account but can't log in.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Forgot password | Use "Forgot Password" to reset |
| Wrong email | Verify email address |
| Account issue | Contact support for account investigation |

### Client Sees Wrong Company

**Symptom:** Client logged in but sees different company data.

**This shouldn't happen.** If it does:
1. Have client sign out immediately
2. Investigate which link they used
3. Contact support to correct account association
4. Generate fresh link for correct client

---

## Permission Issues

### User Can't See Admin Menu

**Symptom:** User expects to be admin but doesn't see Admin menu.

**Cause:** User is not an Admin.

**Solution:**
1. Have existing admin open Admin Console
2. Go to Users tab
3. Promote the user

### Can't Perform Admin Actions

**Symptom:** Admin menu visible but actions fail.

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Session issue | Refresh page, sign out/in |
| Permission changed | Verify still has admin role |
| System issue | Contact support |

---

## Sync Issues

### Data Not Updating

**Symptom:** Changes made but not reflecting.

**General solutions:**
1. **Refresh the page** — Most common fix
2. **Wait 30 seconds** — Sync may be in progress
3. **Clear browser cache** — Stale data issue
4. **Check other views** — May be display-specific

### Jira and Milestone Out of Sync

**Symptom:** Jira shows different data than Milestone.

**For status differences:**
- Verify which system has correct status
- Update the incorrect one
- Allow sync to occur

**For worklog differences:**
- Source of truth is Jira
- Milestone reads from Jira
- Check Jira is correct

---

## Performance Issues

### Milestone Loading Slowly

**Possible Causes & Solutions:**

| Cause | Solution |
|-------|----------|
| Large dataset | Use filters to reduce data |
| Network latency | Check internet connection |
| Browser performance | Try different browser or clear cache |
| Many open tabs | Close unnecessary tabs |

### Search Not Working

**Symptom:** Search returns wrong or no results.

**Solutions:**
1. Check spelling
2. Try partial terms
3. Clear filters that may conflict
4. Refresh and try again

---

## Installation Issues

### App Not Appearing After Install

**Solutions:**
1. Refresh browser
2. Clear browser cache
3. Sign out and back into Jira
4. Check Apps menu carefully

### Permission Request Failed

**Symptom:** Installation fails at permission step.

**Causes:**
- May need organization admin approval
- Policy restrictions on app installations

**Solutions:**
1. Contact Jira organization admin
2. Review organization app policies
3. Request approval if required

---

## When to Contact Support

Contact support@getmilestone.io when:

- Issue persists after trying documented solutions
- Data appears corrupted or incorrect
- Security concerns (unauthorized access)
- Account or billing issues
- Feature not working as documented

**Include in support request:**
- Description of issue
- Steps to reproduce
- Expected vs actual behavior
- Screenshots if applicable
- Time issue occurred

---

## Quick Reference

### Most Common Fixes

| Issue | First Try |
|-------|-----------|
| Data not showing | Refresh page |
| Feature not working | Clear filters |
| Sync seems stuck | Wait 30 sec, refresh |
| Permission denied | Verify role |
| Link not working | Generate new link |

### Diagnostic Steps

1. **Refresh** the page
2. **Check filters** — clear them
3. **Verify configuration** — SLA, client, hours
4. **Check permissions** — role, access
5. **Try different browser** — rule out browser issues
6. **Contact support** — if none of above work

---

## Related Documentation

- **[SLA Tracking](../02-features/sla-tracking.md)** — SLA-specific guidance
- **[Hours Tracking](../02-features/hours-tracking.md)** — Hours-specific guidance
- **[Portal Links](../03-client-portal/portal-links.md)** — Portal access issues

---

*For additional help, contact support@getmilestone.io*
