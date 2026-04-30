---
title: Set File Attributes activity
description: The Set File Attributes activity sets common file attributes, such as timestamps, size, permissions, and UID/GID, for a file or directory on an SFTP server.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [SFTP File Transfer activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Set File Attributes activity

The Set File Attributes activity sets common file attributes, such as timestamps, size, permissions, and UID/GID, for a file or directory on an SFTP server.

A good practice is to use the Get File List activity to return a list of files and their attributes first. Then, when you moved a file from a source host to a target host, use the Set File Attributes activity to set the source file attributes on the target file. This is demonstrated in the [SFTP File Transfer](r_SFTPWorkflow.md)workflow.

## Input variables

<table id="table_mbr_hxv_mt"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sourceHost

</td><td>

Name or IP address of the server containing the file or directory whose attributes you want to change.

</td></tr><tr><td>

sourcePort

</td><td>

Port number to use to communicate with the target server. The default port number is **22**.

</td></tr><tr><td>

sourceFilePath

</td><td>

Full path to the file or directory whose attributes you want to change.

</td></tr><tr><td>

userID

</td><td>

User ID attribute to apply to the file or directory. The UID and GUID variables must be set together as a pair.

</td></tr><tr><td>

groupID

</td><td>

Group ID attribute to apply to the file or directory. The UID and GUID variables must be set together as a pair.

</td></tr><tr><td>

permissions

</td><td>

File or directory permissions to set for the user and group specified. This value must be expressed as an integer, such as **16877**, which defines these permissions: **rwxr-xr-x**. **Note:** The permissions number is an internal value returned by the Get File List activity.

</td></tr><tr><td>

accessTimestamp

</td><td>

Override the timestamp when the file or directory was last accessed. The access and modification timestamps must be set together as a pair.

</td></tr><tr><td>

modificationTimestamp

</td><td>

Override the timestamp when the file or directory was last modified. The access and modification timestamps must be set together as a pair.

</td></tr><tr><td>

sizeInBytes

</td><td>

Size of the file or directory, expressed in bytes.

</td></tr><tr><td>

sourceCredentialTag

</td><td>

Specific [Credential aliases for Orchestration activities](https://www.servicenow.com/docs/access?context=c_AssignCredsOrchActivities&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) this activity must use to run SSH commands on the host.

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#). If this variable is not null, the operation has failed.|
|result|Text message advising that the command was executed successfully.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The activity succeeded in changing the attributes of the specified file or directory.|
|Failure|The activity failed to change the attributes of the specified file or directory.|

**Parent Topic:**[SFTP File Transfer activity pack](../concept/c_OrchestrationSFTPActivityPack.md)

