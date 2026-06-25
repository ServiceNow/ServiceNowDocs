---
title: Costing add-on in Project Management
description: The Project Management costing add-on connects the Project Management application to the Cost Management application to allow for estimating and tracking the costs associated with projects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/c\_ProjectManagementCostingAddOn.html
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
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

\[Omitted image "project\_costing\_concepts.png"\] Alt text: screenshot for Project and Cost applications relationship

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

**Parent Topic:**[Starting a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_CreateAProject.md)

**Related topics**  


[Create a project task from a project]()

[Create a parent-child relationship on the Project Task form]()

[Create a monetary benefit plan for a project]()

[Create a non-monetary benefit plan for a project]()

[Associate monetary and non-monetary benefit plans]()

[Create a project cost plan]()

[Recalculating costs of all resource plans in a project]()

[Create an expense line]()

[Create and manage waterfall projects]()

[Update a project]()

[Copy a project]()

[Assign a project schedule]()

[Create baseline of a project]()

[Create a milestone]()

[Activate project task email notifications]()

[Change the planned start date of a project]()

[Create a cost type definition]()

[Generate labor costs]()

[Create a project status report]()

[Allocate budget to a project]()

[Migrate budget of active projects to Next Experience]()

[Migrate financial baselines of projects to Next Experience]()

