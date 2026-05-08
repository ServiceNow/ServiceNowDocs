---
title: Get Sensor ID Flow Action
description: The Get Sensor ID flow action gathers sensor identifiers to use in the flow.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Get Running Processes Flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get Sensor ID Flow Action

The Get Sensor ID flow action gathers sensor identifiers to use in the flow.

The Get Sensor ID flow action can be used with any flow to gather sensor information to use in the flow.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Found sensor identifiers.|
|Failure|No sensors found. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|api\_token|Carbon Black API key.|
|use\_mid\_server|Determines whether the REST activity uses the MID server to interact with Carbon Black or not.|
|endpoint\_base|Base URL of the Carbon Black API.|
|ci\_ip\_address|Configuration item IP address.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|status\_code|Determines if the request was successful. If not, displays an HTTP error code and message.|
|Array Element type|API variables.|
|sensor\_detail|Description of the Carbon Black sensor in JSON format.|

**Parent Topic:**[Security Operations Carbon Black Integration - Get Running Processes Flow](../concept/secops-integration-cb-get-running-processes-workflow.md)

**Parent Topic:**[Security Operations Carbon Black Integration - Isolate Host Flow](../task/secops-integration-cb-isolate-host-workflow.md)

