---
title: Get Supported Security Capabilities action
description: The Get Supported Capabilities flow action retrieves the name and number of integrations that are active and support the requested capability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/get-supported-security-capabilities-activity.html
release: australia
product: Security Operations
classification: security-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get Supported Security Capabilities action

The Get Supported Capabilities flow action retrieves the name and number of integrations that are active and support the requested capability.

The Get Supported Capabilities action can be used with any flow to determine which capabilities are supported.

## Results

Possible results for this action are:

|Result|Description|
|------|-----------|
|Success|Integration that supports the capability found.|
|Failure|An error occurred while attempting to find an active integration that supports the capability. More error information is available in the action output error.|

## Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|capabilityName|Name of the capability.|
|taskId|System identifier for any task associated with the flow.|
|domainId|System identifier for any domain associated with the flow.|

## Output variables

The output variables contain data that can be used in subsequent actions.

|Variable|Description|
|--------|-----------|
|supportedCapabilities|List of integrations that support the capability.|
|capabilityCount|Number of integrations that support the capability.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/common-wf-activities.md)

