---
title: Legacy - Add multiple files from global update sets to a global application
description: Add multiple globally scoped application files at once from one or more global update sets to a new or existing global application.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy - Global application file management, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Add multiple files from global update sets to a global application

Add multiple globally scoped application files at once from one or more global update sets to a new or existing global application.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Role required: admin

The Global App File Management plugin must be activated.

## About this task

This feature is for customers who manage their customizations to globally scoped files via update sets. You can migrate these files in bulk to new or existing global applications. The global application can then leverage ServiceNow CICD tools which support only applications. Select multiple update sets to move globally scoped application files to a new or existing global application. All the eligible application files associated with the customer updates in those update sets will be moved. This operation moves only the application file as it is loaded on the instance. The payload in different customer updates to the same file is ignored.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Select the check box beside each update set you want to move, and then select **Migrate to Global Application** in the **Actions on selected rows** list.

3.  Enter the name of a new global application or select an existing global application.

    ![Migrate to global application](../image/migrate-global-app-updates.png)

4.  Select **Migrate**.

    **Note:** Selecting update sets to migrate does not move application files that are part of other global applications. Only files that are in the global scope are moved. To add files that are part of other global applications, see [Legacy - Add multiple files from customer updates to a global application](add-multiple-files-from-customer-updates-to-global-app.md).

    If an application file associated with an update was not moved, it could be because:

    -   The application file is not global.
    -   The application file is part of another global application.
    -   The application file was deleted.
    -   The application file is not eligible to move to another global application. For example, a `sys_app` file. \\
    -   The application file is read-only.

**Parent Topic:**[Legacy - Global application file management](../concept/manage_global_application_files.md)

