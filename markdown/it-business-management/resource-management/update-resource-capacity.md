---
title: Update the resource capacity
description: From the Resource Manager view, update the capacity of a user for a specific duration. Based on the schedule of the user and the specified duration, the capacity of the user is accordingly populated in all resource aggregate tables.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [User resources and group resources, Resource allocation, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Update the resource capacity

From the Resource Manager view, update the capacity of a user for a specific duration. Based on the schedule of the user and the specified duration, the capacity of the user is accordingly populated in all resource aggregate tables.

## Before you begin

Role required: resource\_manager

## About this task

Use the **Update resource capacity** related link in the following scenarios:

-   If a user is newly added and you want to update the capacity for the user.
-   If the schedule of an existing user is changed and you want to update the capacity of the user.

The scheduled job that is used for this action is Update resource capacity.

Capacity is generated for only the date range between employment start date and employment end date specified in the employee profile in the HR application. This information is available when the Employee Profile plugin is installed. If the start and end date are unavailable for an employee, manually specify these dates.

Also, if an employee is available after the year has begun, then the capacity is generated from the current year's beginning, to ensure that missing capacity is accounted for. For example, if the employee's capacity is available from March 1, 2022 to June 1, 2022, then the updated capacity is generated from January 1, 2022 to June 1, 2022.

Capacity and availability for terminated resources is automatically updated to 0 when you run the Resource Termination Handler job when the termination date is after the date on which the job is run. If resources are booked for a time period beyond the user's termination dates, those bookings are also updated to 0 in the resource plan.

Use the **Update resource capacity** related link in the following scenarios:

-   If a user is newly added and you want to update the capacity for the user.
-   If the schedule of an existing user is changed and you want to update the capacity of the user.

The scheduled job that is used for this action is Update resource capacity.

Before updating capacity for a new hire: Ensure the following are configured for the user before running the capacity update:

1.  Employment dates: Set the employment start date \(and optionally end date\) in the user's employee profile. Capacity is only generated within these dates. If the Employee Profile plugin is not installed, manually specify these dates on the user record.
2.  Schedule: Assign a work schedule to the user. The capacity calculation is based on the user's schedule \(for example, a standard 8-hour workday schedule\). Without a schedule, capacity values may be incorrect.
3.  PPS resource role: Ensure the user has the `pps_resource` role so they appear in resource plans and capacity views.

Capacity is generated for only the date range between employment start date and employment end date specified in the employee profile. If an employee is available after the year has begun, capacity is generated from the current year's beginning to ensure missing capacity is accounted for.

Capacity and availability for terminated resources is automatically updated to 0 when you run the Resource Termination Handler job.

## Procedure

1.  Navigate to **All** &gt; **Resource Management** &gt; **Resources** &gt; **Users**.

2.  Select a **User ID**.

3.  Select the **Update Resource Capacity** related link.

4.  In the window, provide a start date and end date.

    **Note:** You can’t select a start date that is before the employment start date or an end date that is after the employment end date when the Employee Profile plugin is installed.

5.  Select **OK**.


**Parent Topic:**[User resources and group resources](../reference/r_UserResourcesAndGroupResources.md)

