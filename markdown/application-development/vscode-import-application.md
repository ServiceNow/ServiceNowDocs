---
title: Import an application into Visual Studio Code
description: After you create a project, import an application from your instance into the project to begin editing.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a project in VS Code, ServiceNow Extensions for Visual Studio Code, Building pro-code applications, Developing your application, Building applications]
---

# Import an application into Visual Studio Code

After you create a project, import an application from your instance into the project to begin editing.

## Before you begin

Role required: none.

## Procedure

1.  Visual Studio Code displays the list of applications available in your instance for the selected application type.

    The list of applications shows once the Manage Developers settings have been applied for the custom application intended to import. If the settings are left unchecked, applications will not be listed in the drop-down.

2.  Select an application.

3.  At the **Configure file types** prompt, click **OK** to select all file types.

    ![Select metadata prompt in Visual Studio Code](../image/vscode-select-metadata.png)

    By default, Visual Studio Code imports all the file types of your application. You can modify the selection of the file types while editing the application, by choosing **Now: Configure File Types** from the command palette and choosing the file types from the list.

    Your ServiceNow application is imported into your workspace.

    **Note:** Even if your application exists on your instance, you must create a project for it in Visual Studio Code.

    You can switch applications within the workspace by clicking the name of the application, for example, EmployeeApp in this case, in the status bar at the bottom of the VS code IDE or choosing **Now: Select Application** from the command palette and selecting the application name from the list. Similarly, you can modify the update set by clicking the current update set icon, for example, EmployeeApp in this case, in the status bar at the bottom of the VS code IDE or by choosing **Now: Select Update Set** from the command pallet and selecting the name of the updateset.


**Parent Topic:**[Create a project in VS Code](create-project.md)

