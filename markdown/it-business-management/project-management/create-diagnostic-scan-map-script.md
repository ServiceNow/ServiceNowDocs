---
title: Create Diagnostic scans and map related scripts
description: Once you have created diagnostic features and scripts, map them to a diagnostic scan to check the health of data in your application. Use fix scripts to rectify any corrupt or invalid data that the diagnostic scan identifies.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project Diagnostics, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create Diagnostic scans and map related scripts

Once you have created diagnostic features and scripts, map them to a diagnostic scan to check the health of data in your application. Use fix scripts to rectify any corrupt or invalid data that the diagnostic scan identifies.

## Before you begin

In order to create a diagnostic scan, you must have already created diagnostic features and scripts For more information, see [Create and add diagnostic features](add-diagnostic-feature.md) and [Add diagnostic and fix scripts](add-diagnostic-and-fix-script.md).

Role required: adt\_admin

## About this task

You can map multiple scripts with each diagnostic scan and define the order of their execution.

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Diagnostics**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the diagnostic scan. This name appears in the application to which this diagnostic scan belongs.![Diagnostic scan name in the application](../image/diagnostic_scan_name.png)|
    |Active|Option for activating the diagnostic scan.|
    |Order|Order in which this diagnostic scan appears in the application.|
    |Feature|Diagnostic feature with which you want to associate this diagnostic scan.|
    |Roles|Option for adding or removing user roles that can access the diagnostic scan.|
    |Description|Details of the diagnostic scan. The description is displayed in the application to which the diagnostic scan belongs.![Diagnostic scan description in application](../image/diagonstic_scan_description.png)|

4.  Click the Roles icon \(![Edit user roles icon](../image/edit_user_roles_icon.png)\) and move the desired roles to the Selected list.

    The users with the selected roles can access the diagnostic script.

5.  Search for and select diagnostic scripts to map with the diagnostic scan in the **Diagnostics and Script Mappings** section.

6.  Click **Submit**.


## What to do next

-   Create related link for navigating to the diagnostic features and scans in the application. For more information, see [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   Run diagnostic scan and view results. For an example of how the diagnostics scan work, see [Use Project Diagnostics to detect corrupt project data](../../project-management/task/project-diagnostics.md).

