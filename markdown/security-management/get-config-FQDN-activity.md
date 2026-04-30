---
title: Get Configuration Item FQDN Flow Action
description: The Security Common Orchestration Get Configuration Item FQDN flow action retrieves the fully qualified domain name \(FQDN\) of a configuration item. This flow action can accelerate the investigation and remediation process.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get Configuration Item FQDN Flow Action

The **Security Common Orchestration** &gt; **Get Configuration Item FQDN** flow action retrieves the fully qualified domain name \(FQDN\) of a configuration item. This flow action can accelerate the investigation and remediation process.

The Get Configuration Item FQDN flow action can be used with any flow to retrieve the fully qualified domain name \(FQDN\) of a configuration item.

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|cmdb\_ci.id \[string\]|The system identifier \(sys\_id\) of a configuration item record.|

## Output variables

The output variables contain data that can be used in subsequent actions.

|Variable|Description|
|--------|-----------|
|fqdn \[string\]|The fully qualified domain name \(FQDN\) of the configuration item.|

## Additional Notes

The fqdn field on the configuration item must be populated.

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)

