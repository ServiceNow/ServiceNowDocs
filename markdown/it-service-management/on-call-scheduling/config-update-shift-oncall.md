---
title: Configure or update an On-Call shift
description: You can add extra coverage, specify extra times for when a shift is active, and schedule time off.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Configure or update an On-Call shift

You can add extra coverage, specify extra times for when a shift is active, and schedule time off.

## Before you begin

Role required: rota\_admin or rota\_manager

## About this task

You can update the calendar only for the time zone specified in your user profile.

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Calendars**.

    The on-call calendar opens.

2.  Click the Timeline view icon \(![Timeline view icon](../image/view-calendar-timeline-icon.png)\).

3.  Click the Filters icon \(![Filters icon](../image/filters-icon.png)\) and then select the group.

    The calendar displays the selected group.

4.  Right-click a block that represents a member of the shift and select **Manage Shift**.

    The Manage Shift dialog box displays the current shift settings.

    ![Manage Shift dialog box](../image/manage-shift-provide-covrg-popup.png)

5.  Select an **Action**, as appropriate.

<table id="choicetable_cvj_ztc_55"><tbody><tr><td id="d382287e137">

**Provide coverage**

</td><td>

Select details of the member who will provide on-call coverage for another roster member. The following options appear when you select this option:-   Rosters: Select one or more rosters for which the member will provide coverage.
-   Member: Select the member to provide extra coverage.
-   Shift start: Select the date from which the coverage will start.
-   Shift end: Select the date on which the coverage will end.
 **Note:** The coverage is created between the start and end date of the shift based on its schedule time.

</td></tr><tr><td id="d382287e164">

**Schedule extra time**

</td><td>

Specify extra coverage for the selected shift. The following options appear when you select this option:-   Shift: Select the shift for which you want to specify extra time.
-   Shift start: Select the date from which the extra time will start.
-   Shift end: Select the date on which the extra time will end.


</td></tr><tr><td id="d382287e185">

**Schedule time off**

</td><td>

Specify the group member who will take scheduled time off during the selected time frame. The following options appear when you select this option:-   Member: Select the member who requested time off.
-   Starts: Select the date and time from which the time-off period will start.
-   Ends: Select the date and time on which the time-off period will end.
-   All day event: Select if the time-off period is a total of one working day.
-   Proposed cover: Select the name of the shift member who you would like to provide cover in your absence.


</td></tr></tbody>
</table>6.  Click **Schedule** to schedule the update.

7.  To save the view settings, click the Bookmark this filter icon \(![Bookmark this filter icon](../image/view-favourite-icon.png)\).


-   **[Configure a roster](config-roster-oncall.md)**  
Edit a roster to specify its reminder and escalation settings and to identify a subset of group members to participate in the On-Call roster.
-   **[Update shift details from the On-Call calendar](update-shift-from-calendar-oncall.md)**  
To save time, update shift details directly from an on-call calendar.
-   **[Send or resend reminders of an upcoming shift](send-shift-remind-email-oncall.md)**  
Remind roster members of an upcoming shift by sending an email notification. You specify the number of days before their shift starts for the email.
-   **[Configure the lead time for email reminders](config-lead-time-reminders-oncall.md)**  
On-Call Scheduling includes a scheduled job that checks if any shift members should be notified about upcoming On-Call commitments. Modify the lead time for the reminder to be sent.
-   **[Manage requests for time off](manage-time-off-requests-oncall.md)**  
As a shift manager, you can review and approve time-off requests from shift members. You also specify the roster member who can cover for the time.
-   **[Resolve gaps, conflicts, and time-off requests in a shift](resolv-gap-conflct-timeoff-oncall.md)**  
Review and resolve gaps and conflicts. Find a replacement on-call member for time-off requests to ensure proper support coverage.
-   **[Managing roster members](../concept/managing-roster-members.md)**  
You can manage roster members by adding and removing users to or from the roster as needed. You can also modify the order number for a member without affecting the past shift schedule.

**Parent Topic:**[Managing schedules and shifts](../../user-administration/concept/manage-schedules-and-shifts.md)

**Related topics**  


[View On-Call schedules](view-schedules-oncall.md)

[Manage shifts from the Calendar view](customize-calendar-view-oncall.md)

