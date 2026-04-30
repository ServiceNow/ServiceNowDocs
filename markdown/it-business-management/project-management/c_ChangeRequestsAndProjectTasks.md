---
title: Change requests and project tasks
description: Large-scale changes approved by your change approval board \(CAB\) require new or existing projects to be implemented.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Basics of Project Management, Explore, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Change requests and project tasks

Large-scale changes approved by your change approval board \(CAB\) require new or existing projects to be implemented.

To bridge the gap between change management and project management, the instance allows you to link one or more change requests to a project task. You can link an existing change request to a project task or create a new change request directly from a project task.

When you link a project task to a change request record, a new project task link record is created. It provides the actual link between the project task record and the change request record. The project task link copies all attributes of the change request record. It then becomes a child task of the project task that you linked to the change request. The rules that govern the relationship between the project task and the project task link are the same as the rules for all parent and child tasks.

![Project tasks linked to change requests](../image/Project_change1.png "Project tasks linked to change requests")

**Note:** A project task cannot have both task link records and child project tasks. When a project task is linked to a change request, you cannot also create child tasks for that project task. Likewise, when a project task has child tasks, you cannot link the parent project task to a change record.

The project task link record is read only. You can view the project task links from a related list on the Project Task form.

![Project Tasks Links related list](../image/Project_task_links_related_list.png "Project Tasks Links related list")

You can also link multiple change requests to a single project task. In this case, a project task link record is created for each link and all the project task link records become child tasks of the project task.

![Project tasks links](../image/Project_change2.png "Project tasks links")

## Change request project task relationship

The rules that apply to all parent-child tasks also govern the relationship between project task and the project task link. The project task link inherits start and end dates from the change request. However, the Project Management application adjusts the dates when these situations occur:

Start and end dates:

-   If the project task and the change request have different planned start dates, the project task link uses the later of the two dates. For example, if the project task starts on October 1 but the change request starts on October 2, the project task link changes to October 2.
-   If the change request has an earlier start date, the **Time constraint** value for the project task link becomes **Start ASAP** when the link is created. The end date remains the same as the end date specified in the change request record.
-   If the change request starts and ends before the project start date, the project task link has a duration of zero \(0\). It also appears as a milestone that occurs when the project starts.
-   If a change request is scheduled to start during non-work time according to the project schedule, the planned start date of the project task link ignores the schedule. It also starts at the time specified by the change request. However, the duration of the project task link does take the schedule into consideration. For example: the project uses the default schedule, which specifies that work hours are Monday to Friday from 08:00 to 17:00 with an hour break from noon to 13:00. A change request with a 13-hour duration starts at midnight. The project task link starts at midnight and continues through the start of the schedule at 08:00. It stops at noon for one hour, and continues from 13:00 until 14:00. The total duration would be 13 hours.

## Project Task Duration

The duration of the change request determines the duration of the project task link. That duration is rolled up to the parent project task just as all child task durations roll up to parent tasks. The **Planned start date** and **Planned end date** in the Change Request form **Schedule** section are the fields that determine the duration. If there are no planned dates on the Change Request form, the default duration is one project day. The project has a schedule or 24 hours when the project has no schedule.

## Multiple Linked Change Requests

If you link additional change requests to a project task, additional project task links are created. All become child tasks of the project task. The dates roll up to the parent task. For example, if a linked project task is planned to finish on October 30. You link a new change request scheduled to finish on November 30, a new project task link is created. The parent task planned end date extends to November 30 to cover the duration of both project task links. A change request can only be linked to one project task. It cannot be linked to multiple tasks in the same project or across multiple projects. A project task that has one or more child tasks cannot also have a project task link connecting it to a change request.

## Project Task State

If the state of a change request changes to **Pending**, **Open**, or **Work in Progress**, the state of the project task link changes accordingly. If the state of the change request changes to any of the closed states, the state of the project task link changes to **Closed Complete**.

## How Modifications Propagate Between Change Requests and Project Tasks

Modifications to a linked change request propagate to the project task link. However, the reverse is not true. You cannot modify the change request record from the Project Management application.

Modifications to the following fields propagate from the change request to the project task link:

-   **Planned start date**
-   **Planned end date**
-   **State**

These change request settings also roll up to the project task that is the parent of the project task link, and also up to the project record. Consider the following example: a project has not yet been started and all its tasks are in the **Pending** state. If you changed the state of a linked change request record from **Open** to **Work in Progress**, the project task link, its parent task, and the project itself all change to **Work in Progress**.

When you start a project, tasks that have **Start ASAP** as the time constraint and have no other start dependencies start immediately. However, project tasks with linked change requests do not start automatically. The project manager must start the task manually by changing the **State** field to **Work in Progress**.

Modifications made in the Project Management application do not propagate to a linked change request record, so closing a project does not close a linked change. When you successfully implement a change and close the project it belongs to, you must go to the change request record and manually change the state to **Closed**.

**Parent Topic:**[Basics of Project Management](c_ProjectTasks.md)

**Related topics**  


[Parent-child rollup task calculations](c_ParentChildRollupTaskCalcs.md)

[Project tasks](../task/t_CreateAProjectTask.md)

[Schedule conflicts between project tasks](scheduling-conflicts.md)

[Project task checklists](c_project-task-checklists.md)

[Task resources](c_TaskResources.md)

[Project and project task states](project-and-project-task-states.md)

[Composite Fields](pm-composite-fields.md)

[Cost plan breakdown](cost-plan-breakdown.md#)

[Actual project costs](actual-project-costs.md)

[Types of external dependencies](external-dependency-types.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Link change requests to a project task](../task/t_LinkChangesToAProjectTask.md)

