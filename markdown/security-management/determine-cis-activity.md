---
title: Capability - Determine CIs activity
description: The Capability - Determine CIs workflow activity determines which configuration items \(CIs\) to include in the workflow.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Capability - Determine CIs activity

The Capability - Determine CIs workflow activity determines which configuration items \(CIs\) to include in the workflow.

The Capability - Determine CIs activity can be used with any workflow to determine which CIs to include in the workflow.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Found configuration items.|
|Failure|No CIs found. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|task\_sys\_id|Task identifier \(maps security incident to CIs\).|
|cis\_affected|Configuration items.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|cis\_affected|Filtered CIs|
|task\_sys\_id|Task identifier \(maps security incident to CIs\).|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)

