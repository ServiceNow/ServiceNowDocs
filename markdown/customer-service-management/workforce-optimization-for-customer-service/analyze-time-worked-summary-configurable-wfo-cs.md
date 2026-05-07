---
title: Analyze adherence and conformance from the time worked summary
description: View the time worked summary of your team members to determine if your teams are adhering to the planned schedules. You can also use historical adherence, which is a reporting view of real-time adherence, to see how well your agents have followed their schedules in the past.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Schedule, Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Analyze adherence and conformance from the time worked summary

View the time worked summary of your team members to determine if your teams are adhering to the planned schedules. You can also use historical adherence, which is a reporting view of real-time adherence, to see how well your agents have followed their schedules in the past.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

Adherence and conformance calculations are based on the [defined configuration](../concept/setup-scheduling-configurable-wfo-cs.md#) and your agents' actual and planned work schedules.

**Note:** Your administrator can disable schedule adherence or change the configuration for adherence and conformance. For more information, see [Configure properties for schedule adherence and conformance](../concept/setup-scheduling-configurable-wfo-cs.md#).

For information about schedule adherence, see the "Schedule adherence" section of [Scheduling in Workforce Optimization for Field Service](https://www.servicenow.com/docs/access?context=scheduling-wfo-fsm&version=australia&pubname=australia-field-service-management&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Manager Workspace**.

2.  Drill down to view the time attendance and time worked summary of your agents.

<table id="table_ttg_rsh_wkb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Analyze time worked summary of your team

</td><td>

1.  Click the Lists icon \(![Lists icon.](../image/list-new.png)\).
2.  Under Schedule Adherence, click **Time Worked Summary**.

**Note:** The **Available Non Planned** time captures the time the agent was available and clocked in outside of the agent's scheduled work events. For example, if an agent is scheduled to attend a training from 13:00 to 14:00 but forgets to clock out that attendance, that time is considered the clocked-in time. The training time from 13:00 to 14:00 is captured as the available non-planned time.

</td></tr><tr><td>

View your agents' time attendance

</td><td>

1.  Click the Lists icon \(![Lists icon.](../image/list-new.png)\).
2.  Under Schedule Adherence, click **Time Attendance**.


</td></tr></tbody>
</table>    The following schedule adherence example shows how to measure how well your team is adhering and conforming with their work schedules.

    ![Complete summary of the attendance, schedule adherence, and conformance of all the agents in the team.](../image/time_worked_summary_new.png)


## Example

To understand the computations of the fields in a time worked summary, consider Fatima Alonzo's work day:

-   Shift time begins at 8 a.m. and goes to 4 p.m. = 8 hours
-   Planned time = 8 hours = 480 minutes​
-   Clocks in 8 a.m. and clocks out at 12 p.m. for a break. Back from the break, clocks in at 12:30 p.m. and clocks out at 4 p.m.
-   Minutes worked in shift = 480 - 30 = 450 minutes​
-   Schedule adherence= \(minutes worked in shift/scheduled shift time in minutes + overtime\) = 450/\(480+65\) = 82.57%
-   Conformance= \(minutes worked in shift + overtime\)/scheduled shift time in minutes = \(450 + 65\) / 480 = 107.29 percent​.

**Note:** Fatima Alonzo is adherent because the schedule adherence and conformance are within the threshold. To see which agents are non-adherent, look for the numbers highlighted in red.

**Parent Topic:**[Schedule in Workforce Optimization for Customer Service](../concept/scheduling-configurable-wfo-cs.md)

