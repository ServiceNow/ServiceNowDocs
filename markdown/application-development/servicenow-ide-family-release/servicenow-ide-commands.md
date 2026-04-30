---
title: ServiceNow IDE commands
description: Use commands from the command palette to perform many actions in the ServiceNow IDE.
locale: en-US
release: yokohama
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# ServiceNow IDE commands

Use commands from the command palette to perform many actions in the ServiceNow IDE.

The command palette includes commands unique to the ServiceNow IDE for creating and managing applications and commands from Visual Studio Code, such as Git commands for using source control. The following commands are unique to the ServiceNow IDE.

To open the command palette, use one of the following keyboard shortcuts:

-   Windows: Ctrl-Shift-P
-   Mac: Cmd-Shift-P

To close the command palette, press the Escape key.

<table id="table_r2y_gzd_42c"><thead><tr><th>

Command

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fluent: Apply Template for an existing Fluent App

</td><td>

Adds template files and directories for development in ServiceNow Fluent to an existing application.

</td></tr><tr><td>

Fluent: Build and Install

</td><td>

Build and install the application across the instance.Learn more: [Build and install an application in the ServiceNow IDE](../task/build-applications-servicenow-ide.md)

</td></tr><tr><td>

Fluent: Build with Now SDK

</td><td>

Build the application into an installable package.

</td></tr><tr><td>

Fluent: Convert a scoped app to Fluent

</td><td>

Convert an existing scoped application to support development in source code.**Note:** With ServiceNow IDE version 3.1.4 and earlier, the sn\_glider.ide\_fluent\_admin role is required to use this command.

Learn more: [Convert an application with the ServiceNow IDE](../task/convert-application-servicenow-ide.md)

</td></tr><tr><td>

Fluent: Create Fluent App

</td><td>

Create a scoped application to develop in source code.Learn more: [Create an application with the ServiceNow IDE](../task/create-application-servicenow-ide.md)

</td></tr><tr><td>

Fluent: Download script dependencies

</td><td>

Download script dependencies in your application to get type-ahead support for Glide APIs and script includes. Type definitions are downloaded into the `@types/servicenow` directory based on the scripts in your application.After downloading script dependencies, you can create a `tsconfig.json` file in the `src/fluent` directory that includes the type definitions. For example:

```json
"include": [
    "./**/*.client.js",
    "./**/*.server.js",
    "../../@types/servicenow/*.client.d.ts",
    "../../@types/servicenow/*.server.d.ts",
]
```

Learn more: [Downloading dependencies with the ServiceNow SDK](../../servicenow-sdk/concept/downloading-dependencies-now-sdk.md#)

</td></tr><tr><td>

Fluent: Force Install Fluent App in Instance

</td><td>

Install an existing build artifact, which might overwrite recent changes.

</td></tr><tr><td>

Fluent: Force Sync of Fluent App with all metadata

</td><td>

Synchronize all metadata in the application rather than only the metadata that changed since the last time that the application was synchronized.**Warning:** Force synchronizing all metadata in the application might overwrite any changes in the application that haven't been built and installed on the instance.

Learn more: [Synchronizing applications in the ServiceNow IDE](../concept/synchronizing-applications.md)

</td></tr><tr><td>

Fluent: Install Fluent App in Instance

</td><td>

Install the application across the instance without building it again.

</td></tr><tr><td>

Fluent: Reinstall Fluent App

</td><td>

Uninstall and reinstall the application on the instance to verify that the metadata on the instance matches the metadata in the installation package. The source files in the application aren’t changed. **Warning:** Changes to metadata on the instance that haven’t been synced into your application in the ServiceNow IDE are removed.

If you have previous versions of modules in the EcmaScript Module \[sys\_module\] table that aren't needed, re-installing an application removes previous versions of the application’s modules from the table.

**Note:** With ServiceNow IDE version 3.1.4 and earlier, the sn\_glider.ide\_fluent\_admin role is required to use this command.

</td></tr><tr><td>

Fluent: Restart Fluent Server

</td><td>

Restart the ServiceNow Fluent language server.

</td></tr><tr><td>

Fluent: Sync Fluent App with changed metadata

</td><td>

Synchronize changes made to the application metadata since the last time that the application was synchronized.Learn more: [Synchronizing applications in the ServiceNow IDE](../concept/synchronizing-applications.md)

</td></tr><tr><td>

Git: Manage Git credentials

</td><td>

Manage existing Git credentials for a Git domain and your user on the instance.

</td></tr><tr><td>

Git: Set IDE Git credentials

</td><td>

Configure basic or OAuth 2.0 credentials that are associated with your user to authenticate with a Git provider.Learn more:

-   [Connect to a Git provider using basic authentication with the ServiceNow IDE](../task/connect-git-provider-basic-auth.md)
-   [Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE](../concept/connect-git-provider-oauth-2.md#)

</td></tr><tr><td>

Metadata Explorer: Focus on Metadata Explorer View

</td><td>

Navigate to the Metadata Explorer view.Learn more: [Create an application file from the Metadata Explorer](../task/create-application-file-servicenow-ide.md)

</td></tr><tr><td>

Metadata Explorer: Open in New Browser Tab

</td><td>

Open the Metadata Explorer in a new browser tab.

</td></tr><tr><td>

Metadata Explorer: Reload

</td><td>

Refresh the Metadata Explorer view.

</td></tr><tr><td>

Package Manager: Install Dependencies

</td><td>

Install third-party dependencies into the `node_modules` directory.Learn more: [Use third-party libraries in applications in the ServiceNow IDE](../task/use-third-party-libraries-ide.md)

</td></tr><tr><td>

Workspaces: Add Application to Workspace

</td><td>

Add an existing application to a workspace.

</td></tr><tr><td>

Workspaces: Add to Workspace

</td><td>

Create, open, or clone an application in a workspace.

</td></tr><tr><td>

Workspaces: Browse Workspaces

</td><td>

Browse through and open your ServiceNow IDE workspaces.

</td></tr><tr><td>

Workspaces: Create a Workspace

</td><td>

Create a ServiceNow IDE workspace.Learn more: [Create a workspace in the ServiceNow IDE](../task/create-workspace-servicenow-ide.md)

</td></tr><tr><td>

Workspaces: Delete a Workspace

</td><td>

Delete a ServiceNow IDE workspace.

</td></tr><tr><td>

Workspaces: Rename a Workspace

</td><td>

Rename a ServiceNow IDE workspace.

</td></tr><tr><td>

Workspaces: Welcome

</td><td>

Navigate to the ServiceNow IDE home page, which lists all of your workspaces.

</td></tr></tbody>
</table>