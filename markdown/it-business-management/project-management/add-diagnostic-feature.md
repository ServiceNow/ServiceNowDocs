---
title: Create and add diagnostic features
description: Create and add diagnostic features, which consist of single or multiple diagnostic scans that execute mapped scripts to detect data corruption or invalid data.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Project Diagnostics, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create and add diagnostic features

Create and add diagnostic features, which consist of single or multiple diagnostic scans that execute mapped scripts to detect data corruption or invalid data.

## Before you begin

Role required: adt\_admin

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Features**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the diagnostic feature. This name appears in the application to which the diagnostic feature belongs.![Diagnostic feature name in application](../image/diagnostic_feature_name.png)|
    |Active|Option for activating the diagnostic feature.|
    |Application|Search for and select the application with which you want to associate this diagnostic feature.|
    |Roles|User roles that allow access to the diagnostic feature.|
    |Description|Details of the scans in the diagnostic feature. The description is displayed in the application to which the diagnostic feature belongs.![Diagnostics feature description on the application page](../image/app_diagnostic_description.png)|

4.  Define the fields available to users for specifying filter conditions in the **Diagnostics Inputs** section.

<table id="table_a5g_2lr_wjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name of the label for the input fields.

</td></tr><tr><td>

Field Type

</td><td>

The **Reference** field type.

</td></tr><tr><td>

Table

</td><td>

Name of the table on which the query specified in the condition should run.

</td></tr><tr><td>

Key

</td><td>

An identifier for the user input condition. If a user specifies multiple conditions, this key acts as a unique identifier for each condition. You can use this key as the input for the **scanContext** section of the diagnostic script. For example, if you specify **projectFilter** as a key, the **scanContext** section of the diagnostic script would appear as follows: `var encodedQuery = scanContext.input.projectFilter;`

</td></tr></tbody>
</table>    The fields that you configure in the **Diagnostics Inputs** section appear in the **Feature Inputs** section of the Application Diagnostics Tool page, as shown in the following example.

    ![User input fields in application](../image/app_diagnostics_feature_inputs.png)

5.  Click **Submit**.


## What to do next

Create diagnostic scripts and add fix scripts to use with the diagnostic feature. For more information, see [Add diagnostic and fix scripts](add-diagnostic-and-fix-script.md).

