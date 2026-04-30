---
title: Diagnostics Feature form
description: Learn about the fields of diagnostics feature form.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Form field information for Project Management, Reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Diagnostics Feature form

Learn about the fields of diagnostics feature form.

|Field|Description|
|-----|-----------|
|Name|Name of the diagnostic feature. This name appears in the application to which the diagnostic feature belongs.![Diagnostic feature name in application](../image/diagnostic_feature_name.png)|
|Active|Option for activating the diagnostic feature.|
|Application|Search for and select the application with which you want to associate this diagnostic feature.|
|Roles|User roles that allow access to the diagnostic feature.|
|Description|Details of the scans in the diagnostic feature. The description is displayed in the application to which the diagnostic feature belongs.![Diagnostics feature description on the application page](../image/app_diagnostic_description.png)|

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
</table>**Related topics**  


[Create and add diagnostic features](../task/add-diagnostic-feature.md)

