---
title: Create an app file in ServiceNow Studio
description: Create an app file to define an aspect of how an application functions. For example, you could add a security file using ServiceNow Studio to define which users can access the app.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create an app file in ServiceNow Studio

Create an app file to define an aspect of how an application functions. For example, you could add a security file using ServiceNow Studio to define which users can access the app.

## Before you begin

Role required: admin or delegated\_developer

## About this task

Application files are essentially metadata records for application logic such as business rules, workflows, and script includes. For more information on app files, see [Application files](../../applications/concept/c_ApplicationFiles.md) and [Working with metadata app file categories in the ServiceNow Studio Navigator](../concept/sn-studio-working-with-metadata.md).

Delegated developers can create app files for apps they have access to. If you need an app created, contact your admin.

This procedure details how to create files from anywhere in ServiceNow Studio. For pared-down information on adding files to a newly created app, see [Add a file to your app in ServiceNow Studio](create-an-application-in-servicenow-studio.md#).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the create icon ![create icon](../image/sn-studio-add-icon.png) next to the Navigator panel or the **Create** button.

    ![There are two create buttons, one on either side of the screen. Select either Create button to start developing an app.](../image/sn-studio-create-button-zs1.png)

3.  If you already have an app open in the Navigator panel, you can select the create icon **+** next to any file type to create a file of that type.

    You can also select the create icon **+** next to the application name to create a new file of any type.

    ![You can create files of any type from an app opened in the navigator panel.](../image/sn-studio-create-file-zs2.png)

4.  Select **File**.

5.  Specify which scope the file belongs to by entering it in the **Application** field.

    **Note:** If you're creating a file directly from within an app, the **Application** field is populated with the name of the application.

    If you want the app file to be available to all apps, select the **Global** scope.

    ![Select an application scope for your file.](../image/sn-studio-create-file-scope.png)

6.  Select the card for the type of file you want to create.

    You can find the file type in several ways:

    -   Select a file from one of the metadata categories in New File tab.
    -   Search for file type you're looking for.
    -   Choose from the list of **Recent** file types.
    **Note:** The types of available files you see depends on your permissions. If you're expecting to see a certain file type but don't see it, contact your administrator.

    ![The Create File page opens in a new integrated tab so you can select the type of file you want to create.](../image/sn-studio-create-file-page.png)

    For a list of all types of files you can create, see [ServiceNow Studio Navigator panel taxonomy](../reference/servicenow-studio-file-navigator-taxonomy.md). For more information about each file type, see [Working with metadata app file categories in the ServiceNow Studio Navigator](../concept/sn-studio-working-with-metadata.md).

7.  Select **Continue**.

    The record for the app file opens in the same integratedbrowser tab in ServiceNow Studio.

8.  Fill in the form with the details for the new app file.

    The form fields vary depending on the type of file you created.

9.  Select **Submit**.


## What to do next

After you finish creating the app file, you must select the refresh icon in the Navigator panel for it to appear in the list of app files.

![Refresh the Navigator panel to see the new files you created.](../image/sn-studio-refresh-list-icon-zs1.png)

**Parent Topic:**[Working with applications in ServiceNow Studio](../concept/working-with-apps-in-servicenow-studio.md)

