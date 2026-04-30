---
title: Update Sensor activity
description: The Update Sensor workflow activity updates the sensor to isolate hosts or endpoints.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Isolate Host Flow, Security Operations Integration- Isolate Host capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Update Sensor activity

The Update Sensor workflow activity updates the sensor to isolate hosts or endpoints.

The Update Sensor activity can be used with any workflow to isolate hosts or endpoints.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Updated sensor.|
|Failure|Unable to update sensor. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|api\_token|Carbon Black API key.|
|use\_mid\_server|Determines whether the REST activity uses the MID server to interact with Carbon Black or not.|
|endpoint\_base|Base URL of the Carbon Black API.|
|sensor\_id|Sensor identifier.|
|sensor\_detail|Description of the Carbon Black sensor in JSON format.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|status\_code|Determines if the request was successful. If not, displays an HTTP error code and message.|

**Parent Topic:**[Security Operations Carbon Black Integration - Isolate Host Flow](../task/secops-integration-cb-isolate-host-workflow.md)

