---
title: Cost plan breakdown
description: A cost plan breakdown captures the estimated cost and actual cost for every fiscal period. Cost plan, project, demand, program, and portfolio are the breakdowns types that are available.When an expense line is created without populating the Cost Plan field, system-generated cost plans are created automatically.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Basics of Project Management, Exploring Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Cost plan breakdown

A cost plan breakdown captures the estimated cost and actual cost for every fiscal period. Cost plan, project, demand, program, and portfolio are the breakdowns types that are available.

-   **Requirement**

    Requirement corresponds to a single cost plan. For example, for a regular calendar and a cost plan spanning across one year, 12 breakdowns would appear.

-   **Task**

    Task corresponds to a project or a demand. The cost across all the cost plans per period is rolled up to the project or demand level. These records have breakdown type set to **Task**. There would be only one record of type **Task** per period. The number of records of type **Task** that are created depends on the duration of the project or demand, and the requirements planned in the project or demand. For example, for a regular calendar and a project with three cost plans, 12 breakdowns appear.

-   **Program**

    If a project or a demand is part of a program, the breakdown type of **Program** provides the aggregate of program level costs per period.

-   **Portfolio**

    If a project or a demand is part of a portfolio, the breakdown type of **Portfolio** provides the aggregate of portfolio level costs per period.


**Parent Topic:**[Basics of Project Management](c_ProjectTasks.md)

**Related topics**  


[Parent-child rollup task calculations](c_ParentChildRollupTaskCalcs.md)

[Project tasks](../task/t_CreateAProjectTask.md)

[Schedule conflicts between project tasks](scheduling-conflicts.md)

[Change requests and project tasks](c_ChangeRequestsAndProjectTasks.md)

[Project task checklists](c_project-task-checklists.md)

[Task resources](c_TaskResources.md)

[Project and project task states](project-and-project-task-states.md)

[Composite Fields](pm-composite-fields.md)

[Actual project costs](actual-project-costs.md)

[Types of external dependencies](external-dependency-types.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Project scheduling in Project Management](project-scheduling.md)

[Task constraints](task-constraints-project-management.md)

## System-generated cost plans

When an expense line is created without populating the **Cost Plan** field, system-generated cost plans are created automatically.

The orphan expense lines are associated to the system-generated cost plans. This association ensures that the project actuals shown on the widgets or the total actuals are the same as the aggregate of the cost plan actuals on the grid shown on the Project Financials page and Investment Portal.

**Note:** System-generated cost plans are created only when the project has a minimum of one cost plan.

System-generated cost plans are created for any of the following reasons:

-   When you create an expense line without populating the **Cost Plan** field.
-   When you create a time card and approve it.

There are two system-generated cost plans, CapEx and OpEx. Depending on the type of expense selected while creating an expense line, the type of system-generated cost plan is created. The following are the name formats for the system-generated cost plans:

-   &lt;project number&gt; System generated CapEx costplan
-   &lt;project number&gt; System generated OpEx costplan

When you create a time card and approve it, an expense line of type CapEx is created and then the orphan expense line is associated to the system-generated cost plan of type CapEx. The system-generated cost plans are created to ensure that none of the expense lines are left without being associated to a cost plan. The system-generated cost plans are read-only.

For customers upgrading to Australia, you can run the project diagnostics, **Associate orphan expense lines to the system generated cost plan**, to associate orphan expense lines to a system-generated cost plan. The diagnostic scan lists the expense lines that are not associated to any cost plan. When you run the fix script, system-generated cost plans are created, and the orphan expense lines are associated to the system-generated cost plans.

