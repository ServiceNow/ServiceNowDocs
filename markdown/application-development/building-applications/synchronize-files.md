---
title: Synchronize the current project between a Visual Studio Code workspace and a ServiceNow instance
description: Synchronize files between the Visual Studio Code workspace \(client/local\) and the instance \(server\) bi-directionally.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-applications/synchronize-files.html
release: australia
product: Building Applications
classification: building-applications
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Synchronization between Visual Studio Code and a ServiceNow instance, ServiceNow Extensions for Visual Studio Code, Building pro-code applications, Developing your application, Building applications]
---

# Synchronize the current project between a Visual Studio Code workspace and a ServiceNow instance

Synchronize files between the Visual Studio Code workspace \(client/local\) and the instance \(server\) bi-directionally.

## Before you begin

[Create your project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/create-project.md) and start editing your applications.

Role required: none.

## About this task

The changes made to the application files in the Visual Studio Code workspace are initially stored in the local file system. When you run the **Sync** command, the local changes made to the application files are sent to the server for persistence.

## Procedure

1.  Click **Sync** on the status bar on the bottom of the Visual Studio Code IDE.

    You can also use a keyboard shortcut, Control+Shift+P on Windows or Command+Shift+P on MacOS, to open the command palette and choose **Now: Sync Current Project** from the list.

    \[Omitted image "vscode-syncproject.png"\] Alt text: Command to sync project

    -   If the changes occur either on the server or on the client, the extension synchronizes the file successfully without showing up any errors.
    -   If there are no differences between local and server versions, then the message **No changes detected** appears on the bottom of the page.
    -   If the same file is modified both on client and server, then the system shows up the conflicts.
2.  If a conflict list is displayed, right-click on the conflicting file to open the context menu and select from the context menu.

    Alternatively, select the file and click **Open Diff** menu from the top of the page.

    \[Omitted image "vscode-conflict-changes.png"\] Alt text: Conflicting files display

    -   Choose **Override Server** if you want to overwrite the server version with the client version
    -   Choose **Override Local** to overwrite the client version with the server version.
    -   Choose **Mark as resolved** to remove the flag indicating a conflict. The server version will be overwritten in the next synchronization.
    \[Omitted image "vscode-opendiff.png"\] Alt text: Differences between client and server file versions

3.  Retain the desired changes in the client file and save.

4.  Once you have resolved all file conflicts, click **Mark as Resolved** under **Conflicting Files**.

    The changes are synchronized on the next sync. When the changes are merged successfully, the message **Sync completed successfully** appears in the bottom of the page.

    **Note:** The files are checked for syntax errors at the beginning of synchronization process. Any errors found are presented in the problem tab at the bottom of the screen.


## What to do next

All the changes are tagged to the update set in the status bar. When a project is loaded or selected, the default update set is displayed in the status bar. Click the update set picker to choose the current update set \(valid until the IDE or project is closed\). If you do not explicitly select an update set, all writes happen to the default update set.

**Parent Topic:**[Synchronization between Visual Studio Code and a ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/vscode-sync.md)

