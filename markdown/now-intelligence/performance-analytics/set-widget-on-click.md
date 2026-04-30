---
title: Set the on-click behavior of a widget
description: You can configure what happens when a user clicks on a widget.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Set the on-click behavior of a widget

You can configure what happens when a user clicks on a widget.

## Before you begin

Role required: pa\_power\_user, pa\_admin, or admin

## About this task

By default, when a user clicks on a widget, the detailed Analytics Hub for the widget indicator appears. You can configure a widget to direct users to a different URL instead.

**Note:** For equivalent functionality in Platform Analytics data visualizations, see [Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md).

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets**.

2.  Select the widget you want to configure.

3.  In the **On-click behaviors** related list, click **New** and create a new record.

    If you create more than one On-click behavior record for a single widget, only the record with the lowest **Order** value is used.

    1.  In the **Label** field, enter the text that appears for this option when a user clicks on the widget.

    2.  In the **Type** field, select **URL**.

    3.  In the **Value** field, enter the URL that you want to direct users to when they click on the widget.

        Only URLs relative to the instance URL are allowed. The value must begin with a / character, such as `/incident.do`.

    4.  Click **Submit**.


