---
title: File Read activity
description: The File Read activity reads a file on a Linux or UNIX computer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/orchestration/r\_FileReadActivity.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SSH activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# File Read activity

The File Read activity reads a file on a Linux or UNIX computer.

This activity replaces an SSH activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [SSH activity designer template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateAnSSHActivity.md), which gives workflow administrators the ability to store input and output variables in the [databus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrationDatabus.md).

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
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateAParsingRule.md).|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully read the contents of the specified file.|
|Failure|Activity could not read the contents of the specified file.|

**Parent Topic:**[SSH activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrationSSHCustomActivities.md)

