# Portal Links

Portal links are the gateway for your clients to access their Client Portal. These secure, time-limited invitation links connect users to their company's portal without requiring you to manage accounts manually.

---

## How Portal Links Work

### The Flow

```
1. YOU GENERATE A LINK
   └── In Client Directory → Portal Access tab
       └── Link is created with expiration date
           └── Unique URL tied to specific client

2. YOU SHARE THE LINK
   └── Email, message, or onboarding materials
       └── Client clicks the link

3. CLIENT CREATES ACCOUNT
   └── Signs up with their email
       └── Account automatically associated with their company
           └── Full portal access granted
```

### Link Security

- **Client-scoped**: Each link connects to one specific client
- **Time-limited**: Links expire after a set period (default 90 days)
- **One-time setup**: After account creation, users sign in normally
- **Revocable**: Generate new links to replace compromised ones

---

## Generating Portal Links

### Step-by-Step

1. Open **Client Directory** in the Milestone Forge app
2. Click the **Portal Access** tab
3. Select the client from the dropdown
4. Configure options:
   - **Company Name**: How the company appears in the portal
   - **Expiration**: How long the link is valid
5. Click **Generate Link**
6. Copy the generated link

### Configuration Options

| Option | Default | Description |
|--------|---------|-------------|
| **Company Name** | Client name | Display name shown in the portal |
| **Expiration** | 90 days | How long until the link stops working |

### Link Formats Available

After generation, you get multiple formats:

**Direct URL:**
```
https://portal.getmilestone.io/join?token=abc123xyz...
```
Best for: Email, chat, direct sharing

**HTML Link:**
```html
<a href="https://portal.getmilestone.io/join?token=abc123xyz">
  Access Your Portal
</a>
```
Best for: Embedding in web pages or HTML emails

**iFrame Embed:**
```html
<iframe src="https://portal.getmilestone.io/join?token=abc123xyz" 
        width="100%" height="600"></iframe>
```
Best for: Embedding portal directly in another website

---

## Sharing Portal Links

### Best Practices

**DO:**
- ✅ Send via secure channels (email, authenticated chat)
- ✅ Include brief instructions
- ✅ Note the expiration date
- ✅ Provide your contact for questions

**DON'T:**
- ❌ Post publicly (links are access tokens)
- ❌ Share on unsecured channels
- ❌ Use expired links

### Email Template

```
Subject: Your Service Portal Access

Hi [Name],

Here's your access link to our service portal:

[Portal Link]

With this portal, you can:
• Submit new service requests
• Track status and SLA timers
• View your hours usage
• Message our team

The link is valid for 90 days. Click it to create your account—
it only takes a minute.

Questions? Just reply to this email.

Best,
[Your name]
```

### Onboarding Checklist

When sharing links with new clients:

- [ ] Generate link with correct client selected
- [ ] Verify company name display is correct
- [ ] Send link via email with instructions
- [ ] Confirm client received the email
- [ ] Follow up to ensure successful registration
- [ ] Record that portal access was provided

---

## Managing Links

### Regenerating Links

If a link expires or is compromised:

1. Go to Client Directory → Portal Access
2. Select the client
3. Generate a new link
4. Send the new link to the client

Old links automatically become invalid when the expiration passes.

### Multiple Users

A single link can be used by multiple people from the same company:
- Share the same link with multiple contacts
- Each person creates their own account
- All accounts connect to the same company

### Tracking Access

Currently, portal link usage isn't directly tracked in Milestone. Monitor access by:
- Client request activity (they're using the portal)
- Message activity
- Login patterns (if you have analytics)

---

## Expiration Handling

### What Happens When Links Expire

- The link URL returns an error message
- No new users can register with that link
- Existing users can still sign in (their accounts aren't affected)

### Expiration Best Practices

| Scenario | Recommended Expiration |
|----------|------------------------|
| New client onboarding | 90 days |
| Quick setup needed | 30 days |
| Security-sensitive | 7-14 days |
| Internal testing | 1-7 days |

### Proactive Renewal

Before links expire:
1. Check when links were generated
2. Generate new links for approaching expirations
3. Send renewal communication to clients

---

## Common Scenarios

### Scenario 1: New Client Setup

1. Create client in Client Directory
2. Configure SLA and hours
3. Generate portal link (90 days)
4. Send welcome email with link
5. Follow up to confirm access

### Scenario 2: Additional User Access

Existing client needs to add a colleague:

1. Find the client's existing link (or generate new one)
2. Share with the new user
3. They create their account
4. Automatically see same company data

### Scenario 3: Link Expired

Client contact says they can't access:

1. Go to Client Directory → Portal Access
2. Generate new link
3. Send to client with apology
4. Note: Set calendar reminder for next expiration

### Scenario 4: Employee Left Client Company

Former employee shouldn't have access:

1. Currently: Generate new link for remaining users
2. Old user can still sign in (account persists)
3. For security, contact support about account removal

---

## Security Considerations

### Link as Access Token

Portal links contain an access token:
- Treat links like passwords
- Don't share on public channels
- Revoke/regenerate if compromised

### Account Security

Once a user creates an account:
- Their access is tied to their login credentials
- The original link is no longer needed
- They sign in directly going forward

### Best Security Practices

1. Use reasonable expiration periods
2. Share via secure channels only
3. Regenerate links if security is questioned
4. Keep records of who received links
5. Audit portal users periodically

---

## Troubleshooting

### "Link not working"

1. Check if link expired
2. Generate new link
3. Verify correct URL was copied
4. Ensure no extra characters in URL

### "Can't create account"

1. User may already have an account (try sign in)
2. Link may be expired
3. Browser/connection issues—try different browser

### "User sees wrong company"

1. They used a different company's link
2. Contact support to correct account association
3. Provide correct link for their company

### "Multiple users, one not working"

1. Verify all users have the same link
2. Check if some users already have accounts
3. Generate fresh link if issues persist

---

## Bulk Link Generation

For multiple clients:

Currently, links must be generated individually. For bulk onboarding:

1. Prepare list of clients to onboard
2. Work through each in Client Directory
3. Generate and send links systematically
4. Track who has been sent links

Consider creating a tracking spreadsheet:
- Client name
- Link generated date
- Link expiration date
- Sent to whom
- Confirmed access

---

## Related Documentation

- **[Portal Overview](portal-overview.md)** — What clients see
- **[Client Directory](../02-features/client-directory.md)** — Managing clients
- **[Portal FAQ](portal-faq.md)** — Common questions

---

*Next: [Portal FAQ →](portal-faq.md)*
