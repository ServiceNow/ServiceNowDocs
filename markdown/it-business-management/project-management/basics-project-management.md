---
title: Basics of Project Management
description: A project is any planned, collaborative effort that is designed to achieve an objective. The Project Management application not only helps you plan and track projects, it integrates with other applications.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Basics of Project Management

A project is any planned, collaborative effort that is designed to achieve an objective. The Project Management application not only helps you plan and track projects, it integrates with other applications.

There are several paths available to manage a project. The best path usually depends on business needs. The phases in the graphic are designed to get a project up and running with the minimum amount of effort:

![Project phases](../image/Project_phases.png "Project phases")

## Set up the project

Setting up a project involves deciding on an approach for creating and linking project tasks. It also involves creating the necessary users and groups in ServiceNow so you can assign them to project tasks.

**Plan the project**

Before creating a project, consider the following questions and issues:

-   Do you want a top-down or bottom-up approach to tasking?

    Top-down tasking involves creating a project first, then identifying major project phases. Later on, phases can be broken down into tasks and subtasks. The emphasis is on creating estimates for high-level items such as phases and parent tasks and then building the project down from there toward a more detailed level. Use caution when creating tasks for top-down tasking. Creating a task under a project that has a start-on date later than the start date of the project, the project shifts to the later start date. The Project Management application supports bottom-up tasking better.

    Bottom-up tasking involves creating several sets of small tasks and estimating task items such as effort, cost, and duration. These estimations are then aggregated into high-level parent tasks \(rollup tasks\) and phases. The emphasis is on estimating smaller chunks of work as accurately as possible first, then letting those estimations roll up into parent tasks, phases, and the project itself.

-   Is the project part of a larger portfolio of projects?

    Also consider [portfolio planning](c_PortfolioManagement.md) and how the project relates to similar projects or initiatives.

-   What types of dependencies do the tasks have with other tasks?

    The Project Management application supports various dependencies. See: [Project task relationships and dependencies](c_ProjectTaskRelationDepend.md).

-   Can milestones and project baselines help manage a project?

    A milestone is a project task with a duration of 0. Use milestones to indicate important dates in a project. If necessary, create dependencies between tasks and milestones so that a task does not start until a milestone has been reached.

    A baseline is a snapshot of the current planned start and end dates at the time the baseline was created for each task. A line appears under each task on the Gantt chart for the original planned start and end dates. The line appears shifted to the left or right depending on whether the task was started early or late. If tasks slip to later dates, the baseline indicator provides an easy way to see how severe the delays are.

-   Have the necessary skills, groups, and resources been created in ServiceNow?

    If project tasks are assigned to different groups or individual resources with the required skills, create users and groups and configure the Skills Management application.

-   Does an existing incident, problem, or change justify creating a project to track it?

    Of these record types, a change is most likely to lead to activities that are tracked as a project.

-   Do you want to track project costs?

    Estimate group resource costs before starting the project. Then track the actual cost of each user resource from time cards. The Project Management application can also calculate the costs of affected CIs in a project. The Project Management Costing add-on is required to track costs.

-   What goals do you want the project to achieve?

    Every project has at least one goal. Project goals are saved in the Goal table and can link to any task. In a typical scenario, link one goal to each project and keep the **State** field of the goal up to date.


**Create the project**

Create the project in the Project Management application after:

-   Choosing an approach
-   Gathering initial estimates for the planned start date
-   Estimating cost
-   Formulating a well-defined business case

**Add project tasks, dependencies, and relationships**

After creating a project record, create tasks.

-   For top-down planning, create a task that you already know includes several child tasks. Then create the child tasks and specify that they are child tasks of the first task you created.
-   For bottom-up planning, create tasks for the smallest units of work first. Then you can create intermediary parent tasks that cover a group of related child tasks. For example, if there are five sequential tasks that comprise a phase of a project called install database, create the five tasks first. Then create another task called Database installation and make it the parent task of the five tasks. Rollup calculations, such as **Planned duration**, for the Database installation task are automatically calculated based on the child tasks.

It is easiest to build task relationships and dependencies while creating sets of tasks.

-   A dependency means that a task relies on other tasks to be performed \(completely or partially\) before it can be performed. For information on different types of dependencies supported, see [Project task relationships and dependencies](c_ProjectTaskRelationDepend.md).
-   A relationship means a parent-child relationship whereby several subtasks are configured under a parent task or phase, which rolls up fields like **Planned duration** and **Estimated cost**.

    Use the [Gantt chart](c_GanttChart.md) with task forms and related lists to [build relationships](c_ProjectTaskRelationDepend.md). Add milestones based on the major events of a project and create dependencies between milestones and tasks, if necessary.

    Also set up notifications to alert project task assignees when their tasks move to the **Work in Progress** state. See Creating Project Tasks for more information on creating tasks.


**Assign resources or assignment groups to the tasks**

User resources are the individuals in an organization who are assigned to project tasks. You can manage your resources with resource plans in the Resource Management application.

**Add the project to a portfolio**

A portfolio is a group of related projects. If the project is related to other projects, create a portfolio and add the project. The Project Management application provides a useful portfolio view that makes it easy to report on the status of all projects in a portfolio. Portfolios also include demands.

## Manage the Project

After the preceding steps are complete, the project can be started. To measure the project against initial estimates, create a baseline, which is a snapshot of the entire project including all planned dates for all project tasks and milestones. The project manager can manage a project from the project workbench.

**Start the Project**

[Start the project](../task/t_StartAProject.md) by changing the project state to **Work in Progress**. When you change the **State** field on the Project form to **Work in Progress**, the Actual start date of the project changes to the planned start date.

**Monitor the Project and Customize Dashboards**

You can update important project status information, such as the number of milestones slipped. You can also view summaries for cost, scope, project risk, and so on. Modify this information as needed with the **Portfolio View** related list on the Portfolio form and display this information on the **Project Overview** homepage. In addition, use the project reports installed with the application, such as **Active projects** or **Projects \(by priority\)**, to show important project information.

When the project is underway, continue to access project records and edit several items, including costs, priority, schedule, and planned values that are not rollups. Keep detailed project records for risks and issues and refer to them after a project is complete. Also create baselines along the way to easily see if any project phases or tasks are slipping at the time you create the baseline.

## Close the Project

When the project is complete, change its state to **Closed complete** on the project form. When a project is in the [closed state](../task/t_CloseAProject.md), the Project Management application calculates actual values like **Actual duration**.

Post-project activities include analyzing project baselines and actual values and generating a final project dashboard. You can [cancel the future resource plans](../../resource-management/task/cancel-resource-plan-from-project-or-demand.md) and [complete the allocated resource plans](../../resource-management/task/complete-resource-plan-from-project-or-demand.md) for the closed project.

If the project was successful and can be used as a template for future projects, make a copy of it. If the project was created from a change, incident, or problem record, there are several other activities to perform in ServiceNow.

**Parent Topic:**[Project Management](c_ProjectApplicationOverview.md)

