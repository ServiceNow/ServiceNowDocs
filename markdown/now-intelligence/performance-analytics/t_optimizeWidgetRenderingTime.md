---
title: Optimize widget rendering time on responsive dashboards
description: Large dashboards can take a long time to render, especially when widgets depend on complex queries or queries on large tables. You can use system properties to optimize how widgets load.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Optimize widget rendering time on responsive dashboards

Large dashboards can take a long time to render, especially when widgets depend on complex queries or queries on large tables. You can use system properties to optimize how widgets load.

## Before you begin

Role required: admin

**Note:** You can optimize widget rendering only for responsive dashboards.

## Procedure

1.  Use these two system properties to optimize dashboard widget rendering.

<table id="choicetable_txm_hjc_wy"><thead><tr><th align="left" id="d130704e57">

Name

</th><th align="left" id="d130704e60">

Description

</th></tr></thead><tbody><tr><td id="d130704e66">

**glide.canvas.grid.widget\_performance\_threshold**

</td><td>

Defines the maximum number of seconds for a widget to render on a dashboard. Widgets that exceed this time aren’t rendered and a warning message is shown. Users can select the message to restart rendering. Set this threshold to prevent slow widgets from blocking other widgets from loading.-   Type: integer
-   Default value: -1
-   Location: **System Properties** &gt; **Dashboard Properties**
The default value of -1 disables the threshold and widget performance isn’t evaluated. Widgets are evaluated against any value greater than or equal to 1.

</td></tr><tr><td id="d130704e97">

**glide.canvas.grid.widget\_render\_concurrent\_max**

</td><td>

Defines the maximum number of widgets that render simultaneously on a dashboard. With smaller values, more requests are made to the server. With larger values, fewer requests are made to the server.

 **Note:** This property reduces the load on the server. It doesn’t necessarily improve the performance of individual dashboards.

 Widgets that are outside of the screen don’t load at all until you scroll past them.

 -   Type: integer
-   Default value: 3 if the property isn’t manually set. The minimum value is 2 if you set the property manually. If you set this property manually to 1 or lower, all widgets on the dashboard load simultaneously.
-   Location: **System Properties** &gt; **Dashboard Properties**


</td></tr></tbody>
</table>    The values to use for these properties depend on the performance of your instance and the contents of its dashboards.

2.  You can also [configure a transaction quota rule](https://www.servicenow.com/docs/access?context=t_ConfigureATransactionQuotaRule&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    Transaction quota rules enable you to set a maximum execution time for a widget or a dashboard.

    **Note:**

    There are two scenarios for a widget that takes a long time to load:

    -   **Transaction quota value is less than the performance threshold**

        If the widget doesn’t load before the transaction quota is reached, the widget doesn’t load. The following message displays: `Widget cancelled - maximum execution time exceeded`.

    -   **Performance threshold value is less than the transaction quota**

        The behavior is the same as if the transaction quota doesn’t exist. The widget stops loading and a message is shown. You can select the widget to reload it. However, the transaction quota still applies and may halt rendering.


**Related topics**  


[Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

