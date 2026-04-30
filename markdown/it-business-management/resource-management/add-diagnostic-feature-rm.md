---
title: Add diagnostic features for resource
description: Create diagnostic features to evaluate an application feature and organize various diagnostic scans for an application. The diagnostic features appear in the target application and list all the diagnostic scans associated with the diagnostic feature for that application.
locale: en-US
release: zurich
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use Resource Diagnostics to detect corrupt resource data, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Add diagnostic features for resource

Create diagnostic features to evaluate an application feature and organize various diagnostic scans for an application. The diagnostic features appear in the target application and list all the diagnostic scans associated with the diagnostic feature for that application.

## Before you begin

Role required: adt\_admin

## About this task

A diagnostic feature can consist of a single or multiple diagnostic scans. These diagnostic scans execute the scripts, that they’re mapped with, to detect data corruption or invalid data. You can then create diagnostic scans with scripts and execute these scans to check resources for any corrupt or invalid data. If a fix script is associated with a scan, you can use it for fixing the corrupt or invalid data.

You can also define fields for users to create a specific filter condition. The diagnostic scripts use the results of these filter conditions as inputs for detecting any corrupt or invalid data.

You can check for the existing features under the **Features** module. If you don't find one matching your needs, create a diagnostic feature and associate it with an application.

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Features**.

2.  Select **New**.

3.  On the Diagnostics Feature form, fill the fields.

    For a description of the field names, see [Diagnostics Feature form](../reference/diag-feature-form.md).

4.  Define user input values for specifying filter conditions in the **Diagnostics Inputs** section.

    The fields in this section are displayed in the application as condition builder. For a description of the field names, see [Diagnostics Inputs form](../reference/diag-input-field.md).

5.  Select **Submit**.


## What to do next

Create diagnostic scripts and add fix scripts to use with the diagnostic feature. For more information, see [Add diagnostics and fix scripts for resource](add-diagnostic-and-fix-script-rm.md).

**Parent Topic:**[Use Resource Diagnostics to detect corrupt resource data](use-resource-diagnostics.md)

