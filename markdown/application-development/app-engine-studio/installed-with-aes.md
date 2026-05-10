---
title: Components installed with AES
description: Several types of components are installed with activation of the App Engine Studio \(AES\) plugin, including tables and user roles.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2026-04-28"
reading_time_minutes: 4
breadcrumb: [Installing, Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Components installed with AES

Several types of components are installed with activation of the App Engine Studio \(AES\) plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

App Engine admin

 \[app\_engine\_admin\]

</td><td>

Administers AES, including users, app configuration, and other management tasks.

 This role is assigned automatically to users in the App Engine Studio Admins group.

</td><td>

-   sn\_request\_read
-   sn\_request\_write
-   sn\_app\_eng\_studio.user

</td></tr><tr><td>

App Engine Studio app template admin

 \[app\_template\_admin\]

</td><td>

Administers the use, sharing, and activation or deactivation of templates.

 This role is assigned by an admin to individual users. For more information, see [Manage template access](../task/manage-template-access.md).

</td><td>

-   app-template-author
-   app-template-runner
-   flow-designer
-   flow-operator

</td></tr><tr><td>

App Engine Studio admin

 \[sn\_app\_eng\_studio.admin\]

</td><td>

Granular admin role that grants access to App Engine Studio and enables administrative access to App Engine Studio tables. You can combine this role with other granular admin roles or delegated development for additional permissions. For more information about granular admin roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

</td><td>

sn\_app\_eng\_studio.user

</td></tr><tr><td>

App Engine Studio user

 \[sn\_app\_eng\_studio.user\]

</td><td>

Builds applications in App Engine Studio.

 This role is assigned automatically to users in the App Engine Studio Users group. For more information, see [Grant user access to AES](../task/grant-aes-access.md).

</td><td>

-   catalog\_builder\_editor
-   app\_template\_runner
-   sn\_g\_app\_creator.app\_creator

</td></tr></tbody>
</table>**Note:** Additional granular admin roles are installed with App Engine Studio dependent applications, including:

-   Collaboration request admin \[sn\_collab\_request.collaboration\_request\_admin\]
-   AES Table Builder Wizard admin \[sn\_table\_bldr\_wzd.table\_bldr\_wzd\_admin\]

You can combine these granular admin roles with other roles to provide the level of access needed for a user's function. For more information about roles in App Engine Studio, see [Configure AES personas and roles](../concept/aes-personas-roles.md). For more information about granular admin roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

App Details

 \[sn\_app\_eng\_studio\_app\_details\]

</td><td>

Details about the operations that a developer used to create an application in App Engine Studio. The table is updated automatically as developers build applications in App Engine Studio.

</td></tr><tr><td>

Applications in Projects

 \[sn\_app\_eng\_studio\_project\_application\_m2m\]

</td><td>

Applications that a developer creates in App Engine Studio. This table is updated automatically as developers build applications in App Engine Studio.

</td></tr><tr><td>

Environment

 \[sn\_pipeline\_environment\]

</td><td>

Instances that you use for the developing, testing, or launching an application. You update this table as you define environments for App Engine Studio.

</td></tr><tr><td>

Deployment Request

 \[sn\_deploy\_pipeline\_deployment\_request\]

</td><td>

Requests to review and publish an application that a developer created in App Engine Studio. From the deployment request form, a reviewer can deploy the application to different environments, accept or reject an application, and send feedback to a developer. For more information, see [Deployment Request form in the Pipelines and Deployments app](deployment-req-form-d-and-p.md).

</td></tr><tr><td>

Pipeline

 \[sn\_pipeline\_pipeline\]

</td><td>

Configurations for deploying applications to different environments. Only one pipeline can be active at a time. You update this table as you create a pipeline for the deployment of applications from App Engine Studio. For more information, see [Managing deployments using Pipelines and Deployments](../concept/manage-deployments-using-p-and-d-aemc.md).

</td></tr><tr><td>

Project

 \[sn\_app\_eng\_studio\_project\]

</td><td>

Details about App Engine Studio development sessions. A project is created automatically when a developer creates an application in App Engine Studio. This table is updated automatically as developers build applications in App Engine Studio.

</td></tr><tr><td>

Resources Content

 \[sn\_app\_eng\_studio\_resources\_content\]

</td><td>

Help resources that a developer can access in App Engine Studio. This table includes configurations to support the default user experience for App Engine Studio.

</td></tr><tr><td>

Resources Content Topic

 \[sn\_app\_eng\_studio\_resources\_content\_topic\]

</td><td>

Categorizations of help resources in App Engine Studio. This table includes configurations to support the default user experience for App Engine Studio.

</td></tr><tr><td>

Taxonomy

 \[sn\_app\_eng\_studio\_taxonomy\]

</td><td>

Application files that a developer creates in App Engine Studio. This table is updated automatically as developers build applications in App Engine Studio.

</td></tr><tr><td>

Taxonomy Category

 \[sn\_app\_eng\_studio\_taxonomy\_category\]

</td><td>

Categorizations for application files in App Engine Studio. By default, application files are categorized as data, experience, logic and automation, or security. This table includes configurations to support the default user experience for App Engine Studio.

</td></tr><tr><td>

Taxonomy Details

 \[sn\_app\_eng\_studio\_taxonomy\_details\]

</td><td>

Details about application files that a developer creates in App Engine Studio. This table includes configurations to support the default user experience for App Engine Studio.

</td></tr></tbody>
</table>**Note:** Data preservers are added for the following tables related to pipelines:

-   Environment
-   Pipeline
-   Pipeline Environment Order
-   Pipeline Types

The data preservers prevent records in these tables from being overwritten during cloning on a non-production instance. For more information, see [Create a clone preserver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-new-clone-preserver.md).

**Parent Topic:**[Installing App Engine Studio](../task/install-aes.md)

