---
title: Delegating development permissions to personnel
description: A system administrator can assign a non-administrator user or group as a developer for a specific application. You can set permissions that designate what specific actions the assigned user can perform in the current instance. You can also make the user a Delegated Admin to grant access to all permissions at once.
locale: en-US
release: zurich
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Delegated Development, Planning your application, Building applications]
---

# Delegating development permissions to personnel

A system administrator can assign a non-administrator user or group as a developer for a specific application. You can set permissions that designate what specific actions the assigned user can perform in the current instance. You can also make the user a Delegated Admin to grant access to all permissions at once.

## Before you begin

-   Role required: admin or application administrator

    If [Application administration](../concept/application-administration.md) is enabled, only an application administrator of the target application can delegate developers to an application. If application administration isn’t enabled, an admin user can delegate developers.

-   Records required:
    -   Application
    -   User
    -   Group

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  Select the name of the application to which you want to add developers.

    The system opens the application record.

3.  Select **Manage Developers**.

    **Note:** If the App Collaboration Component is installed, the link appears as **Manage Collaborators**.

    The system displays the Developer Permissions window.

    **Note:** Developer permissions are available only for scoped apps, not global apps.

4.  Select the type of developer \(or user without system admin roles\) you want to assign.

    |Option|Description|
    |------|-----------|
    |**Developers**|To add individual users as developers.|
    |**Groups**|To add all members of a group as developers.|

5.  In **Developer Name** or **Group Name**, enter the name of the user or group you want to grant developer permissions.

6.  Select custom developer permissions for the application, or select **Delegated Admin** to grant access to all permissions for the application.

    For details, see [Developer permissions](../reference/developer-permissions.md).

7.  Select **Save**.

    The system assigns the designated developer and deployment permissions for the application.


