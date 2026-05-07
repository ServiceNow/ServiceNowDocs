---
title: Reassign or unassign work using Resource Management Workspace
description: Reassign or unassign any assigned work from the Resource Management Workspace. You can group the resource board by primary attributes to identify the resources with same primary attributes.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Reassign or unassign work using Resource Management Workspace

Reassign or unassign any assigned work from the Resource Management Workspace. You can group the resource board by primary attributes to identify the resources with same primary attributes.

## Before you begin

-   When you reassign work, the primary attributes of both the resource should match. For more information about mapping primary attributes to resources, see [Map primary attributes to resources](../../spw-capacity-planning/task/map-primary-attributes-cp.md).
-   You can reassign a work item for the period for which actual hours are not captured.
-   You cannot reassign a work item if it has associated actual hours captured for the entire duration.
-   You cannot unassign a work item if it has any associated actual hours captured.
-   You cannot unassign an assignment if it has any associated actual hours captured.
-   You cannot reassign or unassign group resource assignments.

Role required: resource\_user, resource\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Resource Management Workspace**

2.  Select the Resource cards icon \(![Resource cards icon.](../images/rmw-resource-cards-L1-icon.png)\) from the menu and open a resource card.

3.  Select the chevron icon \(![Chevron](../images/rmw-chevron-image.png)\) to expand the resource view in the top tray.

4.  To reassign any assigned work:

    1.  Select the row context menu \(![Three vertical dots icon for row context menu.](../../project-workspace/image/icon-row-context-menu.png)\) for the required work item.
    2.  Select **Reassign work**.

        **Tip:** [Group the resource board](../concept/using-rmw.md#section_mcj_3sl_cdc) by the primary attributes to drag and drop the resource assignments to another resource to completely reassign work.

    3.  On the Reassign work window, enter the name of the resource in the **User** field to whom you want to reassign the work and duration using the **Start month** and **End month** date picker.

        ![Reassign work window displaying current user assignment and options to select another resource to reassign work.](../images/rmw-reassign-work-window.png)

5.  Select **Update**.

    **Note:** Use the reassign feature to assign a partial or fraction of a task among resources without overlapping the assignment dates.

    The selected work item will be reassigned to the selected resource.

6.  To unassign any assigned work:

    1.  Select the row context menu \(![Three vertical dots icon for row context menu.](../../project-workspace/image/icon-row-context-menu.png)\) for the required work item.
    2.  Select **Unassign work**.
    The selected work item will be moved to Unassigned task tray.


## Result

The reassigned tasks are assigned to the selected resource and unassigned tasks are moved to the Unassigned tasks tray.

## Reassigning work

Consider a development task spanning from January 1, 2024 to September 30, 2024 which is assigned to Tom, a developer who has the following primary attributes.

-   Primary Group - Development
-   Primary Skill - Java
-   Primary Role - Java Developer 1

Tom has actual hours captured from January 1, 2024 through March 31, 2024 and will be unavailable for next 2 months.

As a resource manager, you can either reassign this task in it's entirety starting from April 1, 2024 till September 30, 2024 to Raj, who has the same primary attributes. Or reassign the task from April 1, 2024 to May 31, 2024 to Raj, leaving the rest of the assignment to Tom.

The actual hours captured by Tom are retained even though the task is reassigned. Raj can capture the actuals hours for the assigned period after completing the work.

## What to do next

You can allocate the unassigned work and approve the reassigned work. For more information, see [Assign and approve unassigned work using Resource Management Workspace](allocate-resources-rmw.md).

**Parent Topic:**[Using Resource Management Workspace](../concept/using-rmw.md)

