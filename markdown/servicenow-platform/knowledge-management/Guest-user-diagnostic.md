---
title: Collect knowledge usage metrics
description: Capture metrics such as article views, page views, and portal searches to track aggregated knowledge usage by users.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User criteria diagnostics for Knowledge Management, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Collect knowledge usage metrics

Capture metrics such as article views, page views, and portal searches to track aggregated knowledge usage by users.

## Before you begin

Set the duration over which the metrics are aggregated through the **glide.knowman.usage\_metrics\_duration** property. For more information, see [Other knowledge properties](../reference/r_KnowledgeProperties.md#). By default, the property value is set to 60 minutes.

You must activate the Knowledge Management v3 plugin \(com.snc.knowledge3\).

Role required: admin

## About this task

Monitor the knowledge usage metrics to improve the overall effectiveness of the knowledge usage across the portals.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search and open the **Knowledge Usage Metrics** scheduled job.

3.  In the **Knowledge Usage Metrics** form, select the **Active** check box to activate the scheduled job.

    The scheduled job is inactive by default.

4.  In the **Run** field, select **Periodically** as the frequency of the scheduled job.

    See the [Scheduled jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ScheduledJobs.md) topic for other frequency options.

5.  In the **Repeat Interval** field, enter the repeated time interval at which the scheduled job should run.

    By default, the duration is set to 60 minutes.

6.  Click **Update**.


## What to do next

[Modify the data retention policy for knowledge usage metrics](Modify-data-retention-policy-knowledge-usage-metrics.md) to remove unwanted and older data from the knowledge usage metrics \[kb\_usage\_metrics\] table.

-   **[Modify the data retention policy for knowledge usage metrics](Modify-data-retention-policy-knowledge-usage-metrics.md)**  
Remove unwanted and older data from the knowledge usage metrics \[kb\_usage\_metrics\] table through the data retention policy.

**Parent Topic:**[User criteria diagnostics for Knowledge Management](../concept/diagnose-knowledge-user-criteria.md)

