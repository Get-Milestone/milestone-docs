# Glossary

A comprehensive reference of terms used throughout Milestone and this documentation.

---

## A

### Admin
A user role with full access to Milestone features including user management, configuration, and all operational functions. See [Roles](04-admin/roles.md).

### Admin Console
The administrative interface in the Forge app where admins manage users, configure settings, and control Delivery App access.

### Assignee
The agent responsible for working a specific request. Shown in the Unified Queue and My Work views.

### Atlassian Cloud
The cloud-hosted version of Atlassian products (Jira, Confluence, etc.) where Milestone integrates as a Forge app.

---

## B

### Breach
When an SLA timer expires before the required action (response or resolution) is completed. Breaches are permanently recorded for reporting.

### Bulk Import
A feature in Client Directory that allows importing multiple clients at once via CSV file.

---

## C

### Client
A company that your MSP provides services to. Each client has their own requests, hours, and portal access. Different from "customer" or "end user."

### Client Directory
The Forge app feature for managing all client configurations, including SLAs, hours, and portal links.

### Client Portal
The standalone web application where your clients (end customers) submit requests, track status, and communicate with your team. No Jira license required.

### Client UUID
The internal unique identifier for a client in Milestone's database. Different from the client ID you assign.

### Cloud Default
SLA or configuration settings that apply to all clients unless overridden at the client level.

### Cloud ID
The unique identifier for an Atlassian Cloud instance (tenant). Used to isolate data between different MSP organizations.

### Completed
The final status of a request indicating work is done and the issue is resolved.

### Consumed Hours
The total hours logged against a client's requests, calculated from Jira worklogs.

### Core API
The backend service that powers Milestone, running on Google Cloud and connecting all applications.

---

## D

### Delivery App
The standalone web application for leadership and executives to view metrics, reports, and client analytics. No Jira license required.

### Demote
To change a user's role from Admin to Member, removing administrative privileges.

---

## E

### End Customer
An employee of your client company who uses the Client Portal. Also called "portal user."

### Expiration
The date/time when a portal link stops working. Configurable when generating links.

---

## F

### Filter
A way to narrow down the requests shown in Unified Queue or other views based on criteria like client, status, or SLA state.

### First Response
The initial reply to a client's request. Stopping the response SLA timer requires a message via Messenger.

### Forge
Atlassian's platform for building cloud apps that run directly within Atlassian products. Milestone's Jira integration is built on Forge.

### Forge App
The Milestone application installed in your Jira instance, providing the Unified Queue, My Work, Messenger, and other features.

---

## G

### Generate Link
The action of creating a portal invitation link for a client in the Client Directory.

---

## H

### HMAC
Hash-based Message Authentication Code. The security mechanism used for communication between the Forge app and Core API.

### Hours
Time tracked against client work, typically measured in hours. Includes purchased, consumed, and remaining.

### Hours Purchased
The total hours allocated to a client, typically based on a service agreement or contract.

### Hours Remaining
The balance of hours a client has left (purchased minus consumed).

---

## I

### In Progress
A request status indicating work has begun but is not yet complete.

### Insights
The analytics dashboard in the Forge app showing SLA metrics, volume analysis, and performance data.

### Issue
A Jira ticket. When a client submits a request, a corresponding Jira issue is created.

### Issue Type
The Jira issue type used when creating tickets from client requests (e.g., Task, Bug, Support).

---

## J

### Jira
Atlassian's project and issue tracking software. Milestone integrates with Jira Cloud.

### Jira Issue Key
The unique identifier for a Jira issue (e.g., PROJ-123). Links requests to their corresponding Jira tickets.

### JWT
JSON Web Token. Used for authentication in the Client Portal and Delivery App.

---

## K

### KPI
Key Performance Indicator. Metrics shown in My Work and Insights to measure performance.

---

## L

### Link
See "Portal Link."

---

## M

### Member
A user role with standard access to operational features (Unified Queue, My Work, Messenger, Insights) but not administrative functions.

### Messenger
The real-time communication feature for exchanging messages between your team and clients. Syncs between Forge app and Client Portal.

### MSP
Managed Service Provider. The type of organization Milestone is designed for—companies that provide IT or software services to other businesses.

### My Work
The personal dashboard in the Forge app showing requests assigned to the current user, along with personal KPIs.

---

## N

### Notification
An alert or message informing users of activity, such as new messages or status changes.

---

## O

### On Track
An SLA status indicating the timer has more than 25% of time remaining (green indicator).

### Open Request
A request that is not yet completed. Includes "Submitted" and "In Progress" statuses.

### Override
A client-specific setting that replaces the cloud default. Used for SLAs and other configurations.

---

## P

### Portal
See "Client Portal."

### Portal Link
A unique URL that allows client employees to access the Client Portal and create accounts. Time-limited and client-specific.

### Portal User
An end customer who has created an account and can access the Client Portal.

### Project Key
The identifier for a Jira project (e.g., PROJ). Each client is typically linked to one Jira project.

### Promote
To change a user's role from Member to Admin, granting administrative privileges.

### Purchased Hours
See "Hours Purchased."

---

## Q

### Queue
See "Unified Queue."

### QBR
Quarterly Business Review. A periodic meeting with clients to review performance. Milestone provides data for QBR preparation.

---

## R

### Remaining Hours
See "Hours Remaining."

### Request
A service request submitted by a client via the Portal. Creates a corresponding Jira issue.

### Resolution
The completion of a request. Stops the resolution SLA timer.

### Resolution SLA
The time commitment for completing a request from submission to resolution. See [SLA Tracking](02-features/sla-tracking.md).

### Resolution Time
The actual time taken to resolve a request (submission to completion).

### Response
The first reply to a client's request via Messenger. Stops the response SLA timer.

### Response SLA
The time commitment for initially responding to a request. See [SLA Tracking](02-features/sla-tracking.md).

### Response Time
The actual time taken to first respond to a request.

### Role
A permission level assigned to users. Milestone has Admin and Member roles.

---

## S

### SLA
Service Level Agreement. Time-based commitments for response and resolution of client requests.

### SLA Compliance
The percentage of requests that met their SLA requirements.

### SLA Override
Client-specific SLA settings that replace cloud defaults.

### SLA Timer
The countdown display showing time remaining until an SLA deadline.

### Sort
The order in which requests are displayed. Options include oldest, newest, SLA expiring, and client name.

### Status
The current state of a request: Submitted, In Progress, or Completed.

### Submitted
The initial status of a new request, before work begins.

---

## T

### Tenant
An isolated instance in a multi-tenant system. In Milestone, each Atlassian Cloud instance is a separate tenant.

### Timer
See "SLA Timer."

### Tracking ID
A unique identifier for a request (e.g., REQ-1234), separate from the Jira issue key.

---

## U

### Unified Queue
The central view of all client requests in the Forge app, with filtering, sorting, and detail panel.

### Unread
Messages or updates that haven't been viewed yet.

### Urgency
A classification set by clients when submitting requests (Low, Normal, High, Critical).

### User
A person who uses Milestone. Can be an MSP team member, portal user, or Delivery App user.

---

## V

### Volume
The number of requests, typically analyzed over time or by client.

---

## W

### Warning
An SLA status indicating the timer has less than 25% of time remaining (yellow indicator).

### Worklog
A time entry in Jira recording work done on an issue. Worklogs sync to Milestone as consumed hours.

---

## Acronyms Quick Reference

| Acronym | Full Term |
|---------|-----------|
| API | Application Programming Interface |
| CDN | Content Delivery Network |
| CSV | Comma-Separated Values |
| GDPR | General Data Protection Regulation |
| HMAC | Hash-based Message Authentication Code |
| JWT | JSON Web Token |
| KPI | Key Performance Indicator |
| MSP | Managed Service Provider |
| QBR | Quarterly Business Review |
| RBAC | Role-Based Access Control |
| SLA | Service Level Agreement |
| TLS | Transport Layer Security |
| UUID | Universally Unique Identifier |

---

## Related Documentation

- **[Overview](00-overview.md)** — Platform introduction
- **[Features](02-features/unified-queue.md)** — Feature documentation
- **[Admin](04-admin/roles.md)** — Administrative concepts

---

*Can't find a term? Contact support@getmilestone.io*
