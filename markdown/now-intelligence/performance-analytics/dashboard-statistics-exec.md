---
title: Dashboard execution statistics
description: The Dashboard Stats Executions list enables you to view how long it takes for your Core UI dashboards to load. The list includes one entry for each launch of a dashboard.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dashboard statistics, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Dashboard execution statistics

The **Dashboard Stats Executions** list enables you to view how long it takes for your Core UI dashboards to load. The list includes one entry for each launch of a dashboard.

To view dashboard execution statistics, navigate to **All** &gt; **dashboard\_stats\_executions.list**. The admin or dashboard\_admin role is required.

**Note:**

-   Adding unused dashboards to this list takes some time, especially if your instance has many dashboards.
-   The **Dashboard Stats Executions** list supports the value of the property **glide.dashboard.recent\_executions\_number** per dashboard. The default value of this property is 25.

-   The [Dashboard statistics](dashboard-statistics.md) list enables you to view how often each of your Core UI dashboards is run and how long it takes to run them.
-   The [Dashboard executions](dashboard-execs.md) list shows how long it takes for your Core UI dashboards to load and the ID of the user who launched it.

By default, the **Dashboard Stats Executions** list has the following columns:

|Column|Description|
|------|-----------|
|Dashboard|The name of the dashboard. Select the hyperlink to view the dashboard properties.|
|Execution duration|The time in milliseconds that it took to run the dashboard.|
|Execution timestamp|The date and time of the launch of the dashboard.|

To view the dashboards that take the most time to run, sort **Execution duration** from z-a.

