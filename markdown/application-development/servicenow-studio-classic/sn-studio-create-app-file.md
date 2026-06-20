---
title: Create an app file in ServiceNow Studio
description: Create an app file to define an aspect of how an application functions. For example, you could add a security file using ServiceNow Studio to define which users can access the app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/servicenow-studio-classic/sn-studio-create-app-file.html
release: xanadu
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2024-09-06"
reading_time_minutes: 2
breadcrumb: [Using ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Create an app file in ServiceNow Studio

Create an app file to define an aspect of how an application functions. For example, you could add a security file using ServiceNow Studio to define which users can access the app.

## Before you begin

Role required: admin or delegated developer

## About this task

Application files are essentially metadata records for application logic such as business rules, workflows, and script includes. For more information on app files, see [Application files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/building-applications/c_ApplicationFiles.md) and [Working with metadata app file categories in the ServiceNow Studio Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.md).

Delegated developers have access to create app files for apps they have access to. If you need an app created, contact your admin.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select either the Create icon \(\[Omitted image "sn-studio-add-icon.png"\] Alt text: create icon\) next to the Navigator panel or the **Create** button.

    \[Omitted image "sn-studio-create-app.png"\] Alt text: Create an app using either the Navigator icon or the Create button

3.  Select **File** from the options that appear.

    \[Omitted image "sn-studio-create-file-modal.png"\] Alt text: The create file modal appears, where you can select which kind of app file you would like to create.

4.  Specify which app the file belongs to by entering it in the **Application** field.

    If you want the app file to be available to all apps, select the **Global** scope.

5.  Select the card for the type of file you want to create.

    You can find the file type in several ways:

    -   Filter the available types by selecting one of the metadata taxonomies in the left of the modal.
    -   Enter the type of file you're looking for in the search bar.
    -   Choose from the list of Recent file types.
    For a list of all types of metadata that you can use to create app files, see [ServiceNow Studio Navigator panel taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/servicenow-studio-file-navigator-taxonomy.md). For more information about each file type, see [Working with metadata app file categories in the ServiceNow Studio Navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/sn-studio-working-with-metadata.md).

6.  Select **Continue**.

    The record for the app file appears in a new browser tab in ServiceNow Studio.

7.  Fill in the form with the details for the new app file.

    The form fields vary depending on the type of file you created.

8.  Select **Submit**.


## What to do next

After you finish creating the app file, you must select the refresh icon in the Navigator panel for it to appear in the list of app files.

\[Omitted image "sn-studio-refresh-nav-panel.png"\] Alt text: Refresh the Navigator panel by selecting the refresh button

**Parent Topic:**[Using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/using-servicenow-studio.md)

