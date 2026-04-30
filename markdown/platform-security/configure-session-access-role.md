---
title: Configuring Session Access role
description: Configure Session Access to reduce user access in a session based on IP, location, Identity Provider attributes, and user attributes using adaptive authentication policies.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Zero Trust Access, Access Management]
---

# Configuring Session Access role

Configure Session Access to reduce user access in a session based on IP, location, Identity Provider attributes, and user attributes using adaptive authentication policies.

## Before you begin

Role required: security\_admin

**Note:**

-   Session Access configurations can only be performed with `security_admin` role. You must elevate your role to `security_admin`.
-   Session Access doesn’t support integrations.
-   Session Access has no impact if the reduced or limited role isn’t assigned to a user. In this case, there are no changes to the logged in session. User will still continue to access the instance with their assigned privileges.
-   Session Access has no impact while the user is already logged in to the instance and simultaneously the admin configures the policy. The user has to log out from the session for the policy to be effective.
-   Session Access is enforced at the time of login. Any change in risk parameters during the session won’t result in reduced access. For example, a user switching from the corporate network to an untrusted network after establishing the session, won’t result in reduced access unless the user logs out and logs in again.
-   Session Access \(Zero trust access - ZTA\) feature, roles like `snc_internal` and `snc_external` cannot be removed.
-   Session Access \(Zero trust access - ZTA\) feature does not remove a role from the `sys_user_has_role` or the user group membership table. Based on the ZTA policy, it establishes the user session with reduced or limited roles.
-   The scripts running in the system context will not honor the ZTA session roles.

## Procedure

1.  Navigate to **All** &gt; **Zero Trust Access** &gt; **Session Access Role Configurations**.

2.  To create a Session Access role configuration, select **New**.

3.  On the form, fill the fields:

<table id="table_vdl_r1g_twb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the configuration

</td></tr><tr><td>

Description

</td><td>

Short description of the configuration.

</td></tr><tr><td>

Policy

</td><td>

Choose the adaptive authentication policy. Use the look-up icon to view the list of policy.

</td></tr><tr><td>

Action

</td><td>

**Remove Roles** or **Limit to Roles**.-   **Remove Roles**: When the configured user logs in, the list of roles provided in the Role or Group List are removed for the session.
-   **Limit To Roles**: When the configured user logs in, only the selected roles are provided to the user and all other roles are removed for the session.


</td></tr><tr><td>

Role List

</td><td>

Choose roles from the Role List.

</td></tr><tr><td>

Group List

</td><td>

Choose the roles from the Group List that you want to remove or limit to the user.

</td></tr></tbody>
</table>4.  Select, **Submit**.

    The login for users based on the configured countries is as follows:

    -   In **Remove Roles**, the users from the configured countries with the selected roles no longer have those roles for the session.
    -   In **Limit To Roles**, the users from the configured countries with the selected roles only have those roles for the session.
    ![Configure Session Access Role](../images/configure-session-access-role.png)

    To know more about how to remove or limit roles for a session explained with a sample use-case, see [Tutorial: Use Zero Trust Access](use-zero-trust-access.md).


