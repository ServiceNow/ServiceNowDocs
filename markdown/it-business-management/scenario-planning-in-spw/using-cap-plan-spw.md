---
title: Planning user capacity in Strategic Planning Workspace
description: Assess the resource capacity and review existing allocations, which help you to make informed decisions while working on assigning resources in Strategic Planning.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Planning user capacity in Strategic Planning Workspace

Assess the resource capacity and review existing allocations, which help you to make informed decisions while working on assigning resources in Strategic Planning.

Use the [manage resource capacity](../task/manage-rsrc-cap-spw.md) screen to generate resource capacity details.

Use the [Capacity screen](../task/using-cap-planning-screen-spw.md) to view detailed information about the resource capacity mapping to a portfolio.

## Manage resource capacity

![Manage resource capacity screen displaying the capacity details for Employee Management group.](../images/cp-manage-resource-capacity-screen.png "Manage resource capacity screen")

Using Manage resource capacity, select a time frame and primary attributes to view number of available resources. Generated resource capacity details are saved. You can regenerate capacity to view latest changes in the resource availability.

Resource capacity screen helps you to view the following data.

-   Resource availability for generated capacity.
-   Total number of available resources in a monthly breakdown view.
-   Latest date of generating the capacity details.
-   Option to regenerate and fetch the latest capacity details from the employee profile mappings.

On the Manage resource capacity screen, you can:

-   Filter resources with specific capacity attributes for a required date range to view the number of available resources.
-   Regenerate capacity details to view the latest details from the resource employee profile mapping.

## Select resource criteria

-   Select a primary attribute to automatically view the available groups, roles, or skills from the resource assignments of the prioritized planning items.
-   Switch between **Auto-select** and **Manual-select** option to view the allocated resource efforts for all planning items or to view a custom data, respectively.
-   Define resource criteria to view the available groups, roles, or skills from the resource assignments of the prioritized planning items.

![Resource criteria screen in Capacity.](../images/cp-resource-criteria-screen.png)

## Capacity

Capacity screen displays the resource efforts from the prioritized planning items.

-   Comprehensive overview of resource capacity and allocations.
-   Current resource capacity allocation.
-   Interactive Gantt chat to view prioritized planning items in the bottom tray to analyze and plan work.

![Capacity view for resource capacity.](../images/cp-capacity-planning-screen.png)

Understanding the Capacity screen.

|Color|Description|
|-----|-----------|
|Yellow \(Gantt bar\)|Planning item with no resource assignments.|
|Blue \(Gantt bar\)|Resource estimates for Planning items are within the resource capacity.|
|Red \(Cells and Gantt bar\)|Overallocation in resource estimates.|
|Green \(Cells\)|Resource estimates within the resource capacity.|

Using Capacity, you can:

-   View the capacity allocations of prioritized planning items for your current portfolio and better forecast your future resource requirements.
-   Use the filter option \(![Capacity filter button.](../images/cp-filter-button.png)\) to view planning items by their type, state, priority or any by any required attributes to create capacity plans.

    **Note:** Default filter is set to display prioritized planning items only.

-   View the updated resource capacity based on the assigned operational resource assignments.
-   View the total resource capacity in the heatmap view.

    ![Resource capacity heatmap view.](../images/cp-heatmap-view.png)

-   View total resource capacity and total estimates.
-   View the efforts for operational work and efforts for estimates outside of portfolio in the **Additional items** list.
-   Redefine the workforce criteria by selecting **Resource criteria** \(![Resource criteria button.](../images/cp-resource-criteria-button.png)\)

## Calculation of Operational Resource Assignment in Capacity

As a Resource Manager, you can [create operation resource assignments](../../resource-management/task/create-op-rsrc-asgnmnts-ppm.md) or [migrate existing operational resource plans](../../resource-management/task/migrate-operational-rsrc-plans.md) of your employees to handle the required meetings, trainings, time off and so on to meet your work requirements.

Consider a group with capacity of 2 FTE and resource manager creates a Group type operation resource assignment for 10% of the capacity for training. This operational assignment can be viewed in the **Operational work** line item in the top-tray of the Capacity screen. The value of the **Operational work** line item will be 0.2, which is 10% of total capacity of the group.

When a resource manager creates a Group type operation resource assignment for time off, this doesn't update the **Operational work** line item but reduces the total available capacity.

Consider the same group for which resource manager creates an operation resource assignment for 25% of the capacity for time off, for a quarter from April to June. The total available capacity of the group for the quarter April to June will be 1.5 FTE, which is 75% of the total capacity after reducing the 25% time off.

0.5 FTE, which is 25% of total capacity of the group will be reduced.

**Note:** The **Operational work** line item is highlighted in gray color.

![Capacity view showing Operational work in a red highlight box.](../images/cp-operational-rsrc-asgnmnt.png)

