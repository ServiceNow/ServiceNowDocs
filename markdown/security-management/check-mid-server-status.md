---
title: Check MID Server Status
description: Determines whether the MID Server identified in the MID Server Host field of the integration's configuration is up and running. If the field is set to Any, the flow action verifies that any MID Server is up and running.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Get Running Processes Flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Check MID Server Status

Determines whether the MID Server identified in the **MID Server Host** field of the integration's configuration is up and running. If the field is set to **Any**, the flow action verifies that any MID Server is up and running.

The Check MID Server Status flow action can be used with any flow to check for the presence of a running MID Server within the flow.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Session status returned.|
|Failure|Session status error. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|capabilityExecutionId|The ID of the capability being executed.|
|flowName|The name of the flow being executed.|
|mid\_server\_host|The MID Server identified in the integration's configuration i|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|mid\_server\_live|Identifies whether the MID Server identified in the **MID Server Host** field of the integration's configuration is up and running. If the field is set to **Any**, the flow action verifies that any MID Server is up and running.|

**Parent Topic:**[Security Operations Carbon Black Integration - Get Running Processes Flow](../concept/secops-integration-cb-get-running-processes-workflow.md)

