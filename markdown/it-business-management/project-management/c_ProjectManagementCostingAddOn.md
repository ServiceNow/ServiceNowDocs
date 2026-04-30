---
title: Project Management costing add-on
description: The Project Management costing add-on connects the Project Management application to the Cost Management application to allow for estimating and tracking the costs associated with projects.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project Management costing add-on

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

**Parent Topic:**[Project Management](c_ProjectApplicationOverview.md)

