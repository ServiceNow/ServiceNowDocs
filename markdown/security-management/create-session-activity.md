---
title: Create Session Flow Action
description: The Create Session flow action establishes a Carbon Black session to use in the flow.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Get Running Processes Flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Create Session Flow Action

The Create Session flow action establishes a Carbon Black session to use in the flow.

The Create Session flow action can be used with any flow to create a Carbon Black session within the flow.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Session created.|
|Failure|Session not created. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|api\_token|Carbon Black API key.|
|endpoint\_base|Base URL of the Carbon Black API.|
|sensor\_id|Sensor identifier.|
|use\_mid\_server|Determines whether the REST activity uses the MID server to interact with Carbon Black or not.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|status\_code|Determines if the request was successful. If not, displays an HTTP error code and message.|
|output|API variables|

**Parent Topic:**[Security Operations Carbon Black Integration - Get Running Processes Flow](../concept/secops-integration-cb-get-running-processes-workflow.md)

