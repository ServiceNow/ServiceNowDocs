---
title: Create group allocations
description: Create group allocations to allocate licenses to all the members of the assignment group.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [group allocation, create group allocation]
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create group allocations

Create group allocations to allocate licenses to all the members of the assignment group.

## Before you begin

Role required: sam\_admin or sam\_user

## About this task

The SAM Manager can add a group allocation record for a software model with valid software entitlement records to create a user allocation for the group members.

**Note:** Licenses are allocated to the group members based on the number of unallocated licenses available for the software entitlement.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Software model**.

2.  Select **Group Allocations**.

3.  Select **New**.

4.  On the Create New Group Allocations form, fill in the fields.

    For a description of the field values, see [Group allocations fields](../reference/group-allocation-fields.md).

5.  Select **Save**.


## Result

-   User allocation records are created for the members of the assignment group and listed in the **User Allocations** tab.
-   The group allocation record is saved in the Group Allocations \[alm\_entitlement\_group\] table.

## What to do next

View the user allocations list by navigating to any of the following paths:

-   Navigate to the **User Allocations** within the group allocation record.
-   Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Licensing** &gt; **Software models** and select a software model record. Select the **User Allocations** tab.
-   Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Licensing** &gt; **Software models** and select a software model record. Select the **Software Entitlements** tab and select a software entitlement record. Select the **User Allocations** tab.

**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

**Related topics**  


[Allocating licenses to a user group](../concept/group-user-allocation.md)

[Group allocations fields](../reference/group-allocation-fields.md)

