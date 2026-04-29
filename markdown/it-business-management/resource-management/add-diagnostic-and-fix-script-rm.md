---
title: Add diagnostics and fix scripts for resource
description: Add existing or new diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Resource Diagnostics to detect corrupt resource data, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Add diagnostics and fix scripts for resource

Add existing or new diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.

## Before you begin

Role required: adt\_admin

## About this task

You can create multiple diagnostic scripts to check various aspects of data. The results of the filter conditions, that you specify in a diagnostic feature, is used as an input for the diagnostic script while executing. You can also use the result of one script in subsequent scripts.

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Scripts**.

2.  Select **New**.

3.  On the Diagnostics Scripts form, fill the fields.

    For a description of the field names, see [Diagnostics Scripts form](../reference/diag-scripts-form.md).

4.  If you want to include a script for fixing the corrupt or invalid data identified by the diagnostic script, select the **Has Fix script** check box.

5.  Use **Fix script Access Roles** to move required roles to the Selected list.

    The users with the selected roles can access the diagnostic script.

6.  In the **Fix script** section, add the actual code for the fix script.

7.  Select **Submit**.


**Parent Topic:**[Use Resource Diagnostics to detect corrupt resource data](use-resource-diagnostics.md)

