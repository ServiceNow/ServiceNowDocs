---
title: Convert an application to Fluent
description: Convert an existing application to support development in source code with ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/convert-app-to-fluent.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-07-31"
reading_time_minutes: 3
keywords: [Convert an app, Fluent source code, ServiceNow Studio]
breadcrumb: [Building apps in source code in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Convert an application to Fluent

Convert an existing application to support development in source code with ServiceNow Studio.

## Before you begin

[Create a workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-a-workspace.md)

Role required: admin

## About this task

Existing applications that weren't created in source code must be converted to support development. Converting an application adds the necessary files and directories for developing it in source code. You can choose whether to convert existing application metadata into ServiceNow Fluent code.

**Important:** Only admins can work on Fluent apps. Don't convert the app if you want delegated developers to continue working on the application.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open a workspace.

3.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
4.  Enter `Fluent: Convert an app to Fluent` and press Enter.

5.  Select an application from the list.

    Applications that haven't been converted are listed as `Is Fluent app: False`.

    The application is added to your workspace with the default application structure but the application metadata isn’t converted into ServiceNow Fluent code. For more information, see [Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md).

6.  To convert existing metadata into ServiceNow Fluent code, complete the following steps.

    1.  From the Navigator panel, select the Explorer tab.

    2.  Right-click the `metadata` directory for the application and select **Convert Directory to Fluent**.

        \[Omitted image "servicenow-ide-convert-dir-fluent.png"\] Alt text: Menu option to convert the metadata directory to ServiceNow Fluent code.

    Application metadata is defined in ServiceNow Fluent code in the `fluent/generated` directory and removed from the `metadata` directory and its sub-directories.

    \[Omitted image "servicenow-ide-fluent-generated.png"\] Alt text: An application with metadata converted into ServiceNow Fluent code.

    **Note:** A limited number of metadata types, such as Metadata Snapshots \[sys\_metadata\_link\] and UX Assets \[sys\_ux\_lib\_asset\], can't be represented as ServiceNow Fluent code and aren't transformed. These metadata types remain as metadata XML files in the `metadata` directory of your application.

7.  Build and install your application to compile source code into application metadata and make your changes available across the instance. For more information, see [Build and install an application in the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/build-applications-servicenow-ide.md).


## Result

The converted application is added to your workspace with the necessary files and directories to support development in source code. After installing a converted application, the **Package JSON** field of the custom application record \[sys\_app\] contains the path to the `package.json` file for the application.

**Note:** For the ServiceNow Studio to install the required dependencies in an application, the public npm registry must respond with the HTTP `Access-Control-Allow-Origin` header.

## What to do next

From your Git provider, create a dedicated Git repository for the application. Initialize a local Git repository for your application and push it to the remote repository. For more information, see [Initialize a Git repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-initialize-git-repo.md).

Continue editing your application in ServiceNow Studio.

**Parent Topic:**[Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md)

