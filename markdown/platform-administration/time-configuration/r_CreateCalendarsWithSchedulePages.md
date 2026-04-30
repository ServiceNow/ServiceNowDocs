---
title: Using schedules and calendars
description: Specific applications within the ServiceNow AI Platform generate graphical calendar displays based on schedule pages.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Schedules, Explore, Time configuration, Configure core features, Administer]
---

# Using schedules and calendars

Specific applications within the ServiceNow AI Platform generate graphical calendar displays based on schedule pages.

These schedule pages appear in daily, weekly, or monthly views. Currently, the applications using schedule pages include:

-   Project Management
-   Maintenance Schedules
-   Group On-Call Rotation
-   Field Service Management

Schedule pages are records that contain the scripts that determine the functionality of the graphical display.

-   Because of the heavy degree of scripting involved in a schedule page, you should, for most instances, use the default schedule pages in the base platform.
-   The schedule page uses a URL with a series of parameters attached to generate the graphical display.
-   A schedule page controls calendar content \(`cmn_schedule_page`\) record.

To access Schedule Pages, navigate to **System Scheduler &gt; Schedules &gt; Schedule Pages**. The Schedule Pages form provides the following fields:

<table id="table_g1z_rs4_r4"><thead><tr><th>

Field

</th><th>

Field Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

String

</td><td>

General name used to identity the current schedule page.

</td></tr><tr><td>

Schedule type

</td><td>

String

</td><td>

Schedule type is a string that is used to uniquely identity the schedule page via the "`sysparm_page_schedule_type`" URI parameter. For example, a schedule page could be accessed as follows: **/show\_schedule\_page.do?sysparm\_page\_schedule\_type=gantt\_chart&amp;sysparm\_timeline\_task\_id=d530bf907f0000015ce594fd929cf6a4**

 Alternatively, you can access the schedule page can by setting the "**sysparm\_page\_sys\_id**" URI parameter to the unique 32 character hexadecimal system identifier of the schedule page.

</td></tr><tr><td>

View Type

</td><td>

Choice

</td><td>

Each view type displays different field combinations. There are two options available:-   **Calendars**
-   [Schedule Pages](https://www.servicenow.com/docs/access?context=c_SchedulePages&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

General description that provides additional information about the current schedule page. This field is not necessary.

</td></tr><tr><td>

Init function name

</td><td>

String

</td><td>

**Note:** This functionality is only used by **Calendar** type schedule pages.

The init function name specifies the name of the JavaScript function to call inside the **Client script** function for calendar type schedule pages.

</td></tr><tr><td>

HTML

</td><td>

String

</td><td>

**Note:** This functionality is only used by **Calendar** type schedule pages.

Jelly parses the HTML field, which is a scriptable section. It then injects it into the display page prior to the rest of the calendar. It can be used to pass in variables from the server and define extra fields are necessary.

</td></tr><tr><td>

Client script

</td><td>

String

</td><td>

The client script is a scriptable section that allows for configuring options of the schedule page display. The API is different depending on the schedule page view type.

</td></tr><tr><td>

Server AJAX processor

</td><td>

String

</td><td>

**Note:** This functionality is only used by **Calendar** type schedule pages.

The Server AJAX processor is specific to calendar type schedule pages that is used to return a set of schedule items and spans that display.

</td></tr></tbody>
</table>-   **[Invoke the Schedule page and view a calendar](../concept/c_GenCalViewsFromSchedPages.md)**  
You can use the URL from arguments module, a field decoration \(dictionary attribute `ref_contributions`\), or a UI Action linking to `show_schedule.do` to invoke the Schedule page.
-   **[Schedule calendar](../concept/schedule-calendar.md)**  
Use the Schedule calendar to create, view, and edit events.

**Parent Topic:**[Schedules](../concept/c_UseSchedules.md)

**Related topics**  


[Default schedules](r_DefaultSchedules.md)

[Holidays](../concept/c_Holidays.md)

[Create a holiday schedule for multiple regions](../task/t_CreateAHolidaySchedMultiRegions.md)

[Parent and child schedules](../concept/c_ParentAndChildSchedules.md)

[Define a schedule](../task/t_DefineASchedule.md)

[Schedule for the fifth instance of a week date](../task/t_FifthInstanceOfADayOfTheWeek.md)

[Repeat a monthly schedule](../task/t_RepeatAMonthlySchedule.md)

[Domain support and schedules](../concept/domain-support-for-schedules.md)

