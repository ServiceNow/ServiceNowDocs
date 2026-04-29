---
title: Upgrade to Contextual Security: Role Management V2
description: Contextual Security: Role Management V2 is automatically installed on new instances. You can upgrade from Contextual Security: Role Management to Contextual Security: Role Management V2 to eliminate duplicate roles in the User Roles table and prevent future duplicates.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Contextual Security Manager, Access Control List Rules, Access Management]
---

# Upgrade to Contextual Security: Role Management V2

Contextual Security: Role Management V2 is automatically installed on new instances. You can upgrade from Contextual Security: Role Management to Contextual Security: Role Management V2 to eliminate duplicate roles in the User Roles table and prevent future duplicates.

## Before you begin

Role required: admin, security\_admin

You must have the admin role and [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md) to obtain the effective security\_admin role.

**Note:** Before upgrading to Contextual Security: Role: Management V2, you must enable the Audit Roles table to create audit records related to user roles. To learn more about setting the required system property, see [Enable role auditing with Contextual Security: Role Management V2](enable-audit-roles.md).

## About this task

This procedure describes how to upgrade your Contextual Security role and how to activate the related plugins described in the following table.

<table id="table_jpm_rh3_hy"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contextual Security: Role Management V2\[com.glide.role\_management.inh\_count\]

</td><td>

Prevents duplicate entries in the User Roles \[sys\_user\_has\_role\] table.The security\_admin role or a user with elevated privileges is required to activate the plugin, or contact Customer Service and Support.

</td></tr><tr><td>

Contextual Security: Role Management V2 REST API\[com.glide.role\_management.inh\_count.rest\_api\]

</td><td>

Enables API functionality for role management.

</td></tr></tbody>
</table>Before upgrading from Contextual Security: Role Management to Contextual Security: Role Management V2, test the results of an upgrade by running the script. The script returns a list of changes that an upgrade will perform. If the changes are acceptable, install the Contextual Security: Role Management V2 plugin. If the changes are not acceptable, do not install the Contextual Security: Role Management V2 plugin. Alternatively, you can perform the upgrade and then manually make any necessary changes.

## Procedure

1.  Test the impact of an upgrade prior to upgrading by running the following script.

    1.  Navigate to **System Definition** &gt; **Scripts - Background**.

    2.  Run the following script in global scope.

        ```
        new RoleManagementVerify().verifyInheritedRoles();
        ```

        For large sys\_user\_has\_role tables, the execution may take up to several hours to complete. Do not edit or add user roles during this time.

        Example result based on test data:

        ```
        *** Script: 2016-12-01 19:58:54 Starting checking of inherited roles for all users... 
        *** Script: User: itam, inherited roles to be ADDED: financial_mgmt_user 
        *** Script: User: bernard.laboy, inherited roles to be DELETED: api_analytics_read,pa_viewer,rest_api_explorer,a123 
        *** Script: User: bernard.laboy, inherited roles to be ADDED: dependency_views 
        *** Script: Number of inherited-role records in sys_user_has role, current: 260, after re-calculation: 258 
        *** Script: Number of users with discrepancies for inherited roles: 2 
        *** Script: 2016-12-01 19:58:55 Finished checking of inherited roles for all users!
        ```

    3.  Evaluate the script results to determine whether the proposed changes are acceptable.

2.  Activate the Contextual Security: Role Management V2 plugin.

    **Important:** The security\_admin role or a user with elevated privileges is required to activate the plugin, or contact Customer Service and Support.

    1.  Navigate to **System Definition** &gt; **Plugins**.

    2.  Find and click the plugin name.

    3.  On the System Plugin form, review the plugin details and then click the **Activate/Upgrade** related link.

    4.  Click **Activate**.


## Result

After activating Role Management V2, the changes outlined in the script result are enacted. The Inheritance Count \(inh\_count\) column in the User Roles table is read-only and automatically reflects the number of times the user inherits a role.

