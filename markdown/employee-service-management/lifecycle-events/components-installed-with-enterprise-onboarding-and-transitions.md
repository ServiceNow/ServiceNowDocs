---
title: Components installed with Lifecycle Events
description: Several types of components install with the activation of the Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\] plugin, including tables and user roles.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 4
breadcrumb: [Lifecycle Events reference, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# Components installed with Lifecycle Events

Several types of components install with the activation of the Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\] plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature, and it’s used in some related example tasks.

**Note:** The Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\] plugin activates the sn\_hr\_le.min\_admin\_count system property \[sys\_properties.list\]. This property helps to prevent you from deleting your only Enterprise Onboarding and Transition admin user by requiring a minimum number \(the default is two\) of active users with this role.

## Roles installed

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Lifecycle Events administrator\[sn\_hr\_le.admin\]

</td><td>

Grants access to create, manage, and add users to groups within Lifecycle Events.Can access:

-   Guided Setup
-   Manage Owner Groups
-   Manage Roles
-   LE UI Configuration
-   Onboarding Executive Dashboard
-   Onboarding Executive View

</td><td>

-   sn\_hr\_le.activity\_set\_manager
-   skill\_admin
-   sn\_hr\_le.case\_reader
-   sn\_hr\_le.case\_writer
-   sn\_hr\_core.content\_writer
-   sn\_hr\_le\_pa.admin \(When PA-Content Pack - HR LE Scoped App plugin activates\)
-   pa\_viewer
-   survey\_admin

</td></tr><tr><td>

Activity reader\[sn\_hr\_le.activity\_reader\]

</td><td>

Can read HR activity sets and activities.

</td><td>

None

</td></tr><tr><td>

Activity set manager\[sn\_hr\_le.activity\_set\_manager\]

</td><td>

Can activate and trigger HR activity sets.

</td><td>

sn\_hr\_le.activity\_writer

</td></tr><tr><td>

Activity writer\[sn\_hr\_le.activity\_writer\]

</td><td>

Can create HR activity sets and activities.

</td><td>

sn\_hr\_le.activity\_reader

</td></tr><tr><td>

Case reader\[sn\_hr\_le.case\_reader\]

</td><td>

Can read Lifecycle Events cases.

</td><td>

sn\_hr\_core.case\_reader

</td></tr><tr><td>

Case writer\[sn\_hr\_le.case\_writer\]

</td><td>

Can create Lifecycle Events cases.

</td><td>

-   sn\_hr\_core.case\_writer
-   sn\_hr\_le.case\_reader

</td></tr><tr><td>

HR Performance Analytics administrator\[sn\_hr\_le\_pa.admin\]

</td><td>

Lifecycle Events Performance Analytics Admin role for the scoped application. -   Access and modify the Lifecycle Events PA content packs.
-   Edits Performance Analytics properties.
-   Accesses Admin Console.
-   Launch Dependency Assessment.

 **Note:** This role is contained in the Lifecycle Events administrator role \[sn\_hr\_le.admin\].

</td><td>

None

</td></tr></tbody>
</table>**Important:** After the Lifecycle Events plugin is installed, the Lifecycle Events administrator \(sn\_hr\_le.admin\) role is automatically assigned to the IT system administrator \(admin\) role. Use the admin role to assign the sn\_hr\_le.admin role to at least two users in your organization. If one of the two users is deactivated in the future, the user that remains active can reassign the sn\_hr\_le.admin role to other people in your organization.

After the sn\_hr\_le.admin role has been assigned, remove the role from the admin role to suppress the IT system administrator from viewing sensitive HR information. The removal of the sn\_hr\_le.admin role from admin role ensures that only the Lifecycle Events administrator has access to the sensitive information.

For more information about the process to remove an HR administrator role from the admin role, see [Remove HR Administrator role from IT System Administrators](../task/t_HRRemoveAdminRole.md).

The Lifecycle Events administrator \(sn\_hr\_le.admin\) role with the Delegated Developer \(delegated\_developer\) role can also configure and create COEs. For more information, see [HR Centers of Excellence data model](../concept/hr-centers-of-excellence-coes.md).

You can assign these roles to the appropriate roles, groups, or users in your application.

-   To assign a role to another role, see [Add a role to an existing role](https://www.servicenow.com/docs/access?context=t_AddARoleToAnExistingRole&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

For further information on user administration and how to manage users, see [User administration](https://www.servicenow.com/docs/access?context=c_UserAdministration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity \[sn\_hr\_le\_activity\]

</td><td>

Details of activities that are part of an activity set and together make up a life cycle event. Extends the Activity Base \[sn\_hr\_le\_activity\_base\] table.

</td></tr><tr><td>

Activity Base\[sn\_hr\_le\_activity\_base\]

</td><td>

Extends `sys_metadata`.

</td></tr><tr><td>

Activity Field Mapping\[sn\_hr\_le\_activity\_field\_mapping\]

</td><td>

Details of an activity field mapping that pass information from the parent life cycle event case to an activity.

</td></tr><tr><td>

Activity Set\[sn\_hr\_le\_activity set\]

</td><td>

Details of activity sets and activities that make up Lifecycle Events.

</td></tr><tr><td>

Activity Set Context\[sn\_hr\_le\_activity\_set\_context\]

</td><td>

Created for each Activity Set when the life cycle event initializes. Tracks the state of each set \(triggered, waiting for activities to complete, and more\).Works with the Activity Status \[sn\_hr\_le\_activity\_status\] table to provide filtering for the Lifecycle Events widget on the Ticket page.

</td></tr><tr><td>

Activity Status\[sn\_hr\_le\_activity\_status\]

</td><td>

Created when an Activity Set triggers and tracks the state of the activity created. Tracks the progress of the Activity for each Lifecycle Events case that initializes. Works with the Activity Set Context \[sn\_hr\_le\_activity\_set\_context\] table to provide filtering for the Lifecycle Events widget on the Ticket page.

</td></tr><tr><td>

Fulfiller Activity Configuration\[sn\_hr\_le\_fulfiller\_activity\_config\]

</td><td>

Fulfiller activity configuration passes field information from the Lifecycle Events Case \[sn\_hr\_le\_case\] table to the HR case \[sn\_hr\_core\_case\] table

</td></tr><tr><td>

Fulfiller Activity Configuration Mapping\[sn\_hr\_le\_fulfiller\_activity\_config\_mapping\]

</td><td>

Fulfiller Activity Configuration Mappings copy to all activities created using the fulfiller configuration.

</td></tr><tr><td>

HR Lifecycle Events Case\[sn\_hr\_le\_case\]

</td><td>

Details of a submitted Lifecycle Events case.-   Account Notification
-   Request Onboarding

Extends the HR Case \[sn\_hr\_core\_case\] table.


</td></tr><tr><td>

Lifecycle Events Type\[sn\_hr\_le\_type\]

</td><td>

Lifecycle Events Types are a way to organize activity sets and activities together. Lifecycle Events Types act as a container for activity sets and activities. Lifecycle Events Types are also associated with an **HR Service**.

</td></tr><tr><td>

LE UI Configuration\[sn\_hr\_le\_builder\_ui\_configuration\]

</td><td>

Lifecycle Events user interface configuration details.

</td></tr><tr><td>

Employee Request sn\_hr\_le\_employee\_request

</td><td>

Tracks details of Employee Requests. Created when an Employee Request is created. Works with the Activity Base \[sn\_hr\_le\_activity\_base\] table.

</td></tr><tr><td>

Future To-dos\[sn\_hr\_le\_future\_todo\]

</td><td>

Tracks details about activities waiting to be triggered.

</td></tr></tbody>
</table>For further information on table administration and how to manage data, see [Table administration](https://www.servicenow.com/docs/access?context=c_TableAdministration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Lifecycle Events reference](../concept/lifecycle-events-reference.md)

