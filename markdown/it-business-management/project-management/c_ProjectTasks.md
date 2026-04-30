---
title: Project tasks
description: Project tasks are the units of work that make up a project.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project tasks

Project tasks are the units of work that make up a project.

The size and number of tasks that comprise a project depends on the level of detail you want. For example:

-   Part of a task requires a specific skill.
-   Other activities in the task do not require the specific skill.

Break down that task further.

## Bottom-up Tasking

Bottom-up \(tactical\) tasking means that you plan small, individual units of work that are required, then build a project up to include larger phases. Take this approach when you know what individual tasks are required to be accomplished and you are more flexible about overall project duration and estimated cost. Use this approach to see how much a project costs and how long it takes if you include every task. Project management supports tactical tasking by using rollup calculations on several project fields, such as project duration, so that the project adjusts to the tasks it contains. It is the recommended approach for the Project Management application.

## Top-down Tasking

Top-down \(strategic\) tasking means that you plan high-level tasks first, then break down the work into smaller units. Take this approach when you want to build a project with fixed or inflexible time and budgetary constraints and well-defined phases. Establish well-defined milestones and dependencies between tasks that you consider from the beginning. Gradually add smaller tasks to the project later. This approach avoids including all possible tasks in a project and stays flexible with what tasks are included.

**Note:** When you use this method, the Project Management application still rolls up several values, such as task duration. Creating a task with a longer duration than the project, expands to cover the entire duration of the task, and defeats the purpose of using this approach. Values are not rolled down from parent tasks, nor are there any restrictions on creating child tasks that are longer than specified duration of the parent.

-   **[Project task relationships and dependencies](c_ProjectTaskRelationDepend.md)**  
The Project Management application enables you a create parent-child relationships between tasks and dependencies, such as finish-to-start and finish-to-finish, between tasks.
-   **[Scheduling conflicts between project tasks](scheduling-conflicts.md)**  
Scheduling conflict helps you to identify project tasks that are not honoring dependencies. A scheduling conflict occurs when one project task prevents other task from starting on the specified date because of dependencies or constraint types.
-   **[Create a project task](../task/t_CreateAProjectTask.md)**  
You can create project tasks in various ways, even from other applications in the instance.
-   **[Create a milestone](../task/t_CreateMilestones.md)**  
A milestone is a project task with a duration of zero \(0\). Use milestones to mark key dates in your project, such as key decision points, approvals, and holidays. Milestones are treated like any other project task and you can create dependencies between tasks and milestones.
-   **[Change requests and project tasks](c_ChangeRequestsAndProjectTasks.md)**  
Large-scale changes approved by your change approval board \(CAB\) require new or existing projects to be implemented.
-   **[Project task checklists](c_project-task-checklists.md)**  
A project task checklist gives you the ability to track activities that must be completed on a task.
-   **[Accept or reject project task notifications](../task/accept-project-task-notifications.md)**  
Approve or reject the changes in a notification for an external soft dependency.
-   **[Task resources](c_TaskResources.md)**  
Resources are the individuals or groups assigned to perform tasks and subtasks in Project Management.

**Parent Topic:**[Project Management](c_ProjectApplicationOverview.md)

