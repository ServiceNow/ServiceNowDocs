---
title: Create a role
description: Create a role to control access to features and capabilities in applications and modules. The new role doesn’t have access to any application or module until you add other roles to it, or add it to the appropriate applications and modules.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing roles, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a role

Create a role to control access to features and capabilities in applications and modules. The new role doesn’t have access to any application or module until you add other roles to it, or add it to the appropriate applications and modules.

## Before you begin

Role required: admin

## About this task

After access has been granted to a role, all groups or users assigned to the role are granted the access. Roles can contain other roles, and any access granted to a role is granted to any role that contains it.

For a complete list of the roles included with the base instance, see [Base system roles](../reference/r_BaseSystemRoles.md)

**Note:**

You can’t rename roles of any kind in the ServiceNow AI Platform. If you manually create a role, you can’t rename it after you save it.

Move this action to the background so you aren’t waiting when adding a number of group members by adding the system property **glide.ui.schedule\_slushbucket\_save\_for\_group\_roles**. Set the system property to **true**. The system user is used to create records or update existing ones since the action is running in the background.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Roles** and create a record.

2.  Complete the form.

<table id="table_cgz_hzf_xq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the role.

</td></tr><tr><td>

Requires Subscription

</td><td>

Indicates whether users with this role require a subscription to stay in compliance. -   **Yes**

Measured-role that requires a subscription. You can allocate subscriptions to users with this role by adding one or more groups to a product subscription. To learn more, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md).

-   **No**

Not a measured-role.

-   **Unspecified**

Neither

</td></tr><tr><td>

Application

</td><td>

Select the application that contains this record.

</td></tr><tr><td>

Elevated privilege

</td><td>

A role that requires elevated privilege can’t be assigned to a user at login by the system. Instead, a user must manually elevate privileges to receive the elevated role. Select this option to mark this role as required to elevate it to high security. See Elevated privilege roles for more information.

</td></tr><tr><td>

Description

</td><td>

Select the roles to delegate to the group member.

</td></tr></tbody>
</table>
-   **[Grant a role access to applications and modules](t_GrantARoleAccessToAppsAndModules.md)**  
Roles control access to features and capabilities in applications and modules. You add a role to an application or module to enable the role to grant access to the application or module for all users with the role.
-   **[Assign a role to a group](t_AssignRoleToGroup.md)**  
You can assign a role to a group to grant access to applications and modules to group members.
-   **[Assign a role to a user](../../users-and-groups/task/t_AssignARoleToAUser.md)**  
A user inherits roles from all groups to which they belong. You can also assign roles directly to a user. Whenever a user is assigned a new role, it only takes effect after logging in with a new session.
-   **[Add a role to an existing role](t_AddARoleToAnExistingRole.md)**  
When you add a new role to an existing role for a user, the user inherits the access that is granted by the new role.
-   **[Create a group role](t_CreateAGroupRole.md)**  
Create a group role to control access to features and capabilities in applications for all members in a group.

**Parent Topic:**[Managing roles](../concept/ua-creating-roles.md)

