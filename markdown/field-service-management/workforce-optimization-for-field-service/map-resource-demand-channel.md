---
title: Associate technicians with demand channels
description: Associate technicians in a territory with demand channels to appropriately assign tasks to the technicians.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/workforce-optimization-for-field-service/map-resource-demand-channel.html
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-05-23"
reading_time_minutes: 2
breadcrumb: [Capacity and Reservations Management, Set up workforce, Configure, Field Service Management]
---

# Associate technicians with demand channels

Associate technicians in a territory with demand channels to appropriately assign tasks to the technicians.

## Before you begin

Role required: sn\_fsm\_tp.territory\_resource\_manager

Ensure you have enabled following.

-   Territory model. For more information, see [Enable the Field Service territory model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/enable-territory-model.md).
-   Work force optimization. For more information, see [Configuring Workforce Optimization for Field Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/configuring-wfo-fsm.md).
-   Enable **Enable Shift Scheduling for FSM to determine availability** and **Enable/disable association of territory resources with demand channels** configurations. For more information, see [Global domain configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/t_ConfigureFieldService.md).
-   Advanced Capacity and Reservations Management. For information, see [Activate Field Service Advanced Capacity and Reservations management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/capacity-console-plugin.md).

## About this task

Mapping technicians to demand channels within a territory on a time-bound, recurring basis allows appropriate scheduling to reflect real-world patterns, so tasks are assigned to technicians qualified to handle them at the time they are scheduled. You can define repeating schedules driven by union rules, part-time shifts, or regional strategies. For example, a technician might handle installations on weekdays and repairs only on alternate Saturdays.

This association helps assign the tasks to the appropriate technicians during dynamic scheduling, schedule optimization, or manual scheduling. This also helps calculate accurate appointment availability in scripted mode based on technician demand channel recurrence.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territories**.

2.  From the territories list, open the territory where you want to map demand channel to a technician.

3.  In the **Resource Demand Channels** related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_cpk_zrv_3jc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

Reference to the name of the technician you want to associate with demand channel.

</td></tr><tr><td>

Recurrence

</td><td>

Days on which a task for the specified demand channel can be assigned to the technician. If you don't specify any days, task for the specified demand channel can be assigned to the technician on any day.

</td></tr><tr><td>

Territory

</td><td>

Reference to the name of the territory associated with the technician.

</td></tr><tr><td>

Demand Channel

</td><td>

The demand channel that the technician supports in the selected territory.

</td></tr><tr><td>

From

</td><td>

Date from which the demand channel association begins.

</td></tr><tr><td>

To

</td><td>

Date on which the demand channel association ends.

</td></tr><tr><td>

All eligible demand channel

</td><td>

Indicates if the technician can be assigned any tasks related to the eligible demand channels. For example, if a technician is associated with Install, Break Fix, and Repair demand channels, the technician can be assigned any tasks related to these demand channels if the value is set to **true**.

</td></tr><tr><td>

Active

</td><td>

Indicates if the association of technician with demand channel is active. Select the check box to activate the association.

</td></tr></tbody>
</table>5.  Select **Update**.


## Result

Technicians are associated with demand channels.

