---
title: Create an app file in ServiceNow Studio
description: Create an app file in ServiceNow Studio to define how an aspect of an application functions — such as which users can access it or how it processes data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sn-studio-create-app-file.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 3
breadcrumb: [Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create an app file in ServiceNow Studio

Create an app file in ServiceNow Studio to define how an aspect of an application functions — such as which users can access it or how it processes data.

## Before you begin

Role required: admin or delegated\_developer

## About this task

Application files are metadata records for application logic such as business rules, workflows, and script includes. For more information about app files, see [Application files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/c_ApplicationFiles.md) and [Metadata app file categories in the ServiceNow Studio Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.md).

Delegated developers can create app files for apps they have access to. To have an app created, contact your admin.

Use this procedure to create files from anywhere in ServiceNow Studio. To add files to a newly created app, see [Add a file to your app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the create icon \[Omitted image "sn-studio-add-icon.png"\] Alt text: create icon next to the Navigator panel or the **Create** button.

    \[Omitted image "sn-studio-create-button-zs1.png"\] Alt text: There are two create buttons, one on either side of the screen. Select either Create button to start developing an app.

3.  If an app is already open in the Navigator panel, select the create icon **+** next to any file type to create a file of that type.

    To create a new file of any type, select the create icon **+** next to the application name.

    \[Omitted image "sn-studio-create-file-zs2.png"\] Alt text: Create files of any type from an app open in the Navigator panel.

4.  Select **File**.

5.  Specify which scope the file belongs to by entering it in the **Application** field.

    **Note:** If you are creating a file directly from within an app, the **Application** field is pre-populated with the application name.

    To make the app file available to all apps, select the **Global** scope.

    \[Omitted image "sn-studio-create-file-scope.png"\] Alt text: Select an application scope for the file.

6.  Select the card for the file type you want to create.

    Find the file type using one of the following options:

    -   Select a file from one of the metadata categories in the **New File** tab.
    -   Search for the file type.
    -   Select from the list of **Recent** file types.
    **Note:** Available file types depend on your permissions. If you do not see a file type you expect, contact your administrator.

    \[Omitted image "sn-studio-create-file-page.png"\] Alt text: The Create File page opens in a new tab so you can select the file type you want to create.

    For a list of all available file types, see [ServiceNow Studio Navigator panel taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-file-navigator-taxonomy.md). For more information about each file type, see [Metadata app file categories in the ServiceNow Studio Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.md).

7.  Select **Continue**.

    The record for the app file opens in the samebrowser tab in ServiceNow Studio.

8.  Enter the details for the new app file in the form.

    The form fields vary depending on the file type.

9.  Select **Submit**.

    The app file is created and added to your application.


## What to do next

Select the refresh icon in the Navigator panel to display the new file in the list of app files.

\[Omitted image "sn-studio-refresh-list-icon-zs1.png"\] Alt text: Refresh the Navigator panel to see the new files you created.

**Parent Topic:**[Applications in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-apps-in-servicenow-studio.md)

