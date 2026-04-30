---
title: Monitor schedule adherence of your agents
description: Use schedule adherence to evaluate whether your agents are adhering to their assigned schedules. You can look for areas where low-value activity can be eliminated or reduced and further analyze staffing levels throughout the day.
locale: en-US
release: zurich
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Scheduling, Workforce Optimization, Workforce, Use, Field Service Management]
---

# Monitor schedule adherence of your agents

Use schedule adherence to evaluate whether your agents are adhering to their assigned schedules. You can look for areas where low-value activity can be eliminated or reduced and further analyze staffing levels throughout the day.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

For information on schedule adherence, see the "Schedule adherence" section in [Scheduling in Workforce Optimization for Field Service](../concept/scheduling-wfo-fsm.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon.](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\).

3.  Monitor the schedule adherence of your agents.

<table id="table_ttg_rsh_wkb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

View schedule adherence at the organization or team level

</td><td>

1.  Click the **Schedule Adherence** tab.

The bar chart appears with the schedule adherence percentage and conformance percentage of your teams.

2.  View the graph and drill down further to view the analytics of your team members by clicking on the bar.


</td></tr><tr><td>

Analyze planned vs. actual scheduling for your team members

</td><td>

1.  Click the **Team Calendar** tab.
2.  Select the date.
3.  View the **Time Worked** summary by clicking on the bar representing the agent's actual time worked.
 **Note:** The clock-in and clock-out timings are the actual work timings of your agents. The events are generated based on the agent's login, logout actions, and presence state. If an agent forgets to clock out, the system automatically generates the clock-out event after 60 minutes by default. However, your administrator can change it using **Default threshold time for clock-out event generation \(in Minutes\)** system property.

Example: A clock-in event gets generated when an agent logs in or changes the presence status to **Available**. Similarly, a clock-out event gets generated when an agent logs out of the system or changes the presence status to either Offline or Break. If an agent fails to clock-out past 60 minutes of the shift end time, the system automatically generates the clock-out event.

</td></tr></tbody>
</table>    The following team calendar snapshot illustrates how to measure how well your team members are adhering to their work schedules. The blue bar indicates the planned work shift time and next to that is the actual worked time. The default representations are purple for clock-in time, green for agent's available duration, red for the clock-out time, and grey for agent's non-available time.

    ![Schedule view in the Team Calendar displaying agent availability.](../../workforce-optimization-for-customer-service-configurable/image/schedule-adherence-cs.png)


