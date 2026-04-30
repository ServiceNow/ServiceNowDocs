---
title: Scheduling in Workforce Optimization for Field Service
description: Scheduling in Workforce Optimization for Field Service enables you to manage your workforce resources efficiently by planning and managing schedules, staffing, and shifts across your teams all from one location. You can also integrate with on-call scheduling and create shifts and schedule for on-call rotations.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Managing Workforce Optimization for Field Service, Using Field Service Management, Field Service Management]
---

# Scheduling in Workforce Optimization for Field Service

Scheduling in Workforce Optimization for Field Service enables you to manage your workforce resources efficiently by planning and managing schedules, staffing, and shifts across your teams all from one location. You can also integrate with on-call scheduling and create shifts and schedule for on-call rotations.

## Key features

With Scheduling, you can do the following:

-   Add meetings, training, time-off requests, or ad hoc work shifts by using the team calendar.
-   Filter agents in the team calendar based on their location, region, assignment groups, or any field in the agent's record.
-   Create shift and schedule plans for agents.
-   Approve or reject agent time off and shift-swap requests.
-   Track and manage the team's schedule on the team calendar by viewing the planned shifts versus the actual clock-in and clock-out times for the selected day or week.
-   Analyze whether your team members are following the schedules. If you see a potential issue, you can easily alert your team so that they can take immediate action.
-   Use historical adherence reports to analyze and recommend coaching opportunities for your agents.

For more information about key performance indicators and sidebars, see [Exploring indicators with KPI Details](https://www.servicenow.com/docs/access?context=kpi-details-components&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

## Schedule adherence

-   Adherence is a metric to analyze how closely agents follow their schedule in completing the work assignments. Conformance measures the work completed regardless of when it was completed.
-   A high adherence rate indicates that agents are sticking to their schedules and offering field service when expected. A low adherence rate suggests changing the processes or decisions to manage the team efficiently. The numbers are highlighted in red for non-adherent agents.
-   Schedule adherence and conformance calculations are based on the formulas, agents' actual and planned work timings. The following are the default formulas that are used to calculate adherence and conformance for agents. However, your administrator can change the [formulas](https://www.servicenow.com/docs/access?context=setup-scheduling-configurable-wfo-cs&version=xanadu&pubname=xanadu-customer-service-management&section=extension-points-schedule-adherence-configurable-wfo&ft:locale=en-US), as required.

    The following components and formulas are used to calculate adherence and conformance:

    -   The **shift\_planning\_clock-in** and **shift\_planning\_clock-out** scripts generate the agents' clock-in and clock-out events from the login and logout sessions. The business rule **Agent Time Work Event Trigger** generates clock-in and clock-out events whenever there is a change in agent's presence state.
    -   **Schedule Adherence**= \(Minutes worked in shift/Scheduled shift time in minutes + Overtime\)
    -   **Conformance**= \(Minutes worked in shift + Overtime\)/Scheduled shift time in minutes
-   The ideal adherence percentage by default is above 70, and conformance is between 80 to 120. However, your administrator can change the threshold values. For more information, see [Scheduling in Workforce Optimization for Field Service](scheduling-wfo-fsm.md). The agents who do not qualify to the defined threshold values are considered as non-adherent and are highlighted in red.

-   **[Create a work shift plan in Workforce Optimization for Field Service](../task/create-shift-plan-wfo-fsm.md)**  
Schedule shifts for your team so that you can make sure that you are covering all work assignments and breaks. You can also specify the days of the week that you might need to override scheduled shifts.
-   **[Create an on-call shift plan in Workforce Optimization for Field Service](../task/create-oncall-shift-plan-wfo-fsm.md)**  
Schedule shifts for your team so that you can make sure that you are covering all work assignments and breaks. You can also specify the days of the week that you might need to override scheduled shifts.
-   **[Create a schedule plan](../task/create-schedule-plan-wfo-fsm.md)**  
Manage your team's schedule by creating a schedule plan that covers a span of time and includes your team's work shifts. You can also assign agents to shifts based on their skills and availability to ensure you are using your resources efficiently.
-   **[Add schedule breaks to a shift](../task/add-break-shift-wfo-fsm.md)**  
After creating a work shift, you can add schedule breaks to the shift.
-   **[Publish a schedule plan for visibility into team coverage](../task/publish-schedule-plan-wfo-fsm.md)**  
Generate a preview of your schedule plan and publish it so that your agents can see their shifts and schedules ahead of time. You can unpublish a schedule to make changes and then publish it again.
-   **[Track and manage your team's schedule](../task/track-team-schedule-wfo-fsm.md)**  
Create, update, or monitor your team's schedule from one location. You can approve or reject requests for swapping shifts or time off for agents within your assignment group.
-   **[Monitor schedule adherence of your agents](../task/monitor-schedule-adherence.md)**  
Use schedule adherence to evaluate whether your agents are adhering to their assigned schedules. You can look for areas where low-value activity can be eliminated or reduced and further analyze staffing levels throughout the day.
-   **[Analyze adherence and conformance from the time worked summary](../task/analyze-adherence-conformance-wfo-fsm.md)**  
View the time worked summary of your team members to determine whether your teams are adhering to planned schedules. You can also use historical adherence, a reporting view of real-time adherence, to see how well your agents have followed their schedules in the past.
-   **[Add events to the team calendar](../task/add-event-to-calendar-wfo-fsm.md)**  
Create a meeting, training, time-off request, personal, or an ad hoc work event from the team calendar.

**Parent Topic:**[Managing Workforce Optimization for Field Service](using-wfo-fsm.md)

