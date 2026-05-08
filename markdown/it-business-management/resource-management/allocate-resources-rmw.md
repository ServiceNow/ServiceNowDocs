---
title: Assign and approve unassigned work using Resource Management Workspace
description: Filter the unassigned work to view priority requests and assign them to resources. Quickly connect with the requester via Microsoft Teams to get additional insights and approve the assigned work using the inline editing feature.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Resource Management Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Assign and approve unassigned work using Resource Management Workspace

Filter the unassigned work to view priority requests and assign them to resources. Quickly connect with the requester via Microsoft Teams to get additional insights and approve the assigned work using the inline editing feature.

## About this task

The assign logic provides you with the flexibility and control for users when assigning work to resources. It addresses the following goals:

-   Efficiency: Quickly allocate unassigned tasks to available resources.
-   Personalization: Enables users to configure how effort is distributed—either automatically or manually.
-   Transparency: Get a preview of the real-time breakdown of effort allocation before assigning the work to resources.
-   Flexibility: Manual distribution supports custom selection of resources, which helps Resource managers manage work allocations based on the availability and remaining capacity of the resources.
-   Fairness: Distributes work equally among the resources maintaining a balanced work.

## Before you begin

-   Create an active employee definition for resources to view their allocation details on the Resource Management Workspace.
-   [Create a resource card](rmw-create-rsrc-card.md).
-   Role required: resource\_user, resource\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Resource Management Workspace**

2.  Select the Resource cards icon \(![Resource cards icon.](../images/rmw-resource-cards-L1-icon.png)\) from the menu and open a resource card.

    Alternatively, you can view unassigned tasks using the Unassigned assignment requests widget from the overview dashboard.

3.  In the Unassigned tasks tray, select the Row context menu for any task \(![3 vertical dots denoting the row context menu.](../../spw-financials/images/row-context-menu-icon.png)\) and select **Assign Work**.

4.  You can assign work using one of the following ways.

<table id="choicetable_qth_yqy_khc"><thead><tr><th align="left" id="d264634e157">

Assign work choices

</th><th align="left" id="d264634e160">

Description

</th></tr></thead><tbody><tr><td id="d264634e166">

**Manual Assign**

</td><td>

Enables you to choose specific resources and decide how much effort to allocate. There are two suboptions which you can choose.1.  Select the required resources from the Select resources list. You can assign efforts using one of the following suboptions:
    1.  Select the **Distribute entire efforts equally** option to distribute the entire requested effort equally among the selected users.
    2.  Select the **Distribute partial effort equally** option and enter the required efforts in the field.
2.  Partial Effort Equally: Assign only the entered efforts equally among the selected resources.


</td></tr><tr><td id="d264634e197">

**Auto Assign**

</td><td>

The system automatically identifies all resources based on the selected primary attributes and distributes the work equally among the resources.In the Assign resources window, select **Assign resources automatically** from the Assign resources list.

</td></tr></tbody>
</table>    **Note:** Remaining efforts after equally distributing the work among the users is retained in the Unassigned tasks tray. Resource managers can again allocate these efforts.

5.  Select **Preview** to see the real-time allocations before assigning the work.

6.  Select **Assign** to assign work to the resources.

    The assigned work is reflected in the top tray nested by resource view and will be in Pending state \(![Yellow rectangular pending state icon.](../images/rmw-pending-state.png)\).

7.  Expand a resource row using the chevron icon \(![Right pointed chevron icon.](../images/icon-expand-arrow.png)\) to view assigned tasks.

8.  Double-click in the Resource status column and select **Approve** to confirm the assigned work so the resource can start working.

    While assigning the work, you can easily identify if a resource is available \(![Green tick mark within a green circle indicating the resource allocation is within the available bandwidth.](../images/rmw-green-tick.png)\) or overutilized \(![Red exclamation mark within a red triangle indication the resource is overallocated.](../images/rmw-red-warning.png)\), even for the future periods, using the iconography.

9.  You can change the status of any assigned assignments using one of the following options.

    |Choice|Description|
    |------|-----------|
    |**Approved**|Approve the assigned work to confirm the work.|
    |**Unapproved**|Unapprove any efforts that don't required work due to a change of business need or priority planning.|
    |**Pending**|Move approved or unapproved tasks to pending to reprioritize the work requests.|

10. You can select the owner's name to collaborate with them over Microsoft Teams to get additional insights regarding the work.


## Result

The assigned work items are Approved \(![Green rectangular approved state icon.](../images/rmw-approved-state.png)\) or Unapproved \(![Pink rectangular approved state icon.](../images/rmw-unapproved-state.png)\) and the status of the work assignments is rolled up to the resource level.

## What to do next

If no tasks appear in the Unassigned tasks tray, verify the following:

1.  Verify the resource requests exist. Project Managers must create resource requests \(resource assignments with status Requested\) on project tasks. Navigate to the project and verify resource requests exist on the Resource Assignments related list.
2.  Check if primary attributes match. The resource card filter must match the primary attributes \(Group, Skill, or Role\) defined in the resource requests. Open your resource card and verify the filter criteria aligns with existing requests.
3.  Check if the employee profiles are generated. Verify employee profile definitions have been generated for the resources in your view.
4.  Request state is correct. Only resource requests in **Requested** state appear as unassigned. Requests that are already Assigned, Approved, or Cancelled don't show.
5.  Check the date range. Verify the resource card's date range overlaps with the resource request dates. Requests outside the visible time frame will not display.
6.  Confirm the permissions. Confirm you have the resource\_manager role, which is required to view and manage unassigned work.

**Parent Topic:**[Using Resource Management Workspace](../concept/using-rmw.md)

