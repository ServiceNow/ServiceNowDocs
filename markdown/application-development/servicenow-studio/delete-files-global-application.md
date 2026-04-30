---
title: Legacy - Remove a file from a global application
description: Remove selected files from the selected global application and return them to the previous global application that owned the file. If there is no previous owner, file is returned back to global scope. The removed files are still considered customized files.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Legacy - Global application file management, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Remove a file from a global application

Remove selected files from the selected global application and return them to the previous global application that owned the file. If there is no previous owner, file is returned back to global scope. The removed files are still considered customized files.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

This option is only available if the Global Application File Management plugin is active.

Role required: admin or a delegated\_developer role that grants full access.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications** &gt; **In Development**.

2.  To the right of the application name, select **Edit in Studio**.

3.  In Studio, select **File** &gt; **Remove Files**.

    The system displays a list of the files in this global application.

4.  Select the file that you want to remove from this application.

5.  Click **Remove**.


**Parent Topic:**[Legacy - Global application file management](../concept/manage_global_application_files.md)

