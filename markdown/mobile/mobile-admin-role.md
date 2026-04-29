---
title: Mobile admin role
description: Administrators can assign roles that grant specific permissions, which govern what users and groups with that role can do within the ServiceNow Mobile Platform.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Mobile admin role

Administrators can assign roles that grant specific permissions, which govern what users and groups with that role can do within the ServiceNow Mobile Platform.

The administrative role available to administrators of the ServiceNow Mobile Platform is **mobile\_admin**.

**Note:** While the **admin** role provides full system access, it grants unrestricted permissions that may pose security risks. For users who only need to perform mobile-related tasks, assign the **mobile\_admin** role, as it provides access to only what is necessary.

For more generic information on roles, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

The mobile\_admin role grants administrators the precise permissions needed to configure mobile applications. Unlike the broader admin role, the mobile\_admin role enhances security by providing more controlled access to your ServiceNow account, reducing unnecessary privileges.

## What the mobile\_admin role includes

The mobile\_admin role includes the following permissions:

-   Provides access \(read, write, create, and delete\) to all mobile-related tables. This coverage includes all products and features that are built on or connected to the mobile platform.
-   Grants view and edit access to mobile-relevant system properties without the need for the general sys\_properties access.
-   Enables use of publishing and builder tools including Mobile App Builder, Mobile Card Builder, and Mobile Publishing \(if purchased from the ServiceNow Store\).

**Note:** The mobile\_admin role doesn't automatically grant access to individual application scopes. For example, if you want to configure Field Service Mobile in Mobile App Builder, you need the appropriate permissions for that scope.

## Resources for working with roles

Learn about roles and how to work with them in the following topics:

-   [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=australia&pubname=australia-platform-administration&ft:locale=en-US)
-   [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US)
-   [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

