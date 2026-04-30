---
title: Explicit Roles in CSM
description: You can give both internal users and external users access to your instance. However, you might not want both types of users to have the same level of access. To provide added security, every user must have at least one role so that the instance can distinguish between internal and external users.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Roles installed with Customer Service Management, Components installed with Customer Service Management, Customer Service Management reference, Customer Service Management]
---

# Explicit Roles in CSM

You can give both internal users and external users access to your instance. However, you might not want both types of users to have the same level of access. To provide added security, every user must have at least one role so that the instance can distinguish between internal and external users.

As of the Paris release, no user can have both of the explicit roles \(snc\_internal and snc\_external\). Groups and role containment cannot include both roles, either, since that would cause any group member or user who is assigned to such a group or such a role to automatically have both roles. The ServiceNow AI Platform aborts any operation that would create such a scenario.

External users must obtain, at minimum, the snc\_external role. The snc\_external role indicates that the user is external to your organization. They should not have any access to resources unless explicitly allowed through ACLs for the snc\_external role or additional roles that inherit the snc\_external role. By default, users with the snc\_external role cannot access:

-   Scripted REST API resources that are not marked external.
-   Tables without the role that inherits the snc\_external role or the public role.
-   Non-record type resources, such as processors and UI pages without granting access to the snc\_external role or a role that inherits the snc\_external role.
-   Platform Analytics dashboards.

Do not mark the snc\_internal role as elevated. Otherwise, internal users cannot access the instance.

## Recommended CSM roles for internal and external users

Customers \(external users\) using the Customer Service Management application should be assigned either the sn\_customerservice.customer or the sn\_customerservice.consumer role. Customer service agents \(internal users\) should be assigned either the sn\_customerservice\_agent or sn\_customerservice\_consumer\_agent role. The system ensures that the same user is not assigned both a customer \(external\) and agent \(internal\) role.

## Explicit Roles plugin

The Customer Service plugin \(com.sn\_customerservice\) activates the Explicit Roles plugin \(com.glide.explicit\_roles\), which adds the snc\_external and snc\_internal roles. When the plugin is activated:

-   All users must have either the snc\_internal role to access internal resources or the snc\_external role to access external resources.
-   All existing users are automatically assigned the snc\_internal role. This role does not change existing access levels or system behavior. Instead, it provides a category to differentiate internal users from external users. All internal users maintain the same level of access as before the plugin was activated.

    **Tip:** To prevent changing existing functionality for users, activating the Explicit Roles plugin assigns the snc\_internal user role to all existing users in the instance. This includes any external users added before the Explicit Roles plugin was activated. After the Explicit Roles plugin is activated, do the following for all external users added before the Explicit Roles plugin was activated:

    -   Remove the snc\_internal role.
    -   Add the snc\_external role.
    Doing the preceding ensures that external users added before activating the Explicit Roles plugin do not have access to internal resource that should be available only to internal users.

-   Newly created users are automatically assigned the snc\_internal role when they first attempt to log in to the instance, unless they have been explicitly assigned the snc\_external role. You can add the snc\_external role to a new user before they first log in to the instance to provide external user rights.

    **Important:** Activate this plugin during a maintenance window or when few users are logged in. Users currently logged in when the plugin is activated will not be dynamically assigned the snc\_internal role. Rather, users must log out and log back in to be assigned the snc\_internal role. Once the plugin is activated, you can add or remove the snc\_internal and snc\_external roles at any time to change user rights.

-   All existing ACLs that do not have a role requirement are automatically assigned the snc\_internal role. Because both existing ACLs and roles are assigned the snc\_internal role, existing access levels do not change.
-   Newly created ACLs that do not have a role requirement are automatically assigned the snc\_internal role. This role assignment does not apply to a newly created ACL with a role assigned.
-   For all existing Processor \[sys\_processor\] records or newly created Processor \[sys\_processor\] records with **Type=script**, the snc\_internal role is automatically added to the **Roles** field if the field is empty.
-   To restrict access to UI pages to internal users, the plugin automatically assigns the snc\_internal role to the **\*** ACL with a **Type** of **ui\_page**.
-   To restrict access to processors to internal users, the plugin automatically assigns the snc\_internal role to the **\*** ACL with a **Type** of **processor**.
-   External users must obtain, at minimum, the snc\_external role to access the instance. This role is automatically assigned to external Customer Service Portal contacts. If the Customer Service Portal is not activated, this role must be manually granted to external users'. Access to records is granted through ACLs.

    **Note:** You can use the `isPublic()` function in scripts for Customer Service Portal to change the privacy setting for a single client-callable script include. For more detail, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

-   [Content Management System](https://www.servicenow.com/docs/access?context=c_ContentManagementSystem&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) site access is also affected. CMS is set up with Sites \(content\_site\), Pages \(content\_page\), and other resources. Some of the sites may have the **Login page** configured.
    -   If CMS sites do not have the **Login page** configured, the public role is automatically added to the **Read Roles** field on Pages \(content\_page\) if the field is empty.
    -   If CMS sites have the **Login page** configured, the snc\_internal role is automatically added to the **Read Roles** field on Pages \(content\_page\) if the field is empty.
-   [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) site access is also affected.

    The snc\_internal role is not automatically added to sp\_page, sp\_widget or sp\_instance records. If desired, you can give new records the role by assigning snc\_internal as a default value in the **Roles** field for these records. For details on this process see [Specify a default field value](https://www.servicenow.com/docs/access?context=t_SpecifyingADefaultValue&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).


Do not move [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) among instances with and without the Explicit Roles plugin enabled.

**Note:** This plugin also requires the [Contextual Security Manager](https://www.servicenow.com/docs/access?context=r_ContextualSecurity&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) plugin.

## The glide.security.explicit\_roles.internal\_user\_blacklist property

The Explicit Roles plugin assumes that all existing users in the sys\_user table at the time the plugin is installed are internal customers. A fix script assigns the snc\_internal role to all existing users and to any ACL that does not have a role.

The fix script may fail or may not finish in time for a user who has not been updated with the role and who attempts to access a resource. To bridge this potential gap, the Contextual Security Manager \(CSM\) auto-assigns the snc\_internal role to any user who logs in and does not have an explicit role \(either internal or external\).

Additionally, CSM has a business rule process that assigns the snc\_external role to a classification of their users. However, when importing large sets of CSM external customers, workflow is set to false, so business rules don't run. As those users attempt to access a resource, they do not have any explicit roles. The Contextual Security Manager assigns the snc\_internal role through a scheduled job called On-Call Gaps Conflicts Report that runs every 7 days. When the Explicit Roles plugin is active, this job assigns the snc\_internal role to the CSM external user, since the user does not have either the snc\_internal or snc\_external role.

To prevent inadvertently providing the snc\_internal role to external users, the Explicit Roles plugin includes a **glide.security.explicit\_roles.internal\_user\_blacklist** property to exclude user types from ever becoming snc\_internal. If there are no users types in the glide.security.explicit\_roles.internal\_user\_blacklist table, the Contextual Security Manager assigns all users the snc\_internal role by default. If there are classnames in the blacklist table, and if the sys\_user class type is in the blacklist table, CSM assigns the snc\_external role. Otherwise, CSM assigns the default snc\_internal role as usual.

For the Paris release, this property is enabled by default for zBoot instances and and disabled by default for upgrades.

## Providing table access to external users

You can provide external users access to a table by adding a role to the table that inherits the snc\_external role. For more information, see [Provide external users access to a table](../task/t_ProvideExternalUsersAccessToTables.md).

## The hasRoles\(\) method

The `hasRoles()` method is still available, but is deprecated in the Geneva release. Use the `hasRole(role name)` method instead.

If you do use the `hasRoles()` method, note these changes:

-   This method automatically excludes the default snc\_internal role when it checks for roles. This means that if a user has only the snc\_internal role, the `hasRoles()` method still returns **false**.
-   If the user has the snc\_external role, the method returns **false** because the instance considers external users to be without a role.

## Mutual exclusion: snc\_external versus snc\_internal

The ServiceNow AI Platform prevents users from having both the snc\_external role and the snc\_internal role. The ServiceNow AI Platform applies this mutual exclusion everywhere in the system and writes error messages to the logs for each conflict.

**Note:** ACLs can have both roles if the ACL resources should be accessible to all users.

Example: Adding both explicit roles to a user \(direct collision\):

1.  Assign user Abel Tuter the snc\_internal role.
2.  Assign user Abel Tuter the snc\_external role.

Result: Adding the snc\_external role fails because Abel Tuter has the snc\_internal role.

Example: Adding both explicit roles to a group \(direct collision\):

1.  Consider a group called Test Group that currently has no explicit roles assigned to the group.
2.  Add Abel Tuter to the Test Group.
3.  Add the snc\_external role to Test Group.

Result: Adding the snc\_external role fails because Abel Tuter already has the snc\_internal role and can't have both roles.

Example: Adding an explicit role to a group where a group member has the conflicting explicit role \(indirect collision\):

1.  Assign user Abel Tuter the snc\_internal role.
2.  Consider a group called Test Group that currently has no explicit roles assigned to the group.
3.  Add Abel Tuter to the Test Group.
4.  Add the snc\_external role to the Test Group.

Result: Adding the snc\_external role to the group fails because Abel Tuter would inherit the snc\_external role through group membership. Both explicit roles would be assigned to the same user, which isn't allowed.

For other examples, see the following table:

<table id="table_eqm_tt2_flb"><thead><tr><th>

Role

</th><th>

Attempted action

</th><th>

Result

</th></tr></thead><tbody><tr><td colspan="3">

Direct collision

</td></tr><tr><td>

The user has the snc\_internal role.

</td><td>

Add the snc\_external role.

</td><td>

The action is aborted.

</td></tr><tr><td>

The user has the snc\_external role.

</td><td>

Add the snc\_internal role.

</td><td>

The action is aborted.

</td></tr><tr><td>

The user has no explicit role.

</td><td>

Add the snc\_internal or snc\_external role.

</td><td>

The role is added.

</td></tr><tr><td>

The user has both explicit roles \(existing collision\).

</td><td>

Add the user to a group with no roles.

</td><td>

The action is aborted.

</td></tr><tr><td>

A role not associated with any users contains the snc\_internal role.

</td><td>

Add the snc\_external role.

</td><td>

The action is aborted.

</td></tr><tr><td>

A role not associated with any users contains the snc\_external role.

</td><td>

Add the snc\_internal role.

</td><td>

The action is aborted.

</td></tr><tr><td>

A role contains both explicit roles \(existing collision\).

</td><td>

Add the role to a user, role, or group.

</td><td>

The action is aborted.

</td></tr><tr><td>

A group with no members has the snc\_internal role.

</td><td>

Add the snc\_external role.

</td><td>

The action is aborted.

</td></tr><tr><td>

A group with no members has the snc\_external role.

</td><td>

Add the snc\_internal role.

</td><td>

The action is aborted.

</td></tr><tr><td>

A group with no members has no roles.

</td><td>

Add the snc\_internal or snc\_external role.

</td><td>

The role is added.

</td></tr><tr><td colspan="3">

Indirect collision

</td></tr><tr><td>

Role containment with collision

</td><td>

1.  Grant a role called Test Role to a user with the snc\_internal role.
2.  Add the snc\_external role Test Role.

</td><td>

The action is aborted.

</td></tr><tr><td>

Role containment without collision

</td><td>

1.  Grant a role called Test Role to a user with no roles.
2.  Add the snc\_external role to Test Role.

</td><td>

The role is added to both the user and Test Role.

</td></tr><tr><td>

Group containment with collision

</td><td>

1.  Add a user who has the snc\_internal role to a group called Test Group 2 \(child of Test Group 1\).
2.  Add the snc\_external role to Test Group 2.
3.  Add the snc\_external role to a parent group called Test Group 1 \(parent of Test Group 2\).

</td><td>

The action is aborted.

</td></tr><tr><td>

Group containment without collision

</td><td>

1.  Add a user with no roles to a group called Test Group 2 \(child of Test Group 1\).
2.  Add the snc\_external or snc\_internal role to Test Group 1 \(parent of Test Group 2\).

</td><td>

The role is added to the parent group, the child group, and the user.

</td></tr><tr><td rowspan="2">

Group containment plus role containment with collision

</td><td>

Add contains\_external to Test Group 1, the parent of Test Group 2.

</td><td>

Test Group 1 and Test Group 2 both get contains\_external, but don't explicitly get the snc\_external role.

</td></tr><tr><td>

Add the snc\_internal role to Test Group 2, the child of Test Group 1.

</td><td>

The action is aborted.

</td></tr><tr><td>

Group parent change plus group containment

</td><td>

1.  Remove Test Group 1 as the parent of Test Group 2.
2.  Add the snc\_internal role to Test Group 1.
3.  Add the snc\_external role to Test Group 2.
4.  In Test Group 2, set Test Group 1 as the parent group and save.

</td><td>

The action is aborted.Repeat for already nested groups, with the same expectation.

</td></tr></tbody>
</table>The cause of an aborted action appears in the error message and must be addressed before another attempt succeeds.

For direct cases, such as adding an explicit role to an individual user, verify which explicit role the user should have. If the user has the wrong explicit role, it must first be removed, and then the correct explicit role must be added.

For indirect cases,such as adding an explicit role to a group \(so that a group member would be assigned both explicit roles\), evaluate whether that user should be in the group. Also determine whether the group should be given the explicit role, including any inheritance through group hierarchy and role containment.

Note that the ServiceNow AI Platform reports only the first potential collision encountered. If repeated attempts continue to fail after remediation, with a new root cause each time, re-evaluate the relevant user/group/role interdependence more broadly. You may want to rethink how groups and role containments are structured.

**Parent Topic:**[Roles installed with Customer Service Management](../../../product/customer-service-management/reference/r_RolesInstalledWithCustomerService.md)

