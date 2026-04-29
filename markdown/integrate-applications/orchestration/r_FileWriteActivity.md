---
title: File Write activity
description: The File Write activity writes a file on a Linux or UNIX computer.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SSH activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# File Write activity

The File Write activity writes a file on a Linux or UNIX computer.

The source file can be an absolute or relative path from the Directory. If an absolute path is used, then no value is required in the Directory field.

This activity replaces an SSH activity by the same name available in releases prior to Istanbul. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Istanbul. However, all new workflows must use the custom version of this activity. This activity was built with the [SSH activity template](../../orchestration-activity-designer/task/t_CreateAnSSHActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

<table id="table_d3s_qvz_zp"><thead><tr><th>

Field

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

Name of the file to be written.

</td></tr><tr><td>

behavior

</td><td>

Select one of the following:-   **overwrite**: Creates the file if it does not exist and overwrites the file if it does exist.
-   **append**: Creates the file if it does not exist and appends the new content to an existing file.
-   **create only**: Creates the file if it does not exist and fails if the file does exist.

</td></tr><tr><td>

contents

</td><td>

What to write or append \(depending on the behavior\) to the file

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|return\_code|Indicates whether or not the file write operation was successful.|
|error\_message|Message that indicates if an error has occurred. Any value other than **0** indicates a failure.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity wrote a file in the target directory.|
|Failure|The activity failed to write a file in the target directory.|

**Parent Topic:**[SSH activity pack](../concept/c_OrchestrationSSHCustomActivities.md)

