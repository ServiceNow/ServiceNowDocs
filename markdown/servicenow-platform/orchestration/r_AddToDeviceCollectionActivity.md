---
title: Add to Device Collection activity
description: The Add to Device Collection activity adds the specified device into a Microsoft System Center Configuration Manager \(SCCM\) device collection.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add to Device Collection activity

The Add to Device Collection activity adds the specified device into a Microsoft System Center Configuration Manager \(SCCM\) device collection.

The Add to Device Collection activity uses the [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to add a specified device to an SCCM device collection. The activity is configured to use a MID Server with Powershell capabilities and to run a MID Server script called AddToDeviceCollection.ps1 to edit the collection.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

**Note:** The Add to Device Collection activity does not use pre-processing or post-processing scripts.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|
|collection|Name of the device collection.|
|device|Name of the device to add to the collection.|

## Output variables

|Variable|Description|
|--------|-----------|
|output|Variable that contains a value that is passed to other activities in the workflow.|
|error|Variable that contains the activity output error message.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully added the device to the SCCM device collection.|
|Failure|Activity failed to add the device to the SCCM device collection.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)

