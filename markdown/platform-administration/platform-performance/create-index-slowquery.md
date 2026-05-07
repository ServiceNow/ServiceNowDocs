---
title: Schedule a slow-query index suggestion for creation
description: Use the Index Suggestion Engine \(ISE\) to schedule an index suggestion for creation.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Resolving slow queries, Resolve issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Schedule a slow-query index suggestion for creation

Use the Index Suggestion Engine \(ISE\) to schedule an index suggestion for creation.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Diagnostics** &gt; **Index Suggestions** &gt; **Index Suggestions &gt; To review**.

2.  In the Index Suggestion table, select the table associated with the index suggestion you want to create from the **Table Name** column.

3.  In the Index Suggestion form, select **Schedule Creation**.

4.  In the Schedule Index Creation window, select the time that you want the index to be created and select **Create**.

    **Note:** If the index you want to create involves large tables, such as the Incident or CMDB table, index creation may take up to one hour or longer.

    -   **Create now** —The Schedule Index Creation progress indicator window shows the progress of the index creation. When index creation is complete, click **Close**.
    -   **Create later** —If you select this option, the state changes to Create Scheduled, and the index is created at the scheduled time. After the index is created, the index state changes to Evaluating Effectiveness.
    When the ISE creates the index at the selected time, it assigns an index name based on the tables used in the slow query.

5.  Verify that the index was created by reviewing the index **State** in the Index Suggestion record or in the Index Suggestion table \(**System Diagnostics** &gt; **Index Suggestions** &gt; **Index Suggestions &gt; In Progress**\).

    The Index Suggestion record shows the state, Evaluating Effectiveness. The ISE begins the 14-day index evaluation period.

6.  During the evaluation period, you can monitor the index **State** in the Index Suggestion record or in the Index Suggestion table \(**System Diagnostics** &gt; **Index Suggestions** &gt; **Index Suggestions &gt; In Progress**\).


**Parent Topic:**[Resolving slow queries](../concept/resolving-slow-queries.md)

