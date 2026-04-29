---
title: Tutorial: Use Zero Trust Access
description: Procedure to use Zero Trust Access feature with an end-to-end use case.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Zero Trust Access, Access Management]
---

# Tutorial: Use Zero Trust Access

Procedure to use Zero Trust Access feature with an end-to-end use case.

## Before you begin

Role required: security\_admin

Enable the **Enable Session Access property**.

**Note:**

-   Session Access configurations can only be performed with `security_admin` role. You must elevate your role to `security_admin`.
-   Session Access doesn’t support integrations.
-   Session Access has no impact if the reduced or limited role isn’t assigned to a user. In this case, there are no changes to the logged in session. User will still continue to access the instance with their assigned privileges.
-   Session Access has no impact while the user is already logged in to the instance and simultaneously the admin configures the policy. The user has to log out from the session for the policy to be effective.
-   Session Access is enforced at the time of login. Any change in risk parameters during the session won’t result in reduced access. For example, a user switching from the corporate network to an untrusted network after establishing the session, won’t result in reduced access unless the user logs out and logs in again.
-   Session Access \(Zero trust access - ZTA\) feature, roles like `snc_internal` and `snc_external` cannot be removed.
-   Session Access \(Zero trust access - ZTA\) feature does not remove a role from the `sys_user_has_role` or the user group membership table. Based on the ZTA policy, it establishes the user session with reduced or limited roles.
-   The scripts running in the system context will not honor the ZTA session roles.

Session Access is a feature that enables the administrators to dynamically reduce or restrict a set of roles to the user, when the user is trying to log in to the instance from different environments such as log in from the untrusted network, log in from a different device, and so on.

Session Access can be controlled by the created policy and selected action when performing the configuration. Some of the scenarios are as follows:

-   If the Policy is true, and the roles action is set to **Remove Roles**, then the selected roles and its associated child roles are removed for the user when trying to log in to the instance.
-   If the Policy is true, and the roles action is set to **Limit To Roles**, then only the selected roles and its associated child roles are assigned to the user when trying to log in to the instance.

The following procedure explains an end-to-end configuration of session access configuration based on which the role is limited to the user who is logging in to the instance. Similarly you can also remove roles by selecting the **Remove Roles** option during the configuration.

## Procedure

1.  Navigate to **All** &gt; **Session Access** &gt; **Session Access Role Configurations**.

2.  On the Session Access Role Configurations page, select **New**.

3.  To limit any role for the user, on the form, fill the fields:

    -   Name
    -   Description
    -   Policy
    -   Action
    -   Role List
    -   Group List
    1.  Choose **Limit To Roles** to limit roles for the user.

        For example, **itil**.

    2.  Choose **knowledge** role from the Role List.

    3.  Choose the **Policy**.

        You can create the Session Access policy using an authentication policies and filter criteria \(Role, Group, IP, Location\) with policy inputs and conditions.

        Use the policy in the Session Access configuration. For example, you want to limit the role \(knowledge\) to the user logging in outside the Location \(Australia\).

    4.  Choose Action as **Limit To Roles**.

        If the Policy is true, then only the selected roles and their associated child roles are available for the user when trying to log in to the instance.![Limited role.](../images/role-limited.png)

    5.  Select **Submit**.

        Similarly, you can choose the group from the Group List to restrict or remove roles for the users within the group.

    When the user logs to the instance outside Australia, only the **Knowledge** role and its associated child roles are assigned for the logged session and other roles to the user are restricted.

    After logging in, the user is displayed with the following error message on the platform in their profile section:

    ![Error message after login.](../images/error-message-upon-login.png)

    The user can contact the administrators and provide the Correlation ID for investigation.

    **Note:** The correlation ID is the sys\_id of the corresponding audit record in the session access audit table.


