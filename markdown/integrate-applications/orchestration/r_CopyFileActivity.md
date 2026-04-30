---
title: Copy File activity
description: The Copy File activity copies a file from an SFTP server \(source host\) to another SFTP server \(target host\).
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SFTP File Transfer activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Copy File activity

The Copy File activity copies a file from an SFTP server \(source host\) to another SFTP server \(target host\).

## Input variables

|Variable|Description|
|--------|-----------|
|sourceHost|Name or IP address of the server containing the files you want to transfer.|
|sourcePort|Port number to use to communicate with the source server. The default port number is **22**.|
|sourceFilePath|Full path to the file to copy from the source host.|
|targetHost|Name or IP address of the server to which you want to move the files.|
|targetPort|Port number to use to communicate with the target server. The default port number is **22**.|
|targetFilePath|Full path to the copied file on the target host.|
|tempFileSuffix|Temporary suffix to use when moving a file. If this field contains a value, the activity deletes the duplicate target file, if it exists, and then copies the source file to a temporary file using **targetFilePath + tempFileSuffix** as the name. Upon completion, the activity renames the file to the actual target file name. If this field is blank, the activity copies the source file directly to the target file and overwrites it, if it already exists.|
|sourceCredentialTag|Specific [Credential aliases for Orchestration activities](https://www.servicenow.com/docs/access?context=c_AssignCredsOrchActivities&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) this activity must use to run SSH commands on the source host.|
|targetCredentialTag|Specific credential tag this activity must use to run SSH commands on the target host.|

## Output variables

|Variable|Description|
|--------|-----------|
|errorMessages|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#). If this variable is not null, the operation has failed.|
|result|Text message advising that the command was executed successfully.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in copying the file.|
|Failure|The activity failed to copy the file.|

**Parent Topic:**[SFTP File Transfer activity pack](../concept/c_OrchestrationSFTPActivityPack.md)

