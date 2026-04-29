---
title: Check Session Status Flow Action
description: Determines the status of a Carbon Black session within the flow.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Get Running Processes Flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Check Session Status Flow Action

Determines the status of a Carbon Black session within the flow.

The Check Session Status flow action can be used with any flow to check Carbon Black session status within the flow .

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Session status returned.|
|Failure|Session status error. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|api\_token|Carbon Black API key.|
|endpoint\_base|Base URL of the Carbon Black API.|
|session\_id|Session identifier.|
|use\_mid\_server|Determines whether the REST activity uses the MID server to interact with Carbon Black or not.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|status\_code|Determines if the request was successful. If not, displays an HTTP error code and message.|
|output|Information on Carbon Black running processes.|

**Parent Topic:**[Security Operations Carbon Black Integration - Get Running Processes Flow](../concept/secops-integration-cb-get-running-processes-workflow.md)

