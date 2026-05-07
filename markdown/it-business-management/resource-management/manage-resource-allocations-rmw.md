---
title: Manage resource allocations in Resource Management Workspace
description: Manage resource allocations to change efforts, start and end dates, extend and so on to adjust resources based on their availability and the priority of the tasks.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Manage resource allocations in Resource Management Workspace

Manage resource allocations to change efforts, start and end dates, extend and so on to adjust resources based on their availability and the priority of the tasks.

## Before you begin

Role required: resource\_user

## Date handling for allocation changes

When you extend or modify resource allocations, the system uses the following date logic:

-   Projects: The allocation dates are bounded by the project task's planned start and end dates. If the task has actual dates, those take precedence over planned dates.
-   Demands: The allocation dates are bounded by the demand's planned start and end dates. If no end date is set on the demand, the allocation can be extended indefinitely.

You cannot extend an allocation beyond the parent record's end date without first updating the project task or demand dates. If the allocation dates exceed the parent boundaries, the system may truncate the allocations or display a warning.

## Procedure

1.  Navigate to **Workspaces** &gt; **Resource Management Workspace**.

2.  Select the Resource cards icon \(![Resource cards icon.](../images/rmw-resource-cards-L1-icon.png)\) from the menu and open a resource card.

3.  Select the chevron icon \(![Chevron](../images/rmw-chevron-image.png)\) to expand the resource view in the top tray.

4.  Edit the following allocation details in the resource board drill-down view.

<table id="choicetable_sbf_jjn_bfc"><thead><tr><th align="left" id="d189241e113">

Choice

</th><th align="left" id="d189241e116">

Description

</th></tr></thead><tbody><tr><td id="d189241e122">

**Manage the assigned task details using inline editing**

</td><td>

Manage the Start date, End date, Task efforts, and Resource status.Example: For a task which is assigned from August to November, you can move the start date to September, freeing up the allocations of that users for August. To adjust any changes to the priority, you can change back the Start date to August. Once changed, the efforts for August will be empty and you can enter the required efforts in the right grid using the inline editing feature.

</td></tr><tr><td id="d189241e133">

**Extend a resource allocation**

</td><td>

Extend the duration of non-child assignments to extend the resource allocation for the required duration.1.  In the top tray, select the row context menu \(![Three vertical dots icon for row context menu.](../../project-workspace/image/icon-row-context-menu.png)\) of a non-child assignment and select **Extend**.
2.  In the Extend Assignment window, select the new end date and the required efforts.
3.  Select **Extend**.
Entered duration for the selected task and time is allocated.

</td></tr><tr><td id="d189241e167">

**Effort type view**

</td><td>

Use the inline editing feature to change the effort for any assigned task. The edited values will honor the effort type selection in the board view.After adjusting the allocation efforts, you can change the view to FTE, Person Days, or Hours. The changed allocation efforts will reflect the respective selected value.

</td></tr><tr><td id="d189241e178">

**Edit child assignments details in the Group Assignment modal**

</td><td>

View the group assignment details and their statuses in the Group Assignment window to manage the efforts and values. Select the assigned efforts value for any child task in the top tray to view Group Assignment window.In this window, you can view the Group, Task, Parent item, Start date, End date, Resource status, and the assigned users for this group type assignment.

Using this window, you can directly change the dates, effort value, and status to directly approve the assigned work.

</td></tr></tbody>
</table>
**Parent Topic:**[Using Resource Management Workspace](../concept/using-rmw.md)

