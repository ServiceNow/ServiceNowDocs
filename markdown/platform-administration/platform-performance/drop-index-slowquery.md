---
title: Drop a slow query index
description: You can drop an index for a slow query when the index isn’t used by the database or doesn’t improve query performance. You can drop the index immediately or schedule the drop for a later time.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-05-12"
reading_time_minutes: 1
breadcrumb: [Resolving slow queries, Resolving platform performance issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Drop a slow query index

You can drop an index for a slow query when the index isn’t used by the database or doesn’t improve query performance. You can drop the index immediately or schedule the drop for a later time.

## Before you begin

Role required: admin

## About this task

During the index evaluation period, the Index Suggestion Engine \(ISE\) might generate a recommendation to drop the index. A recommendation to drop an index is generated in the following cases:

-   The database doesn't use the index
-   The index doesn't improve query execution time

**Note:** If you want to retain an index even though the ISE generates a recommendation to drop it, you can use the **Accept** option in the Index Suggestion record to continue using the index. Before using this option, contact Customer Service and Support for guidance.

## Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Index Suggestions** &gt; **Index Suggestions &gt; In Progress**.

2.  In the Index Suggestions table, select the table associated with the index suggestion you want to drop in the **Table Name** column.

3.  In the Index Suggestion record, select **Schedule Drop**.

4.  In the Schedule Index Drop window, select the time when you want the index dropped and select **Drop**.

    **Note:** If the index you want dropped involves large tables, such as the Incident or CMDB table, dropping the index may take up to one hour or longer.

    -   **Drop now** —The Schedule Index Drop progress indicator window shows the progress of the index drop. When the index drop completes, select **Close**. If the drop is successful, the Index Suggestion record shows the index state as Dropped.
    -   **Drop later** —When you schedule the drop, the index state changes to Drop Scheduled. When the system drops the index at the scheduled time, the index state changes to Dropped.
5.  Verify that the index was dropped by reviewing the index state in the Index Suggestion record or in the Index Suggestion table \(**System Diagnostics** &gt; **Index Suggestions** &gt; **Index Suggestions &gt; Done**\).


**Parent Topic:**[Resolving slow queries](../concept/resolving-slow-queries.md)

