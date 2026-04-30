---
title: Associate a schedule template to matching records
description: The instance adds templates to a maintenance schedule so the appropriate requests and tasks, such as work orders and facilities requests, can be auto-generated when a maintenance schedule runs.
locale: en-US
release: xanadu
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing maintenance plans, Planned Maintenance, Service Management]
---

# Associate a schedule template to matching records

The instance adds templates to a maintenance schedule so the appropriate requests and tasks, such as work orders and facilities requests, can be auto-generated when a maintenance schedule runs.

## Before you begin

Role required: SM admin

## About this task

A maintenance schedule runs and the requests or orders are generated, when a scheduled job called Planned Maintenance Nightly Run evaluates the schedule and determines that the meter or interval criteria in the schedule is met or exceeded. You can [run a scheduled job to execute a maintenance schedule](t_RunSchedJobToExecMaintSched.md) that runs at a day or time convenient for your business.

Each auto-generated service order is linked to the record under maintenance in the following ways:

-   Each service order **Record table** and **Record ID** field is always populated with the table name and ID of the record under maintenance.
-   If the record under maintenance is a configuration item, the service orders **Affected CI** field is populated.

## Procedure

1.  [Create a maintenance plan](t_CreateAMaintPlan.md).

2.  Add a **Filter condition** to identify those records for which you want to apply the maintenance plan.

    **Note:** You can click **Refresh** \(![Refresh icon, showing two horizontal arrows going opposite directions](../image/RefreshIcon.png)\) to display the number of matching records.

3.  Click **Submit**.

4.  [Define or select a maintenance schedule.](t_DefineAMaintSched.md)

5.  In the **Maintenance Schedules** related list, click the name of the schedule.

    In the **Maintenance Schedule** form, a **Schedule Templates** related list appears.

6.  In the **Schedule Templates** related list, click **Edit**.

    The **Edit Members** slushbucket displays all the service order, work management, and facilities request templates defined using any of the following applications:

    -   **Product Catalog** &gt; **Templates** &gt; **Work Order Templates**
    -   **Facilities** &gt; **Catalog&amp;Knowledge** &gt; **Facilities Request Templates**
7.  Move the templates you want to apply to the matching record from the **Collection** bucket to the **Model List** bucket and then click **Save**.

8.  In the Maintenance Schedule header, click **Back**.


## Result

Work orders or facilities requests created by the scheduled jobs running on the associated records contain the selected template.

**Parent Topic:**[Managing maintenance plans](../concept/c_MaintPlanMgmt.md)

