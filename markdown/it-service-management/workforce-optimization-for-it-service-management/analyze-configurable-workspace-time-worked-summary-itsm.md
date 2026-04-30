---
title: Use time-worked summary to analyze agent schedule adherence and conformance
description: Analyze if your teams are adhering to planned schedules. Use historical adherence to see how well your agents have followed their schedules in the past.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Schedule Adherence in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Use time-worked summary to analyze agent schedule adherence and conformance

Analyze if your teams are adhering to planned schedules. Use historical adherence to see how well your agents have followed their schedules in the past.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

**Note:**

-   Historical adherence provides a reports of real-time adherence.
-   Adherence and conformance calculations are based on your agents' actual and planned work schedules. Your administrator can modify the schedule adherence and conformance configurations. For more information, see [Schedule Adherence reference](../reference/configure-adherence-parameters-wfo-itsm.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Lists icon \(![Lists icon](../../itsm-manager-workspace/image/lists_icon.png)\)

3.  In the **Schedule Adherence** category, do any of the following:

    -   To analyze your agents' time-worked summary, select **Time Worked Summary**.
    -   To analyze your agents' time attendance, select **Time Attendance**.
    **Note:** The **Available Non Planned time** captures the time the agent was available and clocked in outside of the agent's scheduled work events. For example, if an agent is scheduled to attend a training from 1 pm to 2 pm, but forgets to clock out that attendance, then that time is considered as the clocked-in time. Therefore, the training time from 1 pm to 2 pm will be captured as the available non-planned time.


## Example

To understand the computations of the fields in a time worked summary, let's consider Fatima Alonzo's work day:

-   Shift time begins at 8 a.m. and goes to 4 p.m. = 8 hours
-   Planned time = 8 hours = 480 minutes​
-   Clocks in 8 a.m. and clocks out at 12 p.m. for a break. Back from the break, clocks in at 12:30 p.m. and clocks out at 4 p.m.
-   Minutes worked in shift = 480 - 30 = 450 minutes​
-   Schedule adherence= \(minutes worked in shift/scheduled shift time in minutes + overtime\) = 450/\(480+65\) = 82.57%
-   Conformance= \(minutes worked in shift + overtime\)/scheduled shift time in minutes = \(450 + 65\) / 480 = 107.29 percent​.

**Note:** Fatima Alonzo is adherent because the schedule adherence and conformance are within the threshold. To see which agents are non-adherent, look for the numbers that are highlighted in red.

**Parent Topic:**[Schedule Adherence in Workforce Optimization for ITSM](../concept/schedule-adherence-configurable-itsm.md)

