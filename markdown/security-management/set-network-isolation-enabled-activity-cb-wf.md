---
title: Set Network Isolation Enabled Flow Action
description: The Set Network Isolation Enabled flow action enables network isolation.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Isolate Host Flow, Security Operations Integration- Isolate Host capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Set Network Isolation Enabled Flow Action

The Set Network Isolation Enabled flow action enables network isolation.

The Set Network Isolation Enabled flow action can be used with any flow to enable network isolation.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Network isolation enabled.|
|Failure|Network isolation cannot be enabled. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

<table id="table_pgm_tfy_jr"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sensor\_detail

</td><td>

Description of the Carbon Black sensor in JSON format.

</td></tr><tr><td>

disable

</td><td>

Determines whether the host is isolated or removes host isolation. -   True = disable isolation
-   False = isolation remains enabled

</td></tr></tbody>
</table>## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|sensor\_detail|Description of the Carbon Black sensor in JSON format.|

**Parent Topic:**[Security Operations Carbon Black Integration - Isolate Host Flow](../task/secops-integration-cb-isolate-host-workflow.md)

