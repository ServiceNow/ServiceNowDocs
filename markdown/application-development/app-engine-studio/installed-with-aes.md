---
title: Components installed with AES
description: Several types of components are installed with activation of the App Engine Studio \(AES\) plugin, including tables and user roles.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Installing App Engine Studio, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Components installed with AES

Several types of components are installed with activation of the App Engine Studio \(AES\) plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

App Engine Studio admin

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
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

App Details

 \[sn\_app\_eng\_studio\_app\_details\]

</td><td>

Details about the operations that a developer used to create an application in App Engine Studio. This table is updated automatically as developers build applications in App Engine Studio.

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

Requests to review and publish an application that a developer created in App Engine Studio. From the deployment request form, a reviewer can deploy the application to different environments, accept or reject an application, and send feedback to a developer. For more information, see [Managing app deployments using Pipelines and Deployments](../concept/aes-review-apps-p-and-d.md).

</td></tr><tr><td>

Pipeline

 \[sn\_pipeline\_pipeline\]

</td><td>

Configurations for deploying applications to different environments. There can be only one active pipeline at a time. You update this table as you create a pipeline for the deployment of applications from App Engine Studio. For more information, see [Managing app deployments using Pipelines and Deployments](../concept/aes-review-apps-p-and-d.md).

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
</table>**Note:** The following data preservers are added for tables related to pipelines:

-   Environment
-   Pipeline
-   Pipeline Environment Order
-   Pipeline Types

The data preservers prevent records in these tables from being overwritten during cloning on a non-production instance. For more information, see [Data preservation on cloning target instances](https://www.servicenow.com/docs/access?context=data-preservation&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Installing App Engine Studio](../task/install-aes.md)

