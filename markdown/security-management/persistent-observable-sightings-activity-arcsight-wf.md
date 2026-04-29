---
title: Persistent Observable Sightings activity
description: The Persistent Observable Sightings workflow activity retrieves observables from the third-party integration.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration - Sightings Search Flow, Create sightings search configuration records, Security Operations Integration- Sightings Search capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Persistent Observable Sightings activity

The **Persistent Observable Sightings** workflow activity retrieves observables from the third-party integration.

The **Persistent Observable Sightings** activity can be used with any workflow to record observables found in the third-party integration.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Observables retrieved.|
|Failure|An error occurred while attempting to gather observables. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|sightingsResponse| |
|taskId|Task identifier.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|response| |

**Parent Topic:**[Security Operations Integration - Sightings Search Flow](../task/secops-integration-sightings-search-workflow.md)

