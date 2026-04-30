---
title: Execution Tracking Begin \(Mail Search\) action
description: The Execution Tracking - Begin \(Mail Search\) capability execution action creates an execution tracking record and marks the record state as Started. This action is used by all capability and implementation flows to keep track of their state.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration - Email Search and Delete flow, Security Operations Integration- Email Search and Delete capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Execution Tracking Begin \(Mail Search\) action

The Execution Tracking - Begin \(Mail Search\) capability execution action creates an execution tracking record and marks the record state as Started. This action is used by all capability and implementation flows to keep track of their state.

## Results

Possible results for this action are:

|Result|Description|
|------|-----------|
|Success|Execution tracking record has been created.|
|Failure|Could not create execution tracking record.|

## Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|capabilityId|System identifier of the Integration Capability being executed.|
|implementationId|System identifier of the integration capability implementation being executed.|
|taskId|System identifier for any task associated with the flow.|
|flowContextId|System identifier of the associated flow context record. Supplied by the system.|
|flowName|Name of the flow. Supplied by the system.|
|parentCapabilityExcutionId|System identifier of the audit record that launched the implementation flow. Only required for Integration Capability implementation flows, such as Splunk, Elasticsearch.|
|emailsearchId|The sysid of the email search record in the Email Search \[sn\_sec\_cmn\_email\_search\] table.|

## Output variables

The output variables contain data that can be used in subsequent actions.

|Variable|Description|
|--------|-----------|
|capabilityExecutionId|System identifier of the execution tracking record.|

-   [Get Supported Security Capabilities action](get-supported-security-capabilities-activity.md)
-   [Capability Execution Tracking- No Impls action](execution-tracking-noimpls-activity.md)

**Parent Topic:**[Security Operations Integration - Email Search and Delete flow](../../security-operations-common/task/secops-integ-email-search-delete.md)

