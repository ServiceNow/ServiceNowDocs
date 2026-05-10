---
title: Create Diagnostic scans and map related scripts
description: Once you have created diagnostic features and scripts, map them to a diagnostic scan to check the health of data in your application. Use fix scripts to rectify any corrupt or invalid data that the diagnostic scan identifies.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Project Diagnostics, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
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

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information, see [Diagnostics form](../../resource-management/reference/diagnostics-form.md).

4.  Select the Roles icon \(![Edit user roles icon](../image/edit_user_roles_icon.png)\) and move the desired roles to the Selected list.

    The users with the selected roles can access the diagnostic script.

5.  Search for and select diagnostic scripts to map with the diagnostic scan in the **Diagnostics and Script Mappings** section.

6.  Select **Submit**.


## What to do next

-   Create related link for navigating to the diagnostic features and scans in the application. For more information, see [Create a UI action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_EditingAUIAction.md).
-   Run diagnostic scan and view results. For an example of how the diagnostics scan work, see [Use Project Diagnostics to detect corrupt project data](../../project-management/task/project-diagnostics.md).

**Related topics**  


[Diagnostics form](../../resource-management/reference/diagnostics-form.md)

