---
title: Assign and approve unassigned work
description: Filter the unassigned work to view priority requests and assign them to resources. Get additional insights and approve the assigned work using the inline editing feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/assign-work-to-resources-dw.html
release: brazil
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 3
breadcrumb: [Manage resources for demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Assign and approve unassigned work

Filter the unassigned work to view priority requests and assign them to resources. Get additional insights and approve the assigned work using the inline editing feature.

## Before you begin

Role required: it\_demand\_manager

[Create an active employee definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/generate-profile-definition.md) for resources to view their allocation details on the Resources grids.

## About this task

The assign logic provides you with the flexibility and control for users when assigning work to resources. It addresses the following goals:

-   Efficiency: Quickly allocate unassigned tasks to available resources.
-   Personalization: Enables you to configure how effort is distributed—either automatically or manually.
-   Transparency: Provides a preview of the real-time breakdown of effort allocation before assigning the work to resources.
-   Flexibility: Manual distribution supports custom selection of resources, which helps manage work allocations based on the availability and remaining capacity of the resources.
-   Fairness: Distributes work equally among the resources maintaining a balanced work.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select the **Resources** tab.

    The resource grid opens for the demand's timeline, grouped by **Primary Group**.

5.  Select the row context menu \(\[Omitted image "icon-row-context-menu.png"\] Alt text: Three vertical dots icon for row context menu.\) for any unassigned task and select **Assign work**.

6.  Assign resources manually or automatically.

<table id="choicetable_qth_yqy_khc"><thead><tr><th align="left" id="d268577e147">

Assign work choices

</th><th align="left" id="d268577e150">

Description

</th></tr></thead><tbody><tr><td id="d268577e156">

**Assign resources manually**

</td><td>

Enables you to choose specific resources and decide how much effort to allocate. There are two suboptions.1.  Select the required resources from the Select resources list. You can assign efforts using one of the following suboptions:
    1.  Select the **Distribute entire efforts equally** option to distribute the entire requested effort equally among the selected users.
    2.  Select the **Distribute partial effort equally** option and enter the required efforts in the field.
2.  Partial Effort Equally: Assign only the entered efforts equally among the selected resources.


</td></tr><tr><td id="d268577e187">

**Assign resources automatically**

</td><td>

The system automatically identifies all resources based on the selected primary attributes and distributes the work equally among the resources.In the Assign resources window, select **Assign resources automatically** from the Assign resources list.

</td></tr></tbody>
</table>    **Note:** Remaining efforts after equally distributing the work among the users is retained as unassigned tasks. Demand managers can again allocate these efforts.

7.  Select **Preview** to see the real-time allocations before assigning the work.

8.  Select **Assign** to assign work to the resources.

    The assigned work is nested by resource view and is in the Pending state \(\[Omitted image "rmw-pending-state.png"\] Alt text: Yellow rectangular pending state icon.\).

9.  Expand a resource row using the chevron icon \(\[Omitted image "icon-expand-arrow.png"\] Alt text: Right pointed chevron icon.\) to view assigned tasks.

10. Double-click in the Resource status column and select **Approved** to confirm the assigned work so the resource can start working.

    |Choice|Description|
    |------|-----------|
    |**Approved**|Approve the assigned work to confirm the work.|
    |**Unapproved**|Unapprove any efforts that don't require work due to a change of business need or priority planning.|
    |**Pending**|Move approved or unapproved tasks to pending to reprioritize the work requests.|

    Iconography indicates if a resource is available \(\[Omitted image "rmw-green-tick.png"\] Alt text: Green tick mark within a green circle indicating the resource allocation is within the available bandwidth.\) or overutilized \(\[Omitted image "rmw-red-warning.png"\] Alt text: Red exclamation mark within a red triangle indicating the resource is overallocated.\), even in future periods.


## Result

The assigned work items are Approved \(\[Omitted image "rmw-approved-state.png"\] Alt text: Green rectangular approved state icon.\) or Unapproved \(\[Omitted image "rmw-unapproved-state.png"\] Alt text: Pink rectangular approved state icon.\) and the status of the work assignments is rolled up to the resource level.

## What to do next

If there are no unassigned tasks, verify the following:

1.  Verify the resource requests exist. Demand managers must create resource requests \(resource assignments with status Requested\) on demand tasks. Navigate to the demand details and verify resource requests exist on the Resource Assignments related list.
2.  Check if primary attributes match. The resource card filter must match the primary attributes \(Group, Skill, or Role\) defined in the resource requests. Open your resource card and verify the filter criteria aligns with existing requests.
3.  Check if the employee profiles are generated. Confirm that employee profile definitions have been generated for the resources in your view.
4.  Request state is correct. Only resource requests in the Requested state appear as unassigned. Requests that are already Assigned, Approved, or Cancelled don't show.
5.  Check the date range. Verify the resource card's date range overlaps with the resource request dates. Requests outside the visible time frame will not display.
6.  Confirm the permissions. Confirm you have the it\_demand\_manager role, which is required to view and manage unassigned work.

