---
title: Allocating licenses to a user group
description: Use the group allocation feature to manage the user allocation to a software entitlement in bulk. This feature enables the SAM managers to streamline and manage the license allocation process efficiently and automatically updates the user allocation when a group composition is changed.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [group allocations, license allocation to assignment group, group license allocation]
breadcrumb: [Explore, Software Asset Management, IT Asset Management]
---

# Allocating licenses to a user group

Use the group allocation feature to manage the user allocation to a software entitlement in bulk. This feature enables the SAM managers to streamline and manage the license allocation process efficiently and automatically updates the user allocation when a group composition is changed.

## How license allocation to a user group works

The SAM Manager can allocate licenses to a group rather than creating user allocation for individual users for the user-based licensing metric software. When a group allocation is created, the Software Asset Management application creates a user allocation record for each group member based on the availability of the unallocated licenses for the software entitlement. When allocating licenses to the group members, the Software Asset Management application avoids duplication of user allocation. If an assignment group includes a child group and some members belong to both the parent and child groups, only the unique members from the parent and child groups are considered for the license allocation.

## Managing license allocation for updated user groups

When a user group is inactivated or updated, the changes are automatically updated for the license allocation to the user. A scheduled job **SAM- Sync group allocations** is triggered every week to identify inactive groups, users, and missing allocations before reconciliation. The following scenarios explain how the user group updates are handled by the Software Asset Management application:

-   When unallocated licenses are available and you add a member to a user group, the Software Asset Management application automatically creates a user allocation for the software entitlement.
-   When unallocated licenses aren't available, the Software Asset Management application doesn’t create a user allocation for the new user. The **Status** field value for the group allocation is updated to show that the user group is partially allocated with a license.
-   When a member is removed from a user group, the license allocation to the user is automatically deleted. The **Allocated Quantity** field value is automatically updated to reflect it.
-   When a group allocation is deleted from the software model, allocations for all members of that group are removed. The unallocated license quantity is automatically updated.

For more information about creating a group allocation record, see [Create group allocations](../task/create-group-allocations.md).

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

**Related topics**  


[Create group allocations](../task/create-group-allocations.md)

[Group allocations fields](../reference/group-allocation-fields.md)

[Software model fields](../reference/software-model-fields.md)

