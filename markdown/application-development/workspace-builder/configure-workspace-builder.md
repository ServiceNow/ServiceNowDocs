---
title: Edit a workspace in Workspace Builder
description: Edit a workspace in Workspace Builder to make customizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/workspace-builder/configure-workspace-builder.html
release: zurich
product: Workspace Builder
classification: workspace-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, Workspace Builder, Builder library, Developing your application, Building applications]
---

# Edit a workspace in Workspace Builder

Edit a workspace in Workspace Builder to make customizations.

This video shows you how to perform the following procedure.

## Before you begin

Before you can configure a workspace in Workspace Builder, you must first create the workspace. See [Add a workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/workspace-builder/workspace-builder-add-workspace.md).

Role required:

-   admin or Guided Application Creator for ServiceNow Studio.
-   sn\_app\_eng\_studio.user or delegated\_developer for AES. For more information, see [Delegate developers using AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-studio/aes-app-dev-workflow.md).

## About this task

You can customize essential elements and components in Workspace Builder. For more complex configurations, or if you don't have the full entitlement for AES, you must edit the workspace in UI Builder.

## Procedure

1.  Navigate to Workspace Builder.

    For details on how to open Workspace Builder in ServiceNow Studio or AES, see [Accessing Workspace Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/workspace-builder/accessing-workspace-builder-aes-crs.md).

    The Workspace Builder tab displays your workspace within AES:

    -   The left navigation panel is a list of pages or components, or building blocks of a page, that you can include in your workspace.

        **Note:** The home page is an essential part of the workspace, and thus can't be hidden or removed.

    -   The middle canvas is an in-line editing space for the home page for workspaces created in AES after Tokyo. For lists and other pages, the middle canvas is a preview of what you configure in the right configuration panel. You can preview workspace home pages built before Tokyo in Workspace Builder, but you must edit them in UI Builder.
    -   The right configuration panel is the configuration panel for working with selected components.
    \[Omitted image "workspace-builder-1-purple.png"\] Alt text: Create a workspace quickly with Workspace Builder

    If you created the workspace that contains a technical dashboard, Workspace Builder prompts you to **Open in UI Builder** when you try to edit the workspace.

2.  Edit the basic settings for the workspace by selecting **Workspace settings**.

    For more information, see [Configure workspace settings in Workspace Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/workspace-builder/configure-workspace-settings.md).

3.  Adjust the home page elements and widgets by resizing, reorganizing, or reconfiguring them.

    For more information on editing a clickable home page, see [Customize a workspace home page in Workspace Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/workspace-builder/edit-workspace-home-page.md).

    **Note:** If the workspace was created before Tokyo, you must edit it in UI Builder. See [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/ui-builder-overview.md) for more information.

4.  Add or edit a list category and any subsequent filtered lists.

    For more information, see [Create lists for a workspace in Workspace Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/workspace-builder/add-workspace-list.md).

5.  Enable an Analytics Center for the workspace.

    For more information, see [Enable analytics for a workspace in Workspace Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/workspace-builder/configure-analytics-workspace.md).

6.  Add and edit a record page to configure the settings, tables, and related links that the workspace should support.

    When you create a record page, you're creating the metadata view, or shell, using a record page template for a type of record. You then edit the record page in Table Builder. Within Workspace Builder, you can only change the contextual side panel and the related items.

    For more information, see [Add a record page for a workspace in Workspace Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/workspace-builder/configure-record-page-workspace.md).

7.  Preview the workspace in a new browser tab by clicking **Preview**.


## Result

If you made additional, more complex configurations to the workspace in UI Builder, such as custom additions to the contextual side panel or custom components, those changes may not appear in Workspace Builder.

**Note:** Your workspace must have a home page and lists for you to edit it in Workspace Builder. If they aren't present, you must edit the workspace in UI Builder.

