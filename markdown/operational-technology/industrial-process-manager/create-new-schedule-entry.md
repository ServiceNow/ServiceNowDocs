---
title: Create a schedule entry
description: Create a schedule entry for an existing equipment model entity schedule in the Industrial Process Manager application. You can create more than one entry for a schedule. Schedule entries allow multiple maintenance tasks to take place for one equipment model entity.
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing an equipment model entity schedule, Configure, Industrial Process Manager, Operational Technology]
---

# Create a schedule entry

Create a schedule entry for an existing equipment model entity schedule in the Industrial Process Manager application. You can create more than one entry for a schedule. Schedule entries allow multiple maintenance tasks to take place for one equipment model entity.

## Before you begin

Role required: sn\_isa\_schedule\_admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Entity Schedules**.

2.  Select an existing equipment model entity schedule record.

3.  Select the **Schedule Entries** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_evl_lgx_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the schedule entry.

</td></tr><tr><td>

Type

</td><td>

Label that describes the purpose of the schedule.

</td></tr><tr><td>

Show as

</td><td>

Option that indicates how the schedule entry should appear in calendar applications.

</td></tr><tr><td>

Repeats

</td><td>

Repetition interval for the schedule entry, if any. If you select a repetition interval, other fields appear so that you can further specify the repeat interval.

</td></tr><tr><td>

Repeat every

</td><td>

Scheduling repetition frequency - weekly, monthly, or yearly. This field appears only when **Daily**, **Weekly**, **Monthly**, or **Yearly** is selected from the **Repeats** field.

</td></tr><tr><td>

Repeat on

</td><td>

Days of the week that a weekly schedule repeats on. This field appears only when **Weekly** is selected from the **Repeats** field.

</td></tr><tr><td>

Monthly type

</td><td>

Monthly schedule repetition frequency. This field appears only when **Monthly** is selected from the **Repeats** field. Options include:-   Repeat on a specific day of the month.
-   Repeat on a specific day in a specific week of the month.
-   Repeat on the last day of the month.
-   Repeat on a specific weekday in the last week of the month.


</td></tr><tr><td>

Yearly type

</td><td>

Yearly schedule repetition frequency. This field appears only when **Yearly** is selected from the **Repeats** field. Options include:

 -   Repeat on a specific day of the year.
-   Repeat on a floating day.


</td></tr><tr><td>

Float week

</td><td>

Week of the month that a floating yearly schedule repeats on. This field appears only when **Floating** is selected from the **Yearly** field.

</td></tr><tr><td>

Float day

</td><td>

Day of the week that a floating yearly schedule repeats on. This field appears only when **Floating** is selected from the **Yearly** field.

</td></tr><tr><td>

Month

</td><td>

Month of the year that a floating yearly schedule repeats on. This field appears only when **Floating** is selected from the **Yearly** field.

</td></tr><tr><td>

Repeat until

</td><td>

Repetition end date. If you leave this field empty, the schedule repeats indefinitely.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

Your schedule entry is created, and now you can edit and update the entry as necessary.

**Parent Topic:**[Managing an equipment model entity schedule](../concept/managing-equipment-entity-schedules.md)

