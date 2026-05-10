---
title: Scheduling in Workforce Optimization for Field Service
description: Scheduling in Workforce Optimization for Field Service enables you to manage your workforce resources efficiently by planning and managing schedules, staffing, and shifts across your teams all from one location. You can also integrate with on-call scheduling and create shifts and schedule for on-call rotations.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workforce Optimization, Managing workforce, Use, Field Service Management]
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

For more information about key performance indicators and sidebars, see [Exploring indicators with KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/kpi-details-components.md).

## Schedule adherence

-   Adherence is a metric to analyze how closely agents follow their schedule in completing the work assignments. Conformance measures the work completed regardless of when it was completed.
-   A high adherence rate indicates that agents are sticking to their schedules and offering field service when expected. A low adherence rate suggests changing the processes or decisions to manage the team efficiently. The numbers are highlighted in red for non-adherent agents.
-   Schedule adherence and conformance calculations are based on the formulas, agents' actual and planned work timings. The following are the default formulas that are used to calculate adherence and conformance for agents. However, your administrator can change the [formulas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setup-scheduling-configurable-wfo-cs.md), as required.

    The following components and formulas are used to calculate adherence and conformance:

    -   The **shift\_planning\_clock-in** and **shift\_planning\_clock-out** scripts generate the agents' clock-in and clock-out events from the login and logout sessions. The business rule **Agent Time Work Event Trigger** generates clock-in and clock-out events whenever there is a change in agent's presence state.
    -   **Schedule Adherence**= \(Minutes worked in shift/Scheduled shift time in minutes + Overtime\)
    -   **Conformance**= \(Minutes worked in shift + Overtime\)/Scheduled shift time in minutes
-   The ideal adherence percentage by default is above 70, and conformance is between 80 to 120. However, your administrator can change the threshold values. For more information, see [Scheduling in Workforce Optimization for Field Service](scheduling-wfo-fsm.md). The agents who do not qualify to the defined threshold values are considered as non-adherent and are highlighted in red.

