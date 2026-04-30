---
title: Generate labor costs
description: Generate labor costs based on the planning attributes configured for financials in the planning attributes page for the resource assignments in a project.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Generate labor costs

Generate labor costs based on the planning attributes configured for financials in the planning attributes page for the resource assignments in a project.

## Before you begin

-   Review the planning attributes enabled for financials. For more information, see [Planning attributes](../concept/planning-attributes.md).
-   Role required: it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All** and select the required project.

    Make sure that the resource assignments are finalized to generate cost plans. If there are no resource assignments for the project, migrate the resource plans to resource assignments. For more information, see [Migrate resource plans and cost plans for projects and demands](../../resource-management/task/migrate-rsrc-plan-rsrc-asgnmnt.md).

2.  Generate labor costs using one of the following options.

<table id="choicetable_v4j_f5z_d1c"><thead><tr><th align="left" id="d50531e103">

Choice

</th><th align="left" id="d50531e106">

Description

</th></tr></thead><tbody><tr><td id="d50531e112">

**Using link from Financials Summary view**

</td><td>

1.  Select **Project Workbench** related link.
2.  Select **Financials** tab and select **Cost Plans**.
3.  Select **Generate Labor Costs**.


</td></tr><tr><td id="d50531e145">

**Using related links**

</td><td>

Select the **Generate Labor Costs** related link.

</td></tr><tr><td id="d50531e157">

**Activate a scheduled job**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Filter the Name field to locate the **Generate labor costs for demands and projects** scheduled job and open it.
3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

For a description of the field names, see [Scheduled Script Execution Form](gen-labor-costs-scheduled-job-ppm.md#).

4.  Select **Update**.


</td></tr></tbody>
</table>3.  Refresh the browser page to view attribute-based labor costs in the Cost Plans related list.


## Result

Attribute-based labor costs are created for the unique combination of attributes that are reflected as the name of the cost plans.

-   **[Activate a scheduled job to generate labor costs](gen-labor-costs-scheduled-job-ppm.md#)**  
Activate and trigger a scheduled job to generate attribute-based labor costs for all the projects and demands at a required cadence.

**Parent Topic:**[Define a project](t_CreateAProject.md)

**Related topics**  


[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Copy a project](t_CopyAProject.md)

[Create baseline of a project](t_CreateAProjectBaseline.md)

[Assign a project schedule](t_UseAProjectSchedule.md)

[Create a project cost plan](t_CreateAProjectCostPlan.md)

[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Create an expense line](t_CreateAExpenseLine.md)

[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)

[Migrate financial baselines of projects to Next Experience](migrate-fin-baselines-projects.md)

[Create a project status report](t_CreateAProjectStatusReport.md)

[View project status reports](project-status-report.md)

[Create a cost type definition](t_CreateAResourceTypeDefinition.md)

[Allocate budget to a project](allocate-budget-to-project.md)

[RIDAC records for a project in Project Workspace](../concept/ridac-entries-for-project.md)

