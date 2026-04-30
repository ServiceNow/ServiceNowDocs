---
title: Prevent duplicate entries with Contextual Security: Role Management V2
description: Roles inherited from other roles are added as individual entries in the User Roles table \[sys\_user\_has\_role\], potentially causing one role to have duplicate entries. Contextual Security: Role Management V2 eliminates these duplicate entries and prevents future duplicates.
locale: en-US
release: xanadu
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Contextual Security Manager, Access Control List Rules, Access Management]
---

# Prevent duplicate entries with Contextual Security: Role Management V2

Roles inherited from other roles are added as individual entries in the User Roles table \[sys\_user\_has\_role\], potentially causing one role to have duplicate entries. Contextual Security: Role Management V2 eliminates these duplicate entries and prevents future duplicates.

## Eliminate duplicate entries through inheritance count

Contextual Security: Role Management V2 uses the Inheritance Count \(inh\_count\) column to track the number of times a role is inherited from another role or group. In the User Roles \[sys\_user\_has\_role\] table, a user can inherit a specific role only one time, eliminating duplicate entries. The Inheritance Count \(inh\_count\) column is read-only and calculates the number of times the user inherits a role.

## Activation changes

Contextual Security: Role Management V2 is automatically installed on new instances and can be activated for upgrades. When activated, Contextual Security: Role Management V2 replaces both Contextual Security and Contextual Security: Role Management Enhancements.

When Contextual Security: Role Management V2 is activated, the following columns are deprecated, but remain in the User Roles table for backward compatibility:

-   granted\_by \(used only by Role Delegation\)
-   included\_in\_role
-   included\_in\_role\_instance

**Warning:** If these columns are in use in any custom scripts on your instance, do not upgrade to Role Management V2.

## Visualize role inheritance through the Role Inheritance Map

The Role Inheritance Map displays a visual representation of inherited roles. You can use this map to understand the roles represented in the Inheritance Count \(inh\_count\) column. To view the Role Inheritance Map, configure the User Roles \[sys\_user\_has\_role\] table to display the Role Inheritance Map column.

![Role inheritance map](../image/RoleInheritanceMap.png "Role Inheritance Map")

**Note:** Concurrent update to group or role assignment may result in incorrect inheritance count. You must enable the `glide.security.inh_count_patcher.enabled` property to get the exact inheritance count.

