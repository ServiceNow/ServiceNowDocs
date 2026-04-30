---
title: Associate a domain configuration with a dashboard
description: Display a domain picker on a dashboard to enable users of that dashboard to view scores from specific domains.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Domain configurations, Domain separation, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Associate a domain configuration with a dashboard

Display a domain picker on a dashboard to enable users of that dashboard to view scores from specific domains.

## Before you begin

Role required: pa\_power\_user or admin

The Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\) must be activated.

## About this task

A user must have visibility into all domains in the domain configuration to view domain-specific scores on a dashboard.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Dashboard Administration**.

2.  Select a dashboard.

3.  In the **Domain Configurations** related list click **Edit**.

4.  Select the domain configurations you want to associate with this dashboard.

5.  Click **Save**.


## Result

A user who has visibility to all the domains in the domain configuration, such as an admin, can select a domain. The reports and widgets on the dashboard show only scores and values from that domain.

![Incident Management dashboard configured with the ACME groups and Cisco groups domain configurations](../image/domain-config-dashboard.png)

## What to do next

If you open the Analytics Hub from a dashboard with a domain picker, you see only the scores collected for the selected domain. Any target, threshold, or comment you add is automatically associated with the current domain. The **Edit scores** option is not available.

**Parent Topic:**[Grouping domains in Performance Analytics domain configurations](../concept/pa-domain-separation-msp.md)

