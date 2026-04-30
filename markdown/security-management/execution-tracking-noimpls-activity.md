---
title: Capability Execution Tracking- No Impls activity
description: The Capability Execution Tracking - No Impls workflow activity creates an error record when no integration capability implementation is found.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration Flow Actions, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Capability Execution Tracking- No Impls activity

The Capability Execution Tracking - No Impls workflow activity creates an error record when no integration capability implementation is found.

The Capability Execution Tracking- No Impls activity can be used with any abstract integration capability workflow to handle the error condition when no configured capability implementation is available.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|The execution tracking record state is set to **Error** and a message indicating the error is recorded.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|capabilityExecutionId|System identifier for the audit record. Output from the activity used to begin execution tracking.|
|workflowName|Name of the workflow. Supplied by the system.|

## Output variables

There are no output variables.

**Parent Topic:**[Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md)

