---
title: Assign a role to a user
description: A user inherits roles from all groups to which they belong. You can also assign roles directly to a user. Whenever a user is assigned a new role, it only takes effect after logging in with a new session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/user-administration/t\_AssignARoleToAUser.html
release: zurich
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a role, Managing roles, User admin, Configure core features, Administer]
---

# Assign a role to a user

A user inherits roles from all groups to which they belong. You can also assign roles directly to a user. Whenever a user is assigned a new role, it only takes effect after logging in with a new session.

## Before you begin

Role required: user\_admin or admin

When possible, simplify user administration by assigning roles to groups. Create groups that contain all the roles necessary for specific personas, and then assign users to those groups.

## About this task

To grant the admin role to a user, you must also have the admin role. To grant the security\_admin role to a user, you must also have the security\_admin role. You must elevate to the security\_admin role before granting the security\_admin role to other users. See [Elevate to a privileged role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/t_ElevateToAPrivilegedRole.md).

You can't delete roles that are assigned to the group from the user record. You must remove the user from the group record.

**Warning:** If your organization hasn't manually allocated user-based subscriptions before,subscription assignments are based on user roles and the kind of access each role permits. Creating, customizing, and assigning roles can have subscription usage impact. For more information about how roles are evaluated for subscription assignment, see [Automatic subscription assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/user-subscription-auto-assignment.md).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and then open a user record.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

    The **Collection** list displays only roles for applications and plugins that are installed on your instance. If a role does not appear, the corresponding application may not be installed.

    **Note:**

    The System administrator\(admin\) role provides access to all system features, functions, and data, regardless of security constraints. Avoid assigning this role to your users when more targeted roles are available.

4.  Select **Save**.


## What to do next

**Note:** If the user is logged in when you update their roles and they’re unable to access records enabled by the new role, they may need to log out and back in again.

**Parent Topic:**[Create a role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/user-administration/t_CreateARole.md)

