---
title: Exploring Delegated Development
description: Delegated development allows designated users without a system admin role to develop or deploy applications on the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/delegated-development-and-deployment/c\_DelegatedDevelopment.html
release: zurich
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Delegated Development, Planning your application, Building applications]
---

# Exploring Delegated Development

Delegated development allows designated users without a system admin role to develop or deploy applications on the ServiceNow AI Platform.

## Delegated Development overview

If you have the application-specific admin role or the system-level admin role, you can delegate application development to designated developers at the application level.

## Delegated Development users

|User|Description|
|----|-----------|
|System Admin|The system admin can delegate admins, developers, or deployment resources to an application.|
|Delegated Admin|A delegated admin can delegate developers or deployment resources to an application.|
|Application Administrator|If [Application administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/application-administration.md) is enabled, only an application administrator of the target application can delegate developers to an application. If application administration isn’t enabled, an admin user can delegate developers.|
|Delegated Developer|Delegated developers can develop applications on the platform.|
|Deployment Resource|Deployment resources can deploy applications developed by delegated developers on the platform.|

## Delegated Development benefits

<table id="table_etm_x52_ddc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Remove the need to add individual roles for users that have access to all Delegated Development capabilities.

</td><td>

You can assign a user the **Delegated Admin** role to grant access to all permissions at once.

</td><td>

System Admin

</td></tr><tr><td>

Safeguard development-   [Assign source control permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/delegated-dev-source-control.md)
-   [Assign delete permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/assign-delete-permissions.md)

</td><td>

You can administer technical standards to specify which users and groups have access to app resources.

</td><td>

-   System Admin
-   Delegated Admin

</td></tr><tr><td>

[Instance-specific deployment user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/delegated_deployment_user_roles.md)

</td><td>

You can assign roles that enable non-admin users to install or upgrade all applications in specific instances.

</td><td>

Deployment Resource

</td></tr><tr><td>

User permission-   [Administer Delegated Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/administer-delegated-development.md)
-   [Developer permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/developer-permissions.md)

</td><td>

You can assign developer permissions that let individuals or groups build apps without an admin role.

</td><td>

-   System Admin
-   Delegated Admin

</td></tr></tbody>
</table>## Developer and deployment permissions example

As a system administrator you can assign a certain developer and deployment permissions for a specific application in your development instance. For more details on developer and deployment permissions, see [Delegating development permissions to personnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/t_AddADeveloper.md).

\[Omitted image "ManageDevelopers2.png"\] Alt text: manage developers permissions..

## What to explore next

To learn more about configuring and using Delegated Development, see:

-   [Configuring Delegated Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/configuring-delegated-development.md)
-   [Administer Delegated Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/administer-delegated-development.md)

**Related topics**  


[Application files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/c_ApplicationFiles.md)

[Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_InstallApplications.md)

[Install an update to a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_InstallUpdates.md)

[Application sharing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/c_SharingApplications.md)

