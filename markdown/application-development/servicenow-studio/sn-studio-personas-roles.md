---
title: ServiceNow Studio personas and roles
description: Admins, delegated developers, and users with Guided Application Creator roles have access to work in ServiceNow Studio.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing access to ServiceNow Studio, Configuring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
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

</td></tr></tbody>
</table>**Parent Topic:**[Managing access to ServiceNow Studio](manage-access-to-servicenow-studio.md)

