---
title: Get IP from CI activity
description: This workflow activity determines the IPV4 address associated with a configuration item \(CI\).
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get IP from CI activity

This workflow activity determines the IPV4 address associated with a configuration item \(CI\).

The **Get IP from CI** activity can be used with any workflow to retrieve the IPv4 address of a CI.

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|ci\_sys\_id \[string\]|Configuration item system identifier|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|ip\_addr \[string\]|IPv4 address. If the IP address cannot be determined, this value is empty.|

## Exit Conditions

Possible results for this activity are:

|Condition|Description|
|---------|-----------|
|Success|An IPv4 address was returned.|
|Failure|An IPv4 address could not be determined.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)

