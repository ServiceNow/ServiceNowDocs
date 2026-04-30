---
title: Disable multiple element selection on a dashboard
description: Dashboard owners have the option to disable multiple element select on an entire breakdown dashboard.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Filter dashboards on breakdown elements, Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Disable multiple element selection on a dashboard

Dashboard owners have the option to disable multiple element select on an entire breakdown dashboard.

## Before you begin

Role required: admin

## About this task

When you disable multiple element selection on a breakdown dashboard, users of that dashboard are only able to filter the dashboard's widgets on one element of the breakdown.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select the breakdown dashboard that you want to filter by only one breakdown element at a time.

3.  From the context menu, select **Dashboard Properties**.

4.  Select **Disable multiple element selection**.

    This option is available when there is at least one breakdown source in the dashboard's Breakdown Source related list.

5.  Click **Update**.


## Result

When you filter the dashboard on breakdown elements, you can select only one breakdown element. The widgets on the dashboard follow the single breakdown element selected. When you select elements or clear selected elements, you have to click **Apply** to make this choice.

<table id="simpletable_a2p_ksn_n3b"><tbody><tr><td>

![Element selection with Multiple element selection disabled, and the Awaiting Approval state selected.](../image/mes-disabled.png "List of breakdown elements - multiple element selection disabled")

</td><td>

![Element selection with Multiple element selection enabled, and Awaiting Approval and Awaiting User states selected.](../image/mes-enabled.png "List of breakdown elements - multiple element selection enabled")

</td></tr></tbody>
</table>