---
title: Elevated privilege roles
description: Elevated privilege roles require you to manually accept the responsibility of using the role before you can access the features of the role.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Security Roles, Access Management]
---

# Elevated privilege roles

Elevated privilege roles require you to manually accept the responsibility of using the role before you can access the features of the role.

By default, you do not have elevated privilege roles upon login. You must manually elevate to the privilege of the role. An elevated privilege role lasts only for the duration of your user session. Session timeout or logout removes the role.

You can designate any role as an elevated privilege role, and then assign that role to one or more users. Do this when you want to restrict users from having access to the rights that the role provides immediately after login. You can designate the privilege role on the Role form. See [Create a role](https://www.servicenow.com/docs/access?context=t_CreateARole&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for instructions.

To use an elevated role, you must meet these conditions:

-   The elevated role must be assigned to you.
-   You must manually elevate to a specific elevated role to get its privileges, even if you are already elevated to a second elevated role that contains the first elevated role.

    For example, if elevated role A contains elevated role B, even if you elevate to role A, you must still elevate to role B to get its privileges.


## The admin role

To grant the admin role to a user, the granting user must also have the admin role. For example, a user with only the user\_admin role cannot grant the admin role to other users.

-   Non-admin users cannot add a user to a group that contains the admin role.
-   To grant the security\_admin role to a user, the granting user must also have the admin role and must elevate to the security\_admin role before granting the security\_admin role to other users. A user with only the admin role cannot grant the security\_admin role to other users.
-   A user without the security\_admin role cannot add a user to a group that contains the security\_admin role.

**Warning:** The use of elevated privilege on an admin role is not supported. Instead, require admins to manually elevate, see [Force administrators to manually elevate](../task/t_ForceAdmManElev.md)

## The security\_admin role

In the base system, the security\_admin role is the only role that has elevated privileges. This role is automatically assigned to the user who is the default System Administrator \(admin\) user. It provides access to [ACLs](../../contextual-security/concept/access-control-rules.md) and [High Security Settings](c_HighSecuritySettings.md).

![The list of roles assigned to the System Administrator user](../image/elevated-privilege-role.png "Roles assigned to the System Administrator (admin) user")

**Note:** To see this role, you must actually elevate to the security\_admin role first. If you are logged in as the System Administrator \(admin\) user only, you cannot see the security\_admin record in the list of roles.

-   **[Security\_admin role](security-admin-role.md)**  
The security\_admin role is an elevated privilege role provided with High Security Settings that lets users create and change access controls and change High Security Settings.
-   **[Elevate to a privileged role](../task/t_ElevateToAPrivilegedRole.md)**  
The base system admin can elevate to a privileged role to have access to the features of High Security Settings.
-   **[Force administrators to manually elevate](../task/t_ForceAdmManElev.md)**  
A property is available to force all users with the administrator role to manually select the role that they want to elevate to.

**Parent Topic:**[Security Roles](security-roles.md)

