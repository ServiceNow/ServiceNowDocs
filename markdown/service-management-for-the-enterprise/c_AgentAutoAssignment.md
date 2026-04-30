---
title: Agent auto assignment
description: When auto assignment is enabled and a task is qualified or marked as Ready for Work, an appropriate agent is automatically assigned to the task and it is moved to the Assigned state. If the task cannot be auto-assigned, a user with the dispatcher role must adjust the values in the request or task form and then save the record.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Agent auto assignment

When auto assignment is enabled and a task is qualified or marked as **Ready for Work**, an appropriate agent is automatically assigned to the task and it is moved to the **Assigned** state. If the task cannot be auto-assigned, a user with the dispatcher role must adjust the values in the request or task form and then save the record.

The Auto-Assignment feature can be enabled for requests or tasks, depending on the configuration settings of Service Management \(SM\) application:

-   If the Requests are assigned via auto-assignment option is enabled, requests are automatically assigned.
-   If the Tasks are assigned via auto-assignment option is enabled, the tasks in a request are automatically assigned.

-   **[Agent auto assignment using rating-based criteria](../../planning-and-policy/concept/c_AgentAutoAssignUseRatBaseCrit.md)**  
Rating-based methods, such as location, skills, and time zones, help to auto assign agents based on configuration settings and optional properties. The calculated ratings are used to determine the best agent to perform the task.
-   **[Agent auto assignment using time-based criteria](../../planning-and-policy/concept/c_AgAtAssgnTime.md)**  
Time-based methods, such as schedules and priority assignment, help you auto assign agents based on configuration settings and optional properties. The calculated ratings are used to determine the best agent to perform the task.
-   **[Agent auto assignment using multiple selection criteria](../../planning-and-policy/concept/c_AgAtAssgmtMlt.md)**  
At its simplest, auto assignment involves identifying a set of selection criteria and automatically assigning the task to the agent who most closely meets the criteria. You can, however, select multiple sets of criteria, including both rating-based and time-based criteria.

**Parent Topic:**[Agent assignment methods](c_AgentAssignment.md)

