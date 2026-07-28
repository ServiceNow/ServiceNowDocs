---
title: Delete a robot schedule in RPA Hub
description: Delete an existing robot schedule of a bot process on the Robot Calendar tab in RPA Hub that you no longer need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/delete-robot-schedule.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Robot calendar, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Delete a robot schedule in RPA Hub

Delete an existing robot schedule of a bot process on the **Robot Calendar** tab in RPA Hub that you no longer need.

## Before you begin

Perform the following tasks before you delete a robot schedule:

-   Create an unattended robot. On the robot form, ensure that you select the **Robot Type** field as **Unattended**. For more information, see [Create an unattended robot in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-unattended-robot.md).
-   Establish the robot connection to an unattended bot process. For more information, see [Assign a robot to a bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/assign-robots.md).
-   Create a schedule for a unattended bot process to view some schedules on the robot calendar. For more information, see [Create a schedule on the robot calendar in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-robot-schedule.md) or [Create a schedule within a bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-schedule-botprocess.md).
-   Verify that the life-cycle stage of the associated bot process isn’t set to **Retired**.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  View a robot calendar either from a robot or from a bot process.

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d482174e162">

Option

</th><th align="left" id="d482174e165">

Action

</th></tr></thead><tbody><tr><td id="d482174e171">

**View a robot calendar from a robot**

</td><td>

1.  On the **Lists** tab, under **Administration**, select **Robots**.
2.  Open a robot to view the robot calendar.
3.  In the form header, select **Robot Calendar**.


</td></tr><tr><td id="d482174e204">

**View a robot calendar from a bot process**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open a bot process to view the robot calendar.
3.  In the form header, select **Show Robot Calendar**.
4.  In the **Select the robot to view the calendar** dialog box, select a robot from the Robot list.
5.  Select **Continue**.


</td></tr></tbody>
</table>4.  To view more bot processes, select the filter icon \(\[Omitted image "filter-rc-rpa.png"\] Alt text: Filter icon.\) and add the appropriate **Process Name** filter and **Life Cycle Stage Status** filter.

5.  To delete a schedule, perform any of the following tasks.

<table id="choicetable_d1k_kk5_1yb"><thead><tr><th align="left" id="d482174e276">

Option

</th><th align="left" id="d482174e279">

Action

</th></tr></thead><tbody><tr><td id="d482174e285">

**Right-click an event**

</td><td>

1.  Right-click an event \(schedule\) and select **Delete schedule**.
2.  In the Confirmation dialog box, select **Delete schedule**.


</td></tr><tr><td id="d482174e309">

**Select the event pop-up window**

</td><td>

Select the delete schedule icon \(\[Omitted image "icon-delete-schedule-rpa.png"\] Alt text: Delete schedule icon.\) on the event pop-up window.

</td></tr></tbody>
</table>    If you are deleting a published bot process, the life cycle change status is changed to **In Maintenance**.


**Parent Topic:**[Using the robot calendar for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/robot-calendar-rpa.md)

**Related topics**  


[Schedule form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-robot-schedule.md)

[Edit a robot schedule in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/edit-robot-schedule.md)

[View current robot events in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/view-robot-calendar.md)

[Using the robot calendar for RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/robot-calendar-rpa.md)

