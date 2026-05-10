---
title: View widget statistics
description: You can view statistics about Performance Analytics widgets to help identify and resolve problems, such as if a widget is loading slowly on dashboards.These properties control how widget statistics are tracked and maintained.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# View widget statistics

You can view statistics about Performance Analytics widgets to help identify and resolve problems, such as if a widget is loading slowly on dashboards.

## Before you begin

Role required: pa\_power\_user, pa\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widget Statistics**.

2.  Select the widget you want to view statistics for.

3.  Review the following fields.

    |Field|Description|
    |-----|-----------|
    |Widget|The widget that the statistics describe.|
    |Number executions total|The total number of times the widget was loaded from the server.|
    |Average execution duration|The average time it took to load the widget, in milliseconds, for all executions of this widget.|
    |Recent number executions|The number of time the widget was recently loaded from the server. The maximum number of recent executions is determined by the property **glide.report.recent\_executions\_number**.|
    |Recent avg execution duration|The average time it took to load the widget, in milliseconds, for recent executions. The maximum number of recent executions is determined by the property **glide.report.recent\_executions\_number**.|
    |Total executions duration|The total sum duration for all executions of the widget.|


## Widget statistics properties

These properties control how widget statistics are tracked and maintained.

<table id="table_qzr_2fh_r5"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.report.recent\_executions\_number

</td><td>

The number of widget executions that are considered recent for the purpose of recent average duration calculations. -   Type: integer
-   Default value: 25
-   Location: [Add the property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md)

</td></tr></tbody>
</table>