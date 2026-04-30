---
title: Get Supported Security Capabilities activity
description: The Get Supported Capabilities workflow activity retrieves the name and number of integrations that are active and support the requested capability.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration Flow Actions, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get Supported Security Capabilities activity

The Get Supported Capabilities workflow activity retrieves the name and number of integrations that are active and support the requested capability.

The Get Supported Capabilities activity can be used with any workflow to determine which capabilities are supported.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Integration that supports the capability found.|
|Failure|An error occurred while attempting to find an active integration that supports the capability. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|capabilityName|Name of the capability.|
|taskId|System identifier for any task associated with the workflow.|
|domainId|System identifier for any domain associated with the workflow.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|supportedCapabilities|List of integrations that support the capability.|
|capabilityCount|Number of integrations that support the capability.|

**Parent Topic:**[Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md)

