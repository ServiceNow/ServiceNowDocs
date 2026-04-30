---
title: Allocate a cost center, department, or workplace entity
description: Assign either a cost center, department, or workplace entity to a workplace location. Manage space consumptions, expenses, workplace assignments, and reservations based on an employee cost center, department, or workplace entity.
locale: en-US
release: zurich
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Allocate a cost center, department, or workplace entity

Assign either a cost center, department, or workplace entity to a workplace location. Manage space consumptions, expenses, workplace assignments, and reservations based on an employee cost center, department, or workplace entity.

## Before you begin

**Important:** Starting from Workplace Core version 2.16.1, the allocation type **Department and cost center** is no longer available. A new allocation type **Workplace entity** is introduced that provides more advantages.

Role required: sn\_wsd\_spcmgmt.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration**.

2.  Select the applicable module.

    -   Spaces
    -   Rooms
    -   Areas
    -   Floors
    For example, if you want to allocate a cost center, department or a workplace entity to a floor, select the Floors module.

3.  Select the location to which you want to add the allocation.

4.  On the form, scroll down and select **New** in the Allocation related list.

5.  On the form, fill in the fields.

    **Note:** The **Start date** and **End date** fields follow the system time zone. Ensure that you fill in the dates in the context of the workplace location.

<table id="table_sdp_b5w_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Option to specify if you want to add a cost center, a department, or a workplace entity.

</td></tr><tr><td>

Cost center

</td><td>

Cost center to which you want to assign the floor. This field appears only when **Cost center** is selected in the **Type** field.

</td></tr><tr><td>

Department

</td><td>

Department to which you want to assign the floor. This field appears only when **Department** is selected in the **Type** field.

</td></tr><tr><td>

Workplace entity

</td><td>

Workplace entity to which you want to assign the space. This field appears only when **Workplace entity** is selected in the **Type** field. A parent entity and its child entity can be allocated to the same workplace location. The start and end date of the child entity must be within the start and end date of the parent entity.

</td></tr><tr><td>

Start date

</td><td>

Date on which the allocation begins.If the start date and end date are not filled, the allocation is considered permanent. If the start date is filled but the end date is not filled, the allocation is considered permanent after the start date.

</td></tr><tr><td>

End date

</td><td>

Date on which the allocation ends. You can set an end date only after setting a start date.After an allocation reaches the end date, the **Deactivate expired allocations** scheduled job sets the allocation record to inactive.

When the end date of the allocation is within thirty days, the **Allocation Expiry Notification** scheduled job sends a notification to the following users:

-   User assigned to the **Primary contact** field of the department
-   User assigned to the **Manager** field of the cost center
-   Users assigned to the **Managed by group** or **Managed by** field of the building
-   Users assigned to the **Managed by group** or **Managed by** field of the workplace entity


</td></tr><tr><td>

Allocation Profile

</td><td>

Specify if the allocation is for rent or for ownership. If the allocation is rented, select **Tenant**, otherwise, if the allocation is owned, select **Owner**.

</td></tr><tr><td>

Allocation Percentage

</td><td>

Specify the percentage of the allocation out of 100%. Ensure that the allocated percentage sums up to 100% including other allocations with the same allocation profile of the location. For example, if A and B allocations have **Tenant** as the allocation profile, then the allocation percentage of both A and B's tenancy in total must be 100 %, like 50-50%, or, 25- 75%, or any sum.

</td></tr><tr><td>

Active

</td><td>

Option to activate the allocation.

</td></tr><tr><td>

Location

</td><td>

Location for which you’re allocating the cost center, department, or a workplace entity. This field is automatically set to the name of the workplace location to which you’re adding the allocation.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

The allocation is added to the workplace location.

You can assign the allocation to the child locations such as areas, rooms, and spaces. Select the **Push down** option on the Floor or Area form to apply the allocation. The allocation is applied depending on the **Push down** setting specified in the child locations.

**Note:** For time-bound allocations, only the dates are considered for allocation.

**Parent Topic:**[Managing workplace locations](../concept/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus](add-a-campus.md)

[Add a building using Workplace Space Management](add-new-building.md)

[Add a floor using Workplace Space Management](add-a-floor.md)

[Add an area using Workplace Space Management](add-an-area.md)

[Add a room using Workplace Space Management](add-a-room.md)

[Add a space using Workplace Space Management](add-a-space.md)

[Configure a workspace or desk as flexible or permanent](assign-a-flex-perm-space.md)

[Update the measurement details of a workplace location](update-measurement-details-of-workplace-location.md)

[Change the status of a workplace location](change-active-status-of-workplace-location.md)

[Configure a BOMA type](configure-a-boma-type.md)

[Map a space type with BOMA type](map-a-space-type-with-boma-type.md)

[Create a Space Recommender rule](create-a-space-recommender-rule.md)

[Raise a space assistance request](raise-a-space-recommendation-request.md)

[Create a view-by configuration](create-view-by-config.md)

[Reviewing allocation changes](../concept/reviewing-allocation-changes.md)

