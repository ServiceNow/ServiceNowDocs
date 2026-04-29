---
title: Infoblox roles and permissions
description: Define the roles and permissions that the Infoblox activities need to access the various resources on the Infoblox server.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Infoblox DDI activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Infoblox roles and permissions

Define the roles and permissions that the Infoblox activities need to access the various resources on the Infoblox server.

## Admin groups

There are three types of admin groups on an Infoblox server:

-   Superuser
-   Default
-   Limited Access

To perform specific operations on the Infoblox server, the Limited Access user must have a minimum set of privileges for the desired resources, using either the user interface or an API. These privileges are based on read and read/write access. For more information, refer to the "About Admin Groups" section in the Infoblox NIOS Administrator Guide.

## Permission hierarchy

1.  **User**: A user can be part of multiple groups.
2.  **Group**: A group can have many roles.
3.  **Role**: Each role consistes of specific resource permissions.

## Required permissions

The ServiceNow Infoblox activity pack requires appropriate read and read/write privileges for these resources:

-   Network
-   DHCP
-   DNS
-   IPAM

This example shows a default DHCP admin role, its resources, and the related permissions for each.

![](../image/InfobloxResourcesAndPermissions.png "Infoblox permissions")

**Parent Topic:**[Infoblox DDI activity pack](../concept/c_InfobloxDDIActivityPack.md)

