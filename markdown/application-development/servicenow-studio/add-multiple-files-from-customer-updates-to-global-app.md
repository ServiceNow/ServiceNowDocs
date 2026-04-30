---
title: Legacy - Add multiple files from customer updates to a global application
description: Add multiple globally scoped application files at once from one or more customer updates to a new or existing global application.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Legacy - Global application file management, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Add multiple files from customer updates to a global application

Add multiple globally scoped application files at once from one or more customer updates to a new or existing global application.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Role required: admin

The Global App File Management plugin must be activated.

To add global files that are part of other global applications, `glide.source_control.customize_files_in_other_global_apps` must be true.

## About this task

This feature is for customers who manage their customizations to globally scoped files via update sets. You can migrate these files in bulk to new or existing global applications. The global application can then leverage ServiceNow CICD tools which support only applications. Select multiple customer updates to move globally scoped application files to a new or existing global application. All the eligible application files associated with the customer updates will be moved. This operation moves only the application file as it is loaded on the instance. The payload in different customer updates to the same file is ignored.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**, open an update set in Form view and go to its Customer Updates Related List.

    **Or**

    Navigate to **System Maintenance** &gt; **Customers Updates \[sys\_update\_xml\]** table and add updates from multiple update sets.

2.  Select the check box beside each update you want to move, and then select **Migrate to Global Application** in the **Actions on selected rows** list.

3.  Select **Migrate**.

    **Note:** To learn how to add multiple files from global update sets to a global application, see [Legacy - Add multiple files from global update sets to a global application](add-multiple-files-to-global-app.md).

4.  Enter the name of a new global application or select an existing global application.

    ![Migrate file from customer update to global application.](../image/migrate-global-app-claim.png)

    If an application file associated with an update was not moved, it could be because:

    -   The application file is not global.
    -   The application file is part of another global application.
    -   The application file was deleted.
    -   The application file is not eligible to move to another global application. For example, a `sys_app` file.
    -   The application file is read-only.
    -   The application file is already associated to the global application being migrated to.

**Parent Topic:**[Legacy - Global application file management](../concept/manage_global_application_files.md)

