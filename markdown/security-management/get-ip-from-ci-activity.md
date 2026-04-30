---
title: Get IP from CI Flow Action
description: The Get IP from CI flow action gathers the IP address from configuration items \(CIs\) to use in the flow.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration Flow Actions, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get IP from CI Flow Action

The Get IP from CI flow action gathers the IP address from configuration items \(CIs\) to use in the flow.

The Get IP from CI flow action can be used with any flow to gather configuration item \(CI\) IP addresses to use in the flow.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Found IP addresses.|
|Failure|No IP addresses found. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|ci\_sys\_id|Configuration item identifier.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|ip\_addr|IP addresses.|

**Parent Topic:**[Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md)

