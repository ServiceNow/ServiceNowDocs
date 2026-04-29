---
title: Agent auto assignment using rating-based criteria
description: Rating-based methods, such as location, skills, and time zones, help to auto assign agents based on configuration settings and optional properties. The calculated ratings are used to determine the best agent to perform the task.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent auto assignment, Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Agent auto assignment using rating-based criteria

Rating-based methods, such as location, skills, and time zones, help to auto assign agents based on configuration settings and optional properties. The calculated ratings are used to determine the best agent to perform the task.

Any combination of rating-based methods can be enabled in configuration screen of the application.

When a task is created, a rating for each type of enabled selection criteria is calculated for each available agent. The agent whose average rating is highest is considered for auto-assignment. The settings for the auto-assignment weighting properties, found in **\[SM application\]** &gt; **Administration** &gt; **Properties**, are included in the rating calculations.

These values help you prioritize which auto-assignment selection criteria is more important to your organization. The priority values should be \[1, 10\] and they are factored between 1 and 0. That is, 10 is a factor of 1, 5 is a factor of 0.5, and so on. For an example of how the weighting properties affect agent ratings, see [Agent auto assignment using multiple selection criteria](c_AgAtAssgmtMlt.md).

-   **[Agent auto assignment using location](c_AgentAutoAssignmentUsingLocation.md)**  
Agents can be auto assigned based on the location defined in their user record and the location of the tasks.
-   **[Agent auto assignment using skills](c_AgentAutoAssignmentUsingSkills.md)**  
Agents can be auto assigned based on the skills of an agent, and the skills required to perform the task. Assign skills to an agent user records using **Skills** &gt; **Users**.
-   **[Agent auto assignment using time zones](c_AgAtAssgnZones.md)**  
Agents can be auto assigned based on the time zone defined in their user records and the time zone of the tasks.

**Parent Topic:**[Agent auto assignment](../../service-management-core/concept/c_AgentAutoAssignment.md)

