---
title: Build and install an application in the ServiceNow IDE
description: Build an application to compile its source code and install application changes across an instance from the ServiceNow IDE.
locale: en-US
release: zurich
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Develop applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Build and installan application in the ServiceNow IDE

Build an application to compile its source code and install application changes across an instance from the ServiceNow IDE.

## Before you begin

Create, convert, or clone an application and add it to your workspace. For more information, see [Adding applications in ServiceNow IDE](../concept/creating-applications-servicenow-ide.md).

Role required: admin

## About this task

When you build an application, ServiceNow Fluent code is compiled into application metadata, and modules in the application are added to the EcmaScript Module \[sys\_module\] table on the instance.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace with an application.

3.  Synchronize changes made to the application metadata from across the instance.

    Syncing an application confirms you have the latest changes before making additional changes.Only the changes made since the last time the application was synced are downloaded and transformed. For more information, see [Synchronizing applications in the ServiceNow IDE](../concept/synchronizing-applications.md).

    1.  From the Activity Bar, select the Now SDK view \(![Now SDK](../image/servicenow-ide-sdk-icon.png)\).

    2.  Select **Sync Changes**.

        The active file that's open in the editor determines which application to synchronize. If no files are open, select the application to synchronize when prompted.

        ![The Sync command in the Now SDK view.](../image/servicenow-ide-sync.png)

4.  From the Activity Bar, select the File Explorer view \(![File Explorer](../image/servicenow-ide-file-explorer-icon.png)\).

5.  Modify your application in one of the following ways and save your changes:

    -   [Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE](define-metadata-code-fluent-ide.md)
    -   [Create and use JavaScript modules in applications in the ServiceNow IDE](create-use-javascript-modules-ide.md)
    -   [Use third-party libraries in applications in the ServiceNow IDE](use-third-party-libraries-ide.md)
6.  From the Status Bar, select **Build and Install**.

    ![Build and deploy](../image/servicenow-ide-build-icon.png)

    The active file that's open in the editor determines which application to build. If no files are open, select the application to build when prompted.

    In the status bar, you can see a message that confirms whether the build was successful or failed. If the build fails, review the output logs and any problems in your code from the panel.

7.  Review your changes as application metadata.

    1.  From the Activity Bar, select the Metadata Explorer view \(![Metadata Explorer](../image/servicenow-ide-metadata-explorer-icon.png)\).

    2.  Open the metadata files that you changed and review your changes from the embedded ServiceNow AI Platform user interfaces.

        **Tip:** To see your changes in source code and metadata side by side, select the Split Editor icon \(![Split Editor](../image/servicenow-ide-split-icon.png)\) or right-click a tab and select one of the **Split** options.


## Result

The application is updated across the instance to reflect your changes. Other users can modify the application metadata simultaneous with modifications to the source code. Also, other developers can reuse module code in other modules or scripts within an application.

If you need to ensure that the metadata on the instance matches the metadata in the installation package, you can uninstall and reinstall the application on the instance using the `Fluent: Reinstall Fluent App` command from the command palette. For more information, see [ServiceNow IDE commands](../reference/servicenow-ide-commands.md).

**Warning:** Changes to metadata on the instance that haven’t been synced into your application in the ServiceNow IDE are removed.

## What to do next

Use source control to stage, commit, and push your changes to a remote Git repository. For more information, see [Using source control in the ServiceNow IDE](../concept/using-source-control-servicenow-ide.md).

**Parent Topic:**[Developing applications with the ServiceNow IDE](../concept/developing-applications-servicenow-ide.md)

