---
title: Legacy - Add a file from the global scope to a global application
description: Add existing globally scoped files into a selected global application. You can search for files in another globally scoped application by the update set name, table, or file name.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Legacy - Global application file management, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Add a file from the global scope to a global application

Add existing globally scoped files into a selected global application. You can search for files in another globally scoped application by the update set name, table, or file name.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

The Global App File Management plugin must be activated.

Role required: admin

## About this task

When you select an application in the application picker, application files are automatically assigned to it. You cannot move an application file into or out of a scoped application. See [Application scope](../concept/c_ApplicationScope.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Applications** &gt; **In Development**.

2.  To the right of the application name, click **Edit in Studio**.

3.  In Studio, click **File**, then select **Add Existing Files**.

4.  Use any of the following options to find existing globally scoped application files that you can add into the current globally scoped application.

    |Option|Description|
    |------|-----------|
    |**Search by update set**|Search and filter application files that are associated with an update set.|
    |**Search by table**|Search and filter application files that are associated with a specific table. For example, if you select Incident, the search returns application files that are associated with that table.|
    |**Search by name**|Perform a custom name search for application files that contain a specified update name \(sys\_update\_name\) or an actual file name \(sys\_name\).|

    **Note:** You can view up to 250 files at a time. If you want to view more files, perform another search with more specific search criteria.

5.  Click **Continue** to list application files that are associated with the selected update set, table, or name.

    You can filter the results as needed.

    The system displays the filtered results but omits any files that are already associated with the current global application. The system displays the file type, application, when the file was last updated, and if it is a customized file.

6.  Select the files that you want to add, and then click **Add**.

    The Confirm Changes dialog appears, stating that the files being moved are now considered customizable files and may appear on a skip list during an upgrade.

7.  Click **Continue** to add the selected files.

    **Note:** The ability to add globally scoped files to globally scoped applications also allows you to move dictionary collection entries to a custom global scope. This action may result in unexpected cross-scope failures as the **sys\_db\_object** table and collection are not in the same scope anymore. The implication of this action is that CRUD operations \(that are allowed based on sys\_db\_object application access and existent cross-scope privileges\) would not be permitted without an obvious reason.


## Result

The system moves the selected files to the selected application from the global scope, and flags them as customizable files. For example, if you select the sys\_ui\_policy file, the associated sys\_ui\_policy\_actions file is also added to the selected application, and flagged as customizable. You see error messages when errors occur in the add process, or a confirmation when your files are successfully added to the globally scoped application.

**Parent Topic:**[Legacy - Global application file management](../concept/manage_global_application_files.md)

