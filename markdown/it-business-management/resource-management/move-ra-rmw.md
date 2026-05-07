---
title: Move a resource assignment
description: Move a resource assignment to a different start and end dates depending on the availability of the resource.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Move a resource assignment

Move a resource assignment to a different start and end dates depending on the availability of the resource.

## Before you begin

Role required: resource\_user, resource\_manager

## About this task

-   The resource assignment dates honor the task dates. The start and end dates of the resource assignments should be within the task start and end dates.
-   When a resource assignment is moved beyond the task dates, the allocations outside the dates are cleared.
-   You cannot move a resource assignment if actual efforts are captured for the work.

    Use the **Show actuals** toggle \(![Toggle button to view actual hours in Resource Management Workspace](../images/rmw-show-actuals-toggle.png)\) from the settings \(![Gear icon to view or hide settings side panel.](../images/rmw-settings-panel-icon.png)\) side panel to view the efforts captured for an assignment via time cards.


## Procedure

1.  Navigate to **Workspaces** &gt; **Resource Management Workspace**.

2.  Select the Resource cards icon \(![Resource cards icon.](../images/rmw-resource-cards-L1-icon.png)\) from the menu and open a resource card.

    Alternatively, you can access a resource board by accessing a widget from the overview dashboard.

3.  Select the chevron icon \(![Chevron](../images/rmw-chevron-image.png)\) for drill down view of the tasks assigned to resources.

4.  In the top tray, select the row context menu \(![Three vertical dots icon for row context menu.](../../project-workspace/image/icon-row-context-menu.png)\) for the required task and select **Move**.

5.  In the move assignment modal, you can either enter or select the new start date using the date picker modal from the **New start date** field.

6.  Change the assignment status using the **New status** list.

7.  Select **Confirm**.


## Moving a resource assignment

Let's consider a resource assignment for Website Overhaul task is assigned to Grace Lee. The task duration is from August 01, 2025 to August 31, 2025. The assignment duration is from August 01, 2025 to August 20, 2025. Now, when you move the assignment start date to August 15, 2025; the new assignment dates will honor the task dates and will auto-assign the work from August 15, 2025 to August 31, 2025. The remaining efforts of the resource are cleared and the cleared capacity is shown as available.

**Parent Topic:**[Using Resource Management Workspace](../concept/using-rmw.md)

