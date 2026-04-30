---
title: Legacy - Global application file management
description: Once you create a globally scoped application in the ServiceNow Studio, you can add existing globally scoped files to it, remove files from it, or move application files between global applications.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Global application file management

Once you create a globally scoped application in the ServiceNow Studio, you can add existing globally scoped files to it, remove files from it, or move application files between global applications.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   **[Legacy - Add a file from the global scope to a global application](../task/add-files-to-global-application.md)**  
Add existing globally scoped files into a selected global application. You can search for files in another globally scoped application by the update set name, table, or file name.
-   **[Legacy - Remove a file from a global application](../task/delete-files-global-application.md)**  
Remove selected files from the selected global application and return them to the previous global application that owned the file. If there is no previous owner, file is returned back to global scope. The removed files are still considered customized files.
-   **[Legacy - Move an application file between global applications](../task/t_MoveAppFilesBetweenGlobalApps.md)**  
Move selected application files and their descendant files to a selected global application. When you select a global application, the selected application files are automatically assigned to it. You cannot move an application file into or out of a scoped application.
-   **[Legacy - Add multiple files from global update sets to a global application](../task/add-multiple-files-to-global-app.md)**  
Add multiple globally scoped application files at once from one or more global update sets to a new or existing global application.
-   **[Legacy - Add multiple files from customer updates to a global application](../task/add-multiple-files-from-customer-updates-to-global-app.md)**  
Add multiple globally scoped application files at once from one or more customer updates to a new or existing global application.
-   **[Legacy - Review claimed or skipped global files](global-app-review-claimed-skipped-files.md)**  
Review files when one or more of your files has been skipped or claimed by another application.

**Parent Topic:**[Legacy - ServiceNow Studio](c_ServiceNowStudio.md)

