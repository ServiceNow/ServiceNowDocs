---
title: Schedule Adherence in Workforce Optimization for ITSM
description: Analyze how closely your agents adhere to their scheduled activities. You can also analyze whether they complete the total time they were scheduled to work. Use these metrics to align your staffing needs better and forecast the demand for agents more effectively.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Schedule Adherence in Workforce Optimization for ITSM

Analyze how closely your agents adhere to their scheduled activities. You can also analyze whether they complete the total time they were scheduled to work. Use these metrics to align your staffing needs better and forecast the demand for agents more effectively.

Adherence measures how closely agents follow their schedule to complete their assigned work. Conformance measures the work completed regardless of when it was completed.

Use Schedule Adherence to:

-   Gain insights into how agent resources were historically used and plan your staffing needs based on that data.
-   Measure whether the effort spent on [forecasting agent demand](explore-demand-forecast-configurable-wfo-itsm.md) and scheduling team members is used in an optimal manner.
-   Discover coaching opportunities for your agents when you find gaps in their adherence. For more information, see [Coaching](explore-coaching-configurable-workforce-optimization-itsm.md).

As a manager, you can do the following actions:

-   Gain insights into whether your team is complying with published schedules.
-   Increase your team's performance by setting expected adherence targets.
-   View the time attendance of your agents by looking at such details as clock-in and clock-out times.
-   Analyze the historical time attendance of your team members.
-   View planned versus actual historical data for your team and individual agents.
-   Modify the clock-in and clock-out times of your agents.

As an administrator, you can set the threshold percentages and change the formulas for calculating schedule adherence and conformance.

As an agent, you can clock-in to and clock-out of your work shift. For more information, see [Service Operations Workspace - Scheduling](../../service-operations-workspace/concept/itsm-sow-workspace-scheduling.md).

Here's a typical schedule adherence and conformance workflow:

1.  The administrator sets the **Agent Time Work Event Trigger** business rule as active to record the clock-in and clock-out times of Workforce Optimization for ITSM agents.
2.  An agent works for the ITSM team and reports to a manager. Let's assume this scenario is a typical work day​:
    1.  The agent logs in to ITSM Agent Workspace ​.
    2.  The agent changes the presence status to **Available** and starts work. The clock-in event gets generated.
    3.  The agent changes the presence status to **Break** and goes for lunch. The clock-out event gets generated.
    4.  When the agent comes back from lunch and answers ​a phone call, the presence state becomes **Busy** and the clock-in event gets generated.
    5.  The agent then logs out from CSM ​Agent Workspace or changes the presence status to **Offline**​. The clock-out event gets generated.
    6.  At the end-of-the-day, the agent's time worked summary is generated with key performance indicators \(KPIs\), such as Start Time, End Time, Planned Work, Time Not Worked, Available Non Planned Time, Time Worked, and Adherence%, Conformance %​.
3.  The agent's manager logs in to Manager Workspace to view the agent's time worked in the **Team Calendar**. The manager can also view the agent's actual time worked and working pattern for all historical days. If required, the manager can coach the agent to a desired performance that fits in with the team culture.

-   **[Monitor schedule adherence of your agents](../task/configurable-workspace-view-schedule-adherence-itsm.md)**  
Evaluate whether or not your agents are adhering to their assigned schedules. Look for areas where agent activities that do not offer much value can be reduced or eliminated and fine-tune your staffing levels requirements based on their adherence.
-   **[Use time-worked summary to analyze agent schedule adherence and conformance](../task/analyze-configurable-workspace-time-worked-summary-itsm.md)**  
Analyze if your teams are adhering to planned schedules. Use historical adherence to see how well your agents have followed their schedules in the past.
-   **[Schedule adherence extension points in Workforce Optimization for ITSM](../reference/extension-points-configurable-schedule-adherence-itsm.md)**  
Use the schedule adherence extension points to call custom scripts for agent schedule adherence and conformance.
-   **[Configure properties for schedule adherence and conformance](../reference/configure-adherence-parameters-wfo-itsm.md)**  
Configure schedule adherence properties to calculate the adherence and conformance of your agents so that you can improve the operational efficiency of your organization.

**Parent Topic:**[Scheduling in Workforce Optimization for ITSM](explore-schedule-configurable-wfo-itsm.md)

