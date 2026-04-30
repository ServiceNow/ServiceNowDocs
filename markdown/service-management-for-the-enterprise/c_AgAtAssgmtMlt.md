---
title: Agent auto assignment using multiple selection criteria
description: At its simplest, auto assignment involves identifying a set of selection criteria and automatically assigning the task to the agent who most closely meets the criteria. You can, however, select multiple sets of criteria, including both rating-based and time-based criteria.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Agent auto assignment, Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Agent auto assignment using multiple selection criteria

At its simplest, auto assignment involves identifying a set of selection criteria and automatically assigning the task to the agent who most closely meets the criteria. You can, however, select multiple sets of criteria, including both rating-based and time-based criteria.

When a task is qualified or marked as **Ready for Work**, the following evaluations are performed:

1.  The ratings of an agent are calculated. If the **Auto-selection of agents will consider agent or task schedules** configuration option is disabled for the application, the ratings of an agent are used exclusively for auto-assigning an agent.

    For more information on how the ratings are calculated, see:

    -   [Agent auto assignment using location](c_AgentAutoAssignmentUsingLocation.md)
    -   [Agent auto assignment using skills](c_AgentAutoAssignmentUsingSkills.md)
    -   [Agent auto assignment using time zones](c_AgAtAssgnZones.md)
2.  If the **Auto-selection of agents will consider agent or task schedules** configuration option is enabled, the schedules of the agents whose ratings are acceptable for auto-assignment are compared to the schedule for the task, and the agent with the best match is auto-assigned. For more information on time-based methods for auto-assigning agents, see:
    -   [Agent auto assignment using schedules](c_AgAtAssgnSchd.md)
    -   [Agent auto assignment using priority assignment](c_AgentAutoAssignUsePrioAssign.md)

Auto assignment is based on the following calculation:

`(Criteria_1 rating x Criteria_1 weight) + (Criteria_2 rating x Criteria_2 weight) + (Criteria_3 rating x Criteria_3 weight) / Number of criteria types used`

Where:

-   Number of criteria types used = 1, 2, or 3 depending on the location, skill, and time zone settings used.

This example calculates agent auto-assignment based on location and skills. The example is based on the following assumptions.

-   The **Auto-selection of agents will consider location of agents** configuration option is enabled for the application.
-   The **Auto-selection of agents requires them to have some of the required skills for the task** configuration option is enabled for the application.
-   The **Skills Weight** property is set to 10 for the application.
-   The **Location Weight** property is set to 5 for the application.
-   Agents A and B are available to perform a task, and the task requires four specific skills.
-   The location of Agent A is 5 miles from the site of the task. Agent A possesses three of the four required skills.
-   The location of Agent B is one-quarter mile from the site. Agent B possesses two of the required skills.

Auto assignment for the agents uses this calculation:

`[(Location rating x Location weight) + (Skills rating x Skills weight)]/ 2`

-   The auto assignment calculation for Agent A is: `[(0.7 x 0.5) + (0.75 x 1)]/ 2 = 0.55`
-   The auto assignment calculation for Agent B is: `[(0.9 x 0.5) + (0.5 x 1)]/ 2 = 0.475`

In this example, Agent A is auto assigned the task.

**Parent Topic:**[Agent auto assignment](../../service-management-core/concept/c_AgentAutoAssignment.md)

