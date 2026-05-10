---
title: Create a schedule to use with the agent calendar
description: Users with the agent calendar administrator role can create a schedule to use with the agent calendar.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring an agent calendar, Agent calendar, Schedules and sites, Use, Customer Service Management]
---

# Create a schedule to use with the agent calendar

Users with the agent calendar administrator role can create a schedule to use with the agent calendar.

## Before you begin

Role required: agent\_schedule\_admin

## About this task

Creating a schedule for the agent calendar uses the schedule feature. For more information, see [Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_UseSchedules.md).

Schedules are configured with two types of records.

-   Schedule records specify a time zone and a type of schedule and use one or more schedule entries. Schedule records are saved in the Schedule \[cmn\_schedule\] table.
-   Schedule entry records specify the time periods that are included or excluded from a schedule. Schedule entries are saved in the Schedule Entry \[cmn\_schedule\_span\] table.

For more information on schedule fields, see [Schedule fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/r_ScheduleFields.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Schedule** &gt; **Schedule**.

2.  Click **New**.

3.  Complete the fields on the Schedule form.

<table id="table_mrk_t4m_bdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the schedule.

</td></tr><tr><td>

Time Zone

</td><td>

Select the time zone for the schedule. If you select **Floating**, the time zone will be relative to whatever is accessing the item at any given time.

</td></tr><tr><td>

Parent

</td><td>

Select a parent schedule to constrain the new schedule.

</td></tr><tr><td>

Type

</td><td>

Enter a label that describes the purpose of the schedule. You can also use one of these system terms to determine how to process certain schedules:-   **excluded:** excludes time periods from SLA counts.
-   **maintenance:** specifies time periods where change management activities are allowed. A schedule containing maintenance schedule entries cannot also contain blackout schedule entries.
-   **blackout:** excludes time periods from change management schedules. A schedule containing blackout schedule entries cannot also contain maintenance schedule entries.


</td></tr><tr><td>

Description

</td><td>

\[Optional\] Describe the schedule.

</td></tr></tbody>
</table>    **Note:** The Schedule form displays a warning message if there are no active entries defined for the current schedule. If your schedule is a child schedule that only contains exclusions, ignore the message because exclusions are non-active entries.

4.  Right-click the header bar and click **Save**.

    **Note:** If you create a schedule of type **maintenance** and save the record, a UI policy hides the **Type** field from the form. To view or change the value for the **Type** field, view the list of schedules rather than the schedule form and add the **Type** column if necessary. You can double-click the cell for the value in the **Type** column and modify from the list view.

5.  Configure one or more schedule entries.

6.  Click **Submit**.


