---
title: Changes to maintenance schedules
description: If you make and save changes to an existing maintenance schedule, any previously associated records are updated accordingly.
locale: en-US
release: xanadu
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure a maintenance schedule, Managing maintenance plans, Planned Maintenance, Service Management]
---

# Changes to maintenance schedules

If you make and save changes to an existing maintenance schedule, any previously associated records are updated accordingly.

The following examples explain the types of behavior you can expect after making changes:

-   If you change a schedule from a duration-based to a meter-based schedule, the next run time is cleared and the associated records are populated with a next run value instead.
-   If the **Every** field is changed on a meter-based schedule, the next run value is updated based on the existing Last Run Value, or from the current value of the asset if no last run value exists.
-   If you change the **Field** value for a meter-based schedule, the records associated with the schedule have their next run values recalculated based on the new **Field** value.
-   For Interval-based schedules, changing from one **Trigger type** to another updates the next run time based on the existing **Last Run Time** value, or from **Now** if no last run time exists.

**Parent Topic:**[Configure a maintenance schedule](../task/t_DefineAMaintSched.md)

