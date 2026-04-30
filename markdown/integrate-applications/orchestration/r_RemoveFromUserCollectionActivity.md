---
title: Remove from User Collection activity
description: The Remove from User Collection activity removes a user from a Microsoft System Center Configuration Manager \(SCCM\) user collection.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Remove from User Collection activity

The Remove from User Collection activity removes a user from a Microsoft System Center Configuration Manager \(SCCM\) user collection.

The Remove from User Collection activity uses the [Powershell activity designer template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to access a user collection on a Microsoft SCCM target host. The activity is configured to use a MID Server with Powershell capabilites and to run a MID Server script called `RemoveFromUserCollection.ps1` to edit the collection.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|
|collection|Name of the user collection.|
|user|Name of the user to add to the collection.|

## Output variables

|Variable|Description|
|--------|-----------|
|output|Variable that contains a value that is passed to other activities in the workflow.|
|error|Variable that contains the activity output error message.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully removed the user from the SCCM user collection.|
|Failure|Activity failed to remove the user from the SCCM user collection.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)

