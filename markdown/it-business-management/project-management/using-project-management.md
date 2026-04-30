---
title: Using Project Management
description: Use Project Management to plan, manage, and track projects effectively.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Using Project Management

Use Project Management to plan, manage, and track projects effectively.

## Plan the project

Before creating a project, consider the following questions and issues:

-   Do you want a top-down or bottom-up approach to tasking?

    Top-down tasking involves creating a project first, then identifying major project phases. Later on, phases can be broken down into tasks and subtasks. The emphasis is on creating estimates for high-level items such as phases and parent tasks and then building the project down from there toward a more detailed level. Use caution when creating tasks for top-down tasking. Creating a task under a project that has a start-on date later than the start date of the project, the project shifts to the later start date. The Project Management application supports bottom-up tasking better.

    Bottom-up tasking involves creating several sets of small tasks and estimating task items such as effort, cost, and duration. These estimations are then aggregated into high-level parent tasks \(rollup tasks\) and phases. The emphasis is on estimating smaller chunks of work as accurately as possible first, then letting those estimations roll up into parent tasks, phases, and the project itself.

-   Is the project part of a larger portfolio of projects?

    Also consider [portfolio planning](c_PortfolioManagement.md) and how the project relates to similar projects or initiatives.

-   What types of dependencies do the tasks have with other tasks?

    The Project Management application supports various dependencies.

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


## Assign resources or assignment groups to the tasks

User resources are the individuals in an organization who are assigned to project tasks. You can manage your resources with resource plans in the Resource Management application.

## Add the project to a portfolio

A portfolio is a group of related projects. If the project is related to other projects, create a portfolio and add the project. The Project Management application provides a useful portfolio view that makes it easy to report on the status of all projects in a portfolio. Portfolios also include demands.

