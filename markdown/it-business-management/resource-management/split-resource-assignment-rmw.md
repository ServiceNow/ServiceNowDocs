---
title: Split resource assignments using Resource Management Workspace
description: Splitting a resource assignment at a specific date creates a resource assignment for the same user.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Split resource assignments using Resource Management Workspace

Splitting a resource assignment at a specific date creates a resource assignment for the same user.

## Before you begin

-   When you split a resource assignment, a new assignment is created from the selected date. Both the assignments are assigned to the same user retaining the state of the assignment.
-   When you split a resource assignment, a new assignment is created from the selected date. Both the assignments are assigned to the same user with Approved state.
-   If a resource assignment has actuals captured for a certain duration, you can split the work only at the dates where there are no actuals captured.
-   Role required: resource\_user, resource\_manager

## About this task

When to use split or reassign for assignments.

Use Split when you need to divide a single resource's assignment into two time periods with different allocation levels, effort distributions, or tracking granularity. For example, split an assignment when a resource needs to reduce their allocation after a project milestone. Use Reassign \([Reassign or unassign work using Resource Management Workspace](rmw-reassign-unassign-work.md)\) when you need to transfer work from one resource to another.

## Procedure

1.  Navigate to **Workspace** &gt; **Resource Management Workspace**.

2.  Select the Resource cards icon \(![Resource cards icon.](../images/rmw-resource-cards-L1-icon.png)\) from the menu and open a resource card.

3.  Select the chevron icon \(![Chevron](../images/rmw-chevron-image.png)\) to expand the resource view in the top tray.

4.  In the top tray, select the row context menu \(![Three vertical dots icon for row context menu.](../../project-workspace/image/icon-row-context-menu.png)\) for the required work item and select **Split**.

    Split modal appears providing you with the insights related to the task such as name of the task, name of the resource, start date, and end date.

5.  On the Split modal, select a date to split the resource assignment using the date picker.

6.  Select **Split**.


## Result

The resource assignment is split at the selected date and a copy of the resource assignment with new dates are displayed under the assignments of the selected resource.

## Split resource assignment

Consider a resource assignment named `Implement GenAI in docs` assigned to Abel Tuter from July 16 through December 02. If you split the resource assignment at September 09, there will be two resource assignments with the same name and state assigned to Abel Tuter.

One resource assignment ranges from July 16 to September 09, and the other assignment ranges from September 10 to December 02.

![Split of a resource assignment.](../images/rmw-split-ra-view.png)

Here, you can see an overlap of efforts for `Implement GenAI in docs` in month of September because the split is happening from September 10.

**Parent Topic:**[Using Resource Management Workspace](../concept/using-rmw.md)

