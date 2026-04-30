---
title: Use Resource Finder to analyze resource availability
description: Search and analyze resource availability using the Resource Finder, so that you can create resource plans for a project or demand.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Use Resource Finder to analyze resource availability

Search and analyze resource availability using the Resource Finder, so that you can create resource plans for a project or demand.

## Before you begin

Role required: it\_project\_manager, it\_demand\_manager, or resource\_manager

## About this task

In the Resource Finder, search for the resources that you need, and create a plan for the selected resources.

-   Steps 1 and 2 take you to the resource finder.
-   Step 3 provides guidance on different options to filter and analyze the resources availability. Choose the options that suit your needs.
-   Step 4 shows how to create a new resource plan for the selected resources.

## Procedure

1.  Open the Resource Plans page for a project or demand.

<table id="choicetable_b5v_xq4_tcb"><thead><tr><th align="left" id="d102634e118">

Option

</th><th align="left" id="d102634e121">

Steps

</th></tr></thead><tbody><tr><td id="d102634e127">

**From a project**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open a project record.
3.  In the **Resource Plan** related list, click **Manage** to open the Resources tab.


</td></tr><tr><td id="d102634e166">

**From a demand**

</td><td>

1.  Navigate to **Demand** &gt; **Demands** &gt; **All**.
2.  Open a demand.
3.  In the **Resource Plans** related list, click **Manage** to open the Resource Plans page.


</td></tr><tr><td id="d102634e205">

**From Allocation Workbench**

</td><td>

1.  Navigate to **Resource** &gt; **Resource Workbench** &gt; **Allocation Workbench**.
2.  In the Allocation Boards page, select the desired allocation board.


</td></tr></tbody>
</table>2.  Select the project or demand in the resource grid section and click the resource finder icon \(![Resource Finder](../../planning-and-policy/image/ResourceFinderIcon.png)\).

    The resource finder section opens at the bottom of the page. A list of up to 50 records are displayed initially. If you have more than 50 resources, you can load them by clicking **Get More**.

3.  Use the following options to filter and analyze the capacity of the resources.

<table id="table_up2_2yn_fsb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display available or over allocated resources

</td><td>

Using the Show/Hide menu \(![Show/Hide](../image/show-hide-icon.png)\) to filter resources by available or over allocated.

</td></tr><tr><td>

Perform a simple search

</td><td>

Search the resources by group, role, or user attributes, by selecting the search criteria.

 ![Resource finder simple search](../image/resource-finder-simple-search.png)

</td></tr><tr><td>

Build your own search criteria

</td><td>

Use the advanced search to add your filter conditions.

 For example, select **Search by group**, click **Advanced**, then click the Advanced search filter icon \(![Advanced search](../../project-management/image/filter_icon.png)\). Here you can add conditions to filter this group further.

**Note:** While adding filters, ensure that you do not add an AND condition for different values of the same attribute. For example, do not filter the user group with conditions for Skill **X** AND Skill **Y**.

 ![Advanced search in resource finder](../image/resource-finder-advanced-search.png)

</td></tr><tr><td>

View the availability of the resources for an extended duration

</td><td>

Use the options from the date range selector.

 From the Xanadu release onwards, you can select a custom date range.

 ![Custom date range.](../image/resource-finder-custom-date-range.png)

 The value of the property **Maximum time duration in Resource Finder in months** determines the maximum duration for which the resource details are displayed in the resource finder.

</td></tr><tr><td>

Analyze the resources list

</td><td>

Use the Configuration menu \(![Configuration](../image/ConfigurationIcon.png)\) to analyze different constraints such as the capacity, availability, actual hours, and others for different time periods.

 By default, only the Availability hours are displayed. To view other details, select Detailed View \(![Detailed view](../image/detailed-view.png)\), and select the required columns from the Configuration menu \(![Configuration](../image/ConfigurationIcon.png)\).

 ![Configuration menu in resource finder.](../image/resource-finder-configuration-menu.png)

 Displaying the requested hours for a user group or role helps you understand immediately if you need to fulfil any resource requests and to do so, if you have enough capacity for that user group or role.

 The **Requested** column would not be available in the Configuration menu under the following conditions.

-   Filtering the resource list further using simple or advanced filters
-   Using the resource finder in the availability view
-   Using the show available or show over allocated options from the Show/Hide menu
Even if the column is already enabled, but any of the above conditions are later met, the **Requested** column is disabled automatically.

 All non-project events created for a user from the calender appear as Operational Work for the user in Resource Finder.

</td></tr><tr><td>

Update the capacity of a resource

</td><td>

Right-click on the user and select **Update Capacity**.

 ![Update capacity option.](../image/update-capacity.png)

</td></tr></tbody>
</table>4.  Select the resources you want to create resource plans for and click **Add New Plan**.


## Result

-   The resource plan is created in the Planning state with zero planned hours.
-   The resource plan appears as a row at the top in the resource plan list of the project or demand. Based on the type of resource selected in finder, the resource plan has one of the following prefixes:

    -   \[G\] for a resource plan created for a group.
    -   \[R\] for a role resource plan created for a role.
    -   \[U\] for a user resource plan created for a user.
    **Note:** The resource plan that is created last appears at the top in the resource plan list of a project or demand.


## What to do next

-   Update the planned hours for the resource plan using the resource grid.
-   To view and update more details for the resource plan, click the information icon \(![information](../../planning-and-policy/image/informationicon.png)\) in the beginning of the resource plan row.
-   You can now [request the resource plan](t_RequestResourcePlanApproval.md).

**Parent Topic:**[Resource plans](../concept/c_ResourcePlans.md)

**Related topics**  


[Create a resource plan](t_CreateResourcePlanProjectTask.md)

[Create an operational resource plan](create-operational-plan.md)

[Request resources](t_RequestResourcePlanApproval.md)

[Confirm a resource plan](confirm-resource-plan.md)

[Confirm and allocate a resource plan](confirm-allocate-resource-plan.md)

[Request a change to a resource plan](t_RequestAChangeToAResourcePlan.md)

[Recalculate costs of a resource plan of a project or demand](recalculate-resource-costs.md)

[Update cost plan related to a resource plan](t_UpdateRelatedCostPlan.md)

[Complete a resource plan](t_CloseAResourcePlan.md)

[Cancel a resource plan](t_CancelAResourcePlan.md)

[Delete a resource plan](t_DeleteAResourcePlan.md)

[Extend a resource plan](extend-resource-plan.md)

[Request extension of an allocated resource plan](request-extension-allocated-resource-plan.md)

[Allocate resources for the extended period](allocate-resources-for-extended-period.md)

[Reduce the duration of a resource plan](reduce-resource-plan.md)

[Time zones in resource plans](../concept/c_TimeZonesInResourcePlans.md)

[Associate a time card with a resource plan](t_AssocATimeCardWithAResourcePlan.md)

