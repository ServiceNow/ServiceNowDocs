---
title: Manage files in the config data model using file nodes
description: Add and manage files using file nodes in the config data model of a CDM app or in a component library.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [File nodes in CDM, File attachments in config data, Attach files in CDM application, collection, deployable]
breadcrumb: [Viewing and editing config data, Using DevOps Config, DevOps Config, IT Service Management]
---

# Manage files in the config data model using file nodes

Add and manage files using file nodes in the config data model of a CDM app or in a component library.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_editor or cdm\_admin

## About this task

When you attach a file to an applicable node, a file node is created under that node. The file node contains a link to the attached file that stores configuration data. For example, a properties file or a logo image file.

-   In an app, you can add the file node to a node under the component, collection, or deployable folder. The file nodes in a component are also included when you include a component to a collection and the collection to the deployable in an app. You can override the file nodes included at the collection or deployable level, like any other config data item.
-   In a component library, you can add a file node to a node under a shared component. When the shared component is used in an app, the file nodes are copied along with the file attached to them.

App developers and members of the authoring group of the app can access the file nodes and also download their attached files. They can manually validate the content of the file and then publish the snapshot. DevOps users can [export the validated config data](cdm-cfg-data-export-from-ui.md), including file nodes with URLs to the attached files hosted on the ServiceNow instance where the export was executed.

## Procedure

1.  Navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace**.

2.  Open a DevOps Config app or a component library to add a file node to its config data model.

<table id="choicetable_mr1_r1p_1yb"><thead><tr><th align="left" id="d95092e114">

Option

</th><th align="left" id="d95092e117">

Steps

</th></tr></thead><tbody><tr><td id="d95092e123">

**Adding a file node in an app**

</td><td>

1.  Select the apps icon \(![DevOps Config apps icon](../../devops-config/image/devops-config-apps-icon.png)\) in the left navigation pane.
2.  Select an app from the Applications list.
3.  Select **Edit config data** to [open a changeset.](cdm-changeset-cr-u.md)


</td></tr><tr><td id="d95092e162">

**Adding a file node in a component library**

</td><td>

1.  Select the component libraries icon \(![Component libraries icon.](../image/icon-component-libraries.png)\) in the left navigation pane.
2.  Select a component library to open or [create one](cdm-comp-library-create.md).
3.  Select **Edit** to open a changeset.


</td></tr></tbody>
</table>    A changeset is opened with the **Config data** tab selected.

3.  In the config data tree, select the more actions icon \(![More actions icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) next to a node to which you want to add a file node, and then select the **Add file** from the menu.

    **Note:** In an app, you can add a file node to a node under the component, collection, or deployable, but not directly to the component, collection, or deployment folder in an app. In a shared library, you can add a file node to a node under a shared component.

4.  Add a file to create a file node.

    1.  In the Add file dialog box, browse and select a file from your system, and select **Add file**.

        You can add a MIME-type file supported by the ServiceNow AI Platform with a maximum file size of 5 MB.

    2.  In the **Node name** field, provide a name for the file node.

        By default, the attached file name is populated as the file node name. The **Content type** field is also populated with the content type of the attached file.

    3.  Select **Add file**.

    The file node is added to the selected node. Select the file node in the config data tree to display its metadata in the File information pane and preview the file's content in the File content pane.

    **Note:** The content preview is available for the files with the following MIME types: `text/yaml,text/css,text/csv,text/html,text/javascript,text/plain,text/richtext,text/x-vcard,text/x-vcalendar,application/xml,application/javascript,application/json`. To view content for additional MIME type files, add them as a comma separated list to the system property **sn\_cdm.attachment.display\_mime\_types**. The preview is not available for binary file MIME types, such as audio, image, and video.

    ![A file node added to a component node.](../image/cdm-file-node-preview.png)

5.  After the file node is added to the config data, you can perform the following actions on the file node or the file attachment within it.

    **Note:** All actions on the file node or its file attachment can only be done via the More actions menu on the file node.

<table id="choicetable_o2f_b2n_1yb"><thead><tr><th align="left" id="d95092e306">

Action

</th><th align="left" id="d95092e309">

Steps

</th></tr></thead><tbody><tr><td id="d95092e315">

**Rename the file node**

</td><td>

1.  Select the more actions icon next to the file node, and then select **Rename** from the menu.
2.  In the Rename dialog box, enter a new name of the file node in the **Node name** field.
 If the file node is included in the collection, it’s renamed there as well.

</td></tr><tr><td id="d95092e342">

**Extract variables**

</td><td>

1.  Select the more actions icon next to the file node, and then select **Extract variables** from the menu.
2.  In the Extract variables dialog box, specify the file path you want to extract the variables to.
 All variables in the file node tagged as @@&lt;variableName&gt;@@ are extracted to the file path you specified. The variable is then modified to also include the file path.

 You can then resolve all the extracted variables. Define the extracted variables and then select **Apply variables** from the form context menu. This action replaces all extracted variables in the file content with the defined variable values.

</td></tr><tr><td id="d95092e372">

**Delete the file node**

</td><td>

1.  Select the more actions icon next to the file node, and then select **Delete** from the menu.
2.  In the Delete pop-up, select **Delete**.
 Deleting the file node has the following effect on it and its file attachment:

-   If the file node is included in the collection, it’s also deleted from there. Any overridden file node becomes a direct file node.
-   If the file node is created in the currently opened changeset that is not yet committed, then the file node and its file attachment are permanently deleted.
-   If the file node was created in a previously committed changeset and is deleted in the currently opened changeset, then the file node is deleted from the config data but the file attachment remains in the system.


</td></tr><tr><td id="d95092e410">

**Download the file attachment**

</td><td>

Select the more actions icon next to the file node, and then select **Download file** from the menu.Alternatively, you can download the file by selecting the file node and then selecting **Download** on the File information pane.

</td></tr><tr><td id="d95092e428">

**Replace the file attachment**

</td><td>

1.  Select the more actions icon next to the file node, and then select **Replace file** from the menu.
2.  In the Replace file dialog box, attach a file from your system, and select **Replace file**.


</td></tr><tr><td id="d95092e452">

**Override an included file node**

</td><td>

If a file node is included in a collection and into a deployable, then you can override it by replacing the attached file with a new one.1.  Select the more actions icon next to the included file node in the collection or deployable folder, and then select **Replace file** from the menu.
2.  In the Replace file dialog box, attach a file from your system, and select **Replace file**.


</td></tr></tbody>
</table>
