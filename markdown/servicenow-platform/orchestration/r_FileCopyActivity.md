---
title: File Copy activity
description: The custom File Copy activity copies a file on a Linux or UNIX computer.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SSH activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# File Copy activity

The custom File Copy activity copies a file on a Linux or UNIX computer.

This activity replaces an SSH activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [SSH activity designer template](../../orchestration-activity-designer/task/t_CreateAnSSHActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Global** &gt; **Orchestration - SSH**.

## Input variables

|Input variable|Description|
|--------------|-----------|
|hostname|Hostname or IP address of destination server for SSH activity.|
|directory|Name of the working directory.|
|src\_file|Name of the source file.|
|dst\_file|The name of the destination file.|

## Output variables

|Output variable|Description|
|---------------|-----------|
|result|Either **success** or **failure**.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully copied the file on the specified host.|
|Failure|Activity failed to copy the file on the specified host.|

**Parent Topic:**[SSH activity pack](../concept/c_OrchestrationSSHCustomActivities.md)

