---
title: Change Service State activity
description: The Change Service State activity starts or stops a Windows service on a remote system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/orchestration/r\_ChangeServiceState.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [PowerShell activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Change Service State activity

The Change Service State activity starts or stops a Windows service on a remote system.

This activity replaces a Powershell activity by the same name available in releases prior to Istanbul. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Istanbul. However, all new workflows must use the custom version of this activity. This activity was built with the [Powershell activity template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/t_CreateAPowershellActivity.md), which gives workflow administrators the ability to store input and output variables in the [databus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/c_OrchestrationDatabus.md).

## Input Variables

|Variable|Description|
|--------|-----------|
|hostname|Hostname or IP address of the target Windows machine on which the service is installed. Use the Resolve DNS activity to resolve hostnames into IP addresses.|
|service|Name of the Windows service to start or stop. The **service** parameter is the service name, not the display name of the service affected.|
|state|There are two actions to select for a service state change: **StartService** or **StopService**.|

## Output variables

|Variable|Description|
|--------|-----------|
|errorMessage|The **executionResult.errorMessages** from the [Activity designer parsing sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/t_CreateAParsingRule.md). If there is no error, this value is null.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|The target service was successfully started or stopped.|
|Failure|The update to the target service was unsuccessful, or the service was not found on the target system.|

**Parent Topic:**[PowerShell activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/c_OrchestrPwrshellActivityPack.md)

