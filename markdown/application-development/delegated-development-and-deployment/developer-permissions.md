---
title: Developer and deployment permissions
description: Using Manage Developers, administrators can assign one or more developer and deployment permissions to a group or user for a specific application. These permissions designate the specific actions the assigned user can perform for the application.
locale: en-US
release: australia
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Delegate permissions, Administer, Delegated Development, Planning your application, Building applications]
---

# Developer and deployment permissions

Using Manage Developers, administrators can assign one or more developer and deployment permissions to a group or user for a specific application. These permissions designate the specific actions the assigned user can perform for the application.

For example, you might grant permissions that enable a user to upgrade the application, publish to the application repository and ServiceNow Store, but prevent publishing to an update set.

## Developer permissions

**Note:** If the App Collaboration Component is installed, the link appears as **Manage Collaborators**.

<table id="table-developer-permissions"><thead><tr><th>

Permission

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delete Application

</td><td>

Grants the assigned developer within a scoped app rights to delete the application.

</td></tr><tr><td>

Source Control

</td><td>

Grants the assigned developer full access to source control.

</td></tr><tr><td>

All File Types

</td><td>

Grants the assigned developer access to all application file types, including some not granted by the other options. This permission is equivalent to granting the user the admin role but with some limitations. Specifically, it provides access to all file types that are configured in your application per the Manage Developers task in the Application Creator. For an example of such file types, see the permissions example in [Delegated development and deployment](../concept/c_DelegatedDevelopment.md).

</td></tr><tr><td>

Playbooks

</td><td>

Grants the assigned developer access to the Playbooks design environment to create processes. Editing activity subflows or actions requires the **Flow Designer** permission.

</td></tr><tr><td>

Integrations

</td><td>

Grants the assigned developer access to web service APIs, REST APIs, data sources, and Integration Hub - Import.

</td></tr><tr><td>

Reporting

</td><td>

Grants the assigned developer access to reports and scheduled reports.

</td></tr><tr><td>

Notifications

</td><td>

Grants the assigned developer access to work with automatic email notifications.

</td></tr><tr><td>

Decision Tables

</td><td>

Grants the assigned developer access to Decision Tables to create decision logic based on multiple if-then rules.

</td></tr><tr><td>

Mobile Builders

</td><td>

Grants the assigned developer access to mobile builders, such as Mobile App Builder.

</td></tr><tr><td>

UI Builder

</td><td>

Grants the assigned developer access to UI Builder to create pages for experiences.

</td></tr><tr><td>

Workflow

</td><td>

Grants the assigned developer access to the Workflow Editor and Activity Creator.

</td></tr><tr><td>

Service Catalog

</td><td>

Grants the assigned developer access to catalog-related file types such as catalog items, record producers, and variables.

</td></tr><tr><td>

Service Portal

</td><td>

Grants the assigned developer access to Service Portal editors and tools.

</td></tr><tr><td>

Workflow Studio

</td><td>

Grants the assigned developer access to the Workflow Studio design environment to create flows and actions. Script action steps require the **Allow Scripting** permission.

</td></tr><tr><td>

Tables &amp; Forms

</td><td>

Grants the assigned developer access to model and layout related file types such as table columns, form layout, and list layout.

</td></tr><tr><td>

Manage ACLs &amp; Roles

</td><td>

Grants the assigned developer access to security-related file types such as access controls and user roles.

</td></tr><tr><td>

Allow Scripting

</td><td>

Grants the assigned developer write access to script fields such as those in business rules, client scripts, and Workflow Studio script action steps.**Note:** The SNC scripting role is also added.

</td></tr><tr><td>

Manage Collaborators

</td><td>

Grants the assigned developer the ability to invite and manage users and groups. This permission allows the delegated developer to further invite and manage other developers to the application.

</td></tr><tr><td>

Invite Collaborators

</td><td>

Grants the assigned developer the ability to invite users and groups. This permission allows the delegated developer to further invite other developers to the application.

</td></tr><tr><td>

Delegated Admin

</td><td>

Grants access to all Delegated Development permissions so that permissions do not need to be granted individually.**Note:** The SNC scripting role is also added.

</td></tr></tbody>
</table>## Deployment permissions

The update set deployment permissions are hidden by default and require a system administrator to enable them with system properties. See [Display or hide update set deployment permissions](../task/display-or-hide-deployment-permissions.md) for more information.

The Submit for Deployment, Manage Collaborators, and Invite Collaborators delegated development permission sets are only available with the Developer Collaborator feature. They will not be shown in Manage Developers.

<table id="table_cdf_vz3_jdb"><thead><tr><th>

Permission

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Upgrade App

</td><td>

Grants a user with an assigned delegated developer role permission to upgrade the associated application after it has been installed in the current instance.

</td></tr><tr><td>

Publish To Update Set

</td><td>

Grants a user with an assigned delegated developer role permission to publish the associated application to an update set in the current instance.**Note:** Users with this permission cannot also have the **Manage Update Set** permission.

</td></tr><tr><td>

Publish To App Store

</td><td>

Grants a user with an assigned delegated developer role permission to publish associated application to the ServiceNow Store in the current instance. **Note:** The **Upgrade App**, **Publish To App Repo**, and **Publish To App Store** permissions display by default. The **Publish To Update Set** permission only displays if manually enabled by a system administrator. For more details, see [Display or hide update set deployment permissions](../task/display-or-hide-deployment-permissions.md).

</td></tr><tr><td>

Manage Update Set

</td><td>

Grants a user with an assigned delegated developer role permission to manage local and retrieved update sets. This permission allows users to create, update, and delete local update sets as well as preview, resolve conflicts, and commit retrieved update sets.**Note:** Users with this permission cannot also have the **Publish To Update Set** permission.

</td></tr><tr><td>

Publish To App Repo

</td><td>

Grants a user with an assigned delegated developer role permission to publish the associated application to the application repository in the current instance.

</td></tr><tr><td>

Submit for Deployment

</td><td>

Grants a user with assigned delegated developer role permission to submit the associated application for review and deployment.

</td></tr></tbody>
</table>