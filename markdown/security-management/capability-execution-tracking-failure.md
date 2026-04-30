---
title: Capability Execution Tracking- Failure Flow Action
description: The Capability Execution Tracking - Failure flow action records a failure to the audit record.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Capability Execution Tracking- Failure Flow Action

The Capability Execution Tracking - Failure flow action records a failure to the audit record.

The Capability Execution Tracking - Failure flow action can be used with any flow to record a failure condition.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|The audit record state is set to **Error** and a message indicating the error is recorded.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|capabilityExecutionId|System identifier for the audit record. This is the output from any of the Begin auditing activities.|
|errorMessage|Message indicating the reason for the failure.|
|flowName|Name of the flow. Supplied by the system.|

## Output variables

There are no output variables.

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](common-wf-activities.md)

