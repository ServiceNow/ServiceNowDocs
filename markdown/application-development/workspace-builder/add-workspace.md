---
title: Add a workspace
description: Create a workspace in App Engine Studio \(AES\) to build a space that provides agents, case managers, help desk professionals, and managers with tools to help answer customer questions and resolve customer problems. Workspaces are primarily used for request and fulfillment processes, such as a service desk to manage tickets.
locale: en-US
release: xanadu
product: Workspace Builder
classification: workspace-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Add an application experience, Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add a workspace

Create a workspace in App Engine Studio \(AES\) to build a space that provides agents, case managers, help desk professionals, and managers with tools to help answer customer questions and resolve customer problems. Workspaces are primarily used for request and fulfillment processes, such as a service desk to manage tickets.

This video shows you how to perform the following procedure.

This video shows you how to add a workspace.

## Before you begin

Role required: sn\_app\_eng\_studio.user or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

When you add a workspace you're creating a basic version of it, which you must then continue editing in Workspace Builder before it's ready to deploy. For more complex customizations, edit the workspace in UI Builder.

If you create a workspace from an App Engine Studio workspace experience template, you can edit the home page, lists, and record pages in Workspace Builder. However, if you create the workspace using an application template, you must edit some of its pages and objects in UI Builder.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, next to Experience, select **Add**.

4.  Select **Workspace**, and then select **Begin**.

5.  On the form, fill in the fields.

<table id="table_wrp_z3h_14b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the workspace that appears to users. By default, the workspace shares the same name as your application.**Tip:** Use a name that uniquely identifies the workspace from other experiences. For example, `Office art requests workspace`.

</td></tr><tr><td>

Description

</td><td>

Description of the workspace.

</td></tr><tr><td>

URL

</td><td>

Unique web address of the workspace. By default, the workspace URL is based on the application name, but you can edit it.

</td></tr><tr><td>

Roles

</td><td>

User roles to limit who can access the workspace. -   You must specify at least one role to grant access to the workspace.
-   To use a custom role for your workspace, you must create one in **Security** first.
 For more information, see [Add application security](../concept/add-security.md).

</td></tr></tbody>
</table>6.  Select **Continue** to define data for your workspace.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Primary Table|Data table that workspace users view or update.|
    |Secondary Tables|Additional data tables that workspace users view and update.|

    **Note:** You can select only tables with default views. You can select from two sections: Tables that are already available in your app, and all tables outside the app scope.

    Workspace Builder automatically generates a record page for the table you select.

8.  Select **Continue**, and then select Done.

    After you create the workspace in AES, you must edit it in Workspace Builder by adding or configuring components on each page.

9.  Next to the workspace you created, select the additional actions icon \(![Additional actions icon](../image/additional-actions-icon-purple.png)\) and then select **Edit**.

    You can also select the bar that lists the workspace in the Experience section of your app.

    ![Select to edit a workspace](../image/wb-edit-worspace-experience-purple.png "Edit a workspace")

10. Edit your workspace home page in the In-line editor by selecting **Preview**.

    1.  On your workspace home page, select **Edit**.

        If you don't see **Edit**, you may not have the permissions needed to edit the workspace home page.

    2.  If the workspace is missing an Access Control List \(ACL\), enter the roles that should have access in the Add user roles to continue modal and select the **Add roles** button.

        For more information, see [Configure workspace settings in Workspace Builder](configure-workspace-settings.md) and [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    3.  Adjust the home page elements and widgets by resizing, reorganizing, or reconfiguring them.

        Editing your workspace home page works similarly to editing a dashboard on your workspace. For more information, see [Edit Platform Analytics dashboards](https://www.servicenow.com/docs/access?context=edit-db-in-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

        **Note:** If the workspace was created before Tokyo, you must edit it in UI Builder. See [UI Builder](../../../administer/ui-builder/concept/ui-builder-overview.md) for more information.

        If you created the workspace that contains a technical dashboard, Workspace Builder prompts you to **Open in UI Builder** when you try to edit the workspace.

    4.  Select **Add new element** to add items to your workspace home page.

    5.  Select **Exit Editing Mode** to stop editing in the In-line editor.

11. Edit the workspace in Workspace Builder. For more information, see [Configure a workspace in Workspace Builder](configure-workspace-builder.md).

    You can also add more record pages to the workspace, if needed.

    **Note:** The default workspace record pages are read-only and can't be edited. To change the content of each record page, create a page variant and edit the variant.


-   **[Sample workspaces you can build](../reference/types-of-workspaces.md)**  
App Engine Studio \(AES\) provides a basic workspace that includes a home page, record pages, lists, an Analytics Center, and other functions.
-   **[Building workspaces in AES](../concept/using-workspace-builder.md)**  
Workspace Builder for App Engine is a streamlined, no-code environment that enables you to create a custom workspace from within App Engine Studio \(AES\) quickly and efficiently.
-   **[Configure a workspace in Workspace Builder](configure-workspace-builder.md)**  
Edit a workspace in Workspace Builder to make customizations in App Engine Studio \(AES\).
-   **[Configure workspace settings in Workspace Builder](configure-workspace-settings.md)**  
Define workspace settings in App Engine Studio \(AES\) to control the basic functionality of the workspace, such as name and record page navigation.
-   **[Configure a workspace home page in Workspace Builder](edit-workspace-home-page.md)**  
Edit the home page for a workspace in App Engine Studio \(AES\). Adjust what users see when first accessing the workspace, which is a dashboard.
-   **[Workspace Builder components for home pages](../reference/workspace-builder-components-ref.md)**  
Several UI Builder components are available as elements to build home pages and contextual side panels in Workspace Builder. Workspace Builder helps you quickly create workspaces in App Engine Studio \(AES\).
-   **[Configure a record page for a workspace in Workspace Builder](configure-record-page-workspace.md)**  
Configure a record page for a workspace in App Engine Studio \(AES\). Use containers and components to guide a user through an experience. Each record page is linked to only one data table.
-   **[Configure lists for a workspace in Workspace Builder](add-workspace-list.md)**  
Create list categories in App Engine Studio \(AES\) to add pages that list table records. You can add filter conditions and change columns to create variations on the list.
-   **[Configure analytics for a workspace in Workspace Builder](configure-analytics-workspace.md)**  
Enable the Analytics Center for a workspace in App Engine Studio \(AES\). The Analytics Center enables users to track and analyze records and usage with dashboards, data visualizations, and insights on the instance.

**Parent Topic:**[Add an application experience](../concept/add-experience.md)

