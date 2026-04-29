---
title: ServiceNow IDE user interface
description: The ServiceNow IDE user interface contains many of the same features as Visual Studio Code for the Web and some unique functionality for creating ServiceNow applications.Learn about features of the ServiceNow IDE user interface.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# ServiceNow IDE user interface

The ServiceNow IDE user interface contains many of the same features as Visual Studio Code for the Web and some unique functionality for creating ServiceNow applications.

## Overview of the ServiceNow IDE user interface

The ServiceNow IDE is an implementation of Visual Studio Code for the Web on the ServiceNow AI Platform, which includes the following features:

-   Basic editing and keyboard shortcuts
-   IntelliSense
-   Code navigation
-   Code and file search
-   Command palette
-   Source control integration

Visual Studio Code for the Web is similar to Visual Studio Code Desktop but doesn't support all of the features that are available in the desktop interface. For information about browser-based implementations of Visual Studio Code, see [Visual Studio Code for the Web](https://code.visualstudio.com/docs/editor/vscode-web). The following Visual Studio Code features aren't supported in the ServiceNow IDE:

-   Integrated terminal
-   Debugger
-   Marketplace extensions
-   Integrated unit testing
-   Remote development

For general information about common features in Visual Studio Code and the ServiceNow IDE, see the [Visual Studio Code documentation](https://code.visualstudio.com/docs) website.

## Features in the ServiceNow IDE

Learn about features of the ServiceNow IDE user interface.

![Identify features in the ServiceNow IDE.](../image/servicenow-ide-user-interface.png "ServiceNow IDE user interface")

1.  [ServiceNow IDE home page](servicenow-ide-user-interface.md#section_sqf_j5j_1cc): Get started creating workspaces and applications and view existing workspaces. Switch between development environments using the experience switcher.
2.  Activity Bar
    -   [File Explorer view](servicenow-ide-user-interface.md#section_vl3_bj2_dbc): Navigate through applications in your workspace and their code.
    -   [Search view](servicenow-ide-user-interface.md#section_oq5_fj2_dbc): Find content within files.
    -   [Source Control view](servicenow-ide-user-interface.md#section_zys_hzd_dbc): Integrate with a Git repository for version control of your code.
    -   [File Categories view](servicenow-ide-user-interface.md#section_xdm_dzd_dbc): Create, update, and view application metadata.
    -   [Now SDK view](servicenow-ide-user-interface.md#section_oqm_xtp_ldc): Synchronize changes to application metadata or build and install applications.
    -   [Manage menu](servicenow-ide-user-interface.md#section_x2f_2rc_qfc): Access and configure various aspects of the user interface.
3.  [Editor](servicenow-ide-user-interface.md#section_agx_c42_dbc): Write source code and view application metadata through embedded ServiceNow AI Platform user interfaces.
4.  [Status bar](servicenow-ide-user-interface.md#section_qnf_d42_dbc): View status information about your applications and files and build applications.

In addition to these features, you can open the command palette to run a variety of commands to develop applications, manage files, use source control, and more. For more information, see [Command palette](servicenow-ide-user-interface.md#section_ftq_gzd_dbc).

### ServiceNow IDE home page

![The ServiceNow IDE home page with the user's workspaces listed.](../image/servicenow-ide-welcome.png)

Create workspaces, access existing workspaces, and create or open applications. Clone a Git repository to add an existing application from a remote repository. To get started creating workspaces and applications, see [Developing applications with the ServiceNow IDE](developing-applications-servicenow-ide.md). To clone a Git repository, see [Clone a Git repository with the ServiceNow IDE](../task/clone-git-repository-servicenow-ide.md).

![Experience switcher from the ServiceNow IDE](../image/servicenow-ide-exp-switcher.png "Experience switcher")

Work in the right environment for your task by using the experience switcher to switch between developing in ServiceNow IDE, ServiceNow Studio, and Creator Studio. For information about configuring the experience switcher, see [Configure non-default access to the experience switcher](../../servicenow-studio/task/configure-access-experience-switcher.md).

### File Explorer view

![File Explorer view](../image/servicenow-ide-file-explorer.png)

Navigate through applications in a workspace and add files or folders. In the Outline section, view the outline of the active file in the editor. In the Timeline section, view a history of changes to the active file. For information about the default application file structure, see the [Application structure](../../custom-application/concept/building-applications-source-code.md#application-structure) section of the Building applications in source code topic.

### Search view

![Search view](../image/servicenow-ide-search.png)

Search across files in the active workspace. The Search view supports using regular expressions, find and replace, and advanced search options.

To search for files by name, open the search box with the following keyboard shortcuts:

-   Windows: Ctrl-P
-   Mac: Cmd-P

### Source Control view

![Source Control view](../image/servicenow-ide-source-control.png)

See changes to files grouped by application and the type of change. Stage, commit, and push changes to a remote repository and pull changes into your local repository. Create and checkout branches for your applications. In the Commits section, see the commit history for branches in the repository. To get started integrating with source control providers, see [Integrating source control with the ServiceNow IDE](integrating-source-control-servicenow-ide.md).

### File Categories view

![File Categories view](../image/servicenow-ide-create-file.png)

Create, update, and view application metadata in the most applicable embedded ServiceNow AI Platform user interface in the editor. If you need to create some application metadata outside of source code, you can create application files from the File Categories view. For more information, see [Create an application file in the ServiceNow IDE](../task/create-application-file-servicenow-ide.md).

### Now SDK view

![Now SDK view](../image/servicenow-ide-now-sdk.png)

Run commands from the ServiceNow SDK application packaging service to synchronize changes to application metadata or build and install an application. For more information, see [Synchronizing applications in the ServiceNow IDE](synchronizing-applications.md) and [Build and install an application in the ServiceNow IDE](../task/build-applications-servicenow-ide.md).

### Manage menu

![Manage menu](../image/servicenow-ide-manage-menu.png)

Access and configure various aspects of the ServiceNow IDE user interface from the Manage menu. You can manage your settings, select a theme preference, view or edit keyboard shortcuts, and more.

### Editor

![Split view editor](../image/servicenow-ide-editor.png)

Write and edit code using IntelliSense, custom language processing and validation for ServiceNow Fluent, side-by-side editing, and more.

After building an application, review changes to ServiceNow Fluent source code as application metadata in embedded ServiceNow AI Platform user interfaces without leaving the ServiceNow IDE. Application metadata opens in the most applicable embedded ServiceNow AI Platform user interface. From links in the editor, you can open the File Categories view for metadata defined with a dedicated ServiceNow Fluent API.

![Code Lens link in the Editor](../image/servicenow-ide-code-lens.png)

Switch between tabs and split the editor into groups. If a file has unsaved changes, the file tab includes a dot icon.

![File with unsaved changes.](../image/servicenow-ide-unsaved-changes.png)

To get started developing applications in source code, see [Developing applications with the ServiceNow IDE](developing-applications-servicenow-ide.md).

### Status bar

![Status bar](../image/servicenow-ide-status-bar.png)

Get information about the state of your application and build applications. View the progress when creating, building, and syncing applications. In addition, the status bar displays the active branch, problems in your code, the active application scope, the active update set, and more.

From the status bar, the panel opens and displays more information about problems in your code and logging related to creating, building, and syncing applications.

![Panel with output logs](../image/servicenow-ide-panel.png)

### Command palette

![Command palette](../image/servicenow-ide-command-palette.png)

Run commands to configure the user interface, develop applications, manage files, use source control, access a list of keyboard shortcuts, and more. The command palette includes commands unique to the ServiceNow IDE and Visual Studio Code commands. For a list of commands specific to the ServiceNow IDE, see [ServiceNow IDE commands](../reference/servicenow-ide-commands.md).

To open the command palette, use one of the following keyboard shortcuts:

-   Windows: Ctrl-Shift-P
-   Mac: Cmd-Shift-P

To close the command palette, press the Escape key.

