---
title: Associate a maintenance plan to filtered records
description: You can configure a maintenance plan with filtering criteria. For example, you can apply a maintenance plan to all records containing computers that start with "apple".
locale: en-US
release: zurich
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing maintenance plans, Planned Maintenance, Service Management]
---

# Associate a maintenance plan to filtered records

You can configure a maintenance plan with filtering criteria. For example, you can apply a maintenance plan to all records containing computers that start with "apple".

## Before you begin

Role required: SM admin

## Procedure

1.  [Create a maintenance plan](t_CreateAMaintPlan.md).

2.  Set up a **Filter condition** to capture the records that should use the maintenance plan.

    **Note:** You can click **Refresh** \(![picture of the refresh icon, showing two horizontal arrows going opposite directions](../image/RefreshIcon.png)\) to view the number of matching records.

3.  Click **Submit**.

4.  [Configure a maintenance schedule](t_DefineAMaintSched.md).

5.  In the **Related Links** for the maintenance plan, click **Apply schedules to filtered records**.


## Result

The schedule is applied to the records that meet the specified filter conditions.

**Note:** If multiple schedules are defined, they all take effect on the matching records when you click **Apply schedules to filtered records**. See [Configure a maintenance schedule](t_DefineAMaintSched.md) for details. This same functionality exists for maintenance schedules. The **Related Links** for the schedule also contains an **Apply schedule to filtered records** link. If you click this link in the maintenance schedule, only this specific schedule is applied to the records that meet the filter conditions in the associated maintenance plan.

**Parent Topic:**[Managing maintenance plans](../concept/c_MaintPlanMgmt.md)

