---
title: Configure or update an On-Call schedule
description: Create an On-Call schedule or edit an existing schedule by defining shifts and rosters.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Configure or update an On-Call schedule

Create an On-Call schedule or edit an existing schedule by defining shifts and rosters.

Set up an on-call schedule

## Before you begin

Role required: rota\_admin, rota\_manager

## About this task

You can use the wizard to create an on-call schedule using an existing template or you can create shifts from scratch. You can create multiple shifts at given time and can preview shifts while creating them. This enables you to create rosters, define escalation policies, and review and publish shifts.

After running the wizard, you can adjust individual roster, escalation, and reminder settings to fine-tune the setup. You can also enable on-call notifications by setting up rotation workflow triggers.

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **Create/Edit Schedule**.

2.  In the **Define Schedule**, from the **Select Group** choice list, select the group for which you are defining the schedule.

    You can edit an existing shift for a selected group. If you want to create a new schedule, click **Add shift** button.

    **Note:** When creating a new on-call group schedule, you are redirected to oc\_creation\_wizard page instead of expert\_shell page which is no longer supported.

3.  Choose an existing template for the shifts or create a new shift.

4.  Select the **Allow Shift Schedule overlap** check box to allow overlapping schedules for shifts within the group.

    For example, if a group has a 24x7 schedule, you can create multiple schedules for the group. Shift overlap is required to have a hand-off period between shifts so that multiple shifts can be on-call for the same duration.

    If you select **Allow Shift Schedule overlap**, then the **Escalation rule on Shift overlap** check box appears.

5.  Select the **Escalation rule on Shift overlap** check box to specify which shift needs to be notified of an escalation during a shift overlap.

    You can escalate to an incoming, an outgoing, or to all shifts.

6.  Fill in the form fields.

<table id="table_jrn_sqs_5v"><thead><tr><th>

Question

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the shift that appears on the **On-call calendar** page.

</td></tr><tr><td>

Would you like to use an existing schedule?

</td><td>

Option to use an existing schedule. -   Select **Yes** to use an existing or predefined shift.
-   Select **No** to create a new schedule.


</td></tr><tr><td>

Schedule

</td><td>

Select the value to base your schedule on. Some options are available in the base system, for example, 24x7, Workday 8-5.This option appears only if you answer **Yes** to **Would you like to use an existing schedule?**.

 The logged-in user's time zone is used as the basis for these schedules. If the logged-in user does not have a time zone specified, the instance time zone is used.

</td></tr><tr><td>

Start date

</td><td>

The date on which the shift is scheduled to begin.

</td></tr><tr><td>

Specify holidays

</td><td>

Option to define holidays.-   Select **Yes** to define holidays for the on-call shift. You can select an existing holiday schedule.
-   Select **No** to not specify holidays for the shift.


</td></tr><tr><td>

Holiday Schedule

</td><td>

Specify a holiday schedule for the group.

</td></tr><tr><td class="sub-head" colspan="2">

Additional fields**Note:** The following fields are displayed only when the **Would you like to use an existing schedule?** field is set to **No**.

</td></tr><tr><td>

Time Zone

</td><td>

The time zone in which the shift operates.

</td></tr><tr><td>

Is the shift for this schedule all day?

</td><td>

List of options. Specify whether this shift is an all-day shift.

</td></tr><tr><td>

Start

</td><td>

The time of day the shift is scheduled to start. The start and end time represent one shift. The date is different only if the shift spans midnight.

</td></tr><tr><td>

End

</td><td>

The time of day the shift is scheduled to end. The start and end time represent one shift. The the date is different only if the shift spans midnight.

 For example, for the 8 a.m. to 8 p.m. shift, the start is 2014-01-01 08:00:00 and the end is 2014-01-01 19:59:59. For the 8 p.m. to 8 a.m. shift, the start is 2014-01-01 20:00:00 and the end is 2014-01-02 07:59:59.

</td></tr><tr><td>

Repeats

</td><td>

The days that the shift repeats.

 **Note:** The wizard does not provide a monthly or yearly option. Creating a monthly or a yearly shift by editing the schedule manually is not advised because it is hard to determine the on-call person over a long period. In this case, create a yearly or a monthly schedule with only one roster and one member so that the same person is always on-call. Make any exceptions as a one-time change in the roster for the shift.

</td></tr><tr><td>

Send On-Call Reminders

</td><td>

Option to send [on-call reminders](../reference/escalation-remind-settings-oncall.md) to members of the roster.

</td></tr><tr><td>

Reminder lead time \(days\)

</td><td>

Lead time for email reminders.**Note:** This field is displayed only when the **Send On-Call Reminders** option is selected.

</td></tr><tr><td>

Coverage interval

</td><td>

Interval for updates of coverage details. Specifies whether you want to update the [subscribed](view-my-schedule-on-my-app-oncall.md) calendar with weekly or daily coverage details.

</td></tr><tr><td>

Get coverage for

</td><td>

Number of weeks or days for which you want to update the subscribed calendar.

</td></tr></tbody>
</table>    **Note:** The instance saves the schedule and adds it to the list of existing schedules.

7.  Click **Next**.

8.  Click **Add Shift** to add another shift to the schedule if needed.

9.  Use the **Members** page to specify members for a shift and rosters.

<table id="table_phk_ky1_kr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roster Name

</td><td>

Use the edit icon to edit the name of the [roster](config-roster-oncall.md) that you are adding members to.

</td></tr><tr><td>

Which members would you like to be in your schedule?

</td><td>

Move the members you want to add from Available list to Selected list.

</td></tr><tr><td>

Rotation start date

</td><td>

Date on which the rotation needs to start.

</td></tr><tr><td>

Rotation interval

</td><td>

Type of the rotation interval.

</td></tr><tr><td>

Rotate every

</td><td>

Frequency of the rotation interval.**Note:** This field appears only if the **Rotation interval** field is set to **Weekly**.

</td></tr><tr><td>

Day of week for rotation

</td><td>

Day of the week on which the roster rotation should start. When this field is specified, roster rotation happens based on the specified frequency and the day of the week.**Note:** This field appears only if the **Rotation interval** field is set to **Weekly**.

</td></tr><tr><td>

Send On-Call Reminders

</td><td>

If selected, on-call reminders are sent to the members of the roster.

</td></tr><tr><td>

Reminder lead time \(days\)

</td><td>

Lead time for email reminders.**Note:** This field is displayed only when the **Send On-Call Reminders** option is selected.

</td></tr></tbody>
</table>10. Click **Next Step**.

11. Use the Escalation Setup form to specify escalation settings.

<table id="table_inz_11m_jhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Escalation type

</td><td>

Method used to determine who receives an escalation notification. Its value is automatically set to **Rotate Through Members** if a shift has only one roster. The escalation path goes through all members of that roster. If a shift has more than one roster, the default value is **Rotate Through Rosters**. The escalation path goes through all the rosters to determine who to notify. [Click **Override escalation** to change the default setting.](create-custom-esc-policy-oncall.md)

</td></tr><tr><td>

Catch-All

</td><td>

Specifies users who receive a notification when no other on-call users have acknowledged the escalation. The value can be none, a group manager, a shift manager, an individual, or any or all roster members. -   Select **Notify Individual** to specify a member of the group to notify.
-   Select **Notify All** to specify a shift. All shift members are notified.


</td></tr></tbody>
</table>12. Click **Next Step**.

13. Click **Edit Reminder** to edit the reminder settings for an escalation.

14. Use the Edit Reminder form to edit the reminder settings for a schedule.

<table id="table_skn_fcj_jhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\# reminders

</td><td>

When escalations are configured for this group, the instance first sends this number of reminders before notifying the backup personnel.

</td></tr><tr><td>

Time between reminders

</td><td>

The interval of time between reminders. Default: 15 minutes

If your choice is not in the list, select the closest value. [Edit the roster](update-shift-from-calendar-oncall.md) to update the number of reminders after the schedule is generated.

</td></tr><tr><td>

Time before escalation

</td><td>

The interval of time to wait before escalating a task.

</td></tr></tbody>
</table>15. Review the schedule and then click **Save**.

    The schedule is saved in Draft mode.

16. Select **Send subscriptions** to send a subscription URL to an on-call member after the shift is published.

17. After the schedule is complete, click **Finish** to save and publish the schedule.


## What to do next

Perform one of the following procedures to update the schedule.

-   **[Updating an On-Call schedule](update-schedule-oncall.md)**  
Shift managers and members can use the **Schedules** tabs to view and update the on-call schedules of a group. Shift managers can review, manage, and resolve gaps or conflicts in your On-Call schedule from a single view.
-   **[Update a schedule entry](schedule-entry-update-oncall.md)**  
You can deactivate a schedule entry or update setting like schedule entry type, date, or time.
-   **[Specify the sources of contact information for schedule notifications](config-contact-sources-oncall.md)**  
Configure the communications methods that shift managers can choose from to send on-call schedule notifications. For example, add email and phone contact sources.
-   **[Manage shifts from the Calendar view](customize-calendar-view-oncall.md)**  
The Calendar view displays all shifts for a user group for a specified time interval. Use the Calendar view of an On-Call schedule to update or manage shifts.
-   **[Manage shifts from the Timeline view](customize-timeline-view-oncall.md)**  
Use the Timeline view of an On-Call schedule to update or manage shifts based on the geographical location of roster members.

**Parent Topic:**[Managing schedules and shifts](../../user-administration/concept/manage-schedules-and-shifts.md)

