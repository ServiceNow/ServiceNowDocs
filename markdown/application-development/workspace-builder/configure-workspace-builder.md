---
title: Edit a workspace in Workspace Builder
description: Edit a workspace in Workspace Builder to make customizations.
locale: en-US
release: australia
product: Workspace Builder
classification: workspace-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, Workspace Builder, Builder library, Developing your application, Building applications]
---

# Edit a workspace in Workspace Builder

Edit a workspace in Workspace Builder to make customizations.

This video shows you how to perform the following procedure.

Configure a workspace in Workspace Builder

## Before you begin

Before you can configure a workspace in Workspace Builder, you must first create the workspace. See [Add a workspace](../../workspace-builder/task/workspace-builder-add-workspace.md).

Role required:

-   admin or Guided Application Creator for ServiceNow Studio.
-   sn\_app\_eng\_studio.user or delegated\_developer for AES. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

You can customize essential elements and components in Workspace Builder. For more complex configurations, or if you don't have the full entitlement for AES, you must edit the workspace in UI Builder.

## Procedure

1.  Navigate to Workspace Builder.

    For details on how to open Workspace Builder in ServiceNow Studio or AES, see [Accessing Workspace Builder](../../workspace-builder/concept/accessing-workspace-builder-aes-crs.md).

    The Workspace Builder tab displays your workspace within AES:

    -   The left navigation panel is a list of pages or components, or building blocks of a page, that you can include in your workspace.

        **Note:** The home page is an essential part of the workspace, and thus can't be hidden or removed.

    -   The middle canvas is an in-line editing space for the home page for workspaces created in AES after Tokyo. For lists and other pages, the middle canvas is a preview of what you configure in the right configuration panel. You can preview workspace home pages built before Tokyo in Workspace Builder, but you must edit them in UI Builder.
    -   The right configuration panel is the configuration panel for working with selected components.
    ![Create a workspace quickly with Workspace Builder](../image/workspace-builder-1-purple.png)

    If you created the workspace that contains a technical dashboard, Workspace Builder prompts you to **Open in UI Builder** when you try to edit the workspace.

2.  Edit the basic settings for the workspace by selecting **Workspace settings**.

    For more information, see [Configure workspace settings in Workspace Builder](configure-workspace-settings.md).

3.  Adjust the home page elements and widgets by resizing, reorganizing, or reconfiguring them.

    For more information on editing a clickable home page, see [Customize a workspace home page in Workspace Builder](edit-workspace-home-page.md).

    **Note:** If the workspace was created before Tokyo, you must edit it in UI Builder. See [UI Builder](../../../administer/ui-builder/concept/ui-builder-overview.md) for more information.

4.  Add or edit a list category and any subsequent filtered lists.

    For more information, see [Create lists for a workspace in Workspace Builder](add-workspace-list.md).

5.  Enable an Analytics Overview for the workspace.

    For more information, see [Enable analytics for a workspace in Workspace Builder](configure-analytics-workspace.md).

6.  Add and edit a record page to configure the settings, tables, and related links that the workspace should support.

    When you create a record page, you're creating the metadata view, or shell, using a record page template for a type of record. You then edit the record page in Table Builder. Within Workspace Builder, you can only change the contextual side panel and the related items.

    For more information, see [Add a record page for a workspace in Workspace Builder](configure-record-page-workspace.md).

7.  Preview the workspace in a new browser tab by clicking **Preview**.


## Result

If you made additional, more complex configurations to the workspace in UI Builder, such as custom additions to the contextual side panel or custom components, those changes may not appear in Workspace Builder.

**Note:** Your workspace must have a home page and lists for you to edit it in Workspace Builder. If they aren't present, you must edit the workspace in UI Builder.

