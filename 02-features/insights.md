# Insights

Insights is your analytics dashboard within the Milestone Forge app. It provides real-time visibility into SLA performance, request volumes, and team productivity—helping you spot trends, identify issues, and prepare for client conversations.

---

## Why Insights Matters

### For Agents
- See how your performance compares to targets
- Identify patterns in your workload
- Understand your SLA compliance rate

### For Team Leads
- Monitor team performance at a glance
- Spot bottlenecks before they become problems
- Identify training or staffing needs

### For Account Managers
- Prepare for client QBRs with data
- Understand client trends over time
- Identify at-risk accounts

---

## Accessing Insights

1. Open the Milestone app in Jira
2. Click **Insights** in the sidebar (trending up icon)
3. Dashboard loads with current metrics

---

## Dashboard Overview

The Insights dashboard shows several key metric areas:

### Key Performance Indicators (KPIs)

At the top, you'll see headline numbers:

| KPI | What It Shows |
|-----|---------------|
| **Total Requests** | All requests in the selected period |
| **Open Requests** | Currently active requests |
| **In Progress** | Requests being actively worked |
| **Completed** | Requests resolved in the period |

### SLA Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| **Response SLA %** | Percentage meeting response time | 95%+ is good |
| **Resolution SLA %** | Percentage meeting resolution time | 90%+ is good |
| **Avg Response Time** | Average time to first response | Lower is better |
| **Avg Resolution Time** | Average time to completion | Lower is better |

### Volume Analysis

- **By Client**: Which clients generate the most requests
- **By Category**: What types of requests are most common
- **Over Time**: Trend of request volume (if date ranges used)

### Agent Performance

- Requests handled per agent
- SLA compliance per agent
- Current workload distribution

---

## Filtering Data

### Date Range

Filter metrics to specific time periods:

1. Click the date range selector
2. Choose a preset (Last 7 days, Last 30 days, etc.) or custom range
3. Dashboard updates with filtered data

**Common periods:**
- **Last 7 days**: Recent performance snapshot
- **Last 30 days**: Monthly review
- **Last quarter**: QBR preparation
- **Custom**: Specific billing periods

### Client Filter

Focus on a specific client:

1. Click the client dropdown
2. Select a client
3. All metrics filter to that client only

Use this when:
- Preparing for a client meeting
- Investigating a specific client's experience
- Comparing client performance

---

## Understanding Each Metric

### Response SLA Percentage

**What it measures:** Of all requests that have received a response, what percentage met the response SLA?

**Calculation:**
```
(Requests responded within SLA / Total responded requests) × 100
```

**Example:** 47 of 50 requests responded within SLA = 94% Response SLA

**Why it matters:** Indicates how quickly your team acknowledges client needs.

### Resolution SLA Percentage

**What it measures:** Of all completed requests, what percentage met the resolution SLA?

**Calculation:**
```
(Requests resolved within SLA / Total resolved requests) × 100
```

**Example:** 45 of 50 resolved requests met SLA = 90% Resolution SLA

**Why it matters:** Indicates how effectively your team delivers complete solutions.

### Average Response Time

**What it measures:** Mean time from request submission to first agent response.

**Example:** Average of 2h, 3h, 1h, 4h = 2.5h average response time

**Why it matters:** Shows typical wait time clients experience before acknowledgment.

### Average Resolution Time

**What it measures:** Mean time from request submission to completion.

**Example:** Average of 24h, 48h, 12h, 36h = 30h average resolution time

**Why it matters:** Shows typical end-to-end service delivery time.

---

## Using Insights for QBRs

Quarterly Business Reviews are perfect for Insights data:

### Data to Present

1. **SLA compliance** for the quarter
2. **Request volume** trends
3. **Response/resolution** time averages
4. **Category breakdown** (what types of issues)

### Preparation Steps

1. Set date range to the quarter
2. Filter to the specific client
3. Note key metrics
4. Identify trends (improving? declining?)
5. Prepare talking points for outliers

### Example QBR Slide Data

```
Q3 2024 Performance - Acme Corp

Requests: 127 total (↑12% vs Q2)
Response SLA: 96% (target: 95%) ✅
Resolution SLA: 91% (target: 90%) ✅
Avg Response: 1.8 hours
Avg Resolution: 18.5 hours

Top Categories:
- Access Issues: 45 (35%)
- Report Requests: 38 (30%)
- Bug Reports: 25 (20%)
- Other: 19 (15%)
```

---

## Best Practices

### Regular Review Cadence

| Frequency | What to Check |
|-----------|---------------|
| **Daily** | Open request count, any breaches |
| **Weekly** | SLA percentages, volume trends |
| **Monthly** | Client-level analysis, agent performance |
| **Quarterly** | Full QBR preparation, trend analysis |

### Setting Team Goals

Use Insights data to set realistic targets:

1. Review historical performance (last 90 days)
2. Identify current baseline
3. Set improvement targets (e.g., +5% SLA compliance)
4. Track progress weekly

### Identifying Issues Early

Warning signs to watch for:

| Signal | Potential Issue |
|--------|-----------------|
| Dropping SLA % | Capacity problem or process issue |
| Rising volume from one client | Client may need more attention |
| One agent with low SLA % | Training or workload imbalance |
| Increasing resolution times | Complexity increasing or efficiency dropping |

### Comparing Periods

To see improvement (or decline):

1. Note metrics for current period
2. Change date range to previous period
3. Compare the numbers
4. Investigate significant changes

---

## Insights vs. Delivery App

| Aspect | Insights (Forge) | Delivery App |
|--------|------------------|--------------|
| **Audience** | Agents & leads | Executives & managers |
| **Access** | Jira users | Standalone app |
| **Depth** | Operational detail | Executive summary |
| **Export** | Basic | Full reporting suite |

Both show similar data—Insights is for day-to-day management, Delivery App is for leadership oversight.

---

## Common Questions

### Why is my SLA percentage different than expected?

- Check the date range—you may be looking at a different period
- Verify the client filter—might be filtered to one client
- Note that in-progress requests aren't counted in SLA % yet

### Why do I see zero data?

- Date range might be empty (no requests in that period)
- Client filter might be for a client with no requests
- Data may still be loading (check for loading indicator)

### Can I export this data?

- Basic export available from Insights
- For full exports, use the Delivery App
- Or contact your admin for custom reports

### How often does data update?

- Metrics refresh when you load the page
- Click refresh icon for latest data
- Real-time—reflects current database state

---

## Troubleshooting

### Metrics not loading

1. Check internet connection
2. Refresh the page
3. Verify you have access to Insights

### Numbers seem wrong

1. Check date range filter
2. Check client filter  
3. Ensure you're comparing like periods
4. Note that completed vs. in-progress affects calculations

### Page loading slowly

1. Narrow the date range (less data to process)
2. Filter to specific client
3. Check browser performance

---

## Related Documentation

- **[SLA Tracking](sla-tracking.md)** — How SLA timers work
- **[Unified Queue](unified-queue.md)** — Where requests are managed
- **[Client Directory](client-directory.md)** — Client configuration

---

*Next: [Client Directory →](client-directory.md)*
