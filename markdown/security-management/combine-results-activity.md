---
title: Combine results activity
description: The Combine results workflow activity merges the results from third-party integrations to use in the workflow.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations System Command Integration- Get Running Processes flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Combine results activity

The Combine results workflow activity merges the results from third-party integrations to use in the workflow.

The Combine results activity can be used with any workflow to execute a MID server shell script in the workflow.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Results combined.|
|Failure|Combination failed. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|inputA|Result set A|
|inputB|Result set B|
|implementation\_id|Implementation identifier.|
|affected\_ci|Configuration item|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|result|Result set A or Result set B based on which one is filled.|

**Parent Topic:**[Security Operations System Command Integration- Get Running Processes flow](../../security-incident-response-orchestration/task/obtain-WMI-retrieval-workflow.md)

