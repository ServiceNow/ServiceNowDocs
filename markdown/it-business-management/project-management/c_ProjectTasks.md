---
title: Basics of Project Management
description: Learn about the basic terms used in Project Management.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Explore, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Basics of Project Management

Learn about the basic terms used in Project Management.

## Bottom-up Tasking

Bottom-up \(tactical\) tasking means that you plan small, individual units of work that are required, then build a project up to include larger phases. Take this approach when you know what individual tasks are required to be accomplished and you are more flexible about overall project duration and estimated cost. Use this approach to see how much a project costs and how long it takes if you include every task. Project management supports tactical tasking by using rollup calculations on several project fields, such as project duration, so that the project adjusts to the tasks it contains. It is the recommended approach for the Project Management application.

## Top-down Tasking

Top-down \(strategic\) tasking means that you plan high-level tasks first, then break down the work into smaller units. Take this approach when you want to build a project with fixed or inflexible time and budgetary constraints and well-defined phases. Establish well-defined milestones and dependencies between tasks that you consider from the beginning. Gradually add smaller tasks to the project later. This approach avoids including all possible tasks in a project and stays flexible with what tasks are included.

**Note:** When you use this method, the Project Management application still rolls up several values, such as task duration. Creating a task with a longer duration than the project, expands to cover the entire duration of the task, and defeats the purpose of using this approach. Values are not rolled down from parent tasks, nor are there any restrictions on creating child tasks that are longer than specified duration of the parent.

## Project relationships and dependencies

The Project Management application enables you a create parent-child relationships between tasks and dependencies, such as finish-to-start and finish-to-finish, between tasks. A task dependency is created when one task is prevented from starting or finishing based on its relationship with the preceding and succeeding tasks.

|Concept|Description|
|-------|-----------|
|Finish-to-start dependency|A dependency that indicates that a task must not be started until its predecessor finishes.|
|Start-to-start dependency|A dependency that indicates that a successor task must not be started until the predecessor task has started.|
|Start-to-finish dependency|A dependency that indicates that a successor must not be finished until the predecessor task starts.|
|Finish-to-finish dependency|A dependency that indicates that a task must not be finished until another task finishes.|
|Lag time|A manually specified time break between predecessor and successor tasks.|
|Parent task|A project task with smaller tasks, referred to as child tasks, underneath it. Child tasks break down the work of a parent task into more manageable subsets. Certain fields for child tasks, such as planned end date, roll up and affect the same field in the parent task.|
|Child task|A project task that is a subset of a larger task. Child task start dates cannot occur before the start date of the parent task.|
|Rollup task|Another term for a parent task in the context of aggregating child task items, such as effort or resources, into a larger parent task calculation. All fields on rollup task forms are read-only.|
|Roll down|State changes roll down from the project to project tasks, and from parent tasks to child tasks.|

**Note:** Only one relationship can exist between two tasks.

The Project Management application provides several properties that control how tasks are calculated and behave. See [Project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) for more information.

## Task time constraints

The Project Management application supports several types of dependencies.

The Project Task form includes a **Time Constraint** field, which can be one of the following values:

-   If a task is set to **Start ASAP**: The task appears on the Gantt chart as starting when the dependency allows it. However, a task can start on a later date when a lag value is set for the relationship.
-   If a task is set to **Start on specific date**: The task appears on the Gantt chart as starting on the constraint date. The start date of such a task is not impacted even after you put the task in a relation to another task, for example, FS relation.
-   If a task is set to **Start no earlier than**: The task appears on the Gantt chart as starting on or after the constraint date. If the task has no predecessor, the task starts on the specified date. The start date changes to a later date based on the predecessor task end date or if the task is in a relation to another task, for example, FS relationship.
-   If a task is set to **Start no later than**: The task appears on the Gantt chart as starting on or before the constraint date. If the task has any predecessor task, the dependency on the predecessor task determines when the task can start. A scheduling conflict occurs if the predecessor task attempts to move the task beyond the date specified in the **Constraint date** field.

    **Note:** The [project property](../reference/r_InstalledWithProjectManagement.md#table_Project-Properties-system-properties) **Retain start on constraint on tasks after adding relations** controls the behavior for **Start on** selection. The property is set to True by default and is not editable.

-   A task that is not honoring dependency is indicated with a red calendar icon ![task with must start on dependency icon](../image/pc-task-dep-icon.png) on the Planning Console. If you want the task to honor the dependency and adjust the start accordingly, change the constraint type of the task to **Start ASAP**.

## Parent-child task relationships

If a task is relatively large and requires several users with different skills to manage, break the task into subtasks and create parent-child relationships. A child task is a relatively smaller, manageable size of work.

When you group child tasks together under a parent, values such as **Estimated cost** aggregate and roll up to the parent task. So the parent task takes on the form of a summary task or rollup task for its child tasks. **Planned start date** and **Planned end date** rollup occurs when you create child tasks: the duration of the parent automatically adjusts to cover its child tasks.

A parent-child relationship is different from a dependency relationship. In a dependency, one task must finish before another begins. In a parent-child relationship, any number of tasks can be nested under a parent task with or without any dependencies. When you create a parent-child relationship, the parent task number is saved in the **Parent** field in the Project Tasks table. All project management tasks have a parent: either another project task or the project itself.

Unlike a dependency, a parent-child relationship is not saved as a record in any table. The only modification that takes place when a parent-child relationship is modified is the **Parent** field in the child task record.

You can create predecessor-successor relationships between child tasks with different parents, between two different parent tasks, or between a child task and another parent task. However, if the predecessor task finishes after the successor task starts, creating a dependency between child tasks that have different parents is not allowed.

**Note:** On the Gantt chart, you can drag-and-drop the parent task to move the entire hierarchy to a new location on the schedule.

## Time constraints in parent-child relationships

Parent-child task relationships have several effects on task time constraints.

-   **When a child task is set to __Start ASAP__**

    The child task starts at the same time as the parent task. If Project itself is set as a parent, the **Start ASAP** tasks starts on the same date as set in the **Constraint Date** field, as long as it does not have dependencies with other child tasks.

-   **When a parent task is set to __Start ASAP__ and child tasks are set to __Start on specific date__:**
    -   The earliest child task start date determines the start date of the parent, assuming no other dependencies.
    -   In this case, the **Time constraint** field of the parent remains **Start ASAP**, but the actual start date is changed to the start date of the earliest child task.
-   **When a parent task is set to __Start ASAP__ and child tasks are set to __Start on specific date__:**

    Child precedence also applies to end dates. If the estimated end date of the child task is later than the end date of the parent task, the estimated end date extends to cover the child. For actual values, a parent has the same start date as the earliest start date of its children. The latest actual end date is the latest end date of its children. Assuming the child tasks are **Closed Complete**. If the child tasks are not in the **Closed Complete** state, the actual end date of the parent is empty.

    For the planned start date of the parent task:

    -   The planned start date is the earliest planned start date of all the children that do not have an actual start date.
    -   If all child tasks have actual start dates, the planned start date of the parent task is set to the actual start date.
    For the planned end date of the parent task: The latest planned end date or actual end date of the child tasks determines the planned end date of the parent.

    A task with **Start no later than** or **Start on specific date** time constraint cannot be a parent task. When a new child task is added to a task with these time constraints, the time constraint for the parent task is changed to **Start ASAP**.


## Top-down and bottom-up planning

-   For top-down planning, create a task that you already know includes several child tasks. Then create the child tasks and specify that they are child tasks of the first task you created.
-   For bottom-up planning, create tasks for the smallest units of work first. Then you can create intermediary parent tasks that cover a group of related child tasks. For example, if there are five sequential tasks that comprise a phase of a project called install database, create the five tasks first. Then create another task called Database installation and make it the parent task of the five tasks. Rollup calculations, such as **Planned duration**, for the Database installation task are automatically calculated based on the child tasks.

It is easiest to build task relationships and dependencies while creating sets of tasks.

-   A dependency means that a task relies on other tasks to be performed \(completely or partially\) before it can be performed.
-   A relationship means a parent-child relationship whereby several subtasks are configured under a parent task or phase, which rolls up fields like **Planned duration** and **Estimated cost**.

    Use the [Gantt chart](c_GanttChart.md) with task forms and related lists to build relationships. Add milestones based on the major events of a project and create dependencies between milestones and tasks, if necessary.

    Also set up notifications to alert project task assignees when their tasks move to the **Work in Progress** state. See Creating Project Tasks for more information on creating tasks.


-   **[Parent-child rollup task calculations](c_ParentChildRollupTaskCalcs.md)**  
Date changes, stage changes, and value calculations roll up from child tasks to parent tasks.
-   **[Project tasks](../task/t_CreateAProjectTask.md)**  
Create project tasks in several ways, even from other applications in the instance.
-   **[Schedule conflicts between project tasks](scheduling-conflicts.md)**  
Scheduling conflict helps you to identify project tasks that are not honoring dependencies. A scheduling conflict occurs when one project task prevents other task from starting on the specified date because of dependencies or constraint types.
-   **[Change requests and project tasks](c_ChangeRequestsAndProjectTasks.md)**  
Large-scale changes approved by your change approval board \(CAB\) require new or existing projects to be implemented.
-   **[Project task checklists](c_project-task-checklists.md)**  
A project task checklist gives you the ability to track activities that must be completed on a task.
-   **[Task resources](c_TaskResources.md)**  
Resources are the individuals or groups assigned to perform tasks and subtasks in Project Management.
-   **[Project and project task states](project-and-project-task-states.md)**  
In the base system, the states in project and project task inherit the states in Task table.
-   **[Composite Fields](pm-composite-fields.md)**  
A composite field combines information from two fields in a table to form a single field.
-   **[Cost plan breakdown](cost-plan-breakdown.md#)**  
A cost plan breakdown captures the estimated cost and actual cost for every fiscal period. Cost plan, project, demand, program, and portfolio are the breakdowns types that are available.
-   **[Actual project costs](actual-project-costs.md)**  
Actual project costs come after you create expense lines for cost plans or after human resources use time cards to create expense lines.
-   **[Types of external dependencies](external-dependency-types.md)**  
The Project management application supports two types of external dependencies - hard and soft.
-   **[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)**  
Specify the amount of money that projects and portfolios are allowed to have.

**Parent Topic:**[Exploring Project Management](exploring-project-management.md)

**Related topics**  


[Parent-child rollup task calculations](c_ParentChildRollupTaskCalcs.md)

[Create a parent-child relationship on the Project Task form](../task/t_CreateParentChildRelationship.md)

