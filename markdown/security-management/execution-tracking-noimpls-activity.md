---
title: Capability Execution Tracking- No Impls action
description: The Capability Execution Tracking - No Impls flow action creates an error record when no integration capability implementation is found.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Capability Execution Tracking- No Impls action

The Capability Execution Tracking - No Impls flow action creates an error record when no integration capability implementation is found.

The Capability Execution Tracking- No Impls action can be used with any abstract integration capability flow to handle the error condition when no configured capability implementation is available.

## Results

Possible results for this action are:

|Result|Description|
|------|-----------|
|Success|The execution tracking record state is set to **Error** and a message indicating the error is recorded.|

## Input variables

Input variables determine the initial behavior of the action.

|Variable|Description|
|--------|-----------|
|capabilityExecutionId|System identifier for the audit record. Output from the action used to begin execution tracking.|
|flowName|Name of the flow. Supplied by the system.|

## Output variables

There are no output variables.

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)

