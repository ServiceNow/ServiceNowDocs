---
title: User resources and group resources
description: When allocating resources, a resource manager might need to work with an administrator to add users to a group with pps\_resource role.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Resource allocation, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# User resources and group resources

When allocating resources, a resource manager might need to work with an administrator to add users to a group with pps\_resource role.

## Resource Manager view

The Resource Manager view in **Resource** &gt; **Resources** &gt; **Users** lists only the users who have the pps\_resource role. In addition to some of the fields displayed in the User Administration &gt; [Users](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) form, the Resource Manager View &gt; Users form also displays the following fields, which are editable only by a user with resource\_manager role:

-   **Location**
-   **Schedule**
-   **Timesheet Policy**
-   **Average Daily FTE Hours/Hours Per Person Day**

    **Note:** Use the Update Resource Capacity related link to specify a date range. User capacity is populated in all aggregate tables based on the schedule of the user.


The Resource Manager view in **Resource** &gt; **Resources** &gt; **Groups** lists only the groups with the pps\_resource role. When a resource manager creates a new group from this view, the pps\_resource role is added by default to the group record. Although resource managers have write access to several fields, the only fields that they should edit are **Average Daily FTE Hours/Hours Per Person Day** and **Hourly rate**.

-   **[Update the resource capacity](../task/update-resource-capacity.md)**  
From the Resource Manager view, update the capacity of a user for a specific duration. Based on the schedule of the user and the specified duration, the capacity of the user is accordingly populated in all resource aggregate tables.
-   **[Update the resource aggregates](../task/update-aggregate-capacity.md)**  
From the Resource Manager view, you can update the resource aggregates for a specific time frame.

**Parent Topic:**[Resource allocation](r_AllocatingResources.md)

**Related topics**  


[Create a resource role](../task/create-resource-role.md)

[Create allocations](../task/t_AllocateWResAllocationsRelList.md)

[Reject a resource plan from the Resource Plan form](../task/t_RejectResourcePlanForm.md)

