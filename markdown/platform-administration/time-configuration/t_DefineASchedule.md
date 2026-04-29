---
title: Define a schedule
description: Configure schedules using schedule and schedule entry records.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Schedules, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a schedule

Configure schedules using schedule and schedule entry records.

## Before you begin

Role required: schedule\_admin or admin

## About this task

-   Schedule records specify a time zone and a type of schedule and use one or more schedule entries. Schedule records are saved in the Schedule \[`cmn_schedule`\] table.
-   Schedule entry records specify the time periods that are included or excluded from a schedule. Schedule entries are saved in the Schedule Entry \[`cmn_schedule_span`\] table.

Alternately, you can also use the Business Calendar functions to create schedules. To learn more about creating business calendars and schedules, see [Creating business calendars](../concept/business-calendars.md).

**Warning:** If you’re using Performance Analytics, use caution when changing time spans. Any change you make to the time span on a business or fiscal calendar can invalidate the Performance Analytics data. Consult with a Performance Analytics administrator before making such changes.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Schedules** &gt; **Schedules**.

2.  Select **New**, enter a unique and meaningful **Name** and **Description** and then fill in the form.

    For detailed information on Schedule form fields, see [Schedule fields](../reference/r_ScheduleFields.md).

    **Note:** If there are no active entries defined for the current schedule, a warning message appears in the Schedule form. If your schedule is a child schedule that contains only exclusions, ignore the message because exclusions are non-active entries.

3.  Right-click the header bar and select **Save**.

    **Note:**

    -   In the Related link, select **Show Schedule** to view the schedule in the calendar using the Next Experience user interface. For more information on this framework, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US). To create schedule entries in the [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US), refer to [Create schedule entries in the Schedule calendar](create-events-next-experience-ui.md).

        To use the [classic schedule calendar](../concept/schedule-calendar.md), you can add the **glide.schedule.enable\_classic\_calendar** property and set it to **true**. For information on how to add a system property, see [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#).

    -   If you create a schedule of type **maintenance** and save the record, a UI policy hides the **Type** field from the form. To view or change the **Type** value, use the list of schedules instead of the schedule form. Add the **Type** column if necessary. You can click the cell for the value in the **Type** column and modify the value in the list view.
4.  Configure one or more schedule entries.

    For detailed information on Schedule Entry form fields, see [Schedule entry fields](../reference/r_ScheduleEntryFields.md).


-   **[Schedule fields](../reference/r_ScheduleFields.md)**  
The Schedule form contains the following fields.
-   **[Schedule entry fields](../reference/r_ScheduleEntryFields.md)**  
You can only associate a schedule entry with one schedule. The **Schedule Entries** related list contains the definitions of the time periods you want to include in or exclude from the schedule.

**Parent Topic:**[Schedules](../concept/c_UseSchedules.md)

**Related topics**  


[Default schedules](../reference/r_DefaultSchedules.md)

[Holidays](../concept/c_Holidays.md)

[Create a holiday schedule for multiple regions](t_CreateAHolidaySchedMultiRegions.md)

[Parent and child schedules](../concept/c_ParentAndChildSchedules.md)

[Schedule for the fifth instance of a week date](t_FifthInstanceOfADayOfTheWeek.md)

[Repeat a monthly schedule](t_RepeatAMonthlySchedule.md)

[Using schedules and calendars](../reference/r_CreateCalendarsWithSchedulePages.md)

[Domain support and schedules](../concept/domain-support-for-schedules.md)

[Schedules](../concept/c_UseSchedules.md)

