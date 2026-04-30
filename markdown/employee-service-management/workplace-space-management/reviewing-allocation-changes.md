---
title: Reviewing allocation changes
description: Review allocation changes in the Space Allocation Type Change Tracker table to plan changes for your scenarios.
locale: en-US
release: xanadu
product: Workplace Space Management
classification: workplace-space-management
topic_type: concept
last_updated: "2025-04-04"
reading_time_minutes: 3
breadcrumb: [Managing workplace locations, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Reviewing allocation changes

Review allocation changes in the Space Allocation Type Change Tracker table to plan changes for your scenarios.

The Space Allocation Type Change Tracker \[sn\_wsd\_spcmgmt\_space\_allocation\_type\_change\_tracker\] table contains information about allocation changes in your workplace.

You can review the table columns for information about the type of allocation changes.

After you review the allocation changes, you can make changes to your scenario. For example, if the parent of a workplace entity is changed, you can move the existing spaces to the previous parent and allocate spaces from the new parent. If a cost center or department is deleted or made inactive, you can remove the allocations from your scenario.

<table id="table_zfk_2lv_w2c"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type of change

</td><td>

Type of allocation change made on the workplace.-   **Inactive**

The allocation was made inactive.

-   **Deleted**

The allocation was deleted.

-   **Reparent**

The parent of the workplace entity was changed.


</td></tr><tr><td>

Cost center

</td><td rowspan="4">

The allocation type that is impacted by the change. Only one of these columns is filled based on the allocation change.

</td></tr><tr><td>

Department

</td></tr><tr><td>

Neighborhood

</td></tr><tr><td>

Workplace Entity

</td></tr><tr><td>

Deleted record ID

</td><td>

Sys ID of the allocation record that was deleted.This field is filled only if the type of change is **Deleted**.

</td></tr><tr><td>

Domain

</td><td>

Domain in which the allocation was changed.

</td></tr><tr><td>

Parent table

</td><td>

Table in which the type of allocation is stored in.

</td></tr><tr><td>

Previous parent

</td><td>

Previous parent of the workplace entity.This field is applicable for workplace entities and filled only if the type of change is **Reparent**.

</td></tr></tbody>
</table>**Parent Topic:**[Managing workplace locations](Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus](../task/add-a-campus.md)

[Add a building using Workplace Space Management](../task/add-new-building-1.md)

[Add a floor using Workplace Space Management](../task/add-a-floor-1.md)

[Add an area using Workplace Space Management](../task/add-an-area.md)

[Add a room using Workplace Space Management](../task/add-a-room.md)

[Add a space using Workplace Space Management](../task/add-a-space.md)

[Allocate a cost center, department, or workplace entity](../task/add-cost-center-department-floor.md)

[Configure a workspace or desk as flexible or permanent](../task/assign-a-flex-perm-space.md)

[Update the measurement details of a workplace location](../task/update-measurement-details-of-workplace-location.md)

[Change the status of a workplace location](../task/change-active-status-of-workplace-location.md)

[Configure a BOMA type](../task/configure-a-boma-type.md)

[Map a space type with BOMA type](../task/map-a-space-type-with-boma-type.md)

[Create a Space Recommender rule](../task/create-a-space-recommender-rule.md)

[Raise a space assistance request](../task/raise-a-space-recommendation-request.md)

[Create a view-by configuration](../task/create-view-by-config.md)

