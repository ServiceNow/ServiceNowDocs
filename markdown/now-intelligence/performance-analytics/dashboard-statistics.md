---
title: Dashboard statistics
description: The Dashboard Stats list enables you to view how often each of your Core UI dashboards is run and how long it takes to run them.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-12-18"
reading_time_minutes: 2
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Dashboard statistics

The **Dashboard Stats** list enables you to view how often each of your Core UI dashboards is run and how long it takes to run them.

To view dashboard statistics, navigate to **All** &gt; **dashboard\_stats.list**. The admin or dashboard\_admin role is required. By default, the Dashboard Statistics list displays all dashboards that have been viewed. There is one entry in this table for each dashboard on the instance that has been viewed at least once. The entries increment until an entry is deleted or the dashboard itself is deleted.

-   The **Dashboard Stats** list enables you to view how often each of your dashboards is run and how long it takes to run them.
-   The [Dashboard executions](dashboard-execs.md) list shows how long it takes for your Core UI dashboards to load and the ID of the user who launched it.
-   The [Dashboard execution statistics](dashboard-statistics-exec.md) list how long it takes for your Core UI dashboards to load. The list includes one entry for the most recent launch of each dashboard per user.

The **Dashboard Stats** list has these columns by default:

<table id="table_lxs_51z_5y"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run time

</td><td>

The average execution time in milliseconds of all runs of the dashboards. \(Runs divided by Execution time.\)

</td></tr><tr id="reportinforeport"><td>

Dashboard

</td><td>

The name of the dashboard. Select the hyperlink to view the dashboard properties.

</td></tr><tr><td>

Dashboard Table

</td><td>

The table on which the dashboard's record is stored:-   **par\_dashboard**

Dashboards created in Platform Analytics experience or migrated to it.

-   **pa\_dashboards**

Dashboards created in the classic environment \(Core UI\) and not migrated.


</td></tr><tr><td>

Last Viewed On

</td><td>

The date and time the dashboard was last opened by any user.

</td></tr><tr id="reportinforuns"><td>

Runs

</td><td>

The total number of times the dashboard has been run.

</td></tr><tr id="reportinforecentruntime"><td>

Recent run time

</td><td>

The average execution time of the dashboard in milliseconds based on the 25 most recent runs. Edit the **glide.dashboard.recent\_executions\_number** property to change the number of runs used to calculate this value.

</td></tr><tr id="reportinforuntime"><td>

Recent No of Execution

</td><td>

The number of values used to calculate recent run time up to up to the value of **glide.dashboard.recent\_executions\_number**.

</td></tr><tr><td>

Execution time

</td><td>

Sum of execution time across all runs of the dashboard.

</td></tr></tbody>
</table>Select the **Personalize List** icon ![Edit columns icon](../image/icon-cogwheel-ac.png) to add these columns:

|Column|Description|
|------|-----------|
|Created|Date the dashboard was created|
|Created by|Dashboard's creator|
|Tags|Use to select tags or add new tags to enhance searchability.|
|Updated|Date of the dashboard's last change.|
|Updated by|Name of the user who made the dashboard's last change.|
|Updates|Total number of updates made to the dashboard.|

-   To view the dashboards that take the most time to run, sort **Recent run time** from z-a.
-   To see the viewed dashboards, filter out the value 0 from the **Runs** column.
-   To view the most viewed dashboards, sort the **Runs** column from z-a.

