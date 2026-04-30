---
title: Execution Tracking Begin \(Mail Search\) activity
description: The Execution Tracking - Begin \(Mail Search\) capability execution activity creates an execution tracking record and marks the record state as Started. This activity is used by all capability and implementation workflows to keep track of their state.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration - Email Search and Delete flow, Security Operations Integration- Email Search and Delete capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Execution Tracking Begin \(Mail Search\) activity

The Execution Tracking - Begin \(Mail Search\) capability execution activity creates an execution tracking record and marks the record state as Started. This activity is used by all capability and implementation workflows to keep track of their state.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Execution tracking record has been created.|
|Failure|Could not create execution tracking record.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|capabilityId|System identifier of the Integration Capability being executed.|
|implementationId|System identifier of the integration capability implementation being executed.|
|taskId|System identifier for any task associated with the workflow.|
|workflowContextId|System identifier of the associated workflow context record. Supplied by the system.|
|workflowName|Name of the workflow. Supplied by the system.|
|parentCapabilityExcutionId|System identifier of the audit record that launched the implementation workflow. Only required for Integration Capability implementation workflows, such as Splunk, Elasticsearch.|
|emailsearchId|The sysid of the email search record in the Email Search \[sn\_sec\_cmn\_email\_search\] table.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|capabilityExecutionId|System identifier of the execution tracking record.|

-   [Get Supported Security Capabilities activity](get-supported-security-capabilities-activity.md)
-   [Capability Execution Tracking- No Impls activity](execution-tracking-noimpls-activity.md)

**Parent Topic:**[Security Operations Integration - Email Search and Delete flow](../../security-operations-common/task/secops-integ-email-search-delete.md)

