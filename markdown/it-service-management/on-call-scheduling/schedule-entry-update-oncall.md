---
title: Update a schedule entry
description: You can deactivate a schedule entry or update setting like schedule entry type, date, or time.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure or update an On-Call schedule, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Update a schedule entry

You can deactivate a schedule entry or update setting like schedule entry type, date, or time.

## Before you begin

Role required: rota\_admin or rota\_manager

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Calendars**.

    The on-call coverage for your group's calendar appears.

2.  Click the shift name and navigate to **Actions** &gt; **Edit span**.

    The **Schedule Entry** dialog box is displayed.

    ![Schedule entry form](../image/OC_SchedEntry.png)

3.  Update the fields as needed.

<table id="table_xdf_t21_w5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Modify the name of the schedule entry, if required.

</td></tr><tr><td>

Type

</td><td>

Select the type of schedule entry. For example, on-call or time off.

</td></tr><tr><td>

Group

</td><td>

The **Group** field is empty by design.**Warning:** If the **Group** field is populated, then the spans for the entry are not displayed.

</td></tr><tr><td>

Show as

</td><td>

Select what the schedule entry must be displayed as. For example, busy or on-call.

</td></tr><tr><td>

When

</td><td>

Select the appropriate start and end date, and time for the schedule entry.

</td></tr><tr><td>

All day check box

</td><td>

Select the check box to make the schedule entry active for the entire duration.

</td></tr><tr><td>

Timezone

</td><td>

Displays the time zone for the schedule entry. This cannot be modified.

</td></tr><tr><td>

Repeats

</td><td>

Select the frequency with which the schedule entry repeats. For example, daily or weekly.The following fields appear if you select **Monthly**:

 **Monthly type**: specify the date of the month when the schedule entry repeats.

 The following fields appear if you select **Yearly**:

 **Yearly type**: specify the date of the year when the schedule entry repeats or if it is floating. If you select the **Floating** option, then the following fields appear:

-   **Float week**: Select the week of the month when the schedule entry repeats.
-   **Float day**: Select the day of that week when the schedule entry repeats.
-   **Month**: Select the month when the schedule entry repeats.


</td></tr><tr><td>

Repeat every

</td><td>

If the schedule entry is selected to repeat, then specify how often it repeats. For example, if you select weekly repetitions, specify the frequency such as every week or every two weeks.

</td></tr><tr><td>

Repeat on

</td><td>

If the schedule entry is selected to repeat, then specify when it repeats. For example, if you select weekly repetitions, specify the days of the week when it would repeat.

</td></tr><tr><td>

Repeat until

</td><td>

If the schedule entry is scheduled to repeat, then specify an end date until which the schedule entry repeats itself.

</td></tr><tr><td>

Deactivate

</td><td>

Deactivate the schedule entry. A warning message appears.

</td></tr><tr><td>

Delete

</td><td>

Delete the schedule entry. A warning message appears.

</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[Configure or update an On-Call schedule](create-update-schedule-oncall.md)

**Related topics**  


[Assigning On-Call Scheduling roles](../concept/roles-assigning-oncall.md)

