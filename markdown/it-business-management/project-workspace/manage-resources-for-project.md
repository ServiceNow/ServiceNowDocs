---
title: Create and manage resource plans for a project in classic Project Workspace
description: As a resource requester, find the availability of the resources, and create and manage the resource plans for the project and project tasks in the project workspace.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Project workspace classic - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Create and manage resource plans for a project in classic Project Workspace

As a resource requester, find the availability of the resources, and create and manage the resource plans for the project and project tasks in the project workspace.

**Important:**

Classic Project Workspace is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Use new Project Workspace with enhanced UI to help you efficiently manage your projects.

## Before you begin

Role required: it\_project\_manager

## About this task

The **Resources** tab in project workspace shows the resource plans for the selected project in an editable grid view. The tab consists of the following sections:

-   **Resource grid**

    It is the top section on the page that enables you to:

    -   Create resource plans for the project or its tasks. You can create a resource plan at a group, role, or user level.
    -   View and manage all the resource plans for the open project and its tasks in one place.
    -   View resource allocations for each resource plan in a grid view.
    Use the grid view in the tab to:

    -   Edit the planned and allocated hours inline without opening the record in a form.
    -   Group, hide, or show columns as per your requirement.
    -   Hide cancelled or completed resource plans.
    -   Request, confirm, or allocate a resource plan.
    -   Move a resource plan and its allocations to a future date for a group, role, or user resource plan.
    -   Replace a user with another user for a group, role, or user resource plan to accommodate situations like a user taking leave during a project.
    -   Request extension of an allocated resource plan.
    -   Shift allocation of a user to a future date for a group or role resource plan.
    -   Identify the resource plans created with specific members preference by viewing the **Resource plan created with specific members** icon \(![Icon for resource plans created with specific members preference](../image/specificmember_allocation_wb_grid.png)\) next to the resource plans.
-   **Resource Finder**

    The section is available at the bottom of the page. The section is hidden by default. It can be made visible by clicking the resource finder icon \( ![Resource Finder icon](../../planning-and-policy/image/ResourceFinderIcon.png) \) in the top right of the page. It enables you to:

    -   Search the resources and view their availability. You can search the resources by group, role, or user.
    -   Add resource plans for the searched resources to the project and its tasks.
    -   Search for resources and view their availability and utilization. You can search resources by group, role, or user.
    -   Add or confirm resource plans for the current resources.
    -   Configure the Actuals column using Detailed View.
    -   Filter resources in the Resource Finder by available, overallocated, or all resources.
    -   Identify resources that are created as specific members for a resource plan by viewing the **Member specified in the resource plan** icon \(![Icon for resources created as specific members](../image/specificmember_allocation_wb_grid.png)\) next to the resources.
    -   View the Resource Availability and Resource Capacity grids by clicking on a capacity or availability column.

        You can view the user and resource allocation details in a pop-up window by selecting the **User** and **Allocated Hours** columns respectively in the **Resource Availability** grid.


When you select a resource plan in the resource grid section, the availability details of that resource are displayed in the resource finder section. For example, if a group resource plan is selected, the availability details of the group and its members are displayed in the Finder section. When you change the selection, the finder is automatically updated based on the current selection.

## Procedure

1.  [Open](access-the-project-workspace.md) the required project in project workspace.

2.  Click the **Resources** tab.

    -   To [create a resource plan](../../resource-management/task/t_CreateResourcePlanProjectTask.md), click **New**.
    -   To view the allocations in weekly or monthly format in the grid, click **Week** or **Month** button. The selected option changes the grid view in both the resource grid and resource finder sections.

        The time duration in the grid is displayed based on the earliest start date of the project or resource plans, and the last end date of the project or resource plans.

    -   To view the allocations in hours, FTE, or person days format in the grid, click **Hours**, **FTE**, or **Person Days** option in the list. The selected option changes the grid view in both the resource grid section and resource finder section.
    -   To [search the resources and create a resource plan for them](../../resource-management/task/create-resource-plan-with-finder.md), click the resource finder icon \( ![Resource Finder icon](../../planning-and-policy/image/ResourceFinderIcon.png) \).
    -   To show or hide certain columns from the grid view, click the configuration icon \(![Configuration icon](../image/configuration_investment.png)\). Hiding or displaying an item column does not update the table. Grouped columns cannot be hidden.
    -   To view the resource allocations at user level, expand a resource plan in the grid. The user level allocations are listed only for Group and Role resource plans.
    -   To edit the planned and allocated hours inline in the grid, double-click a row. You can update the planned hours for future period for resource plans in Requested, Confirmed, and Allocated state.
    -   To view and update resource plan details in a form, click the information icon \( ![Information icon](../../planning-and-policy/image/informationicon.png) \) in the beginning of the resource plan row.
    -   To request a resource plan in the **Actions** column, click the actions icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png) \) and select **Request**.
    -   To delete a resource plan in the **Actions** column, click the actions icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png) \) and select **Delete**.
    -   To request all the resource plans created for the project in the **Actions** column, click the actions icon \(![Actions icon](../../planning-and-policy/image/ellipsis-vertical-icon.png)\) in the project row and select **Request All**. The icon is enabled when at least one of the listed resource plans for the project is in the Planning or Rejected state.

**Parent Topic:**[Project workspace classic - Legacy](../concept/project-workspace-classic.md)

