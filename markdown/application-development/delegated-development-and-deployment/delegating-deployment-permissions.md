---
title: Delegating deployment permissions
description: A system administrator can assign a non-administrator user or group as a deployment resource for a specific application. You can set specific permissions, or grant access to all permissions, that designate what specific actions the assigned user can perform in the current instance.
locale: en-US
release: zurich
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: task
last_updated: "2025-08-20"
reading_time_minutes: 1
breadcrumb: [Administer, Delegated Development, Planning your application, Building applications]
---

# Delegating deployment permissions

A system administrator can assign a non-administrator user or group as a deployment resource for a specific application. You can set specific permissions, or grant access to all permissions, that designate what specific actions the assigned user can perform in the current instance.

## Before you begin

-   Role required: admin or application administrator

    If [Application administration](../concept/application-administration.md) is enabled, only an application administrator of the target application can delegate deployment resources to an application. If application administration isn’t enabled, an admin user can delegate deployment resources.

-   System properties control the visibility of the **Publish To Update Set** and **Manage Update Sets** permissions. By default, both deployment permissions for update sets are hidden. See [Delegated Development System Properties](../reference/delegated-development-system-properties.md).

-   Records required:
    -   Application
    -   User
    -   Group

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  Select the name of the application to which you want to add deployment resources.

    The system opens the application record.

3.  Select **Manage Developers**.

    **Note:** If the App Collaboration Component is installed, the link appears as **Manage Collaborators**.

    The system displays the Developer Permissions window.

    **Note:** Developer permissions are available only for scoped apps, not global apps.

4.  Select the type of developer \(or user without system admin roles\) you want to assign.

    |Option|Description|
    |------|-----------|
    |**Developers**|To add individual users as deployment resources.|
    |**Groups**|To add all members of a group as deployment resources.|

5.  In **Developer Name** or **Group Name**, enter the name of the user or group you want to grant deployment permissions.

6.  Select custom deployment permissions for the application, or select **Delegated Admin** to grant access to all permissions for the application.

    For details, see [Developer permissions](../reference/developer-permissions.md).

7.  Select **Save**.

    The system assigns the designated deployment permissions for the application.


