---
title: Costing add-on in Project Management
description: The Project Management costing add-on connects the Project Management application to the Cost Management application to allow for estimating and tracking the costs associated with projects.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Costing add-on in Project Management

The Project Management costing add-on connects the Project Management application to the Cost Management application to allow for estimating and tracking the costs associated with projects.

This plugin enables the following project costing features:

-   Estimate group resource costs during project planning.
-   Tracking the actual cost of each user resource for a project.
-   Track actual project task costs from time cards and other project expenses.
-   Allocate project costs to the business.
-   Represent project costs to the CIs that the project affects.
-   Rollups of actual task expenses to parent tasks and the project record.

The Project and Cost applications work together as shown in the diagram:

![screenshot for Project and Cost applications relationship](../image/project_costing_concepts.png "Project and Cost applications")

The following properties are available with this plugin:

|Description|Property Name|Notes|
|-----------|-------------|-----|
|For planned tasks types, calculate the actual cost field using the total of expense lines for the task.|glide.cost\_mgmt.calc\_actual\_cost|Default: **true**. This property is from Cost Management. When an expense line is created against any task of **planned\_tasktype** and this property is true, the system gets a sum of the costs for all the expense lines and sets the total cost in the **work\_cost** field.|
|When creating a task expense line should the system also create expense lines for the top task?|glide.cost\_mgmt.process\_task\_top\_task|Default: **true**|
|Enable project cost rollup \(estimated and actual\) - updating the cost of a project task updates the cost of its parent.|com.snc.project.rollup.cost|Default: **true**|

The following business rules are added or modified with this plugin:

|Name|Table|Description|
|----|-----|-----------|
|Project Cost Rollup|Planned task \[planned\_task\]|Default: **true**. This property is from Cost Management. When an expense line is created against any task of **planned\_tasktype** and this property is true, the system gets a sum of the costs for all the expense lines and sets the total cost in the **work\_cost** field.|
|Process Top Task Parent|\[fm\_expense\_line\]|Default: **true**|

**Parent Topic:**[Starting a project](../task/t_CreateAProject.md)

**Related topics**  


[Create a project task from a project](../task/t_CreateATaskFromAProject.md)

[Create a parent-child relationship on the Project Task form](../task/t_CreateParentChildRelationship.md)

[Create a monetary benefit plan for a project](../task/create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](../task/create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](../task/associate-monetary-and-non-monetary-benefit-plans-project.md)

[Create a project cost plan](../task/t_CreateAProjectCostPlan.md)

[Recalculating costs of all resource plans in a project](../task/recalculate-resource-costs-of-a-project.md)

[Create an expense line](../task/t_CreateAExpenseLine.md)

[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Update a project](../task/t_UpdateAProjectInProgress.md)

[Copy a project](../task/t_CopyAProject.md)

[Assign a project schedule](../task/t_UseAProjectSchedule.md)

[Create baseline of a project](../task/t_CreateAProjectBaseline.md)

[Create a milestone](../task/t_CreateMilestones.md)

[Activate project task email notifications](../task/t_ActivateProjTaskEmailNot.md)

[Change the planned start date of a project](../task/change-planned-start-date-of-project.md)

[Create a cost type definition](../task/t_CreateAResourceTypeDefinition.md)

[Generate labor costs](../task/gen-cost-pln-prj-wrkspc.md)

[Create a project status report](../task/t_CreateAProjectStatusReport.md)

[Allocate budget to a project](../task/allocate-budget-to-project.md)

[Migrate budget of active projects to Next Experience](../task/fin-migrate-budget-project-ppm.md)

[Migrate financial baselines of projects to Next Experience](../task/migrate-fin-baselines-projects.md)

