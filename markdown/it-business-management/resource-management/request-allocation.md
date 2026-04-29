---
title: Create requested allocations for a resource plan
description: Requested Allocations are automatically created when a resource plan is submitted and is in Planning state. If required, the resource requester can create new requested allocations for a resource plan in Planning or Rejected state. Resource managers can create requested allocations for the plans in Requested state.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Create requested allocations for a resource plan

Requested Allocations are automatically created when a resource plan is submitted and is in Planning state. If required, the resource requester can create new requested allocations for a resource plan in Planning or Rejected state. Resource managers can create requested allocations for the plans in Requested state.

## Before you begin

Role required: resource\_user

## About this task

A requested allocation doesn’t have an allocation for a named resource. It only details the start date, end date, and the planned hours.

To specify the breakup of resource requirements for monthly or weekly Allocations types, you can modify the requested allocations. For example, if you've requested 100 hours of a resource from January to February, but you want 20 hours in January and 80 hours in February. You can specify these details on the Requested Allocations form.

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Plans** &gt; **Planning** or **Rejected**.

2.  Open a resource plan.

3.  In the **Requested Allocations** related list, select **New**.

4.  On the Requested Allocation form, fill in the fields.

    For a description of the field values, see [Requested Allocation form](../reference/requested-allocation-form.md).

5.  To save the record and return to the resource plan, select **Submit**.


## Example

If a resource is requested from September 1 to Nov 30 for 360 hours, requested allocation records are created as follows:

-   **Case 1: Plan duration allocation type**

    For a plan duration [allocation type](t_CreateResourcePlanProjectTask.md), the following requested allocation records would be created:

    |Start date|End date|Planned hours|
    |----------|--------|-------------|
    |Sep 01 \(Resource plan start date\)|Nov 30 \(Resource plan end date\)|360|

-   **Case 2: Monthly allocation type**

    For a monthly allocation type, hours are proportionally distributed based on working days as follows:

    -   Total working days for the planned duration = 65 days
    -   Hours to allocate per working day = `360/65` = 5 hours
    The following requested allocation records would be created:

    |Start date|End date|No. of working days|Planned hours|
    |----------|--------|-------------------|-------------|
    |Sep 01|Sep 30|22|22 \* 5 = 110|
    |Oct 01|Oct 31|21|21 \* 5 = 105|
    |Nov 01|Nov 30|22|22 \* 5 = 110|


For a weekly allocation, requested allocation records created similar to monthly. Three allocation records, one for each month are created.

**Parent Topic:**[Resource Management classic](../concept/c_ResourceManagement.md)

