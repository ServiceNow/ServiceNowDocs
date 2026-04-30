---
title: Is Device in Collection activity
description: This activity verifies if a device exists in an SCCM device collection.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, Creating integrations with applications]
---

# Is Device in Collection activity

This activity verifies if a device exists in an SCCM device collection.

The Is Device in Collection activity uses the [PowerShell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to verify if a specific device exists in an SCCM device collection. The activity is configured to use a MID Server with PowerShell capabilities and to run a MID Server script called IsDeviceInCollection.ps1 to perform the test.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|
|collection|Name of the device collection.|
|device|Name of the device to verify is in the collection.|

## Output variables

|Variable|Description|
|--------|-----------|
|output|Variable that contains the test result: True/False|
|errorMessage|Variable that contains the activity output error message.|

## Conditions

|Condition|Description|
|---------|-----------|
|Exist|The device exists in the collection.|
|Not exist|The device does not exist in the collection.|
|Failure|Activity failed.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)

