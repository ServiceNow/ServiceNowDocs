---
title: Dashboard executions
description: The Dashboard Executions list enables you to view how long it takes for your Core UI dashboards to load and the ID of the user who launched it. The list includes one entry for the most recent launch of each dashboard per user.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Dashboard statistics, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Dashboard executions

The **Dashboard Executions** list enables you to view how long it takes for your Core UI dashboards to load and the ID of the user who launched it. The list includes one entry for the most recent launch of each dashboard per user.

To view dashboard execution statistics, navigate to **All** &gt; **dashboard\_executions.list**. The admin or dashboard\_admin role is required.

**Note:**

-   Adding unused dashboards to this list takes some time, especially if your instance has many dashboards.
-   The **Dashboard Executions** list supports the most recent 10 runs per user per dashboard. Edit the system property **glide.dashboard.log.max\_user\_executions\_x\_dashboard** to change this value.

-   The [Dashboard statistics](dashboard-statistics.md) list enables you to view how often each of your Core UI dashboards is run and how long it takes to run them.
-   The [Dashboard execution statistics](dashboard-statistics-exec.md) list how long it takes for your Core UI dashboards to load. The list includes one entry for the most recent launch of each dashboard per user.

By default, the **Dashboard Executions** list has the following columns:

|Column|Description|
|------|-----------|
|Dashboard|The name of the dashboard. Select the hyperlink to view the dashboard properties.|
|Execution duration|The time in milliseconds that it took to run the dashboard. There is one entry per unique user.|
|Execution timestamp|The date and time of the launch of the dashboard.|
|User sys ID|The user associated with the sys ID that launched the dashboard. Select the user to view their information.|

To view the dashboards that take the most time to run, sort **Execution duration** from z-a.

