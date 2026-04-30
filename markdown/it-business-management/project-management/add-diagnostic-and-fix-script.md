---
title: Add diagnostic and fix scripts
description: Add diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Project Diagnostics, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add diagnostic and fix scripts

Add diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.

## Before you begin

Role required: adt\_admin

## About this task

The results of the filter conditions that you specify in a [diagnostic feature](add-diagnostic-feature.md) are used as an input for the diagnostic script while executing. You can also use the result of one script in subsequent scripts.

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Scripts**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information, see [Diagnostic Scripts form](../reference/diagnostic-scripts-form.md).

4.  Include a script for fixing the corrupt or invalid data identified by the diagnostic script.

    1.  Select the **Has Fix script** check box.

    2.  Select the Edit User Roles icon \(![Edit User Roles icon](../image/edit_user_roles_icon.png)\) and choose the roles that can access the diagnostic script.

    3.  In the **Fix script** section, add the code for the fix script.

5.  Select **Submit**.


**Related topics**  


[Project Diagnostics](../../project-management/concept/project-diagnostics-overview.md)

