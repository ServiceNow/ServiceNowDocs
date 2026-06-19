---
title: Files Compare activity
description: The Files Compare activity compares two files on a Linux or UNIX computer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/orchestration/r\_FilesCompareActivity.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SSH activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Files Compare activity

The Files Compare activity compares two files on a Linux or UNIX computer.

This activity replaces an SSH activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [SSH activity designer template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateAnSSHActivity.md), which gives workflow administrators the ability to store input and output variables in the [databus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrationDatabus.md).

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Global** &gt; **Orchestration - SSH**.

## Input variables

|Input variable|Description|
|--------------|-----------|
|Hostname|Hostname or IP address of the destination server for SSH activity.|
|Directory|Name of the working directory.|
|OldFile|Name of the first file to compare.|
|NewFile|Name of the second file to compare.|

## Output variables

|Output variable|Description|
|---------------|-----------|
|contents|File comparison result. This is the difference of the two compared files.|
|result|Either **success** or **failure**.|
|return-code|Either **0**, if the two files are the same, or **1**, if the two files are different.|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateAParsingRule.md).|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully compared the specified files.|
|Failure|Activity could not complare the specified files.|

