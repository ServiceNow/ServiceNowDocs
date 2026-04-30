---
title: Dashboard statistics
description: The Dashboard Stats list enables you to view how often each of your Core UI dashboards is run and how long it takes to run them.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-11-20"
reading_time_minutes: 2
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Dashboard statistics

The **Dashboard Stats** list enables you to view how often each of your Core UI dashboards is run and how long it takes to run them.

To view dashboard statistics, navigate to **All** &gt; **dashboard\_stats.list**. The admin or dashboard\_admin role is required. By default, the Dashboard Statistics list displays all dashboards that have been viewed. There is one entry in this table for each dashboard on the instance that has been viewed at least once. The entries increment until an entry is deleted or the dashboard itself is deleted.

-   The **Dashboard Stats** list enables you to view how often each of your Core UI dashboards is run and how long it takes to run them.
-   The [Dashboard executions](dashboard-execs.md) list shows how long it takes for your Core UI dashboards to load and the ID of the user who launched it.
-   The [Dashboard execution statistics](dashboard-statistics-exec.md) list how long it takes for your Core UI dashboards to load. The list includes one entry for the most recent launch of each dashboard per user.

The **Dashboard Stats** list has these columns by default:

|Column|Description|
|------|-----------|
|Run time|The average execution time in milliseconds of all runs of the dashboards. \(Runs divided by Execution time.\)|
|Dashboard|The name of the dashboard. Select the hyperlink to view the dashboard properties.|
|Runs|The total number of times the dashboard has been run.|
|Recent run time|The average execution time of the dashboard in milliseconds based on the 25 most recent runs. Edit the **glide.dashboard.recent\_executions\_number** property to change the number of runs used to calculate this value.|
|Recent No of Execution|The number of values used to calculate recent run time up to up to the value of **glide.dashboard.recent\_executions\_number**.|
|Execution time|Sum of execution time across all runs of the dashboard.|

Select the **Personalize List** icon ![Edit columns icon](../image/icon-cogwheel-ac.png) to add these columns:

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

