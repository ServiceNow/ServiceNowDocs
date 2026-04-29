---
title: Create an equipment model entity schedule
description: Create an equipment model entity schedule with the Industrial Process Manager application. With these schedules, you can easily maintain multiple equipment model entities.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing an equipment model entity schedule, Configure, Industrial Process Manager, Operational Technology]
---

# Create an equipment model entity schedule

Create an equipment model entity schedule with the Industrial Process Manager application. With these schedules, you can easily maintain multiple equipment model entities.

## Before you begin

Role required: sn\_isa\_schedule\_admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Entity Schedules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_e2d_dfx_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the schedule.

</td></tr><tr><td>

Time zone

</td><td>

Time zone for the schedule. If you select **Floating**, the time zone is relative to whatever process is accessing the item at. For example, if a resource manager in Amsterdam sets a floating schedule for 8:00 to 17:00, a user in San Jose, California, also sees the schedule as 8:00 to 17:00. When you define a schedule in one time zone, users in different time zones see the schedule in their own time zone.

</td></tr><tr><td>

Type

</td><td>

Text label that describes the purpose of the schedule.

</td></tr><tr><td>

Description

</td><td>

Description of the schedule.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Now, you can create the entries for an equipment model entity schedule. For more information, see [Create a schedule entry](create-new-schedule-entry.md).

**Parent Topic:**[Managing an equipment model entity schedule](../concept/managing-equipment-entity-schedules.md)

