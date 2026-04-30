---
title: Configuring Field Service Crew Operations
description: Create, modify, and enable crews and their requirements to complete work order tasks that require a crew of agents.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Configuring Field Service Crew Operations

Create, modify, and enable crews and their requirements to complete work order tasks that require a crew of agents.

Once administrators identify the type of work that requires a crew, they can enable the crew requirement for the task directly from the work type form and the work order template. Whenever a work order is created using the template or the work type is selected in the task that requires a crew, the **Needs Crew** field is automatically enabled. This field enables dispatchers to schedule and dispatch a crew for work order tasks created using the work order templates. For more information about enabling the crew requirement directly from the work order template, see [Create a work order template](../../it-services/task/t_CreateAWorkOrderTemplate.md).

If a crew requirement is not mentioned while creating a work order task, an administrator or dispatcher can select the **Needs Crew** option in the work order task form when the task is in the Draft, Assigned, or Pending dispatch state.

Activate the Field Service Crew Operations plugin, to add the **Needs Crew** option to the work order task form, work type form, and the work order templates.

## Dynamic Scheduling for crew operations

Auto-assignment of tasks in dynamic scheduling is enabled for work order tasks that require a crew. New criteria are defined in the dynamic scheduling configurations to include work order tasks with the crew requirement enabled. These criteria are set to perform the following actions on work order tasks that require a crew:

-   The Task Filters related list includes:

    -   **Crew Appointment Tasks**

        This filter is specific to the task that requires crew and has an appointment window

    -   **Crew Assignment: Pending Dispatch Work Order Tasks**

        This filter is specific to the task that requires crew and is in the Pending Dispatch state.

    -   **Agents for crew tasks**

        This filter is specific to the task that requires crew to recommend the eligible agents. The agents is recommended to the crew task based on the selection criteria defined in the filter.

    Task filters evaluate work order tasks and schedule them automatically if they require a crew.

-   A constraint prevents unassigning the task if it requires a crew.
-   The auto-assigment feature prevents assigning tasks to the agents who are part of a crew at the same time for which the task is set to be scheduled.

## Configuration overview

The steps for configuring Field Service Crew Operations are:

1.  [Activate Field Service Crew Operations](../task/activate-fsm-crew-scheduling.md)

    You can activate the Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.

2.  [Create crews in Field Service Management](../task/create-crews-fsm.md)

    Create crews to assign work order tasks to a predefined group of agents.

3.  [Add skills to a crew](../task/add-skill-to-crew.md)

    Add skills to a crew so you know what crews are right for work order tasks that require unique skills.

4.  [Add an equipment skill](../task/mark-equipment-skill.md)

    Designate skills as equipment-related skills so that when a task that requires equipment skills is assigned, the correct equipment skills can be selected.

5.  [Create ad hoc task-specific crews](../task/create-adhoc-crew.md)

    Create an ad hoc task-specific crew for a task if existing crews are not available to work on the task or the task requires specific skills.

6.  [Update the crew requirement of a work order task](../task/create-crew-size.md)

    Add or update the number of agents to perform a particular type of work for a work order task.

7.  [Add Field Service crew members](../task/add-crew-members.md)

    Add agents to a Field Service crew as needed.

8.  [Configure the leader role to identify crew leaders](../task/add-skill-leader-role.md)

    Identify a crew leader if one isn’t specified by the dispatcher by adding skills to the leader role.


**Related topics**  


[Using Field Service Crew Operations](Using-crew-operations-fsm.md)

[Assign work order tasks to crews](../task/assign-wot-crew-operations.md)

[Using Dispatcher Workspace for crew operations](using-disp-wrkspc-crew-operations.md)

[Managing crew tasks using the Now Mobile Agent application](executing-crew-tasks.md)

