---
title: Developer permissions
description: Using Manage Developers, administrators can assign one or more developer and deployment permissions to a group or user for a specific application. These permissions designate the specific actions the assigned user can perform for the application.
locale: en-US
release: zurich
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Delegated Development reference, Delegated Development, Planning your application, Building applications]
---

# Developer permissions

Using Manage Developers, administrators can assign one or more developer and deployment permissions to a group or user for a specific application. These permissions designate the specific actions the assigned user can perform for the application.

## Developer permissions

**Note:** If the App Collaboration component is installed, the link appears as **Manage Collaborators**.

|Permission|Description|
|----------|-----------|
|Delete Application|Enables the assigned developer within a scoped app to delete the application.|
|Source Control|Enables the assigned developer full access to source control.|
|All file types|Enables the assigned developer to access all application file types, including some not granted by the other options. This permission is equivalent to granting the user the admin role but with some limitations. Specifically, it provides access to all file types that are configured in your application via the Manage Developers task in the Application Creator.|
|Playbooks|Enables the assigned developer access to the Playbooks design environment to create processes. Editing activity subflows or actions requires the **Flow Designer** permission.|
|Integrations|Enables the assigned developer access to web service APIs, REST APIs, data sources, and Integration Hub - Import.|
|Reporting|Enables the assigned developer access to reports and scheduled reports.|
|Notifications|Enables the assigned developer access to work with automatic email notifications.|
|Decision Tables|Enables the assigned developer access to Decision Tables to create decision logic based on multiple if-then rules.|
|Mobile Builders|Enables the assigned developer access to mobile builders, such as Mobile App Builder.|
|UI Builder|Enables the assigned developer access to UI Builder to create pages for experiences.|
|Workflow|Enables the assigned developer access to the Workflow Editor and Activity Creator.|
|Service Catalog|Enables the assigned developer access to catalog-related file types such as catalog items, record producers, and variables.|
|Service Portal|Enables the assigned developer access to Service Portal editors and tools.|
|Workflow Studio|Enables the assigned developer access to the Workflow Studio design environment to create flows and actions. Script action steps require the **Allow Scripting** permission.|
|Tables &amp; Forms|Enables the assigned developer access to model and layout related file types such as table columns, form layout, and list layout.|
|Manage ACLs &amp; Roles|Enables the assigned developer access to security-related file types such as access controls and user roles.|
|Enable Scripting|Enables the assigned developer write access to script fields such as those in business rules, client scripts, and Workflow Studio script action steps.**Note:** The SNC scripting role is also added.|
|Manage Collaborators|Enables the assigned developer the ability to invite and manage users and groups. This permission enables the delegated developer to invite and manage other developers to the application.|
|Invite Collaborators|Enables the assigned developer the ability to invite users and groups. This permission enables the delegated developer to invite other developers to the application.|
|Delegated Admin|Enables access to all Delegated Development permissions so that permissions don’t need to be granted individually.**Note:** The SNC scripting role is also added.|

## Deployment permissions

Deployment, Manage Collaborators, and Invite Collaborators delegated development permission sets are only available with the Developer Collaborator feature. They don't show in **Manage Developers**.

<table id="developer-permissions_table_cdf_vz3_jdb"><thead><tr><th id="developer-permissions_table_cdf_vz3_jdb_entry_1">

Permission

</th><th id="developer-permissions_table_cdf_vz3_jdb_entry_2">

Description

</th></tr></thead><tbody><tr><td>

Upgrade App

</td><td>

Enables a user with an assigned delegated developer role permission to upgrade the associated application after it has been installed in the current instance.

</td></tr><tr><td>

Publish To Update Set

</td><td>

Enables a user with an assigned delegated developer role permission to publish the associated application to an update set in the current instance. **Note:** Users with this permission can't also have the **Manage Update Set** permission

.

</td></tr><tr><td>

Publish To App Store

</td><td>

Enables a user with an assigned delegated developer role permission to publish associated application to the ServiceNow Store in the current instance. **Note:** The **Upgrade App**, **Publish To App Repo**, and **Publish To App Store** permissions display by default. The **Publish To Update Set** permission only displays if manually enabled by a system administrator.

</td></tr><tr><td>

Manage Update Set

</td><td>

Enables a user with an assigned delegated developer role permission to manage local and retrieved update sets. This permission enables users to create, update, and delete local update sets as well as preview, resolve conflicts, and commit retrieved update sets. **Note:** Users with this permission can't also have the **Publish To Update Set** permission.

</td></tr><tr><td>

Publish To App Repo

</td><td>

Enables a user with an assigned delegated developer role permission to publish the associated application to the application repository in the current instance.

</td></tr><tr><td>

Submit for Deployment

</td><td>

Enables a user with assigned delegated developer role permission to submit the associated application for review and deployment.

</td></tr></tbody>
</table>**Parent Topic:**[Delegated Development reference](delegated-development-reference.md)

