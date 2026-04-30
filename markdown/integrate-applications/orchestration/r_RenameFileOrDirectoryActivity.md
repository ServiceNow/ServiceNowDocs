---
title: Rename File or Directory activity
description: The Rename File or Directory activity renames a file or directory to a new name on an SFTP server.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SFTP File Transfer activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Rename File or Directory activity

The Rename File or Directory activity renames a file or directory to a new name on an SFTP server.

## Input variables

|Variable|Description|
|--------|-----------|
|sourceHost|Name or IP address of the server containing the file or directory you want to rename.|
|sourcePort|Port number to use to communicate with the target server. The default port number is **22**.|
|sourceFilePath|Full path to the file or directory to rename.|
|targetFilePath|Full path to the renamed file or directory.|
|sourceCredentialTag|Specific [Credential aliases for Orchestration activities](https://www.servicenow.com/docs/access?context=c_AssignCredsOrchActivities&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) this activity must use to run SSH commands on the host.|

## Output variables

|Variable|Description|
|--------|-----------|
|errorMessages|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#). If this variable is not null, the operation has failed.|
|result|A message saying that the operation has been successful. For example, you might see: `Rename /tmp/sftp_test/subdir1 to /tmp/sftp_test/subdir2 complete`.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in renaming the file or directory.|
|Failure|The activity failed to rename the file or directory.|

**Parent Topic:**[SFTP File Transfer activity pack](../concept/c_OrchestrationSFTPActivityPack.md)

