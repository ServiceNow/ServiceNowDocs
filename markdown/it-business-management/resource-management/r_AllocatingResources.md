---
title: Resource allocation
description: After resource requesters create a resource plan, resource managers can confirm the resources to move the plan to the Confirmed state. Resource managers can then allocate resources to the plan and move it to the Allocated state.
locale: en-US
release: zurich
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource allocation

After resource requesters create a resource plan, resource managers can confirm the resources to move the plan to the Confirmed state. Resource managers can then allocate resources to the plan and move it to the Allocated state.

Based on calendar and schedule information, resource managers view resource availability and select the resources under their management that can be confirmed and allocated to specific tasks.

## Soft and hard allocations

When a resource plan moves to the Confirmed state, resource allocations corresponding to [requested allocations](../task/request-allocation.md) are created automatically. The **Booking type** for these allocations is **Soft**. Soft allocations are like temporary allocations for the requested users and do not create any calendar events.

When the plan is moved to the Allocated state, the **Booking type** changes from **Soft** to **Hard**. For a hard booking, the resource is assigned to the plan and is not available for other plans during the allocated times. The booked time also appears on the user calendar. If the requested resource cannot be allocated for the entire allocation duration, the allocation record booking type remains as soft.

Any errors or warnings during allocations are logged in the Resource Plan Logs related list on the Resource Plan form. You can review these logs to take correct actions for further resource allocation.

**Note:** The resource property **com.snc.resource\_management.allocation\_interval\_minutes** enables the creation of soft and hard allocations with a decimal value.

## Calculation of hours for soft allocations

-   **Case 1: Proportional distribution**

    For example, the requested allocation for a group with two resources when the **Members preference** value is set to **All members** or **Specific members** is as follows:

    |Start date|End date|Planned hours|
    |----------|--------|-------------|
    |October 03|October 07|40|

    The [planned hours](../task/t_CreateResourcePlanProjectTask.md) on the Resource Plan form are proportionally distributed among all the requested allocations based on number of working days for each requested allocation record.

    |Resource|Resource time-off|Available capacity \(hours\)|Soft Allocation hours|
    |--------|-----------------|----------------------------|---------------------|
    |Resource 1|2 days|3 \* 8 = 24|24 \* 0.625 = 15|
    |Resource 2| |5 \* 8 = 40|40 \* 0.625 = 25|

    The following calculations are used:

    -   `Total available capacity = Available capacity User 1 + Available capacity User 2 = 24 + 40 = 64 hours`
    -   `Hours to allocate per hour of available capacity = Planned hours/total available capacity = 40/64 = 0.625 hours`
    **Note:** Multiple soft allocations could be created for one requested allocation for group resource plans.

-   **Case 2: Most available resource requested first**

    For example, the requested allocation for a group with three resources when the **Members preference** value is set to **Any member** is as follows:

    |Start date|End date|Planned hours|
    |----------|--------|-------------|
    |October03|October 07|40|

    The system finds the most available resources in the specified time frame and creates soft allocations for these resources.

    |Resource|Available hours|Soft Allocation hours|
    |--------|---------------|---------------------|
    |Resource 1|24|10|
    |Resource 2|30|30|
    |Resource 3|20| |

    Resource 2 is the most available resource. The system creates soft allocations for resource 2 first until it consumes all available hours from resource 2. The system then moves to the next most available resource, and so on. Once available hours for all resources are consumed, and the planned hours are still left over after allocating across all members \(from most available to least available\), the remaining hours are equally distributed among all resources.


## Calculation of hours for hard allocations

-   **Case 1: Even spread**

    Selecting **Even** as hard allocation spread type creates resource events for the resource by splitting the hours evenly across all working days. The Smart Even Load allocation spread takes the availability of resources into account while allocating and only applies hours evenly where possible. If a resource is over-allocated for a day, it bypasses that day and resumes allocations to succeeding days until the resource plan is fulfilled.

    For example, for a resource requested for 20 hours in a week, the even spread hard allocation is as follows:

    |Day of the week|Monday|Tuesday|Wednesday|Thursday|Friday|
    |---------------|------|-------|---------|--------|------|
    |**Available hours**|6|6|6|6|Time-off|
    |**Allocated hours**|5|5|5|5|0|

-   **Case 2: Front load**

    Selecting **Front load** as the hard allocation spread type fills up all available resource slots from the start date of the allocation. Once the resource is fully allocated between start and end dates, the remaining hours are filled from the start date up to 24 hours.

    For example, for a resource requested for 20 hours in a week, the front load spread hard allocation is as follows:

    |Day of the week|Monday|Tuesday|Wednesday|Thursday|Friday|
    |---------------|------|-------|---------|--------|------|
    |**Available hours**|6|6|6|6|Time-off|
    |**Allocated hours**|6|6|6|2|0|


## Event creation during hard allocation

You can control the minimum unit for an event by modifying the Calendar Event Duration \(minutes\) \(**com.snc.resource\_management.allocation\_interval\_minutes property**\). The default is 60 minutes.

Resource allocations use this property to create allocations with a decimal value.  Use the following table to verify you set the property value correctly.

|Scheduled hours of the user|Calendar Event Duration value|
|---------------------------|-----------------------------|
|0.5|30|
|0.25/0.5/0.75|15|
|0.2/0.4/0.6/0.8|12|
|0.1, 0.2, and so on|6|

-   **Example: 4 hours for 1 week, with an allocation interval of 60 minutes**

    Creates a 60-minute block from Monday through Thursday.

    |Monday|Tuesday|Wednesday|Thursday|Friday|
    |------|-------|---------|--------|------|
    |60 mins|60 mins|60 mins|60 mins| |

-   **Example: 4 hours for 1 week, with an allocation interval of 30 minutes**

    If the value of this property is set to  30  minutes, and  1  hour needs to be allocated to the user, the allocation is divided into the two 30-minute blocks when the user is available.  This setting creates a 60-minute block from Monday through Wednesday and 30-minutes blocks for Thursday and Friday.

    |Monday|Tuesday|Wednesday|Thursday|Friday|
    |------|-------|---------|--------|------|
    |30 mins+30 mins|30 mins+30 mins|30 mins+30 mins|30 mins|30 mins|


**Note:** If the scheduled  hours are not divisible by  the Calendar Event Duration property, then there will be  a  loss  of few hours for each day.  For example, the per day scheduled  hours  per day are  8.5  and the property value is set to 60. Then, the  maximum  allocated  hours  for  each  day  will  be  8,  resulting  in  a  loss  of  0.5  hours  per  day.

## Time-off handling

Resource events from a resource plan are not created for the days where the resource has marked time-off or engaged in other events \(such as training and meetings\). An administrator can manage the resource capacity and allocation with the property, **com.snc.resource\_management.exclude\_events\_from\_schedule**, to specify:

-   Which events must be excluded for capacity calculations. For example, if a resource has time-off between Monday and Wednesday, the weekly capacity for the resource is calculated as 16 hours \(as opposed to 40 hours\).
-   When the system must not create allocations. For example, if a resource is in training on Friday, the resource is not allocated for a task on Friday.

## Over-allocation

Over-allocated resources are allowed. Over-allocating resources creates overlapping events in the user calendar within the user's scheduled hours. However, a maximum of 24 total hours can be allocated in any given day. Overlapping events appear overlapped in the calendar in the weekly view. In the monthly view, overlapping events appear above or below another event.

For example, a user has a schedule that specifies the daily work day from 08:00 to 17:00. Event 1 is in the user's calendar from 08:00 to 14:00. If an additional five hours are added for the same day for Event 2, an event is created for the three hours of free time \(14:00 to 17:00\). An overlapping event is also created for the remaining two hours, starting at the beginning of the day \(08:00 to 10:00\).

-   **[Create a resource role](../task/create-resource-role.md)**  
Define project-specific roles for team members based on their skills and competencies.
-   **[User resources and group resources](r_UserResourcesAndGroupResources.md)**  
When allocating resources, a resource manager might need to work with an administrator to add users to a group with pps\_resource role.
-   **[Create allocations](../task/t_AllocateWResAllocationsRelList.md)**  
Resource managers can create allocations using the Resource Allocations related list.
-   **[Reject a resource plan from the Resource Plan form](../task/t_RejectResourcePlanForm.md)**  
Resource managers can reject plans from the Resource Plan form or from the Resource Workbench.

**Parent Topic:**[Resource Management classic](../concept/c_ResourceManagement.md)

