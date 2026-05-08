---
title: Get File List activity
description: The Get File List activity returns a list of files from a given directory and its subdirectories on an SFTP server \(source host\).
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SFTP File Transfer activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Get File List activity

The Get File List activity returns a list of files from a given directory and its subdirectories on an SFTP server \(source host\).

## Input variables

|Variable|Description|
|--------|-----------|
|sourceHost|Name or IP address of the server containing the files you want to list.|
|sourcePort|Port number to use to communicate with the target server. The default port number is **22**.|
|sourceDirectory|Path to the target directory containing the files to list.|
|sourceFiles|List of target files to return. This is a comma separated list that accepts wildcards, such as **\*.txt**.|
|excludedFiles|List of target files to exclude. This is a comma separated list that accepts wildcards, such as **\*.txt**.|
|includeSubfolders|True/false variable that determines if files from subfolders are included in the list. The default value for this variable is **false**.|
|sourceCredentialTag|Specific Credential aliases for Orchestration activities this activity must use to run SSH commands on the host.|

## Output variables

|Variable|Description|
|--------|-----------|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#). If this variable is not null, the operation has failed. An activity can examine the error message to customize a condition. For example, if the error message contains **NO\_SUCH\_FILE**, the activity can be considered successful, depending on circumstances.|
|result|List of requested files, returned as a JSON string.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in listing the requested files.|
|Failure|The activity failed to list the requested files.|

**Parent Topic:**[SFTP File Transfer activity pack](../concept/c_OrchestrationSFTPActivityPack.md)

