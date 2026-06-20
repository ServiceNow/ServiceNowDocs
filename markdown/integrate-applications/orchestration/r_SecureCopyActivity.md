---
title: Secure Copy activity
description: The Secure Copy activity copies a file from one host to another, without storing the copied file on the MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/orchestration/r\_SecureCopyActivity.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SSH activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Secure Copy activity

The Secure Copy activity copies a file from one host to another, without storing the copied file on the MID Server.

This activity replaces an SSH activity by the same name available in releases prior to Geneva. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Geneva. However, all new workflows must use the custom version of this activity. This activity was built with the [SSH activity designer template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateAnSSHActivity.md), which gives workflow administrators the ability to store input and output variables in the [databus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrationDatabus.md).

## Input variables

|Input variable|Description|
|--------------|-----------|
|from\_host|Host name or IP address of the source machine.|
|from\_scp\_file|Name of the file to copy, including the absolute path.|
|to\_host|Host name or IP address of the target machine.|
|to\_scp\_file|Path to the target file. This path can be absolute or relative to the logged in user's home directory.|
|debug\_mid|Check box that enables debug logging when selected.|
|debug\_ssh|Check box that enables J2SSH debug logging when selected.|

## Output variables

|Output variable|Description|
|---------------|-----------|
|payload|The **executionResult.payload** from the [Activity designer parsing sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateAParsingRule.md).|
|output|The **executionResult.output** from the parsing sources.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully copied the file from one host to another.|
|Failure|Activity failed to copy the file from one host to another.|

**Parent Topic:**[SSH activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrationSSHCustomActivities.md)

