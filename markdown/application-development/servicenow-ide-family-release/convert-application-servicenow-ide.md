---
title: Convert an application with the ServiceNow IDE
description: Convert an existing scoped application to support development in source code with the ServiceNow IDE.
locale: en-US
release: yokohama
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Add applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Convert an application with the ServiceNow IDE

Convert an existing scoped application to support development in source code with the ServiceNow IDE.

## Before you begin

Create a workspace for your applications. For more information, see [Create a workspace in the ServiceNow IDE](create-workspace-servicenow-ide.md).

Role required: admin

**Note:** With ServiceNow IDE version 3.1.4 and earlier, the sn\_glider.ide\_fluent\_admin role is also required to convert applications.

## About this task

Existing scoped applications that weren't created with the ServiceNow IDE or ServiceNow SDK must be converted to support development in source code. Converting an application adds the necessary files and directories for developing it in source code. You can choose whether to convert existing application metadata into ServiceNow Fluent code.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace.

3.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
4.  Enter `Fluent: Convert a scoped app to Fluent` and press Enter.

5.  Select a scoped application from the list.

    Applications that haven't been converted are listed as `Is Fluent app: False`.

    The scoped application is added to your workspace with the default application structure but the application metadata isn’t converted into ServiceNow Fluent code. For information about the application structure, see the [Application structure](../../custom-application/concept/building-applications-source-code.md#application-structure) section of the Building applications in source code topic.

6.  To convert existing metadata into ServiceNow Fluent code, complete the following steps.

    1.  From the Activity Bar, select the File Explorer view \(![File Explorer](../image/servicenow-ide-file-explorer-icon.png)\).

    2.  Right-click the `metadata` directory for the application and select **Convert Directory to Fluent**.

        ![Menu option to convert the metadata directory to ServiceNow Fluent code.](../image/servicenow-ide-convert-dir-fluent.png)

    Application metadata is defined in ServiceNow Fluent code in the `fluent/generated` directory and removed from the `metadata` directory and its sub-directories.

    ![An application with metadata converted into ServiceNow Fluent code.](../image/servicenow-ide-fluent-generated.png)

    **Note:** A limited number of metadata types, such as Metadata Snapshots \[sys\_metadata\_link\] and UX Assets \[sys\_ux\_lib\_asset\], can't be represented as ServiceNow Fluent code and aren't transformed. These metadata types remain as metadata XML files in the `metadata` directory of your application.

7.  Build and install your application to compile source code into application metadata and make your changes available across the instance. For more information, see [Build and install an application in the ServiceNow IDE](build-applications-servicenow-ide.md).


## Result

The converted application is added to your workspace with the necessary files and directories to support development in source code. After installing a converted application, the **Package JSON** field of the custom application record \[sys\_app\] contains the path to the `package.json` file for the application.

**Note:** For the ServiceNow IDE to install the required dependencies in an application, the public npm registry must respond with the HTTP `Access-Control-Allow-Origin` header.

## What to do next

From your Git provider, create a dedicated Git repository for the application. Initialize a local Git repository for your application and push it to the remote repository. For more information, see [Initialize a Git repository with the ServiceNow IDE](initialize-git-repository-servicenow-ide.md).

In the ServiceNow IDE, start developing your application in source code with ServiceNow Fluent, writing custom JavaScript modules, or adding third-party libraries.

