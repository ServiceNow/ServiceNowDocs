---
title: Group allocations fields
description: Group allocations form and related fields description.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [group allocations]
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Group allocations fields

Group allocations form and related fields description.

## Group allocations form

<table id="table_cql_sx5_hp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment Group

</td><td>

Name of the user group to which license is allocated. Software licenses are allocated to all the members of this assignment group based on the availability of unallocated licenses for the software entitlement.

</td></tr><tr><td>

Status

</td><td>

Status of the group allocation to the software model. When a group allocation is created, this field is automatically set to **New**. When the group allocation record is saved and the Software Asset Management application allocates licenses, the **Status** field value is automatically updated based on the availability of unallocated licenses. Possible values are:-   **Not allocated**: None of the group members are allocated to the software entitlement.
-   **Fully allocated**: All the members from the user group are allocated to the software entitlement.
-   **Partially allocated**: A partial number of group members are allocated to the software model.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the user group allocation to the software entitlement is active. When a group allocation is created, the **Active** field value is empty. When the record is saved, the **Active** field value gets updated. Possible values are:-   **true**: The allocation record is active and users from the assignment group are allocated to the software entitlement.
-   **false**: The allocation record is inactive and the users from the assignment group aren't allocated to the software entitlement. When a user group is changed to inactive, the group allocation record is marked as inactive and the **Allocated Quantity** field value is updated.

</td></tr><tr><td>

License metric

</td><td>

User-based license metric for user allocation to the software entitlement. License metric values include:-   Per Named User
-   Per User
-   User Subscription

</td></tr><tr><td>

Group Members

</td><td>

Number of users available in the assignment group. The number is automatically populated when the **Assignment Group** field value is selected.

</td></tr><tr><td>

Software model

</td><td>

This field value is automatically set to the selected software model.

</td></tr><tr><td>

Allocated Quantity

</td><td>

Number of users from the assignment group allocated to the software entitlement. The number is automatically populated when the allocation group record is saved.

</td></tr><tr><td>

Entitlement condition

</td><td>

Entitlement condition to allocate a user group to the filtered software entitlement records. 1.  Select **Set conditions**.
2.  In the Entitlement condition pop-up window, build a filter by adding conditions.
3.  Select **Set** to save the record or **Cancel** to close the Entitlement condition pop-up window without saving the changes.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

**Related topics**  


[Create group allocations](../task/create-group-allocations.md)

[Allocating licenses to a user group](../concept/group-user-allocation.md)

