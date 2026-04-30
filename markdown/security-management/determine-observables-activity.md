---
title: Determine Observables activity
description: The Determine Observables workflow activity determines which observable to include in the workflow
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration Flow Actions, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Determine Observables activity

The **Determine Observables** workflow activity determines which observable to include in the workflow

The **Determine Observables** activity can be used with any workflow to determine which observables to include in the workflow.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Found observables|
|Failure|No observables found. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|task\_sys\_id|Task identifier \(maps security incident to observables\).|
|observables|IP addresses, hash, URLs, domain names.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|observables|Filtered observables|

**Parent Topic:**[Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md)

