---
title: Is User in Collection activity
description: This activity verifies if a user exists in an SCCM user collection.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Is User in Collection activity

This activity verifies if a user exists in an SCCM user collection.

The Is User in Collection activity uses the [PowerShell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to verify if a specific user exists in an SCCM user collection. The activity is configured to use a MID Server with PowerShell capabilities and to run a MID Server script called IsUserInCollection.ps1 to perform the test.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|
|collection|Name of the user collection.|
|user|Name of the user to verify is in the collection.|

## Output variables

|Variable|Description|
|--------|-----------|
|output|Variable that contains the test result: True/False|
|errorMessage|Variable that contains the activity output error message.|

## Conditions

|Condition|Description|
|---------|-----------|
|Exist|The user exists in the collection.|
|Not exist|The user does not exist in the collection.|
|Failure|Activity failed.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)

