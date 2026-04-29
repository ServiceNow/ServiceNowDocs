---
title: Map Processes Data Flow Action
description: The Map Processes Data flow action maps Carbon Black process data within the flow.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations Carbon Black Integration - Get Running Processes Flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Map Processes Data Flow Action

The Map Processes Data flow action maps Carbon Black process data within the flow.

The Map Processes Data flow action can be used with any flow to map Carbon Black processes.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Processes mapped|
|Failure|Processes not mapped. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|affected\_ci|Configuration item affected.|
|implementation\_id|Implementation identifier.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|output|Formatted return data on running processes used by the abstract workflow.|
|processes|List of processes in an array.|

**Parent Topic:**[Security Operations Carbon Black Integration - Get Running Processes Flow](../concept/secops-integration-cb-get-running-processes-workflow.md)

