---
title: Create an app file in ServiceNow Studio
description: Create an app file to define an aspect of how an application functions. For example, you could add a security file using ServiceNow Studio to define which users can access the app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sn-studio-create-app-file.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Create an app file in ServiceNow Studio

Create an app file to define an aspect of how an application functions. For example, you could add a security file using ServiceNow Studio to define which users can access the app.

## Before you begin

Role required: admin or delegated\_developer

## About this task

Application files are essentially metadata records for application logic such as business rules, workflows, and script includes. For more information on app files, see [Application files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/c_ApplicationFiles.md) and [Working with metadata app file categories in the ServiceNow Studio Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.md).

Delegated developers have access to create app files for apps they have access to. If you need an app created, contact your admin.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the create icon \(\[Omitted image "sn-studio-add-icon.png"\] Alt text: create icon\) next to the Navigator panel or the **Create** button.

    \[Omitted image "sn-studio-create-button-zs1.png"\] Alt text: There are two create buttons, one on either side of the screen. Click either Create button to start developing an app.

3.  If you already have an app open in the Navigator panel, you can select the create icon **+** next to any file type to create a file of that type.

    You can also select the create icon **+** next to the application name to create a new file of any type.

    \[Omitted image "sn-studio-create-file-zs2.png"\] Alt text: You can create files of any type from an app opened in the navigator panel.

4.  Select **File**.

5.  Specify which scope the file belongs to by entering it in the **Application** field.

    **Note:** If you are creating a file directly from within an app, the **Application** field is populated with the name of the application.

    If you want the app file to be available to all apps, select the **Global** scope.

    \[Omitted image "sn-studio-create-file-scope.png"\] Alt text: Select an application scope for your file.

6.  Select the card for the type of file you want to create.

    You can find the file type in several ways:

    -   Filter the available types by selecting one of the metadata categories in the left of the integrated tab.
    -   Enter the type of file you're looking for in the search bar.
    -   Choose from the list of **Recent** file types.
    **Note:** The types of available files you see depends on your permissions. If you're expecting to see a certain file type but don't see it, contact your administrator.

    \[Omitted image "sn-studio-create-file-page.png"\] Alt text: The Create File page opens in a new integrated tab so you can select the type of file you want to create.

    For a list of all types of metadata that you can use to create app files, see [ServiceNow Studio Navigator panel taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/servicenow-studio-file-navigator-taxonomy.md). For more information about each file type, see [Working with metadata app file categories in the ServiceNow Studio Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.md).

7.  Select **Continue**.

    The record for the app file opens in the same integratedbrowser tab in ServiceNow Studio.

8.  Fill in the form with the details for the new app file.

    The form fields vary depending on the type of file you created.

9.  Select **Submit**.


## What to do next

After you finish creating the app file, you must select the refresh icon in the Navigator panel for it to appear in the list of app files.

\[Omitted image "sn-studio-refresh-list-icon-zs1.png"\] Alt text: Refresh the Navigator panel to see the new files you created.

**Parent Topic:**[Applications in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/working-with-apps-in-servicenow-studio.md)

