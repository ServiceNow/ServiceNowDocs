---
title: Remove File or Directory activity
description: The Remove File or Directory activity removes a file or a directory on an SFTP server, including subdirectories, when configured.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SFTP File Transfer activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Remove File or Directory activity

The Remove File or Directory activity removes a file or a directory on an SFTP server, including subdirectories, when configured.

## Input variables

|Variable|Description|
|--------|-----------|
|sourceHost|Name or IP address of the server containing the files you want to remove.|
|sourcePort|Port number to use to communicate with the target server. The default port number is **22**.|
|sourceFilePath|Full path to the file or directory to remove. To remove multiple files or directories using a single activity, enter a semicolon-separated list of paths in this field.|
|isDirectory|True/false variable that determines if the specified file path is a directory. The default value for this variable is **false**.|
|includeSubfolders|True/false variable that determines if the given directory and all of its subfolders should be removed. The default value for this variable is **false**. If the value for this field is **false**, then the activity can only remove an empty directory. This field appears when the **isDirectory** checkbox is selected.|
|sourceCredentialTag|Specific [Credential aliases for Orchestration activities](https://www.servicenow.com/docs/access?context=c_AssignCredsOrchActivities&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) this activity must use to run SSH commands on the host.|

## Output variables

<table id="table_omt_xqw_mt"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errorMessage

</td><td>

The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#). If this variable is not null, the operation has failed.

</td></tr><tr><td>

result

</td><td>

Either **success** or **failure**.

</td></tr><tr><td>

deletionResults

</td><td>

The **deletionResults** array contains these attributes:-   **fullPath**: Full path to the file or directory targeted.
-   **status**: Either **succeeded** or **failed**.
-   **reason**: Text message describing the cause of a failure.

</td></tr></tbody>
</table>## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in removing the file or directory specified.|
|Failure|The activity failed to remove the file or directory specified.|

**Parent Topic:**[SFTP File Transfer activity pack](../concept/c_OrchestrationSFTPActivityPack.md)

