---
title: Access, assign, and approve unassigned work in Project Workspace
description: View, assign and authorize resources directly from Project Workspace without navigating to Resource Management Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/project-workspace/assign-approve-unassigned-work-pw.html
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-02-18"
reading_time_minutes: 3
breadcrumb: [Resource assignments in Project Workspace, Plan resources, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Access, assign, and approve unassigned work in Project Workspace

View, assign and authorize resources directly from Project Workspace without navigating to Resource Management Workspace.

## Before you begin

Role required: it\_project\_manager

## About this task

In Project Workspace, when you select **Resources** page from the left menu, you are redirected to a page that displays the project associated resources and their resource assignments for better resource planning. By embedding the resource page through interoperability, the Project Workspace application supports these actions:

-   View assigned and unassigned work from the resource page.
-   Assign unassigned work using automatic or manual effort distribution.
-   Preview real-time effort allocations before assignment.
-   Identify resource availability and over-utilization using visual indicators.
-   Approve, unapprove, or reprioritize assignments by changing the resource status directly from the resource page.
-   Extend or update assignments without leaving Project Workspace.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  Open the resource page of the project by selecting **Resources** page from the left menu.

3.  Enable the Unassigned tasks toggle \(\[Omitted image "rmw-unassigned-tasks-toggle.png"\] Alt text: Unassigned tasks toggle.\) to view the unassigned work requests in the lower pane.

    \[Omitted image "resource-board-pw.png"\] Alt text: Resource board view of a Project in Project Workspace.

    You can create resource assignments based on the primary attributes \(Group, Skill, or Role\). You can see a comprehensive view resource allocations and group them by primary group, skill, role, owner, and parent item.

4.  From unassigned tasks pane, select the context menu row \(\[Omitted image "row-context-menu-icon.png"\] Alt text: 3 vertical dots denoting the row context menu.\) for any task and select **Assign Work**.

5.  You can assign work using one of the following ways.

<table id="choicetable_qth_yqy_khc"><thead><tr><th align="left" id="d217809e158">

Assign work choices

</th><th align="left" id="d217809e161">

Description

</th></tr></thead><tbody><tr><td id="d217809e167">

**Auto Assign**

</td><td>

The system automatically identifies all resources based on the selected primary attributes and distributes the work equally among the resources.In the Assign resources window, select **Assign resources automatically** from the Assign resources list.

</td></tr><tr><td id="d217809e181">

**Manual Assign**

</td><td>

Enables you to choose specific resources and decide how much effort to allocate. There are two sub options which you can choose.1.  Select the required resources from the Select resources list. You can assign efforts using one of the following sub options:
    1.  Select the **Distribute entire efforts equally** option to distribute the entire requested effort equally among the selected users.
    2.  Select the **Distribute partial effort equally** option and enter the required efforts in the field.
2.  Partial Effort Equally: Assign only the entered efforts equally among the selected resources.


</td></tr></tbody>
</table>    **Note:** Remaining efforts after equally distributing the work among the users is retained in the Unassigned tasks tray. Resource managers can again allocate these efforts.

6.  Select the **Preview** button to see the real-time allocations before assigning the work.

7.  Select the **Assign** button to assign work to the resources.

    The assigned work is reflected in the top pane nested by resource view and will be in Pending state \(\[Omitted image "rmw-pending-state.png"\] Alt text: Yellow rectangular pending state icon.\).

8.  Expand a resource row using the expand row icon \(\[Omitted image "icon-expand-arrow.png"\] Alt text: expand row icon.\) to view assigned tasks.

9.  Double-click in the Resource status column and select **Approve** to confirm the assigned work so the resource can start working.

    While assigning the work, you can easily identify if a resource is available \(\[Omitted image "rmw-green-tick.png"\] Alt text: Green tick mark within a green circle indicating the resource allocation is within the available bandwidth.\) or overutilized \(\[Omitted image "rmw-red-warning.png"\] Alt text: Red exclamation mark within a red triangle indication the resource is overallocated.\), even for the future periods, using the iconography.

10. You can change the status of any assigned assignments using one of the following options.

    |Choice|Description|
    |------|-----------|
    |**Approved**|Approve the assigned work to confirm the work.|
    |**Unapproved**|Unapprove any efforts that don't required work due to a change of business need or priority planning.|
    |**Pending**|Move approved or unapproved tasks to pending to reprioritize the work requests.|


## Result

The assigned work items are Approved \(\[Omitted image "rmw-approved-state.png"\] Alt text: Green rectangular approved state icon.\) or Unapproved \(\[Omitted image "rmw-unapproved-state.png"\] Alt text: Pink rectangular approved state icon.\) and the status of the work assignments is rolled up to the resource level.

## What to do next

-   Reassign or unassign any assigned work from the Project Workspace. For more information, see [Reassign or unassign work using Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/resource-management/rmw-reassign-unassign-work.md).
-   Split resource assignments at a specific date from the Project Workspace. For more information, see [Split resource assignments using Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/resource-management/split-resource-assignment-rmw.md).

**Parent Topic:**[Resource assignments in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/resource-assignments-pw.md)

