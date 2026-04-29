---
title: Delegating roles
description: Administrators can grant users the ability to assign roles within groups. However, these users can only assign roles that they already have.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing roles, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Delegating roles

Administrators can grant users the ability to assign roles within groups. However, these users can only assign roles that they already have.

Role delegators are users responsible for assigning roles to other users within a group. This role can be assigned manually by granting the role\_delegator role to the user, or through the **Group Manager Change** business rule.

The **Group Manager Change** business rule, which is disabled by default, automatically grants the role\_delegator role to a user who is designated manager of a group in the **Manager** field on the **Group** form. The role is removed when the user is no longer the manager of the group.

Activate the business rule to take advantage of it. For more information on **Business rules**, see [Classic Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-api-reference&ft:locale=en-US).

## Reviewing Roles and Role Changes

To view roles and role changes:

-   Individual users: Navigate to **User administration** &gt; **Users** select a user, and review the **Roles** related list.
-   Role delegators: Review who can give roles in which groups by navigating to **User administration** &gt; **Role delegators**.
-   For all role changes: To see a history of role changes, navigate to **System security** &gt; **Reports** &gt; **Role audit**. See [Audit user roles](../task/audit-user-roles.md) for more information.

-   **[Designate role delegators](../task/t_RoleDelegation.md)**  
Designate role delegators to assign roles to users who are in a particular group.
-   **[Assign roles as a role delegator](../task/delegate-roles.md)**  
If you're a role delegator, you can delegate roles that are assigned to you for groups that you manage.
-   **[Prevent a role from being delegated](../task/t_PreventARoleFromBeingDelegated.md)**  
You can prevent roles from being delegated to users.

**Parent Topic:**[Managing roles](ua-creating-roles.md)

