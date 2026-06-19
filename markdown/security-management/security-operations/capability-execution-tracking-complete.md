---
title: Capability Execution Tracking - Complete Flow Action
description: The Capability Execution Tracking - Complete flow action updates the audit record when the flow is complete.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/capability-execution-tracking-complete.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Get Running Processes Flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
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

**Parent Topic:**[Security Operations Carbon Black Integration - Get Running Processes Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/secops-integration-cb-get-running-processes-workflow.md)

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/common-wf-activities.md)

