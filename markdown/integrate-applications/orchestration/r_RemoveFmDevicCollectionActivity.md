---
title: Remove from Device Collection activity
description: The Remove from Device Collection activity removes a device from a Microsoft System Center Configuration Manager \(SCCM\) device collection.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Remove from Device Collection activity

The Remove from Device Collection activity removes a device from a Microsoft System Center Configuration Manager \(SCCM\) device collection.

The Remove from Device Collection activity uses the [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to remove a device from a device collection on a Microsoft SCCM server. The activity is configured to use a MID Server with Powershell capabilites and to run a MID Server script called RemoveFromUserCollection.ps1 to edit the collection.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|
|collection|Name of the device collection.|
|device|Name of the device to add to the collection.|

## Output variables

|Variable|Description|
|--------|-----------|
|output|Variable that contains a value that is passed to other activities in the workflow|
|error|Variable that contains the activity output error message.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully removed the device from the SCCM device collection.|
|Failure|Activity failed to remove the device from the SCCM device collection.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)

