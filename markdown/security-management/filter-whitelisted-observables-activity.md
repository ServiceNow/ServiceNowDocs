---
title: Filter Allowlisted Observables activity
description: The Filtered Allowlisted Observables workflow activity removes observables that can be ignored from the list of observables. This activity can accelerate the investigation and remediation process.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration Flow Actions, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Filter Allowlisted Observables activity

The Filtered Allowlisted Observables workflow activity removes observables that can be ignored from the list of observables. This activity can accelerate the investigation and remediation process.

The Filter Allowlisted Observables activity can be used with any workflow to filter observables prior to taking any action.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Filter list created.|
|Failure|An error occurred while attempting to filter the observables. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|observables|List of available observables.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|filteredObservables|Filtered observables.|

**Parent Topic:**[Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md)

