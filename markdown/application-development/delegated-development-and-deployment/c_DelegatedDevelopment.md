---
title: Delegated development and deployment
description: Delegated development allows designated users without a system admin role to develop or deploy applications on the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Delegated Development, Delegated Development, Planning your application, Building applications]
---

# Delegated development and deployment

Delegated development allows designated users without a system admin role to develop or deploy applications on the ServiceNow AI Platform.

If you have the application-specific admin role or the system-level admin role, you can delegate application development to designated developers at the application level.

## Delegated deployment tasks

You can also delegate deployment tasks \(application publishing, first-time installation, or update\) to developers or non-admin users, such as Change Management personnel. You delegate deployment tasks to specific users at the application level, or through assignment of specific user roles at the instance level.

<table id="table_ugl_svv_jdb"><thead><tr><th>

Assignment Method

</th><th>

Applies to

</th><th>

Available options

</th></tr></thead><tbody><tr><td>

Setting deployment permissions in Manage Developers. See [Delegate development and deployment permissions to personnel](../task/t_AddADeveloper.md)

</td><td>

Specific applications

</td><td>

Publishing and upgrades of specific applications. Publishing options include the application repository, ServiceNow Store, and update sets.

</td></tr><tr><td>

Assignment of deployment user roles to specific persons. See [Instance-specific deployment user roles](delegated_deployment_user_roles.md).

</td><td>

Local non-production instance \(for example, Development or QA\)

</td><td>

First-time installations and upgrades of all applications that contain the same company as the current instance. For example, applications for ABC Company and XYZ Company display on the Application Client page. A user with this role can only install XYZ Company applications when logged in to a XYZ Company instance. The user cannot install applications for ABC Company.

</td></tr></tbody>
</table>## Application-specific permissions

Developer and deployment permissions are application-specific. For example, a developer who has permission to access all file types for one application does not necessarily have any developer permissions for another application. Administrators must set developer \(and optionally deployment\) permissions for each application. Administrators must be familiar with application files and the system table structure to set developer permissions. For example, a developer expected to create advanced business rules needs both the **All File Types** and **Allow Scripting** developer permissions.

**Important:** If [Application administration](application-administration.md) is enabled, only an application administrator for the target application can delegate developers for an application. Application administrators do not have system admin privileges. To enable a delegated developer to perform the functions granted in the developer permissions, the delegated developer must also be given the application administrator role.

Setting each permission grants one or more system-managed delegated development roles, allowing system admins to retain control over the system. System admins no longer have to elevate developers \(or users who deploy applications\) to the system admin role to enable them to develop or deploy applications.

## Developer and deployment permissions example

As a system administrator, you want to assign Abel Tuter certain developer and deployment permissions for a specific application in your development instance. For more details on developer and deployment permissions, see [Delegate development and deployment permissions to personnel](../task/t_AddADeveloper.md).

![manage developers permissions.](../image/ManageDevelopers2.png).

**Related topics**  


[Application files](c_ApplicationFiles.md)

[Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Install an update to a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallUpdates&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Application sharing](c_SharingApplications.md)

