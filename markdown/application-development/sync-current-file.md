---
title: Sync the current file between a Visual Studio Code workspace and a ServiceNow instance
description: Identify conflicting files and merge or overwrite the changes, between the current file in your Visual Studio Code workspace and your instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Synchronization between Visual Studio Code and a ServiceNow instance, ServiceNow Extensions for Visual Studio Code, Building pro-code applications, Developing your application, Building applications]
---

# Sync the current file between a Visual Studio Code workspace and a ServiceNow instance

Identify conflicting files and merge or overwrite the changes, between the current file in your Visual Studio Code workspace and your instance.

## Before you begin

Role required: admin

## Procedure

1.  Click the **Sync** icon ![Sync current file icon](../image/vscode-sync-current-file.png) from the menu on the top-right corner of the Visual Studio Code IDE.

    You can also use a keyboard shortcut Control+Shift+P in Windows and Command+Shift+P in MacOS to open the command palette and choose **Now: Sync Current File** from the list.

    -   If the changes occur either on the server or on the client, the extension synchronizes the file successfully without showing up any errors.
    -   If there are no differences between the local and server versions, then the message **No changes detected** appears on the bottom of the page.
    -   If the same file is modified both on the client and the server, then the system displays the conflicts in a **Conflicting Files** dialog box.
2.  If a conflict list is displayed in a **Conflicting Files** dialog box, check the conflicts.

    -   Compare the **Server** and **Client** version using the **Diff** window, and evaluate the changes.
    -   Override the **Server** or **Client** changes.
    ![Conflicting Files changes list](../image/vscode-conflict-changes.png "Conflicting Files list")

3.  Check for the differences in the **Conflicting Files** list.

    ![Conflicting changes display](../image/vscode-opendiff.png "Conflicting changes display")

    A dialog box displays the following options:

    -   Open Diff: Check for the differences between two versions and make the necessary changes.
    -   Mark Resolved: Resolve the differences and sync the versions.
    -   Overwrite Server: Choose if you want to override the server version with the client version.
    -   Overwrite Local: Choose **Override Local** to override the local version with the server version.
4.  Click **Open Diff**.

    You can see two versions of the file with the differences highlighted.

    ![Window showing differences between client and server](../image/vscode-differences-sync.png "Differences in client and server")

5.  Make changes to the server version from the client version and save the file.

6.  Click **Mark as Resolved** under **Conflicting Files**.

    The changes are successfully synchronized upon the next synchronization. When the changes are merged successfully, the message **Sync completed successfully** appears at the bottom of the page.


**Parent Topic:**[Synchronization between Visual Studio Code and a ServiceNow instance](../concept/vscode-sync.md)

