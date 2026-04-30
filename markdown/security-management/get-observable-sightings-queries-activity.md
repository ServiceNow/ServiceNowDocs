---
title: Get Observable Sightings Queries activity
description: The Get Observable Sightings Queries workflow activity retrieves queries from the integration configuration.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration - Sightings Search Flow, Create sightings search configuration records, Security Operations Integration- Sightings Search capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get Observable Sightings Queries activity

The **Get Observable Sightings Queries** workflow activity retrieves queries from the integration configuration.

The **Get Observable Sightings Queries** activity can be used with any workflow to get queries to send to the specified implementation using the **Parallel Flow Launcher**.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Queries found.|
|Failure|An error occurred while attempting to get queries. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|observables|List of filtered observables.|
|capabilities|List of supported capabilities.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|queries|Search string.|
|queryCount|Number of queries to run.|

**Parent Topic:**[Security Operations Integration - Sightings Search Flow](../task/secops-integration-sightings-search-workflow.md)

