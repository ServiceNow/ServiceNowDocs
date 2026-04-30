---
title: Convert your installed applications to development mode
description: Convert the installed applications that your company owns to development mode after you install an application onto a non-production instance to use for development or clone a production instance into a non-production instance for development. With this conversion, you enable newer versions of the application to be created, committed, and published.
locale: en-US
release: zurich
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage customizations to applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Convert your installed applications to development mode

Convert the installed applications that your company owns to development mode after you install an application onto a non-production instance to use for development or clone a production instance into a non-production instance for development. With this conversion, you enable newer versions of the application to be created, committed, and published.

## Before you begin

You must set the instance scope to the desired application scope. For example, if converting Agent Workspace, the application scope is set to Agent Workspace.

Role required: admin

## About this task

The system properties feature \[sn\_appclient.store\_app\_convert\_enabled\] controls this action, which is enabled by default. You can disable this feature by setting sn\_appclient.store\_app\_convert\_enabled to false.

You can convert only the applications that your company owns. The application scope must match a key that is set in sn\_appauthor.all\_company\_keys.

**Note:** Installed global applications are eligible for conversion.

After you convert the application, it can't receive updates from the application repository on this instance. Ensure that the version of the application that is installed on the instance is the version that you intend to develop as a new version.

**Note:** Applications that are installed with demo data lose their reference to this data on installation. If an application is converted, you must re-create any sys\_metadata\_link records to the demo data before you link the application to the source control or publish a new version.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  In the **Installed** tab, click the name of the application record that you want to convert.

3.  Select the Convert to Development Mode related link.

4.  Select **Convert**.

    -   If the installed version of the application is equal to the latest version that is published to the Application Repository, you see the following dialog:

        ![Convert installed app dialog is displayed.](../image/convert_dialog.png)

    -   If the installed version of the application is lower than the latest version that is published to the Application Repository, you see the following warning:
        -   ![Version warning is displayed.](../image/warning.png)

        -   If an instance is connected to a self-hosted application repository, you may see this warning regardless of the availability of a higher version in the repository. Check your repository to ensure that the development version that you require is installed in this case.
    -   After the successful conversion, the following message is displayed:
        -   ![Successful conversion message.](../image/convert-success.png)

        -   Close the window to be redirected to the development application form.

