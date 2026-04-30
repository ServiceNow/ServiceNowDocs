---
title: Create a planned work schedule for your work plan
description: Create a planned work schedule to specify when you want the work plan to run and how frequently the schedule should run. You can apply one or more planned work schedules to a single work plan.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a work plan for your enterprise assets, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Create a planned work schedule for your work plan

Create a planned work schedule to specify when you want the work plan to run and how frequently the schedule should run. You can apply one or more planned work schedules to a single work plan.

## Before you begin

Before you create a planned work schedule, ensure that you have [created a work plan](create-work-plan-eam.md).

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## Procedure

1.  On the **Planned Work Schedules** tab of the work plan record, select **New**.

2.  On the Create New Planned Work Schedule form, fill in the fields.

    For a detailed description of the planned work schedule fields, see [Work plan schedule fields for Enterprise Asset Management](../reference/work-plan-schedule-fields-eam.md).

3.  Select **Save**.

    The form closes and you’re automatically redirected to the new planned work order schedule record.

4.  Select the **More Actions** ellipsis icon and then select **Associate schedule with filtered records** to associate the schedule with the assets that the work plan is applied to.

    A confirmation message appears, indicating that the enterprise assets are now associated with the planned work plan schedule. You can verify that the association is successful using the **Planned Work Records** tab on either the planned work plan schedule record or the work plan record.

5.  Apply a planned work schedule template to the work plan schedule.

    Planned work schedule templates enable the Enterprise Asset Management application to automatically populate information, generate appropriate requests and tasks, and create part requirements for your work plans each time the planned work schedule runs.

    1.  On the **Planned Work Schedule Templates** tab of the work plan schedule record, select **New**.

        The Create New Planned Work Schedule Template form opens.

    2.  On the form, fill in the fields.

<table id="table_o3p_zxg_3bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Model of the work order template.

</td></tr><tr><td>

Schedule

</td><td>

Planned work schedule to which you’re applying the work order template. This field populates automatically.

</td></tr><tr><td>

Table

</td><td>

Table that is associated with the corresponding work plan of this planned schedule.

 This field is automatically set to the table name selected for the work plan.

</td></tr><tr><td>

Conditions

</td><td>

Filter conditions to determine the work order template to be used to create work orders based on the planned schedule.

</td></tr><tr><td>

Notes

</td><td>

Any work notes regarding the template.

</td></tr></tbody>
</table>    3.  Select **Save**.
    4.  Close the form to return to the planned work plan schedule record.
6.  On the planned work plan schedule record, select the **More Actions** ellipsis icon and then select **Run on demand** to create work orders for each asset.

    Work orders are created for each asset. You can view the work orders in the **Work Orders** tab.


