---
title: Create or configure a responsive dashboard
description: Create a dashboard where you can add Performance Analytics widgets, data visualizations, and other content that you frequently use. You can then share the dashboard with other users.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-11-27"
reading_time_minutes: 3
keywords: [configure a dashboard, create a dashboard, create a new dashboard, create dashboards, make a dashboard, set up a dashboard, what role do I need to create dashboards, what role do I need to make a dashboard, what role do I need to make a responsive dashboard]
breadcrumb: [Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create or configure a responsive dashboard

Create a dashboard where you can add Performance Analytics widgets, data visualizations, and other content that you frequently use. You can then share the dashboard with other users.

## Before you begin

If you are new to dashboards, the Visualize and Next Experience Dashboards sections of the ServiceNow University [Platform Analytics \(PA\) Overview training](https://learning.servicenow.com/lxp/en/now-intelligence/platform-analytics-pa-overview?id=learning_course_prev&course_id=fb9decf8932f06905402393d6cba10f6&s=1&ssa=3) provide an overview of these features. \(Registration and enrollment required.\)

**Note:** This topic refers to Dashboards in the Core UI. If your instance is migrated to Platform Analytics experience, see [Create a dashboard with the in-line editor](../../dashboards/task/create-db-in-ac.md).

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  Select **Create a dashboard**.

3.  Fill in the following fields:

<table id="choicetable_bfl_jhv_yw"><thead><tr><th align="left" id="d53284e159">

Field

</th><th align="left" id="d53284e162">

Description

</th></tr></thead><tbody><tr id="chrow_lxl_nrq_dz"><td id="d53284e168">

**Name**

</td><td>

Name the dashboard.

</td></tr><tr id="chrow_lkc_4rq_dz"><td id="d53284e177">

**Order**

</td><td>

Enter an **Order** number to indicate the order the dashboard appears on the dashboard picker. Dashboards with lower numbers are listed first.

</td></tr><tr id="chrow_hd3_4rq_dz"><td id="d53284e189">

**Active**

</td><td>

Clear this field to mark the dashboard **inactive**. Inactive dashboards are accessible only if they appear on the **Recent** tab \(the nine most recently visited dashboards\) or if the user has a direct link to the dashboard.

 **Note:** When you activate responsive dashboards, the permissions associated with both active and inactive non-responsive dashboard are carried over to the responsive version.

</td></tr><tr id="chrow_gf4_4rq_dz"><td id="d53284e210">

**Owner**

</td><td>

The dashboard owner. Only a user with the administrator role can change this value.

</td></tr></tbody>
</table>4.  Select the **Restrict to roles** edit icon \(![](../../reporting/image/Pencil.png)\) to specify the roles that a user must have to access this dashboard.

    For more information, see [Share a responsive dashboard](../../dashboards/task/t_ControlAccessToADashboard.md).

5.  Users with admin, pa\_admin, and pa\_power\_user roles can configure these additional fields:

    |Field|Description|
    |-----|-----------|
    |**Group**|Click the magnifier icon to add the dashboard to a **Group**. Groups organize dashboards in the dashboard picker list. Grouped dashboards appear at the top of the list. Ungrouped dashboards appear in the list under **Other**.|
    |**Breakdown Source**|Select one or more breakdown sources in the **Breakdown Source** related list. Breakdowns enable users to filter Performance Analytics data on the dashboard. The **Breakdown Source** related list is available on the Dashboard form after you create the dashboard. For more information, see [Using breakdowns on dashboards](../concept/c_SpecialDashboards.md).|
    |**Act as filter**|You can configure a Performance Analytics breakdown on a dashboard to act as an interactive filter for reports on the dashboard. The dashboard must be configured as a breakdown dashboard. Select the interactive filter that you want this breakdown source to act as.|

6.  Select **Submit**.


## Result

The dashboard is created with no content. To add your first content, select a widget type and a widget and click **Add**.

## What to do next

Add more content to your new dashboard. For more information, see [Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md).

**Related topics**  


[Performance Analytics breakdowns](../concept/c_CreatingBreakdowns.md)

[Add a breakdown to a dashboard](../concept/c_SpecialDashboards.md)

[Organize dashboards into groups](../../dashboards/task/t_GroupDashboards.md#)

