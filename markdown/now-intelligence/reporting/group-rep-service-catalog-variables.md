---
title: Group a report by service catalog variables
description: You can create reports grouped by variable on a selected service catalog item. In addition, you can create filters on the same variable. For example, if a mobile phone item has a storage variable, you can create a report that only shows those phones with 32 GB of storage.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Report on service catalog variables, Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Group a report by service catalog variables

You can create reports grouped by variable on a selected service catalog item. In addition, you can create filters on the same variable. For example, if a mobile phone item has a storage variable, you can create a report that only shows those phones with 32 GB of storage.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## About this task

You can apply these steps to any report type as long as the report source has variables associated with it. If the report source doesn’t have variables, the **Variables** option doesn’t display in the **Group by** and **Stack by** fields.

**Note:** List, Box, Trendbox, and Pivot reports can’t use service catalog variables as a primary or secondary **Group by**. Single Score, Calendar, Control, and Map reports don’t support **Group by** on any fields. List reports can use service catalog variables as columns.

## Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  Select a report source that has variables associated with it.

    There are two kinds of report sources.

    |Report source|Description|
    |-------------|-----------|
    |Data source|A table with filters applied to provide a single source of information for all users.|
    |Table|The raw data from a table with no filters applied.|

4.  Select **Next**.

5.  On the **Type** tab, select the report type and select **Next**.

6.  On the **Configure** tab, select **Variables** from the **Group by** or **Stack by** filters.

    ![Configure tab > group by or stack by variables](../image/group-by-variables.png)

7.  Search for and select the variable associated with the item to group or stack by.

8.  Continue to configure and style the report according to its report type.

    See [Report types](../reference/report-types-creation-details-rd.md).


**Parent Topic:**[Report on service catalog variables](../concept/rep-service-catalog-variables.md)

