---
title: Building workspaces in AES
description: Workspace Builder for App Engine is a streamlined, no-code environment that enables you to create a custom workspace from within App Engine Studio \(AES\) quickly and efficiently.
locale: en-US
release: xanadu
product: Workspace Builder
classification: workspace-builder
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Add a workspace, Add an application experience, Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Building workspaces in AES

Workspace Builder for App Engine is a streamlined, no-code environment that enables you to create a custom workspace from within App Engine Studio \(AES\) quickly and efficiently.

You can use Workspace Builder to quickly create workspaces for workspaces built starting with Xanadu. Workspace Builder enables you to edit the workspace home page, list pages, and record page contextual side panel directly in the Workspace Builder preview canvas. For workspaces created before Xanadu, or if you need more robust functionalities and configurations, edit the workspace in UI Builder from a tab within AES.

## Parts of a workspace

Build your workspace by including the following pages and elements.

<table id="table_zs3_tzv_15b"><thead><tr><th>

Component

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Home

</td><td>

Landing page for the workspace, which contains a dashboard and appears to users when first accessing the workspace. **Note:** The home page is an essential part of the workspace, and thus can't be hidden or removed.

 For more information on configuring the home page, see [Configure a workspace home page in Workspace Builder](../task/edit-workspace-home-page.md).

 For information on configuring the basic settings for a workspace, see [Configure workspace settings in Workspace Builder](../task/configure-workspace-settings.md).

</td></tr><tr><td>

List

</td><td>

List pages for records from the specified tables, which help users to find individual records in a workspace. **Note:** If you remove the list page/route, you must use UI Builder to edit the workspace, not Workspace Builder.

 You can create a list category and then add filtered lists for each list category. Filtered lists apply unique conditions, ensuring that only the filtered subset of records appears.

 For more information on adding and editing lists in Workspace Builder, see [Configure lists for a workspace in Workspace Builder](../task/add-workspace-list.md).

</td></tr><tr><td>

Analytics

</td><td>

The customizable Analytics Center enables users to track and analyze records and usage with dashboards, data visualizations, and insights on your instance. **Note:** If Analytics Center page/route doesn't exist for a workspace, Workspace Builder is still available, but the Analytics Center tab doesn't appear in the workspace.

 For more information on enabling the Analytics Center for a workspace, see [Configure analytics for a workspace in Workspace Builder](../task/configure-analytics-workspace.md).

</td></tr><tr><td>

Record pages

</td><td>

Pages in a table that give users useful information to work on a task, issue, or incident. Useful information can include priority, state, activity, and so on.Create and customize record pages by using containers and components in different sections of the layout. You can also add a Playbook Experience to a record page.

 For more information, see [Configure a record page for a workspace in Workspace Builder](../task/configure-record-page-workspace.md).

</td></tr></tbody>
</table>**Note:** Your workspace must have a home page and lists for you to edit it in Workspace Builder. If they aren't present, you must edit the workspace in UI Builder.

## Layout for Workspace Builder

The first time you access Workspace Builder, an onboarding modal displays a brief tour of what you can do in Workspace Builder.

Workspace Builder consists of the following sections:

-   A left navigation panel to configure the pages that users can navigate to within the workspace.
-   A preview of the workspace in the middle canvas.
-   A right configuration panel for configuring the selected workspace component.
-   An option to preview the workspace in a new browser tab.

![Basic layout for Workspace Builder: Header, Navigation panel, Configuration panel, and preview pane](../image/wb-home-page-callouts-purple.png "Workspace Builder layout")

The Workspace Builder header has the following navigation options just below the tab, where you can work with the following:

-   Navigation configuration
-   Record pages

## Workspace Builder plugin

To use Workspace Builder, you must enable the com.devsnc\_sn\_workspace\_builder plugin in the sn\_ws\_builder scope. It is a dependency of com.snc.aes.starter\_workspace\_template.

**Parent Topic:**[Add a workspace](../task/add-workspace.md)

