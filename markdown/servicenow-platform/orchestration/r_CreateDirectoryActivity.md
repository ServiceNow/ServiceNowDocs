---
title: Create Directory activity
description: The Create Directory activity creates a new directory on an SFTP server.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SFTP File Transfer activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create Directory activity

The Create Directory activity creates a new directory on an SFTP server.

## Input variables

|Variable|Description|
|--------|-----------|
|sourceHost|Name or IP address of the server containing the files you want to move.|
|sourcePort|Port number to use to communicate with the source server. The default port number is **22**.|
|sourceDirectory|Path to the target directory to create.|
|sourceCredentialTag|Specific [Credential aliases for Orchestration activities](https://www.servicenow.com/docs/access?context=c_AssignCredsOrchActivities&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) this activity must use to run SSH commands on the host.|

## Output variables

|Variable|Description|
|--------|-----------|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#). If this variable is not null, the operation has failed.|
|result|Text message advising that the command was executed successfully.|

## Conditions

|Variable|Description|
|--------|-----------|
|Success|The activity succeeded in creating the directory.|
|Failure|The activity failed to create the directory.|

**Parent Topic:**[SFTP File Transfer activity pack](../concept/c_OrchestrationSFTPActivityPack.md)

