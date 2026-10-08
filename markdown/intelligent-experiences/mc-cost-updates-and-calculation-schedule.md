---
title: Cost updates and calculation schedule
description: AI Control Tower preserves recorded cost data and calculates cost and value on a daily schedule. These rules determine when a cost change takes effect and when it appears in your dashboards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mc-cost-updates-and-calculation-schedule.html
release: brazil
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [cost configuration, historical data, scheduled job, value calculation, AI Control Tower]
breadcrumb: [Cost, Explore, Measure AI system, Measure AI systems, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Cost updates and calculation schedule

AI Control Tower preserves recorded cost data and calculates cost and value on a daily schedule. These rules determine when a cost change takes effect and when it appears in your dashboards.

You can update a vendor's cost configuration at any time, such as when your vendor contract is renewed at a new rate. AI Control Tower applies these changes based on two rules: historical cost data is preserved, and cost and value calculations are performed on a daily schedule.

## Cost changes take effect the next day

You can't change cost data for the current date or a previous date. AI Control Tower retains recorded costs to maintain consistency in historical cost and value reports.

A cost change takes effect the day after you make it. Costs recorded through the current date continue to use the previous value.

For example, assume that the cost per seat is $25 starting in January. If you change the cost to $30 on September 22, AI Control Tower uses the $25 rate through September 22 and the $30 rate starting September 23. You can't apply the $30 rate to September 22 or an earlier date.

Because you can't backdate cost changes, update the cost configuration before the new contract rate takes effect.

## Calculation schedule

AI Control Tower uses scheduled jobs to calculate cost and value:

-   A nightly job processes data from the previous day.
-   A value calculation job runs every 24 hours.

Cost and value figures on your dashboards reflect data up to the previous day. Any costs you add or change don't appear in the dashboards until the scheduled jobs process them.

**Related topics**  


[Cost types and sub-vendor rates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mc-ai-cost-types-and-sub-vendor-rates.md)

