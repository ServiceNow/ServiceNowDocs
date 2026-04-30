---
title: Configure workspace settings in Workspace Builder
description: Define workspace settings in Workspace Builder to control the basic functionality of the workspace, such as name and record page navigation.
locale: en-US
release: zurich
product: Workspace Builder
classification: workspace-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Workspace Builder, Builder library, Developing your application, Building applications]
---

# Configure workspace settings in Workspace Builder

Define workspace settings in Workspace Builder to control the basic functionality of the workspace, such as name and record page navigation.

This video shows you how to perform the following procedure.

This video shows you how to configure workspace settings in Workspace Builder.

## Before you begin

Role required:

-   admin or Guided Application Creator for ServiceNow Studio.
-   sn\_app\_eng\_studio.user or delegated\_developer for AES. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## Procedure

1.  Navigate to Workspace Builder.

    For details on how to open Workspace Builder in ServiceNow Studio or AES, see [Accessing Workspace Builder](../../workspace-builder/concept/accessing-workspace-builder-aes-crs.md).

2.  Display the Settings form by selecting **Workspace settings** in the Workspace Builder header.

    ![Define settings for your workplace](../image/wb-settings-dialog-new-theme.png)

3.  On the **General** tab of the form, specify or change the basic settings for the workspace by filling in the editable fields.

    **Note:** Some settings are specified when adding a workspace, and can't be changed.

<table id="table_hvw_5sj_wtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the workspace, which is visible to users.

</td></tr><tr><td>

URL

</td><td>

Relative URL for the workspace. The path is automatically created based on the name of your workspace, and is preceded by your instance URL. However, you can customize the path in this field.

</td></tr><tr><td>

Description

</td><td>

Brief description of the purpose of the workspace.

</td></tr><tr><td>

User access

</td><td>

People and groups that can access the workspace. To give unrestricted access to the workspace, leave this field empty.

</td></tr><tr><td>

Search configuration

</td><td>

Source of information when users perform a search in the workspace. You can reuse an existing search configuration by selecting the profile from the menu. Select the **Edit search application** link to make additional, advanced configuration changes.If you select an AI Search profile, the following features are available:

-   Selection of multiple facet values simultaneously, which you can apply using the condition builder.
-   Ability to view parent documents with linked attachments, which you can download.
-   Dark mode.
**Note:** AI Search must be enabled for your instance to select an AI Search profile.

For more information, see [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Show tables included in search configuration

</td><td>

Option that displays one or more tables that the workspace searches as sources.

</td></tr><tr><td>

Workspace theme

</td><td>

Theme to define the visual style of the workspace, which you can select only if Polaris isn't enabled for the instance. Themes are retrieved from the UX Themes \[**sys\_ux\_theme**\] table..

</td></tr></tbody>
</table>    Add only one **User access** role at a time. For more information, see this [Knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1561167).

4.  Select **Save**.

5.  Specify what type of records users can create by selecting the **Record navigation** tab of the form and then filling in the fields.

<table id="table_fkb_3zx_wtb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Navigation type

</td><td>

How users interact with or navigate the workspace. **Tabbed navigation** creates separate tabs for each page, enabling users to work on multiple records at a time. Choose tabs if you anticipate that users must change between records quickly. Tabs also enable users to create records directly from the navigation.

 **Note:** The default navigation type for workspaces built in AES is tabbed, and can't be changed after the workspace is created. You must create the workspace in UI Builder to specify breadcrumb navigation. You can't change the navigation type after the workspace is created.

</td></tr><tr><td>

Table

</td><td>

Data table that is added to when a user creates a record. The table you select automatically has associated lists.**Note:** The tables specified when the workspace was created appear automatically. Select **Add a table** to incorporate additional tables into the workspace. You can add each table only once.

 To remove a table, select its delete icon \(![Delete a table from record navigation](../image/trash-icon.png)\). No confirmation message appears, but you can select **Cancel** to revert the deletion.

</td></tr><tr><td>

Label

</td><td>

Brief label for the option that appears when users select the new record menu. Specify a label that tells users what the record is used for.

</td></tr></tbody>
</table>6.  Select **Save**.


