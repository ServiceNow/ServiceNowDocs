---
title: Use the agent calendar
description: Users with the agent calendar user role can add events to their personal calendar and configure the calendar to show or hide different types of events.Users with the agent schedule user role can add events to their personal calendar.Users with the agent schedule user role can move events on their personal calendar.Users with the agent schedule user role can personalize their calendar and show or hide different types of events.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Managing agent skills,schedules, and tasks, Managing workforce, Use, Field Service Management]
---

# Use the agent calendar

Users with the agent calendar user role can add events to their personal calendar and configure the calendar to show or hide different types of events.

**Related topics**  


[Configuring an agent calendar](configure-agent-calendar.md)

[Managing agent calendar](agent-calendar.md)

## Add an event to the agent calendar

Users with the agent schedule user role can add events to their personal calendar.

### Before you begin

Role required: agent\_schedule\_user

### Procedure

1.  Navigate to your calendar.

    -   **Customer Service** &gt; **My Schedule**
    -   **Field Service** &gt; **Agent** &gt; **My Schedule**
2.  Double-click a timeslot or click and drag over a timeslot on the calendar to open the New Event form.

    ![The agent schedule shows an event on Tuesday, July 9, and a new event being selected for Wednesday, July 10.](../../field-service-management/image/agent-my-schedule.png "Agent schedule")

3.  Fill in the fields on the New Event form, as necessary.

<table id="table_agv_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the event.

</td></tr><tr><td>

Type

</td><td>

The type of event:-   Time off
-   Appointment
-   Meeting
-   Phone call
-   Excluded
-   On call
-   Time off - in approval
-   Time off - rejected


</td></tr><tr><td>

Show as

</td><td>

Show this event on the agent's personal calendar as one of the following:-   Busy
-   Free
-   Tentative
-   On call
 Select **Busy** to exclude the block of time from agent availability calculations for the auto assignment and the case assignment workbench.

</td></tr><tr><td>

When

</td><td>

The start date and time of the personal event.

</td></tr><tr><td>

To

</td><td>

The end date and time of the personal event.

</td></tr><tr><td>

All day

</td><td>

Enable this check box if the event lasts all day.

</td></tr><tr><td>

Time zone

</td><td>

\[Read only\] If an agent has selected a specific time zone in their user profile, that time zone is displayed here and is used as the time zone for this event. Subsequent changes to the **Time zone** field in the user profile do not change the time zone designation for this event.

</td></tr><tr><td>

Repeats

</td><td>

Create a repeating event by selecting the frequency. Depending on the selection, other fields are required to complete the frequency information.-   Does not repeat
-   Daily
-   Every Weekday \(Mon-Fri\)
-   Every Weekend \(Sat, Sun\)
-   Every Mon, Wed, Fri
-   Every Tue, Thu
-   Weekly
-   Monthly
-   Yearly


</td></tr><tr><td>

Repeat every

</td><td>

Enter a number for the frequency of the repeated event.

</td></tr><tr><td>

Repeat on

</td><td>

For weekly events, select a day of the week.

</td></tr><tr><td>

Monthly type

</td><td>

For monthly events, select one of the following. These selections use the day and date in the **When** field as the basis for repetition.-   Day of the month
-   Day of the week
-   Last day of the month
-   Last week of the month


</td></tr><tr><td>

Yearly type

</td><td>

For monthly events, select one of the following:-   Day of the year: this selection uses the day and date in the **When** field as the basis for repetition.
-   Floating: for this selection, complete the **Float week**, **Float day**, and **Float month** fields.


</td></tr><tr><td>

Repeat until

</td><td>

Select a date for the end of the repeated event.

</td></tr><tr><td>

Float week

</td><td>

For a floating yearly repeating event, select the week.

</td></tr><tr><td>

Float day

</td><td>

For a floating yearly repeating event, select the day.

</td></tr><tr><td>

Float month

</td><td>

For a floating yearly repeating event, select the month.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The new event appears on the agent calendar and also in the **Schedule Entries** related list on the Agent Personal Schedule form.


## Move an event on the agent calendar

Users with the agent schedule user role can move events on their personal calendar.

### Before you begin

Role required: agent\_schedule\_user

### Procedure

1.  Navigate to your calendar.

    -   **Customer Service** &gt; **My Schedule**
    -   **Field Service** &gt; **Agent** &gt; **My Schedule**
2.  Use one of the following methods to move an event.

<table id="choicetable_ezl_bqb_hx"><tbody><tr><td id="d74727e628">

**Click an event and drag it to a new day or time**

</td><td>

The **When** and **To** fields in the event record are updated with the new information.

</td></tr><tr><td id="d74727e643">

**Double-click an event to open the event record**

</td><td>

Change the date and time information in the **When** and **To** fields and click **Submit**. The event appears on the calendar in the new location.

</td></tr></tbody>
</table>
## Show or hide event types on the agent calendar

Users with the agent schedule user role can personalize their calendar and show or hide different types of events.

### Before you begin

Role required: agent\_schedule\_user

### Procedure

1.  Navigate to your calendar.

    -   **Customer Service** &gt; **My Schedule**
    -   **Field Service** &gt; **Agent** &gt; **My Schedule**
2.  Click the configuration icon \(![Configuration icon.](../../field-service-management/image/icon-agent-sched-config.png)\) in the calendar header to display the Schedule Configuration menu.

3.  Enable or disable the switches for the different types of events.

    An option is enabled when the switch is moved to the right and appears with a green background.

4.  Click the configuration icon \(![Configuration icon.](../../field-service-management/image/icon-agent-sched-config.png)\) again to hide the Schedule Configuration menu.

    The calendar displays the enabled task types.


