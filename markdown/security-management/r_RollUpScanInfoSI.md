---
title: Roll up lookup info to security incident activity
description: The Roll up lookup info to security incident activity can be used with any workflow to gather information from a threat lookup and output a summary of the contents as well as the ID of the originating security incident in task work notes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Roll up lookup info to security incident activity

The **Roll up lookup info to security incident** activity can be used with any workflow to gather information from a threat lookup and output a summary of the contents as well as the ID of the originating security incident in task work notes.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Lookup report summary rolled up to security incident.|
|Failure|Originating task and lookup summary report are empty.|

|Variable|Description|
|--------|-----------|
|scanID\[string\]|Lookup identifier.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|siId\[string\]|Security incident identifier.|
|response \[string\]|Summary of lookup results including: IoC value, Result, Failure reason, lookup reference, and so on.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)

