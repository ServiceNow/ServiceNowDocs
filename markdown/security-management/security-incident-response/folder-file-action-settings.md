---
title: Configure Folder and File Action Settings
description: Configure the folder and file actions you would like to be enabled from the File Explorer component on the Major Security Incident Management workspace, using the Folder and File Action Settings setup page. As an MSI Administrator, you can control the individual Folder and File Actions displayed on the File Explorer Component.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure File Explorer Component, Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Folder and File Action Settings

Configure the folder and file actions you would like to be enabled from the File Explorer component on the Major Security Incident Management workspace, using the Folder and File Action Settings setup page. As an MSI Administrator, you can control the individual Folder and File Actions displayed on the File Explorer Component.

## Before you begin

Following are the implemented file operations capabilities in the file explorer component using the ServiceNow® flow designer:

<table id="table_u1h_mbr_cqb"><thead><tr><th>

File Operation

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open in Microsoft SharePoint

</td><td>

Opens new browser tab to display Microsoft SharePoint document library file view

</td></tr><tr><td>

Create Folder

</td><td>

Ability to create additional ad hoc folders after the major security incident is created.

</td></tr><tr><td>

Rename Folder

</td><td>

Ability to rename the folders created.

</td></tr><tr><td>

Move File

</td><td>

Allows you to move files between folders in File Explorer component of workspace, resulting in movement of files in Microsoft SharePoint

</td></tr><tr><td>

Locate File

</td><td>

Shows folder location when using the **Recents** view of the File Explorer.

</td></tr><tr><td>

Delete File

</td><td>

Delete the file.

</td></tr><tr><td>

Delete Folder

</td><td>

Delete the folder.

</td></tr><tr><td>

Download File

</td><td>

Downloads the file within the existing MSIM Workspace browser tab for quick viewing.

</td></tr><tr><td>

Rename File

</td><td>

Renames the file.

</td></tr></tbody>
</table>**Note:**

1.  All actions listed are currently enabled by default. You will need to edit the **File Action Settings** if you do not want certain actions to appear. All the settings are currently global for all users, which means no ability to enable actions for a subset of the users that have a specific role.
2.  **Revoke User Access** and **Add Permissions** actions are system related actions. It is recommended not to modify these file actions.

The following sample procedure describes one of the file operations capabilities to disable any specific folder and file action during the configuration of the File Explorer Repository. This procedure is applicable to all other actions that may need to be edited:

Role required: sn\_msi.workspace\_admin

## Procedure

1.  Navigate to **Major Security Incident Management** &gt; **File Explorer** &gt; **Folder and File Action Settings**.

2.  Select the desired record to enable or disable the folder or file action respectively.

3.  Deselect the **Active** check box to disable the folder and file action.

    ![Clearing the Active check box](../image/folder-file-actions-settings-example.png)

4.  **Update** the drive record.

    **Note:** You can also perform the file action directly from the list of displayed file operations by choosing the **Active** column values to either True or False. ![Active column highlighted](../image/folder-file-action-settings.png)

    If the file action performed is disabled then the action will not be displayed on the **Collaborations** tab of the **Major Security Incident Management** workspace.

    ![Three-dot menu with Folder and File Actions highlighted](../image/msim-workspace-folder-file-actions-page.png)


**Parent Topic:**[Configure File Explorer Component](../concept/file-explorer.md)

