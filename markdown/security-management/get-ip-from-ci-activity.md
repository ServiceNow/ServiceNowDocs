---
title: Get IP from CI activity
description: The Get IP from CI flow activity gathers the IP address from configuration items \(CIs\) to use in the flow.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get IP from CI activity

The Get IP from CI flow activity gathers the IP address from configuration items \(CIs\) to use in the flow.

The Get IP from CI activity can be used with any flow to gather configuration item \(CI\) IP addresses to use in the flow.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Found IP addresses.|
|Failure|No IP addresses found. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|ci\_sys\_id|Configuration item identifier.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|ip\_addr|IP addresses.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)

