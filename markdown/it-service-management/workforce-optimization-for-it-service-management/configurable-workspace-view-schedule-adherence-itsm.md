---
title: Monitor schedule adherence of your agents
description: Evaluate whether or not your agents are adhering to their assigned schedules. Look for areas where agent activities that do not offer much value can be reduced or eliminated and fine-tune your staffing levels requirements based on their adherence.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Schedule Adherence in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Monitor schedule adherence of your agents

Evaluate whether or not your agents are adhering to their assigned schedules. Look for areas where agent activities that do not offer much value can be reduced or eliminated and fine-tune your staffing levels requirements based on their adherence.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

-   A high adherence rate indicates that agents are sticking to their schedules and resolving work items as expected. Low adherence rates indicate that you may want to analyze the processes or decisions and tweak them to manage your teams' schedule efficiently. The numbers are highlighted in red for non-adherent agents.
-   Schedule adherence and conformance calculations are based on the formulas to calculate schedule adherence and conformance and also the agents' actual and planned work timings. The following are the default formulas that are used to calculate adherence and conformance for agents. However, your administrator can customize the Schedule adherence extension points to configure the formulas as required.

    Components and formulas used in schedule adherence:

    -   The **Agent Time Work Event Trigger** business rule generates clock-in and clock-out events anytime there's a change in agent's presence state. The **shift\_planning\_clock-in** and **shift\_planning\_clock-out** scripts generate the agents' clock-in and clock-out events from the login and logout sessions.
    -   Formulas:
        -   Schedule adherence is calculated as `(Minutes worked in shift/Scheduled shift time in minutes + Overtime)`.
        -   Conformance is calculated as `(Minutes worked in shift + Overtime)/Scheduled shift time in minutes`.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Schedule icon \(![Schedule icon](../../itsm-manager-workspace/image/schedule-icon.png)\).

3.  Monitor the schedule adherence of your agents.

<table id="choicetable_c54_ns5_hrb"><thead><tr><th align="left" id="d188325e128">

To

</th><th align="left" id="d188325e131">

Do this

</th></tr></thead><tbody><tr><td id="d188325e137">

**View schedule adherence at organization or team level**

</td><td>

Click the **Schedule Adherence** tab.The bar displays the schedule adherence and conformance in percentage for your teams. Click on the bar chart to drill down and view more analytics.

</td></tr><tr><td id="d188325e152">

**Analyze planned vs actual scheduling for your team members**

</td><td>

1.  Click the **Team Calendar** tab.
2.  Select a date on the calendar.
3.  Click on the bar that represents the agent's actual time worked to view the summary.
 **Note:** The clock-in and clock-out timings are the actual work timings of your agents. The events are generated based on the agent's login, logout actions, and presence state. If an agent forgets to clock-out, the system automatically generates the clock-out event after 60 min, by default. However, your administrator can change it the using **Default threshold time for clock-out event generation \(in Minutes\)** .

Example: A clock-in event gets generated when an agent logs in or changes the presence status to **Available**. Similarly, a clock-out event gets generated when an agent logs out of the system or changes the presence status to either **Offline** or **Break**. If an agent fails to clock-out even after 60 min of the shift end time, the system automatically generates the clock-out event.

</td></tr></tbody>
</table>    The image below shows an example of how well the team members are adhering to their work schedules. The bar colors are represented as follows:

    -   Blue—planned work shift
    -   Gray—agent not available
    -   Green—agent is available
    -   Purple—agent clock-in-time
    -   Red—agent clock-out-time
    ![Schedule Adherence](../image/schedule-adherence-itsm.png)


**Parent Topic:**[Schedule Adherence in Workforce Optimization for ITSM](../concept/schedule-adherence-configurable-itsm.md)

