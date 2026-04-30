---
title: Monitor schedule adherence
description: Use schedule adherence to evaluate whether or not your agents are adhering to their assigned schedules. You can look for areas where low-value activity can be eliminated or reduced and further analyze staffing levels throughout the day.
locale: en-US
release: xanadu
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Scheduling in Workforce Optimization for HR, Using Workforce Optimization for HR, Workforce Optimization for HR Overview, HR Service Delivery, Employee Service Management]
---

# Monitor schedule adherence

Use schedule adherence to evaluate whether or not your agents are adhering to their assigned schedules. You can look for areas where low-value activity can be eliminated or reduced and further analyze staffing levels throughout the day.

## Before you begin

Role required: sn\_hr\_wfo.admin

## About this task

-   Adherence is a metric to analyze how closely agents follow their schedule in completing the work assignments. Conformance measures the work completed, regardless of when it was completed.
-   A high adherence rate indicates that agents are sticking to their schedules and offering customer service when expected. Low adherence suggests changing the processes or decisions to manage the team efficiently. The numbers are highlighted in red for non-adherent agents.
-   Schedule adherence and conformance calculations are based on the formulas, agents' actual and planned work timings. The following are the default formulas that are used to calculate adherence and conformance for agents. However, your administrator can change the [formulas](../concept/configure-wfo-hr.md#), as required. The following components and formulas are used to calculate adherence and conformance:
    -   The **shift\_planning\_clock-in** and **shift\_planning\_clock-out** scripts generate the agents' clock-in and clock-out events from the login and logout sessions. The business rule **Agent Time Work Event Trigger** generates clock-in and clock-out events whenever there is a change in agent's presence state.
    -   **Schedule Adherence**= \(Minutes worked in shift/Scheduled shift time in minutes + Overtime\)
    -   **Conformance**= \(Minutes worked in shift + Overtime\)/Scheduled shift time in minutes
-   The ideal adherence percentage by default is above 70, and conformance is between 80–120. However, your administrator can change the threshold values. The agents who do not qualify to the defined threshold values are considered as non-adherent and are highlighted in red.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon](../../workforce-optimization-for-customer-service-configurable/image/schedule-new.png)\).

3.  Monitor the schedule adherence of your agents.

<table id="table_ttg_rsh_wkb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

View schedule adherence at organization or team level

</td><td>

1.  Click the **Schedule Adherence** tab. The bar chart appears with the schedule adherence percentage and conformance percentage of your teams.
2.  Click the bar to view the graph and drill down further to view the analytics of your team members.


</td></tr><tr><td>

Analyze planned vs actual scheduling for your team members

</td><td>

1.  Click the **Team Calendar** tab.
2.  Select the date.
3.  Click the bar representing the agent's actual time worked of an agent to view the **Time Worked** summary.
 **Note:** The clock-in and clock-out timings are the actual work timings of your agents. The events are generated based on the agent's login, logout actions, and presence state. If an agent forgets to clock-out, the system automatically generates the clock-out event after 60 min, by default. However, your administrator can change it using **Default threshold time for clock-out event generation \(in Minutes\)**.

Example: A clock-in event gets generated when an agent logs in or changes the presence status to **Available**. Similarly, a clock-out event gets generated when an agent logs out of the system or changes the presence status to either **Offline** or **Break**. If an agent fails to clock-out even after 60 min of the shift end time, the system automatically generates the clock-out event.

</td></tr></tbody>
</table>
