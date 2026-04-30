---
title: Assign a role to a user
description: A user inherits roles from all groups to which they belong. You can also assign roles directly to a user. Whenever a user is assigned a new role, it only takes effect after logging in with a new session.
locale: en-US
release: xanadu
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a role, Managing roles, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Assign a role to a user

A user inherits roles from all groups to which they belong. You can also assign roles directly to a user. Whenever a user is assigned a new role, it only takes effect after logging in with a new session.

## Before you begin

Role required: user\_admin or admin

When possible, simplify user administration by assigning roles to groups. Create groups that contain all the roles necessary for specific personas, and then assign users to those groups.

## About this task

To grant the admin role to a user, you must also have the admin role. To grant the security\_admin role to a user, you must also have the security\_admin role. You must elevate to the security\_admin role before granting the security\_admin role to other users. See [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

**Note:**

The System administrator\(admin\) role provides access to all system features, functions, and data, regardless of security constraints. Avoid assigning this role to your users when more targeted roles are available.

You can’t delete roles that are assigned to the group from the user record. You must remove the user from the group record.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and then open a user record.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

4.  Select **Save**.


## What to do next

**Note:** If the user is logged in when you update their roles and they’re unable to access records enabled by the new role, they may need to log out and back in again.

**Parent Topic:**[Create a role](../../roles/task/t_CreateARole.md)

