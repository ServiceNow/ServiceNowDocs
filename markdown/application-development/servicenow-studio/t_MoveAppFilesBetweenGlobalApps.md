---
title: Legacy - Move an application file between global applications
description: Move selected application files and their descendant files to a selected global application. When you select a global application, the selected application files are automatically assigned to it. You cannot move an application file into or out of a scoped application.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy - Global application file management, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Move an application file between global applications

Move selected application files and their descendant files to a selected global application. When you select a global application, the selected application files are automatically assigned to it. You cannot move an application file into or out of a scoped application.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Roles required: admin or a delegated\_developer role that grants full access.

This option is only available if the Global App File Management plugin is active.

## Procedure

1.  Navigate to the application file in a list or form view.

    For example, navigate to **All** &gt; **System UI** &gt; **UI Policies** to select UI policy files to move.

2.  Select the check box beside each file you wish to move, and then select **Move to Application** in the **Actions on selected rows** choice list.

3.  Select the global application.

    ![Move application files to a global application](../image/MoveToApplication.png)

4.  Click **Move**.

    The selected application files and its descendant files are moved to the selected global application.


**Parent Topic:**[Legacy - Global application file management](../concept/manage_global_application_files.md)

