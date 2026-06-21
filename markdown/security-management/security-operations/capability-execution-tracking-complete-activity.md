---
title: Capability Execution Tracking - Complete Flow Action
description: The Capability Execution Tracking - Complete flow action updates the audit record when the flow is complete.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/security-operations/capability-execution-tracking-complete-activity.html
release: xanadu
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration Flow Actions, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Capability Execution Tracking - Complete Flow Action

The Capability Execution Tracking - Complete flow action updates the audit record when the flow is complete.

The Capability Execution Tracking - Complete flow action can be used with any flow to record the completion of the flow.

**Note:** The **Return Value** array from the **Parallel Launcher** core flow action contains an array of results from all integration flows run and prompts the successful completion of execution tracking.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|The audit record state is updated to **Complete**.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|capabilityExecutionId|System identifier for the audit record. This field was the output from any of the Begin auditing activities.|
|flowName|Name of the flow. Supplied by the system.|
|message|Completion message.|

## Output variables

There are no output variables.

**Parent Topic:**[Common Security Operations integration flows and orchestration Flow Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-operations/common-wf-activities.md)

