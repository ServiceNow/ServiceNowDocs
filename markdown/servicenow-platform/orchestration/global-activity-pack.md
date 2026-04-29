---
title: Global activities
description: Global activities are Orchestration activities created in the global scope.The Test Server Alive activity determines if a target system is alive by its response to a particular protocol.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Global activities

Global activities are Orchestration activities created in the global scope.

Any activities you create in the global scope are listed in the Global category in the **Packs** and **Custom** tabs of the Workflow Editor.

![Global activity pack](../image/GlobalPacks.png "Global activities")

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

## Test Server Alive activity

The Test Server Alive activity determines if a target system is alive by its response to a particular protocol.

This activity replaces an activity by the same name available in releases prior to Istanbul. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Istanbul. However, all new workflows must use the custom version of this activity. This activity was built with the [Probe activity template](../../orchestration-activity-designer/task/t_CreateAProbeActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

### Input variables

|Variable|Description|
|--------|-----------|
|port\_probes|A comma separated list of protocols to use to check for signs of activity on the target machine \(example: *wmi,wins,https,ssh,http,https,snmp,dns*\)|
|hostname|Hostname or IP address of the target system to check.|

### Output variables

|Variable|Description|
|--------|-----------|
|alive|Code that indicates whether or not the server is alive. If any value but **'1'** is returned, the server is not alive.|

### Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity determined that the device is running.|
|Failure|Activity failed to determine if the target device is running. Failure could be caused by a missing protocol or a device that is not accessible.|

