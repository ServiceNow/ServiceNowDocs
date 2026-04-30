---
title: Scheduling conflicts between project tasks
description: Scheduling conflict helps you to identify project tasks that are not honoring dependencies. A scheduling conflict occurs when one project task prevents other task from starting on the specified date because of dependencies or constraint types.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project tasks, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Scheduling conflicts between project tasks

Scheduling conflict helps you to identify project tasks that are not honoring dependencies. A scheduling conflict occurs when one project task prevents other task from starting on the specified date because of dependencies or constraint types.

A scheduling conflict occurs when any action such as applying a dependency, changing constraint type, or constraint date causes the task start date to violate the project's constraint date.

When a scheduling conflict occurs, the system warns you about the conflict. You can choose to cancel the action that is causing the conflict or continue with the conflict. If you choose to continue with the conflict, the constraint date is given highest precedence and dates are recalculated. The start date is moved till allowed by the task constraint date, but dependency is not honored.

For example, consider the following scenario:

For a project with project task's **Constraint date** set as 20 January, there are two tasks:

-   T1 with constraint type set to As soon as possible and start date of 20 January.
-   T2 with constraint type set to Start no later than and start date of 20 January.

If you add an FS dependency between tasks T1 and T2, the task T2 should start on 21 January, but due to Start no later than constraint, task T2 cannot start on 21 January. This inability of starting task T2 on the specified date is an example of conflict.

In this example, if you choose to proceed with the conflict, the start date of task T2 is moved to 20 January which is the constraint date.

Scheduling conflict between tasks is shown for tasks with **Start no later than** and **Start on specific date** time constraints.

If you want the task to honor the dependency and adjust the start accordingly, change the constraint type of the task to **Start ASAP**.

When a scheduling conflict is identified, you can identify such tasks in the planning console.

-   The client-side planning console displays a pop-up message with an option to proceed with the conflict or cancel the action. If you proceed with the conflict, the constraint type is applied or date is changed appropriately to the next feasible date.
-   The calendar icon \(![Calendar icon](../image/calendar-icon.png)\) on the client side planning console changes to red \(![Conflict icon](../image/pc-task-dep-icon.png)\) to indicate the conflict.
-   The calendar icon on the server side planning console changes to red \(![Conflict icon](../image/pc-task-dep-icon.png)\) to indicate the conflict.

**Parent Topic:**[Project tasks](c_ProjectTasks.md)

**Related topics**  


[Project task relationships and dependencies](c_ProjectTaskRelationDepend.md)

[Create a project task](../task/t_CreateAProjectTask.md)

[Create a milestone](../task/t_CreateMilestones.md)

[Change requests and project tasks](c_ChangeRequestsAndProjectTasks.md)

[Project task checklists](c_project-task-checklists.md)

[Accept or reject project task notifications](../task/accept-project-task-notifications.md)

[Task resources](c_TaskResources.md)

