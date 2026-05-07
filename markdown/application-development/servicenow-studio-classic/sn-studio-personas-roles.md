---
title: ServiceNow Studio personas and roles
description: Admins, delegated developers, and users with Guided Application Creator roles have access to work in ServiceNow Studio.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing access to ServiceNow Studio, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio personas and roles

Admins, delegated developers, and users with Guided Application Creator roles have access to work in ServiceNow Studio.

## ServiceNow Studio personas

Admins and delegated developers have different capabilities in ServiceNow Studio. Admins can delegate people to work on certain apps and app files by providing delegated developer permissions.

For more information about roles and access to different app development tools, see [Working with roles and access in app development tools](working-with-roles-and-access.md).

<table id="table_clb_2w1_xcc"><thead><tr><th>

Role

</th><th>

Permissions

</th><th>

Capabilities

</th></tr></thead><tbody><tr><td>

Delegated developer \(delegated\_developer\)

</td><td>

Delegated developers have access to just the app or apps they're delegated to. These permissions may vary based on your configuration.

</td><td>

-   Access ServiceNow Studio.
-   Update apps that they are given delegated development permissions for.
-   Create an update set to package changes.
-   Create and update app files and other metadata records.
-   Submit an app for deployment through update sets, pipelines, or the Application Repository.

</td></tr><tr><td>

Admin

</td><td>

Admins can review and approve tasks related to custom application development.

</td><td>

-   Access ServiceNow Studio.
-   Create apps in ServiceNow Studio.
-   Edit existing apps and app files or delegate development to someone else.
-   Create, edit, and manage update sets.
-   Update existing metadata records.
-   Create and edit global \(unscoped\) metadata records.

</td></tr><tr><td>

Guided Application Creator \(GAC\) roles \(sn\_g\_app\_creator.app\_creator, sn\_g\_app\_creator.global\)

</td><td>

Users with GAC roles can access ServiceNow Studio and create apps. After creating an application, the user receives the delegated\_developer role for that application.

</td><td>

-   Access ServiceNow Studio.
-   Create custom applications.
-   With the GAC Global role, create custom global apps.

</td></tr><tr><td>

ServiceNow Studio admin / Unified Developer Core \(UDC\) admin \(sn\_udc.admin\)

</td><td>

Provides administrative access to tables within ServiceNow Studio scope and configuration access to the experience switcher roles.

</td><td>

Granular admin role that enables the following actions:-   Managing all ServiceNow Studio system properties, settings, and configurations.
-   Managing roles and permissions specific to ServiceNow Studio.
-   Configuring the experience switcher roles across Creator Studio, ServiceNow Studio, and ServiceNow IDE.

For more information about granular admin roles, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Preferred tables admin \(sn\_prfrd\_tables.admin\)

</td><td>

Provides administrative access to configure preferred tables for Table Builder.

</td><td>

Granular admin role that enables you to configure preferred tables in your instance for Table Builder.**Note:** Table Builder itself does not require an additional admin role.

</td></tr><tr><td>

Metadata-specific admin roles-   Business rule admin
-   Script include admin

</td><td>

Provide access to ServiceNow Studio

</td><td>

Metadata-specific admin roles are existing roles on the ServiceNow AI Platform that provide developers with admin access to a specific metadata type. For example, a script include admin allows a developer to CRUD any script include on the ServiceNow AI Platform and perform development on script includes in ServiceNow Studio. Each granular metadata-specific admin role must:

-   Enable CRUD access to the metadata types they represent directly within ServiceNow Studio.
-   Be configurable within the experience switcher.

</td></tr></tbody>
</table>**Parent Topic:**[Managing access to ServiceNow Studio](manage-access-to-servicenow-studio.md)

