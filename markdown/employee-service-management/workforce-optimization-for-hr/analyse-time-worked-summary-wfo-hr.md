---
title: Analyze adherence and conformance
description: View the time worked summary of your team members to determine if your teams are adhering to the planned schedules. You can also use historical adherence, which is a reporting view of real-time adherence, to see how well your agents have followed their schedules in the past.
locale: en-US
release: xanadu
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Scheduling in Workforce Optimization for HR, Using Workforce Optimization for HR, Workforce Optimization for HR Overview, HR Service Delivery, Employee Service Management]
---

# Analyze adherence and conformance

View the time worked summary of your team members to determine if your teams are adhering to the planned schedules. You can also use historical adherence, which is a reporting view of real-time adherence, to see how well your agents have followed their schedules in the past.

## Before you begin

s

Role required: sn\_shift\_planning.admin

## About this task

Adherence and conformance calculations are based on the [defined configuration](../concept/configure-wfo-hr.md#) and your agents' actual and planned work schedules.

**Note:** Your administrator can disable schedule adherence or change the configuration for adherence and conformance. For more information, see [Configure schedule adherence properties](../concept/configure-wfo-hr.md#).

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

1.  Click the Lists \(![Lists icon.](../../workforce-optimization-for-customer-service-configurable/image/list-new.png)\) icon.
2.  Under Schedule Adherence, click **Time Worked Summary**.

**Note:** The **Available Non Planned** time captures the time the agent was available and clocked in outside of the agent's scheduled work events. For example, if an agent is scheduled to attend a training from 13:00 to 14:00, but forgets to clock out that attendance, then that time is considered as the clocked-in time. Therefore, the training time from 13:00 to 14:00 will be captured as the available non-planned time.

</td></tr><tr><td>

View your agents' time attendance

</td><td>

1.  Click the Lists \(![Lists icon.](../../workforce-optimization-for-customer-service-configurable/image/list-new.png)\) icon.
2.  Under Schedule Adherence, click **Time Attendance**.


</td></tr></tbody>
</table>
## Example

To understand the computations of the fields in a time worked summary, let's consider Fatima Alonzo's work day:

-   Shift time begins at 8 a.m. and goes to 5 p.m. = 8 hours
-   Planned time = 8 hours = 480 minutes​
-   Clocks in 8 a.m. and clocks out at 12 p.m. for a break. Back from the break, clocks in at 12:30 p.m. and clocks out at 5:05 p.m.
-   Minutes worked in shift = 480 - 30 = 450 minutes​
-   Schedule adherence= \(minutes worked in shift/scheduled shift time in minutes + overtime\) = 450/\(480+65\) = 82.57%
-   Conformance= \(minutes worked in shift + overtime\)/scheduled shift time in minutes = \(450 + 65\) / 480 = 107.29 percent​.

**Note:** Fatima Alonzo is adherent because the schedule adherence and conformance are within the threshold. To see which agents are non-adherent, look for the numbers that are highlighted in red.

