---
title: Copy a project
description: Another option for creating a project is to copy an existing project with all its tasks and relationships. After you specify the start date for the copy, the system adjusts all task start and end dates automatically.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Copy a project

Another option for creating a project is to copy an existing project with all its tasks and relationships. After you specify the start date for the copy, the system adjusts all task start and end dates automatically.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  On the Project form, right-click the header and select **Copy Project**.

2.  Enter the new project name for the new project that you are creating.

3.  Select a start date.

4.  Click **OK**.

    Copy partial project, which is available from the Project Task form, provides similar functionality. It copies all task or project relationships and children from the selected project and inserts them into the current project. In this case, a new project record is not created.


## Result

Actual duration and the actual start and end dates are reset to null values. The state is set to **New** and percent complete is set to **0**.

By default only the short description, planned dates and duration fields are copied from source project to the target project. If additional columns must be copied, they should be declared in the [project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) **List of attributes that will be copied from the originating project task**.

-   **[Change default values of copied project](t_ModifyTheCopyProjectUIPage.md)**  
Reset or change the default values for copied fields in the new copied partial or complete project.

**Parent Topic:**[Define a project](t_CreateAProject.md)

**Related topics**  


[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Create baseline of a project](t_CreateAProjectBaseline.md)

[Assign a project schedule](t_UseAProjectSchedule.md)

[Create a project cost plan](t_CreateAProjectCostPlan.md)

[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Create an expense line](t_CreateAExpenseLine.md)

[Generate labor costs](gen-cost-pln-prj-wrkspc.md)

[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)

[Migrate financial baselines of projects to Next Experience](migrate-fin-baselines-projects.md)

[Create a project status report](t_CreateAProjectStatusReport.md)

[View project status reports](project-status-report.md)

[Create a cost type definition](t_CreateAResourceTypeDefinition.md)

[Allocate budget to a project](allocate-budget-to-project.md)

[RIDAC records for a project in Project Workspace](../concept/ridac-entries-for-project.md)

