---
title: Create a work order task for an Enterprise Asset Management work order
description: Create a work order task to track and manage an individual task for your Enterprise Asset Management work order.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a work order for an enterprise asset, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Create a work order task for an Enterprise Asset Management work order

Create a work order task to track and manage an individual task for your Enterprise Asset Management work order.

## Before you begin

Role required: wm\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Work management**.

2.  On the **Work orders** tab, select the work order to which you want to add a work order task.

    The work order record opens.

3.  Select the **Work Order Tasks** tab and select **New**.

4.  On the Create New Work Order Task form, fill in the fields.

<table id="table_m3h_rtp_hvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Work Order Task

</td></tr><tr><td>

Assignment group

</td><td>

Agent group to which the work order task is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

Agent to whom the work order task is assigned.

</td></tr><tr><td>

Work type

</td><td>

Type of work that the assigned agent must perform on the associated enterprise asset. The options are **Break Fix**, **Install**, **Planned Maintenance**, **Asset condition**, **Shutdown**, **Startup**,and **Calibration**.

</td></tr><tr><td>

Asset

</td><td>

Enterprise asset that the assigned agent is performing work on. This field populates automatically.

</td></tr><tr><td>

Location

</td><td>

Current location of the associated enterprise asset. This field populates automatically.**Note:** If you select a linear asset, the Work order linear asset location icon ![](../../../reuse/icons/product-icons/pencil-outline-24.svg) appears to enable you to choose the work order location between the Start marker and End marker. To select a location, follow these steps:

1.  Select the pencil icon ![](../../../reuse/icons/product-icons/pencil-outline-24.svg).

A Map location form appears, showing the start and the end markers on the map.

2.  Select a location on the map between the start and end markers.
3.  In the **Name** field, enter the name for the work order location.
4.  Select **Submit**.


</td></tr><tr><td>

Start marker

</td><td>

Start point of the linear asset or the linear asset.**Note:** This field only appears if you select Linear asset or linear segment from the **Asset** field.

</td></tr><tr><td>

End marker

</td><td>

End point of the linear asset or the linear segment.**Note:** This field only appears if you select linear asset or linear segment from the **Asset** field.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the work order task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the work order task.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the work order task that are visible to all users within your organization.

</td></tr><tr><td class="sub-head" colspan="2">

Scheduling

</td></tr><tr><td>

Window start

</td><td>

Estimated start date and time of the work order task.

</td></tr><tr><td>

Window end

</td><td>

Estimated completion date and time of the work order task.

</td></tr><tr><td>

Estimated work duration

</td><td>

Amount of time that you estimate it will take to complete the work order task.

</td></tr><tr><td>

Actual work start

</td><td>

Actual start date and time of the work order task.

</td></tr><tr><td>

Actual work end

</td><td>

Actual completion date and time of the work order task.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

-   The work order task is created in the **Draft** state.
-   Assets associated with the work order are added to the work order task and listed on the **Affected assets** tab.

