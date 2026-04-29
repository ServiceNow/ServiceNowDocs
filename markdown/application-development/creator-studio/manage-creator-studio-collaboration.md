---
title: Manage Creator Studio collaboration permissions on the ServiceNow AI Platform
description: In Creator Studio, you can control how people work together on apps by setting up permissions called collaboration descriptors. These descriptors define what users can and cannot do.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Collaboration, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Manage Creator Studio collaboration permissions on the ServiceNow AI Platform

In Creator Studio, you can control how people work together on apps by setting up permissions called collaboration descriptors. These descriptors define what users can and cannot do.

## Before you begin

Role required: app\_engine\_admin, and permission to Manage collaborators

## About this task

Users with the Manage collaborators permission can adjust who can collaborate on the apps they own. For more information, check [Manage collaborators for an app in Creator Studio](creator-studio-manage-collaborators.md).

**Note:** The way that collaboration permissions appear may vary depending on whether your instance has App Engine Studio installed.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Collaboration** &gt; **Descriptors**.

2.  Edit the permissions for a [collaboration descriptor](../concept/creator-studio-glossary.md#), such as owner or editor.

    1.  Find and select the **Name** of the descriptor you want to modify.

    2.  Choose a **Development permission set**, such as **Service Catalog**, to update its permissions.

        For a list of permissions, see [Collaboration permissions](../../applications/reference/collaboration-permissions.md).

    3.  Select **Save** and **Update**.

3.  Assign the updated descriptor to users or groups.

    1.  Select the descriptor **Name**, such as **Owner** or **Editor**.

    2.  Select the applicable tab to assign either users or groups:

        -   **App Collaboration Users** tab: For individual users
        -   **App Collaboration Groups** tab: For groups of users
    3.  Select the **New** button.

    4.  On the form, fill in the fields.

        For more information, see the following topics:

        -   [Assign collaboration descriptors to users](../../applications/task/assign-descriptor-user.md)
        -   [Assign collaboration descriptors to groups](../../applications/task/assign-descriptor-group.md)
    5.  Select **Save**.

4.  If you need a new collaboration descriptor, create a custom one.

    1.  Select the **New** button.

    2.  On the form, fill in the fields.

<table id="table_gk1_tzs_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the descriptor.

</td></tr><tr><td>

Description

</td><td>

Description of what the descriptor can do. Examples are as follows: -   Owner
-   Editor


</td></tr><tr><td>

Application

</td><td>

Scope of the collaboration descriptor. Currently, all collaboration descriptors must be created in the global scope.

</td></tr><tr><td>

Standard

</td><td>

Option for inviting other collaborators with this role.

</td></tr></tbody>
</table>    3.  Select **Submit**.


## Result

You've now set up collaboration descriptors, defined permissions, and assigned roles to users and groups for specific apps. For complete details on using the Collaboration app, see [Application collaboration](../../applications/concept/application-collaboration.md).

**Parent Topic:**[Administering collaboration in Creator Studio](../concept/creator-studio-admin-collab-tasks.md)

