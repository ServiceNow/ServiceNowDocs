---
title: Create a work order for an enterprise asset
description: Create a work order to track and manage work for an enterprise asset, linear asset, or linear segment.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Create a work order for an enterprise asset

Create a work order to track and manage work for an enterprise asset, linear asset, or linear segment.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Work management view.

2.  On the **Work orders** tab, select **New**.

    **Note:**

    If you created a maintenance plan to manage and schedule maintenance for your enterprise assets, the Enterprise Asset Management application automatically creates a corresponding work order for each asset to which the maintenance plan is applied.

    See [Create a maintenance plan for your enterprise assets](create-eam-maintenance-plan.md) for more information on maintenance plans.

3.  On the Create New Work Order form, fill in the fields.

<table id="table_xcb_frp_hvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Work Order

</td></tr><tr><td>

Company

</td><td>

Company that you are creating the work order for.

</td></tr><tr><td>

Contract

</td><td>

Contract that defines the lease details of the associated enterprise asset.

</td></tr><tr><td>

Asset

</td><td>

Asset that you want to manage work for through this work order.**Note:** You can also select linear assets and linear segments from this field.

</td></tr><tr><td>

Location

</td><td>

Current location of the associated enterprise asset.**Note:** If you select a linear asset, a pencil icon \[![Pencil icon](../../../reuse/icons/product-icons/pencil-outline-24.svg)\] appears to enable you to choose the work order location between the Start marker and End marker. This option is available with Enterprise Asset Management version 9.0 and later. To select a location, follow these steps:

1.  Select the Work order linear asset location icon \[![Pencil icon](../../../reuse/icons/product-icons/pencil-outline-24.svg)\].

A Map location form appears, showing the start and the end markers on the map.

2.  Select a location on the map between the start and end markers.
3.  In the **Name** field, enter the name for the work order location.
4.  Select **Submit**.


</td></tr><tr><td>

Start marker

</td><td>

Start point of the linear asset or the linear segment.**Note:** This field only appears if you select Linear asset or linear segment from the **Asset** field.

</td></tr><tr><td>

End marker

</td><td>

End point of the linear asset or the linear segment.**Note:** This field only appears if you select linear asset or linear segment from the **Asset** field.

</td></tr><tr><td>

Priority

</td><td>

Priority of the work order.

</td></tr><tr><td>

Template

</td><td>

Work order template that you want to apply to this work order. Work order templates enable you to automatically populate information, generate appropriate tasks, and create part requirements for your work orders. See [Create a template for your Enterprise Asset Management work orders](create-eam-work-order-template.md) for more information on work order templates.

 To apply a template to a work order in the draft state and view the work order tasks and part requirements generated from the template, the sn\_eam.enterprise\_asset\_manager role must ensure that the **Apply Work Order template in draft status** field in the Field Service Management application is enabled. To accomplish this, navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration** and enable the **Apply Work Order template in draft status** field in the **Business Process** tab.

</td></tr><tr><td>

Closed

</td><td>

Date and time at which the work order is closed and complete.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the work order.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the work order.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the work order that are visible to all users within your organization.

</td></tr><tr><td class="sub-head" colspan="2">

Scheduling

</td></tr><tr><td>

Due date

</td><td>

Date and time at which the work order must be completed.

</td></tr></tbody>
</table>4.  Select **Save**.

    The work order is created in the draft state. Any work order tasks and parts requirements pertaining to the work order automatically appear in the **Work Order Tasks** and the **Part Requirements**tabs.

5.  To add additional work order tasks, select **New**in the **Work Order Tasks** tab.

    See [Create a work order task for an Enterprise Asset Management work order](create-eam-work-order-task.md) for detailed instructions.

6.  To track all items that you must complete for your work order or an associated work order task, create a checklist.

    See [Create a checklist for an Enterprise Asset Management work order or work order task](create-checklist-items-eam-work-order.md) for detailed instructions.

7.  If the enterprise asset that is associated with your work order is missing a required asset or part, create a part requirement.

    See [Create a part requirement for an Enterprise Asset Management work order or work order task](create-part-requirement-eam-work-order.md) for detailed instructions.

8.  Specify any upstream or downstream task dependencies for the associated work order tasks.

    See [Create dependencies for an Enterprise Asset Management work order task](create-dependencies-eam-work-order-task.md) for detailed instructions.

9.  Select **Ready to Work** to initiate work for the given work order


## What to do next

Work with the assigned agent to complete and close all subsequent tasks for your work order.

-   **[Create a work order task for an Enterprise Asset Management work order](create-eam-work-order-task.md)**  
Create a work order task to track and manage an individual task for your Enterprise Asset Management work order.
-   **[Create a checklist for an Enterprise Asset Management work order or work order task](create-checklist-items-eam-work-order.md)**  
Create a checklist of all items that you must complete for your work order or work order task.
-   **[Create a part requirement for an Enterprise Asset Management work order or work order task](create-part-requirement-eam-work-order.md)**  
If the enterprise asset that is associated with your work order or work order task is missing a required asset or part, create a part requirement to track and verify the missing asset or part.
-   **[Select descendant models of multi-component assets to create part requirements](add-part-reqs-eam.md)**  
For work orders and work order tasks that have multi-component assets, select descendant models to create part requirement records.
-   **[Create dependencies for an Enterprise Asset Management work order task](create-dependencies-eam-work-order-task.md)**  
If your work order task requires any upstream or downstream task dependencies, add them to your work order task.

**Parent Topic:**[Managing work orders for your enterprise assets](../concept/create-manage-wo-enterprise-assets.md)

