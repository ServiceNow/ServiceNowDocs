---
title: File Replace String activity
description: The File Replace String activity finds and replaces a string in a file on a Linux or UNIX computer.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SSH activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# File Replace String activity

The File Replace String activity finds and replaces a string in a file on a Linux or UNIX computer.

This activity replaces an SSH activity by the same name available in releases prior to Istanbul. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Istanbul. However, all new workflows must use the custom version of this activity. This activity was built with the [SSH activity template](../../orchestration-activity-designer/task/t_CreateAnSSHActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

<table id="table_dpc_r5z_zp"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hostname

</td><td>

Hostname or IP address of destination server for SSH activity.

</td></tr><tr><td>

directory

</td><td>

Name of the working \(target\) directory.

</td></tr><tr><td>

file

</td><td>

Name of the file in which the string is to be replaced.

</td></tr><tr><td>

find\_pattern

</td><td>

A regular expression of the text to replace.

</td></tr><tr><td>

replace\_string

</td><td>

The replacement string for the text found by the expression in the **find\_pattern** variable.

</td></tr><tr><td>

options

</td><td>

Replacement options:-   **first**: Replaces the first occurence of the pattern.
-   **all**: Replaces all occurrences of the pattern.

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|return\_code|Indicates whether or not the string was replaced successfully in the target file.|
|error\_message|Message that indicates if an error has occurred. Any value other than **0** indicates a failure.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity has successfully replaced the string in the file.|
|Failure|The activity has failed to replaced the string in the file.|

**Parent Topic:**[SSH activity pack](../concept/c_OrchestrationSSHCustomActivities.md)

