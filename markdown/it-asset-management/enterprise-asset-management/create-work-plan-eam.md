---
title: Create a work plan for your enterprise assets
description: Create and manage work plans to specify how and when the work should be performed for any activity.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Create a work plan for your enterprise assets

Create and manage work plans to specify how and when the work should be performed for any activity.

## About this task

Use the Planned Work Management application's functionality to create work plans from within the Enterprise Asset Workspace. This enables managers to create work orders for the future and allocate them to technicians so that the technicians can review and plan their work accordingly.

**Note:** Ensure that you have activated the Planned Work Management plugin \[sn\_fsm\_planned\_wm\] plugin.

A work plan consists of an effective start and end date that determines the period for which the plan can be scheduled for execution. Each work plan must have at least one or more records associated with it for which you want to apply the work plan.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## Procedure

1.  From the Enterprise Asset Workspace, open the Work management view.

2.  On the **Maintenance plans** tab, select **New** to open the Select target asset table pop-up window.

3.  Select **Work plan** from the **Plan type** list.

4.  Select a table from the **Asset table** list.

    The Enterprise asset table is selected by default.

5.  Select **Create**.

6.  On the Create New Work Plan page, fill in the details.

    For a detailed description of all the work plan fields, see [Work plan fields for Enterprise Asset Management](../reference/wp-fields-eam.md).

7.  Select **Save**.

    The page closes and you’re automatically redirected to the new work plan record.

    You can further configure your work plan by creating [planned work schedules](create-eam-planned-work-schedule.md), planned work records, and work orders.

    You can view all your work plan records in the list view in the **Maintenance plans** tab. Every work plan record is prefixed with **WP**.


-   **[Create a planned work schedule for your work plan](create-eam-planned-work-schedule.md)**  
Create a planned work schedule to specify when you want the work plan to run and how frequently the schedule should run. You can apply one or more planned work schedules to a single work plan.

**Parent Topic:**[Managing work orders for your enterprise assets](../concept/create-manage-wo-enterprise-assets.md)

