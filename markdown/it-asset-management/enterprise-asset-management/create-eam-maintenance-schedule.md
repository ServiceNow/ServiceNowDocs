---
title: Create a maintenance schedule
description: Create a maintenance schedule to specify when you want the maintenance to run using criteria such as time intervals or field values and apply a work order template to the schedule. You can apply one or more maintenance schedules to a single maintenance plan.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a maintenance plan for your enterprise assets, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Create a maintenance schedule

Create a maintenance schedule to specify when you want the maintenance to run using criteria such as time intervals or field values and apply a work order template to the schedule. You can apply one or more maintenance schedules to a single maintenance plan.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  On the **Maintenance Schedules** tab of the maintenance plan record, select **New**.

2.  On the Create new Maintenance Schedule form, fill in the fields.

    See [Maintenance schedule fields for Enterprise Asset Management](../reference/maintenance-schedule-fields-eam.md) for a detailed description of each field.

3.  Select **Save**.

    The form closes and you’re automatically redirected to the new maintenance schedule record.

4.  Apply a work order template to the maintenance schedule.

    Work order templates enable the Enterprise Asset Management application to automatically populate information, generate appropriate requests and tasks, and create part requirements for your work orders each time the scheduled maintenance runs.

    1.  On the **Schedule Templates** tab of the maintenance schedule record, select **New**.

        The Create New Schedule Template form opens.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Model|Model of the work order template.|
        |Schedule|Maintenance schedule to which you’re applying the work order template. This field populates automatically.|

    3.  Select **Save**.
    4.  Close the form to return to the maintenance schedule record.
5.  On the maintenance schedule record, select the **More Options** ellipsis icon and then select **Associate records** to associate the maintenance schedule with the enterprise assets that the maintenance plan is applied to.

    A confirmation message appears, indicating that the enterprise assets are now associated with the maintenance schedule. You can verify that the association is successful using the **Maintenance Plan Records** tab on either the maintenance schedule record or maintenance plan record.


## Result

Maintenance runs automatically based on the schedule that you set for the maintenance plan. You can also run maintenance on-demand by selecting **Run on demand** on the maintenance schedule record.

Each time maintenance runs, the Enterprise Asset Management application automatically creates a corresponding work order for every enterprise asset that the maintenance plan is applied to, given that the asset isn't already associated with an existing work order. You can use these work orders to track and manage all the work that you need to perform on the specified enterprise assets. See [Managing work for your enterprise assets](../concept/managing-work-enterprise-assets.md) for more information on work orders.

