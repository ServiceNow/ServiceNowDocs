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
reading_time_minutes: 2
keywords: [Convert an app, Fluent source code, ServiceNow Studio]
breadcrumb: [Building apps in source code in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Convert an application to Fluent

Convert an existing application to support development in source code with ServiceNow Studio.

## Before you begin

Role required: admin

## About this task

Existing applications that weren't created in source code must be converted to support development. Converting an application adds the necessary files and directories for developing it in source code. You can choose whether to convert existing application metadata into ServiceNow Fluent code.

**Important:** Only admins can work on Fluent apps. Don't convert the app if you want delegated developers to continue working on the application.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open the application you want to convert.

3.  Select **App details**.

4.  In the Convert app to ServiceNow Fluent message, select **Convert**.

5.  Select **Convert**.

    The application is added to your workspace with the default application structure, but the application metadata isn’t converted into ServiceNow Fluent code. For more information, see [Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md).

6.  To convert existing metadata into ServiceNow Fluent code, complete the following steps.

    1.  From the Navigator panel, select the Explorer tab.

    2.  Right-click the `metadata` directory for the application and select **Convert Directory to Fluent**.

        \[Omitted image "sn-studio-convert-metadata-fluent.png"\] Alt text: Menu option to convert application metadata to ServiceNow Fluent.

    Application metadata is defined in ServiceNow Fluent code in the `fluent/generated` directory and removed from the `metadata` directory and its sub-directories.

    \[Omitted image "sn-studio-fluent-generated-metadata.png"\] Alt text: An application with metadata converted to Fluent in ServiceNow Studio.

    **Note:** A limited number of metadata types, such as Metadata Snapshots \[sys\_metadata\_link\] and UX Assets \[sys\_ux\_lib\_asset\], can't be represented as ServiceNow Fluent code and aren't transformed. These metadata types remain as metadata XML files in the `metadata` directory of your application.

7.  Build and install your application to compile source code into application metadata and make your changes available across the instance.

    For more information, see [Build and install a Fluent app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/build-install-fluent-app-sns.md).


## Result

The converted application is added to your workspace with the necessary files and directories to support development in source code. After installing a converted application, the **Package JSON** field of the custom application record \[sys\_app\] contains the path to the `package.json` file for the application.

**Note:** For ServiceNow Studio to install the required dependencies in an application, the public npm registry must respond with the HTTP `Access-Control-Allow-Origin` header.

## What to do next

From your Git provider, create a dedicated Git repository for the application. Initialize a local Git repository for your application and push it to the remote repository. For more information, see [Initialize a Git repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-initialize-git-repo.md).

Continue editing your application in ServiceNow Studio.

**Parent Topic:**[Building apps in source code in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.md)

