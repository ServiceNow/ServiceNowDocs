---
title: Generate resource capacity
description: Generate and view the total capacity of the resources with primary attributes. Capacity details helps Portfolio Managers to plan and manage planning items depending on the resource availability.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Capacity Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Generate resource capacity

Generate and view the total capacity of the resources with primary attributes. Capacity details helps Portfolio Managers to plan and manage planning items depending on the resource availability.

## Before you begin

1.  Enable planning attributes for capacity planning. For more information, see [Enable planning attributes for capacity in Portfolio Planning](cp-enable-planning-attributes-pp.md).
2.  Generate employee profiles for resources. For more information, see [Generate employee profiles for resources to work with Capacity](gen-emp-profiles-cp-pp.md).

Role required: sn\_align\_ws.spw\_capacity\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace**.

2.  Select the **Resource capacity** option \(![Manage resource capacity option.](../../spw-capacity-planning/images/cp-manage-resource-capacity-icon.png)\).

    **Note:** If planning attributes aren’t enabled for capacity planning, you see an empty state screen with an option to configure. Contact your admin to enable planning attributes for capacity planning. For more information, see [enable planning attributes for capacity planning](../../spw-capacity-planning/task/cp-enable-planning-attributes-spw.md).

3.  Use one the following options to view and regenerate the capacity details.

<table id="choicetable_gk4_244_byb"><thead><tr><th align="left" id="d154804e122">

Choice

</th><th align="left" id="d154804e125">

Description

</th></tr></thead><tbody><tr><td id="d154804e131">

**Generate capacity details**

</td><td>

Use the Resource capacity filters to filter and view the resource capacity within the selected date range for their primary attributes.1.  Select **Start Month** and **End Month** to define a time frame.

You can select a date range up to 3 years.

2.  Select at least one of the primary attributes from **Group**, **Role**, or **Skill**.
3.  Select **View capacity** \(![View capacity button.](../../spw-capacity-planning/images/cp-view-capacity-button.png)\).
4.  On the Generate capacity details window, select **Generate**.

The resource capacity details for the selected combination of primary attributes and time frame is displayed.

**Note:** Capacity generation is an asynchronous process. You can generate capacity for multiple combination of dates and attributes.

</td></tr><tr><td id="d154804e187">

**Regenerate capacity details**

</td><td>

1.  Select **Regenerate capacity** \(![Regenerate capacity button.](../../spw-capacity-planning/images/cp-regenerate-capacity.png)\).
2.  In the Regenerate capacity window, filter the date range, if needed, and select **Regenerate**.


</td></tr><tr><td id="d154804e217">

**Scheduled job**

</td><td>

Activate a schedule job to automatically generate the capacity details of your resources at required cadence. For more information on how to activate a scheduled job, see [Activate a scheduled job to automatically generate resource capacity](generate-capacity-scheduled-job-pp.md).

</td></tr></tbody>
</table>
## What to do next

[Use Capacity Planning](using-cap-planning-screen-pp.md) to view the resource capacity, resource-to-work mapping and re-prioritize resource allocations to effective execute your prioritized planning items.

