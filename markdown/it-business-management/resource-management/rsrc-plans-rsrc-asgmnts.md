---
title: Migration of resource plans, operational resource plans, and cost plans
description: Migrate resource plans to resource assignments and the associated cost plans to attribute-based labor costs of your projects or demands and easily work on resource allocations using Project Workspace.
locale: en-US
release: zurich
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Migration of resource plans, operational resource plans, and cost plans

Migrate resource plans to resource assignments and the associated cost plans to attribute-based labor costs of your projects or demands and easily work on resource allocations using Project Workspace.

**Tip:** Resource Managers are encouraged to view the [Resource Management Workspace boot camp](https://learning.servicenow.com/lxp/en/strategic-portfolio-management/resource-management-migration-to-the-next?id=learning_course_prev&course_id=832423fe97264a9ce4fb72de2153af07) to learn about Resource Management Migration to the Next Experience.

## Resource plans to resource assignments

Migrate all the resource plans of a project or demand to attribute-based resource assignments depending on the [planning attributes](../../project-management/concept/planning-attributes.md) to easily manage your projects on Next experience using [Project Workspace](../../project-workspace/concept/project-workspace-landing-page.md) and [Capacity Planning](../../spw-capacity-planning/concept/capacity-planning-spw.md).

Group, Skill, and Role are the primary attributes enabled for Resource Management depending on which the resource plans are migrated to resource assignments.

**Important:** Resource plans in Planning, Requested, Confirmed, Allocated, Rejected, and Completed states are only migrated to Resource assignments. Resource plans in Canceled and In-progress states aren’t migrated.

Let us see how the status of the resource plans is mapped to the status of resource assignments.

|Resource plan status|Resource assignments status|
|--------------------|---------------------------|
|Planned or Requested|Unassigned|
|Allocated|Approved|
|Confirmed|Approved|
|Completed|Approved|
|Canceled or In-progress|Resource plan isn’t migrated|
|Rejected|Unapproved|

Migrating requested efforts of resource plans

When a resource plan is migrated, a corresponding resource assignment is created based on the primary attributes from the resource plan. Resource assignments don’t support custom selection of allocation type and allocation spread.

Resource assignments only support even spread of resource allocations by default.

The efforts of the resource plan in requested state are also migrated to resource assignments. For example, if a resource plan is in Requested state with 20 additional hours requested, but not yet approved, the new migration flow accounts for these requested 20 hours and the total efforts are reflected in the migrated resource plan. See the following screenshots for more details.

![Classic ServiceNow view of a resource plan in Requested state.](../../resource-management-workspace/images/RP-RA-requested-efforts.png "Existing resource plan in requested state")

![Monthly allocations view of resource assignment with requested efforts.](../../resource-management-workspace/images/RP-RA-requested-efforts-migrated.png "Monthly aggregates of migrated resource plan with requested allocations")

With the migration of resource plans:

-   Resource plans in Planning or Requested states, resource assignments are created based on the planned dates and planned duration with their default state as Unassigned.
-   Allocation type is set to planned duration.
-   Allocation spread is always Even.
-   Existing resource allocations are deleted and created again to accommodate resource allocations with the resource name and planned duration.
-   The allocated costs and allocated hours are copied to planned costs and planned hours.
-   Actual hours for the resource plan in Confirmed and Allocated states are retained with the resource plans.

**Note:** Only one resource assignment is created for every unique combination of primary attributes, Group, Skill, and Role, and one for every user if the resource plans are created with selected member preferences. After migration, if you create resource assignments with any of the existing combinations, the available resource assignments are updated with the new requests.

Allocation contour while migrating to resource assignments

The existing contour of allocations in resource plans is maintained while migrating to resource assignments.

Maintaining the existing contour ensures that the planned effort, timing, and effort distribution remain consistent before and after migration. By carrying forward the same allocation contours, you can continue managing ongoing work without disruption, maintaining accurate capacity and utilization insights, and trust that financial and resource plans reflect your original intent. This seamless transition helps you adopt the workspace experience confidently, without the need to replan or manually adjust allocations.

## Migration of Resource plans to Resource assignments

Resource plans in different states.

![Resource plans list.](../image/rp-ra-resource-plans.png)

Resource plans migrated as resource assignments.

![Resource assignments list.](../image/rp-ra-resource-assignments.png)

## Operational resource plans to operational resource assignments

Operational resource plans also follow the same logic to migrate operational resource plans to operational resource assignments.

**Important:** Operational resource plans in Allocated and Completed states are only migrated as Operational resource assignments.

After migration, the Request type of operational resource plans is changed to Hours.

## Migration of Operational resource plans to Operational resource assignments

Operational resource plan in Allocated state created for Demo GroupA.

![Operational resource plans form.](../image/rm-op-rsrc-plan.png)

After migration, we will have the following Operational resource assignments for every member of the group.

**Note:** The parent-child mapping is retained and you may see an additional resource assignment with an empty resource.

![Operational resource assignments view after migration from Operational resource plans.](../image/rm-op-rsrc-asgnmnts.png)

## Migration of cost plans to attribute-based cost plans

When resource plans of a project or demand are migrated to resource assignments, the corresponding financial cost plans based on the resource plans will be migrated to new attribute-based labor costs. Migrate resource plans related link trigger migrates the cost plans along with resource plans migration.

Every resource plan has an associated a cost plan with Labor capex as the cost type. While migrating, the [planning attributes](../../project-management/concept/planning-attributes.md) of the resource plans are analyzed to create attribute-based cost plans for the unique combination of the three [planning attributes enabled for financials](../../project-management/concept/planning-attributes.md#table_f1y_wvh_wwb) \(Employee type, Expense Type, and Role\). After migration, there will be no one-to-one association between resource assignments and attribute-based cost plans.

**Note:** If a resource plan isn’t associated with either Employee Type or Role, the migrated cost plans costs are consolidated into a single cost plan.

The planned costs are moved to the new attribute-based cost plans while the actual costs remain on the existing cost plan records. The [rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md) values associated with project or a demand are considered to generate attribute-based labor costs.

## Migration of cost plans to attribute-based cost plans

Cost plans associated with a resource plan.

![List of cost plans with accounted planned and actual expenses.](../image/rp-ra-cost-plans-traditional.png)

Attribute-based cost plan **Resource\_Internal\_Capex** is created after migration.

![List of attribute-based labor costs capturing the aggregate planned costs.](../image/rp-ra-cost-plans-migrated.png)

-   **[Migrate resource plans and cost plans for projects and demands](../task/migrate-rsrc-plan-rsrc-asgnmnt.md)**  
Migrate resource plans and cost plans of your projects or demands to resource assignments and attribute-bases cost plans and work on the resource allocations and project financials using Project Workspace.
-   **[Enable attribute-based resource assignments](../task/enable-resource-assignments.md)**  
Enable the property to work on attribute-based resource assignments to request efforts for your planning items.
-   **[Create resource assignments](../task/create-rsrc-asgnmnts-ppm.md)**  
Create resource assignments to request a portion of team or resource capacity for project or demand.
-   **[Migrate operational resource plans](../task/migrate-operational-rsrc-plans.md)**  
Migrate the required Operational resource plans to attribute-based Operational resource assignments.
-   **[Create operational resource assignments](../task/create-op-rsrc-asgnmnts-ppm.md)**  
Create operational resource assignments to allocate a portion of team or resource capacity for operational work such as administration work, meetings, trainings, and so on.
-   **[Activate a scheduled job to migrate resource plans and cost plans](../task/migrate-rsrc-plan-cost-plan-scheduled-job.md)**  
Activate the Migrate Resource Plans scheduled job to migrate resource plans, operational resource plans, and cost plans of your projects and demands to resource assignments and attribute-based cost plans.

**Parent Topic:**[Resource Management classic](c_ResourceManagement.md)

