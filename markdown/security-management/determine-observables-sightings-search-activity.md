---
title: Sightings Search - Determine Observables activity
description: The Sightings Search - Determine Observables workflow activity determines which observables to include in the workflow.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration - Sightings Search Flow, Create sightings search configuration records, Security Operations Integration- Sightings Search capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Sightings Search - Determine Observables activity

The **Sightings Search - Determine Observables** workflow activity determines which observables to include in the workflow.

The **Sightings Search - Determine Observables** activity can be used with any workflow to determine which observables to include in the workflow.

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
|workflow\_current\_sys\_id|System identifier of the current record. \(Used only if `task_sys_id`, observable inputs are not available\).|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|observables|Filtered observables|

**Parent Topic:**[Security Operations Integration - Sightings Search Flow](../task/secops-integration-sightings-search-workflow.md)

