---
title: Build and install a Fluent app in ServiceNow Studio
description: Build an application to compile its source code and install application changes across an instance from ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/build-install-fluent-app-sns.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-08-03"
reading_time_minutes: 2
breadcrumb: [Building apps in source code in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Build and install a Fluent app in ServiceNow Studio

Build an application to compile its source code and install application changes across an instance from ServiceNow Studio.

## Before you begin

Create, convert, or clone an application and add it to the Explorer. For more information, see [Create an app in source code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-an-app-in-source-code.md).

Role required: admin

## About this task

When you build an application, ServiceNow Fluent code is compiled into application metadata, and modules in the application are added to the EcmaScript Module \[sys\_module\] table on the instance.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  From the Status bar, select **Sync Changes** to synchronize changes made to the application metadata from across the instance.

    Synchronizing an application confirms you have the latest changes before making additional changes. Only the changes made since the last time the app was synched are downloaded and transformed. For more information, see [Synchronizing Fluent apps in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/synchronizing-fluent-apps.md).

3.  Select the Explorer tab, and modify your application in one of the following ways.

    -   [Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/define-metadata-code-fluent-ide.md)
    -   [Create and use JavaScript modules in applications in the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/create-use-javascript-modules-ide.md)
    -   [Use third-party libraries in applications in the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/use-third-party-libraries-ide.md)
4.  From the Status bar, select **Build and Install**.

    The active file that's open in the editor determines which application to build. If no files are open, select the application to build when prompted.

    In the status bar, you can see a message that confirms whether the build was successful or failed. If the build fails, review the output logs and any problems in your code from the panel.

5.  Review your changes as application metadata.

    1.  From the Navigator panel, select the File Categories or Apps tabs.

    2.  Open the metadata files that you changed and review your changes from the embedded ServiceNow AI Platform user interfaces.

        **Tip:** To see your changes in source code and metadata side by side, select the show XML icon \[Omitted image "sn-studio-show-xml-icon.png"\] Alt text:.


## Result

The application is updated across the instance to reflect your changes. Other users can modify the application metadata simultaneous with modifications to the source code. Also, other developers can reuse module code in other modules or scripts within an application.

Confirm that the metadata on the instance matches the metadata in the installation package by uninstalling and reinstalling the application on the instance using the `Fluent: Reinstall Fluent App` command. For more information, see [ServiceNow IDE commands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/servicenow-ide-commands.md).

**Warning:** Changes to metadata on the instance that haven’t been synced into your application in ServiceNow Studio are removed.

## What to do next

Use source control to stage, commit, and push your changes to a remote Git repository. For more information, see [Using Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-using-fluent-source-control.md).

**Parent Topic:**[Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md)

