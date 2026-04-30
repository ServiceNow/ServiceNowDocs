---
title: File Read activity
description: The File Read activity reads a file on a Linux or UNIX computer.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SSH activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# File Read activity

The File Read activity reads a file on a Linux or UNIX computer.

This activity replaces an SSH activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [SSH activity designer template](../../orchestration-activity-designer/task/t_CreateAnSSHActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Global** &gt; **Orchestration - SSH**.

## Input variables

|Input variable|Description|
|--------------|-----------|
|Hostname|Hostname or IP address of the destination server for SSH activity.|
|Directory|Name of the working directory.|
|File|The name of the file to read.|

## Output variables

|Output variable|Description|
|---------------|-----------|
|contents|Content of the file to read.|
|result|Either **success** or **failure**.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](../../orchestration-activity-designer/task/t_CreateAParsingRule.md#).|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully read the contents of the specified file.|
|Failure|Activity could not read the contents of the specified file.|

**Parent Topic:**[SSH activity pack](../concept/c_OrchestrationSSHCustomActivities.md)

