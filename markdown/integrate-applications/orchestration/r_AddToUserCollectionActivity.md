---
title: Add to User Collection activity
description: The Add to User Collection activity adds a user to a Microsoft System Center Configuration Manager \(SCCM\) user collection.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, Creating integrations with applications]
---

# Add to User Collection activity

The Add to User Collection activity adds a user to a Microsoft System Center Configuration Manager \(SCCM\) user collection.

The Add to User Collection activity uses the [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to access the SCCM server. The activity is configured to use a MID Server with Powershell capabilities and to run a MID Server script called AddToUserCollection.ps1 to edit the collection.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

**Note:** The Add to User Collection activity does not use pre-processing or post processing scripts.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|
|collection|Name of the user collection.|
|user|Name of the user to add to the collection.|

## Output variable

|Variable|Description|
|--------|-----------|
|output|Variable that contains a value that is passed to other activities in the workflow.|
|error|Variable that contains the activity output error message.|

## Conditions

| | |
|---|---|
|Success|Activity successfully added a user to the SCCM user collection.|
|Failure|Activity failed to add a user to the SCCM user collection.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)

