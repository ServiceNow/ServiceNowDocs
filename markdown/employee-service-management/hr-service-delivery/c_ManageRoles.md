---
title: Manage HR roles
description: Roles control access to features and capabilities in modules in the HR application.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Manage HR roles

Roles control access to features and capabilities in modules in the HR application.

The HR Service Delivery Scoped app can help prevent users outside of the HR organization from accessing HR data.

Scoped roles for both HR case workers and HR clients \(employees, contractors, alumni, and others\) grant access to HR services. Users without an HR scoped role typically cannot view HR cases or HR profile information. For information on all the roles installed with Case and Knowledge Management plugin, see [Components installed with Case and Knowledge Management](../reference/components-installed-with-case-and-knowledge-management.md).

Only the HR Administrator \[sn\_hr\_core.admin\] can assign scoped HR roles.

To configure your system, you must log in as a System Administrator \[admin\]. The HR Administrator \[sn\_hr\_core.admin\] role is contained in the System Administrator \[admin\] role. The combination of these two roles allows a user to perform all tasks associated with configuring your system.

After system configuration, ensure that only the HR Administrator \[sn\_hr\_core.admin\] role has access to sensitive information. Remove the HR Administrator role from System Administrator \[admin\] role to help prevent the System Administrator from viewing sensitive HR information via forms, lists and UI.

After granting access to a role, all the groups or users assigned to the role also have access. Roles can contain other roles, and grants access to any role that contains it.

**Note:** IT System Administrators \(admin\) can still impersonate ServiceNow users. When impersonating a user with an HR scope-protected role, an admin cannot access features granted by that role unless the admin already possesses those HR scope-protected roles. For more information on impersonating a user, see [Impersonate a user](https://www.servicenow.com/docs/access?context=c_ImpersonateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## HR Performance Analytics

To configure the Performance Analytics \(PA\) dashboard, assign the Performance Analytics Administrator \[pa\_admin\] role to the HR Administrator \[sn\_hr\_core.admin\] role.

**Note:** Only the System Administrator \[admin\] can assign PA roles to employees.

<table id="table_alz_h4f_gw"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

System Administrator \[admin\]

</td><td>

Also known as admin and IT admin.Within the global scope of the application, has access to all system features, functions, and data, regardless of security constraints.

 -   Grant users with the delegated developer role \[delegated\_developer\].
-   Build export sets, move content between instances \(development to production\), and clone instances.
-   Run guided setup or modules to manage:

Company-wide objects like user, departments, and locations.


</td></tr><tr><td>

HR Administrator \[sn\_hr\_core.admin\]

</td><td>

This role can:

-   Assign users any of the HR roles.
-   View and access the HR Service Portal.
-   View, create, and edit HR cases in **HR Case Management**.
-   Access and create HR tasks inside an HR case using the **Add Task** related link.
-   View, create, and edit HR profiles including sensitive information like salary.
-   Create HR profiles and generate for multiple users through custom criteria.
-   Associate any user to HR roles, groups, and skills.
-   View and access **HR Administration**.
-   View and access **HR Dashboards &amp; Reports**.
-   Run **Application View** to manage:

HR objects like HR roles and profiles.

**Note:** When the Human Resources Scoped App: Core \(com.sn\_hr\_core\) and Lifecycle Events \(com.sn\_hr\_lifecycle\_events\) plugins are active, the Lifecycle Admin \(sn\_hr\_le.admin\) role is part of HR Admin \(sn\_hr\_core.admin\).


</td></tr><tr><td>

Delegated Developer \[delegated\_developer\]

</td><td>

When added to the HR Administrator role, can:-   Access, and manage HR objects like HR profile, cases, groups, roles, service catalog objects, and Service Portal.
-   Modify HR application-related objects like skills, Knowledge Base, chat, notifications, surveys, reports, integrations, and SC.
-   Modify application structures like tables, business rules, and client-side validation,

</td></tr><tr><td>

User with HR role

</td><td>

There are specific HR roles that allow users access to specific areas of the system. For example, the HR profile reviewer \[sn\_hr\_core.profile\_reader\] role can read profiles, but not edit them.

</td></tr></tbody>
</table>After system configuration, to help prevent the System Administrator from accessing sensitive information:

-   Remove the HR Administrator \[sn\_hr\_core.admin\] role from System Administrator \[admin\].
    -   The base system requires a user with the System Administrator role to run scheduled jobs. For details on HR scheduled jobs, see [Components installed with Case and Knowledge Management](../reference/components-installed-with-case-and-knowledge-management.md).
    -   To ensure the scheduled jobs run, change the user in the **Run as** field for each scheduled job to a user that has the HR admin role.

        **Note:** Changing the user allows the scheduled jobs to run, but only a user with the System Admin role can view and run a scheduled job on demand.

    -   Change the scope of the application to Human Resources: Core application. For information on changing the scope, see [Contextual development edit messages](https://www.servicenow.com/docs/access?context=c_WarningMessages&version=australia&pubname=australia-application-development&ft:locale=en-US).
    -   Reveal the **Run as** field. For information on revealing hidden fields on a form, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Log out and log back in to ensure that the changes take effect.

    **Note:** Ensure that you have completed setup before removing the HR Administrator role.

    -   **Minimum number of scoped admins required**

        System properties determine the minimum number \(default is two\) of scoped admins that must be active for an application.

        To list the properties, enter `sys_properties.list` in the filter navigator and search for the property to configure.

        The list of system properties and what scoped admin can access:

    -   **System properties**

        |Property Name|Scoped Admin|
        |-------------|------------|
        |sn\_hr\_core.min\_admin\_count|HR admin \[sn\_hr\_core.admin\]|
        |sn\_hr\_ef.min\_admin\_count|Employee Document Management admin \[sn\_hr\_ef.admin\]|
        |sn\_hr\_integrations.min\_admin\_count|HR Integration Admin \[sn\_hr\_integrations.admin\]|
        |sn\_hr\_le.min\_admin\_count|HR Lifecycle Event Admin \[sn\_hr\_le.admin\]|
        |sn\_hr\_le\_pa.admin\_count|HR Lifecycle Event Performance Analytics Admin \[sn\_hr\_le\_pa.admin\]|
        |sn\_hr\_pa.min\_admin\_count|HR Performance Analytics Admin \[sn\_hr\_pa.admin\]|
        |sn\_hr\_pj.min\_admin\_count|HR Parental Journey Admin \[sn\_hr\_le\_pj.admin\]|
        |sn\_hr\_sp.min\_admin\_count|HR Service Portal Admin \[sn\_hr\_sp.admin\]|
        |sn\_hr\_va.min\_admin\_count|HR Virtual Agent Admin \[sn\_hr\_va.admin\]|
        |sn\_templated\_snip.min\_admin\_count|Response Template Admin \[sn\_templated\_snip.admin\]|
        |sn\_hr\_ws.min\_admin\_count|HR Agent Workspace Admin \[sn\_hr\_ws.admin\]|


-   **[Remove HR Administrator role from IT System Administrators](../task/t_HRRemoveAdminRole.md)**  
After system configuration, remove the HR Administrator role \(sn\_hr\_core.admin\) from IT System Administrator role \(admin\) to help prevent IT System Administrators from viewing sensitive HR information via forms, lists and UI.
-   **[Add Delegated Developer to HR Administrator](../task/t_HRAdminRoles.md)**  
For an HR Administrator \[sn\_hr\_core.admin\] to perform some platform duties, the delegated developer role must be added.
-   **[Manage HR Groups](../task/t_ManageHRGroups.md)**  
HR Groups are a set of users with common job skills.
-   **[HR skills management](c_HRSkillsManagement.md)**  
Your organization can define HR skills to establish the qualifications of HR staff. Skills can be included in the auto-assignment process used to assign HR agents to HR cases and tasks.
-   **[Configure escalation rules for HR cases](../task/t_CreateOrModifyEscalationRules.md)**  
Create escalation rules to automatically route HR cases from one tier to another based on agent skills and workload.
-   **[Client roles](c_ClientRoles.md)**  
You can control what HR functionality that an employee can access using Client Roles. You can license all employees or provide HR services to users in a specific location or group.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

