---
title: Delegated Development application-specific permissions
description: Developer and deployment permissions are application-specific. Administrators must set developer \(and optionally deployment\) permissions for each application.
locale: en-US
release: zurich
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: concept
last_updated: "2025-08-20"
reading_time_minutes: 1
breadcrumb: [Explore, Delegated Development, Planning your application, Building applications]
---

# Delegated Development application-specific permissions

Developer and deployment permissions are application-specific. Administrators must set developer \(and optionally deployment\) permissions for each application.

## Application-specific permissions

A developer who has permission to access all file types for one application doesn’t necessarily have any developer permissions for another application. Administrators must be familiar with application files and the system table structure to set developer permissions. For example, a developer expected to create advanced business rules needs both the **All File Types** and **Allow Scripting** developer permissions.

**Important:** If [Application administration](application-administration.md) is enabled, only an application administrator for the target application can delegate developers for an application. Application administrators do not have system admin privileges. To enable a delegated developer to perform the functions granted in the developer permissions, the delegated developer must also be given the application administrator role.

Setting each permission grants one or more system-managed delegated development roles, enabling system admins to retain control over the system. System admins don't have to assign the system admin role to enable them to develop or deploy applications.

