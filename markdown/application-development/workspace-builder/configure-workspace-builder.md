---
title: Configure a workspace in Workspace Builder
description: Edit a workspace in Workspace Builder to make customizations in App Engine Studio \(AES\).
locale: en-US
release: xanadu
product: Workspace Builder
classification: workspace-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Add a workspace, Add an application experience, Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure a workspace in Workspace Builder

Edit a workspace in Workspace Builder to make customizations in App Engine Studio \(AES\).

This video shows you how to perform the following procedure.

Configure a workspace in Workspace Builder

## Before you begin

Before you can configure a workspace in Workspace Builder, you must first create the workspace. See [Add a workspace](add-workspace.md).

Role required: sn\_app\_eng\_studio.user or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

You can customize essential elements and components in Workspace Builder. For more complex configurations, or if you don't have the full entitlement for AES, you must edit the workspace in UI Builder.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Next to the workspace you created, select the additional actions icon \(![Additional actions icon](../image/additional-actions-icon-purple.png)\) and then select **Edit**.

    You can also select the bar that lists the workspace in the Experience section of your app.

    ![Select to edit a workspace](../image/wb-edit-worspace-experience-purple.png "Edit a workspace")

    The Workspace Builder tab displays your workspace within AES:

    -   The left navigation panel is a list of pages or components, or building blocks of a page, that you can include in your workspace.

        **Note:** The home page is an essential part of the workspace, and thus can't be hidden or removed.

    -   The middle canvas is an in-line editing space for the home page for workspaces created in AES after Tokyo. For lists and other pages, the middle canvas is a preview of what you configure in the right configuration panel. You can preview workspace home pages built before Tokyo in Workspace Builder, but you must edit them in UI Builder.
    -   The right configuration panel is the configuration panel for working with selected components.
    ![Create a workspace quickly with Workspace Builder](../image/workspace-builder-1-purple.png)

    If you created the workspace that contains a technical dashboard, Workspace Builder prompts you to **Open in UI Builder** when you try to edit the workspace.

4.  Edit the basic settings for the workspace by selecting **Workspace settings**.

    For more information, see [Configure workspace settings in Workspace Builder](configure-workspace-settings.md).

5.  Adjust the home page elements and widgets by resizing, reorganizing, or reconfiguring them.

    For more information on editing a clickable home page, see [Configure a workspace home page in Workspace Builder](edit-workspace-home-page.md).

    **Note:** If the workspace was created before Tokyo, you must edit it in UI Builder. See [UI Builder](../../../administer/ui-builder/concept/ui-builder-overview.md) for more information.

6.  Add or edit a list category and any subsequent filtered lists.

    For more information, see [Configure lists for a workspace in Workspace Builder](add-workspace-list.md).

7.  Enable an Analytics Center for the workspace.

    For more information, see [Configure analytics for a workspace in Workspace Builder](configure-analytics-workspace.md).

8.  Add and edit a record page to configure the settings, tables, and related links that the workspace should support.

    When you create a record page, you're creating the metadata view, or shell, using a record page template for a type of record. You then edit the record page in Table Builder. Within Workspace Builder, you can only change the contextual side panel and the related items.

    For more information, see [Configure a record page for a workspace in Workspace Builder](configure-record-page-workspace.md).

9.  Preview the workspace in a new browser tab by clicking **Preview**.


## Result

If you made additional, more complex configurations to the workspace in UI Builder, such as custom additions to the contextual side panel or custom components, those changes may not appear in Workspace Builder.

**Note:** Your workspace must have a home page and lists for you to edit it in Workspace Builder. If they aren't present, you must edit the workspace in UI Builder.

**Parent Topic:**[Add a workspace](add-workspace.md)

