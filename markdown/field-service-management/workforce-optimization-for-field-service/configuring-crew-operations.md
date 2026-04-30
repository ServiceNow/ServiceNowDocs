---
title: Configuring Field Service Crew Operations
description: Create, modify, and enable crews and their requirements to complete work order tasks that require a crew of agents.
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Set up workforce, Configure, Field Service Management]
---

# Configuring Field Service Crew Operations

Create, modify, and enable crews and their requirements to complete work order tasks that require a crew of agents.

Once an administrator identifies the type of work that requires a crew, the requirement can be designated from the work type form and the work order template. Whenever a work order is created using the template or the work type is selected in the task that requires a crew, the **Needs Crew** field is automatically enabled. This field enables dispatchers to schedule and dispatch a crew for work order tasks created using the work order templates. For more information about enabling crew requirements from work order templates, see [Create a work order template](../../it-services/task/t_CreateAWorkOrderTemplate.md).

An administrator or dispatcher can select the **Needs Crew** option in the work order task form if a crew is required to complete a work order task. This selection can be done when the task is in the Draft, Assigned, or Pending dispatch state if a crew a crew is required to complete a work order task.

Activate the Field Service Crew Operations plugin, to add the **Needs Crew** option to the work order task form, work type form, and the work order templates.

## Dynamic Scheduling for crew operations

Auto-assignment of tasks in dynamic scheduling is enabled for work order tasks that require a crew. New criteria are defined in the dynamic scheduling configurations to include work order tasks with the crew requirement enabled. These criteria are set to perform the following actions on work order tasks that require a crew:

-   The Task Filters related list includes:

    -   **Crew Appointment Tasks**

        This filter is specific to the task that requires a crew and has an appointment window

    -   **Crew Assignment: Pending Dispatch Work Order Tasks**

        This filter is specific to the task that requires crew and is in the Pending Dispatch state.

    -   **Agents for crew tasks**

        This filter is specific to the task that requires the crew to suggest the eligible agents. The criterion selected in the filter determines what agents are recommended for the crew task.

    Task filters evaluate work order tasks and schedule them automatically when they require a crew.

-   A constraint helps prevent unassigning the task when it requires a crew.
-   The auto-assigment feature helps prevent assigning tasks to the agents who are part of a crew at the same time for which the task is set to be scheduled.

## Configuration overview

The steps for configuring Field Service Crew Operations are:

1.  [Activate Field Service Crew Operations](../task/activate-fsm-crew-scheduling.md)

    You can activate the Field Service Crew Operations plugin \(com.snc.fsm\_crew\_scheduling\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.

2.  [Create crews in Field Service Management](../task/create-crews-fsm.md)

    Create crews to assign work order tasks to a predefined group of agents.

3.  [Add skills to a crew](../task/add-skill-to-crew.md)

    Add skills to a crew so you understand what crews are correct for work order tasks that require unique skills.

4.  [Add an equipment skill](../task/mark-equipment-skill.md)

    Designate skills as equipment-related skills so that when a task that requires equipment skills is assigned, the correct equipment skills can be selected.

5.  [Create ad hoc task-specific crews](../task/create-adhoc-crew.md)

    Create an ad-hoc task-specific crew for a task if existing crews aren’t available to work on the task or the task requires specific skills.

6.  [Update the crew requirement of a work order task](../task/create-crew-size.md)

    Add or update the number of agents to perform a particular type of work for a work order task.

7.  [Add Field Service crew members](../task/add-crew-members.md)

    Add agents to a Field Service crew as needed.

8.  [Configure the leader role to identify crew leaders](../task/add-skill-leader-role.md)

    Identify a crew leader if one isn’t specified by the dispatcher by adding skills to the leader role.


**Related topics**  


[Using Field Service Crew operations](Using-crew-operations-fsm.md)

[Assign work order tasks to crews](../task/assign-wot-crew-operations.md)

[Using Dispatcher Workspace for crew operations](using-disp-wrkspc-crew-operations.md)

[Managing crew tasks using the ServiceNow Agent application](executing-crew-tasks.md)

