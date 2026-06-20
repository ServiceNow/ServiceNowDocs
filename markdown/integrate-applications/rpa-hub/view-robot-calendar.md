---
title: View current robot events in RPA Hub
description: View the current robot events on the Robot Calendar tab in RPA Hub for unattended robots. By using the calendar, you can manage and plan a robot's schedule in a single view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/view-robot-calendar.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
keywords: [unattended bot process intervals rpa hub]
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# View current robot events in RPA Hub

View the current robot events on the **Robot Calendar** tab in RPA Hub for unattended robots. By using the calendar, you can manage and plan a robot's schedule in a single view.

## Before you begin

Create an unattended robot. On the robot form, ensure that you select the **Robot Type** field as **Unattended**. For more information, see [Creating an attended or an unattended robot in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-robot.md).

Establish the robot connection to an unattended bot process. For more information, see [Assign a robot to a bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/assign-robots.md).

Create a schedule within an unattended bot process to view some schedules on the robot calendar. Ensure that one or more active schedules are associated with the robot. For more information, see [Create a schedule within a bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-schedule-botprocess.md).

Verify that the life-cycle stage of the associated bot process isn’t set to **Retired**.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_business\_user, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

If a robot is associated to multiple bot processes, the landing page of the robot calendar is the schedule view of a published bot process. There can be more than one published bot process associated with a robot.

To view more robot events, add the appropriate **Life Cycle Stage Status** filter in the Robot Calendar.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  View a robot calendar either from a robot or from a bot process.

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d198491e157">

Option

</th><th align="left" id="d198491e160">

Action

</th></tr></thead><tbody><tr><td id="d198491e166">

**View a robot calendar from a robot**

</td><td>

1.  On the **Lists** tab, under **Administration**, select **Robots**.
2.  Open a robot to view the robot calendar.
3.  In the form header, select **Robot Calendar**.


</td></tr><tr><td id="d198491e199">

**View a robot calendar from a bot process**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open a bot process to view the robot calendar.
3.  In the form header, select **Show Robot Calendar**.
4.  In the **Select the robot to view the calendar** dialog box, select a robot from the Robot list.
5.  Select **Continue**.


</td></tr></tbody>
</table>4.  On the **Robot Calendar** tab, perform any of the following actions.

<table id="choicetable_jxq_nft_v5b"><thead><tr><th align="left" id="d198491e256">

Option

</th><th align="left" id="d198491e259">

Action

</th></tr></thead><tbody><tr><td id="d198491e265">

**Today**

</td><td>

Highlights the current date.

</td></tr><tr><td id="d198491e274">

**Date range \(&lt;, &gt;\)**

</td><td>

Select the arrow buttons \(**&lt;**, **&gt;**\) to view the next calendar view that is based on the defined date range.

</td></tr><tr><td id="d198491e289">

**Schedule Timezones**

</td><td>

View the time zones that are defined for the robot, such as, the robot time zone \(workstation time zone\), user profile time zone, and schedule time zone. This field is a drop down list. There can be multiple schedule time zones, based on various schedules defined across different time zones.

 The time zones are sorted alphabetically in ascending order and the user profile time zone is the default time zone.

 The workstation time zone contains the time zone information of the machine on which robot is running.

 The workstation time zone appears in the time zone list only when at least one schedule is defined with the workstation time zone and the robot is connected to the same RPA Hub instance at least once.

 The user profile time zone is defined at the instance level, you can modify it from your profile.

 The schedule time zone is defined in the **Timezone** field while creating a schedule for a bot process.

 The schedule time zone is mapped to the Windows time zone.

 The schedule time zone appears in the time zone list only when at least one active schedule is defined with a specific time zone instead of a workstation time zone.

 If the robot is associated with bot processes that have schedules to be triggered in different time zones, then all those time zones are displayed in the time zone list.

 Along with these scheduled timezones, timezone of current user is also be added to the list. This user profile time zone becomes the default time zone.

 If the robot is associated with a bot process whose schedule has to be triggered based on workstation time zone, then those workstation time zones are displayed in the time zone list.

</td></tr><tr><td id="d198491e341">

**Day**

</td><td>

View events in the calendar for a particular day. See the following example for a snapshot of the Robot calendar view.\[Omitted image "day-rc-rpa.png"\] Alt text: Example: Snapshot of the Robot Calendar view for a day, October 20, 2022.

</td></tr><tr><td id="d198491e363">

**Week**

</td><td>

View events in the calendar for a particular week. The week view starts from Sunday to Saturday. The default first day of the week is Sunday. See the following example for a snapshot of the Robot calendar view.This is the default view of the robot calendar.

 Every event must be specific to the start date and end date of the schedule.

 The cadence of the events must be based on weekdays that are mentioned in the schedule.

 The events are generated based on the **Start Date** field on the schedule form. For more information, see [Schedule form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/schedule-rpa-form.md).

 \[Omitted image "week-rc-rpa.png"\] Alt text: Example: Snapshot of the Robot Calendar view for a week, November 13 to 19, 2022.

</td></tr><tr><td id="d198491e409">

**Month**

</td><td>

View events in the calendar for a particular month. See the following example for a snapshot of the Robot calendar view.\[Omitted image "month-rc-rpa.png"\] Alt text: Example: Snapshot of the Robot Calendar view for a month, November 2022.

</td></tr><tr><td id="d198491e430">

**New Schedule**

</td><td>

Create a schedule on the **Robot Calendar** tab by selecting the **New Schedule** button, to execute unattended robots.You can also create a schedule by right-clicking or double-clicking an empty slot of the robot calendar. For more information about creating a schedule, see [Create a schedule on the robot calendar in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-robot-schedule.md).

</td></tr><tr><td id="d198491e463">

**Refresh**

</td><td>

View new or updated schedules on the robot calendar by selecting the refresh icon \(\[Omitted image "refresh-rc-icon.png"\] Alt text: Refresh icon.\).

</td></tr><tr><td id="d198491e478">

**Show or hide agenda view**

</td><td>

Show or hide events for the particular day, week, or month by selecting the agenda icon \(\[Omitted image "agenda-rc-rpa-icon.png"\] Alt text: Agenda icon.\). See the following example for a snapshot of the show or hide agenda filter view.\[Omitted image "agenda-view-rc-rpa.gif"\] Alt text: Show or hide the agenda view filter.

</td></tr><tr><td id="d198491e505">

**Show Filter**

</td><td>

View the filter options to display the schedules on the life-cycle stage status of the bot process and the bot process name.You can view schedules and scheduled maintenance days of a published bot processes.

Select the filter icon \(\[Omitted image "filter-rc-rpa.png"\] Alt text: Filter icon.\) to view the filter options.

 In the Process Name list or the Life Cycle Stage Status list, perform any of the following actions:

-   To add items to the selection, double-click an available item on the left or select an item and select the add icon \(**&gt;**\). Then, select **Apply**. The new item is added at the bottom of the selected items column on the right.\[Omitted image "filter-process-name-rc-rpa.gif"\] Alt text: Process Name filter. \[Omitted image "filter-lcss-rc-rpa.gif"\] Alt text: Life-cycle stage status filter.
-   To remove items from the selection, double-click the item on the right, or select the item and select the remove icon \(**&lt;**\). Then, select **Apply**.


</td></tr><tr><td id="d198491e560">

**Event cards**

</td><td>

View the event cards in the Scheduled events section.Limited information about the associated bot process and its schedule is displayed.

 \[Omitted image "event-card-rc-rpa.png"\] Alt text: Example: Snapshot of the event cards on the robot landing page.

</td></tr><tr><td id="d198491e584">

**Event details**

</td><td>

To view more event details of the bot process and its schedule, double-click an event card.\[Omitted image "event-details-rc-rpa.gif"\] Alt text: Event details snapshot of the associated bot process whose interval type is Daily.

 \[Omitted image "rpa-rc-snap-bot-process.jpg"\] Alt text: Event details snapshot of the associated bot process whose interval type is Hours.

 \[Omitted image "event-card-weekly.png"\] Alt text: Event details snapshot of the associated bot process whose interval type is Weekly.

</td></tr><tr><td id="d198491e629">

**Event pop-up windows**

</td><td>

On the event pop-up window, select the following icons to view, edit, and delete a schedule:-   Select the view bot process details icon \(\[Omitted image "icon-view-bp-rpa.png"\] Alt text: View bot process details icon.\) to get the bot process details in a new tab.
-   Select the view event details icon \(\[Omitted image "icon-view-event-rpa.png"\] Alt text: View event details icon.\) to view more details about the schedule in the contextual side panel.
-   Select the edit schedule icon \(\[Omitted image "icon-edit-schedule-rpa.png"\] Alt text: Edit schedule icon.\) to edit an existing schedule.
-   Select the delete schedule icon \(\[Omitted image "icon-delete-schedule-rpa.png"\] Alt text: Delete schedule icon.\) to delete a schedule that you no longer need.
\[Omitted image "event-pop-card-icons.png"\] Alt text: Snapshot of an event card pop over.

For more information, see [Create a schedule on the robot calendar in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-robot-schedule.md), [Edit a robot schedule in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/edit-robot-schedule.md), and [Delete a robot schedule in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/delete-robot-schedule.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Managing RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/managing-rpa-hub.md)

