---
title: Get Running Processes via PowerShell activity
description: The Get Sensor ID workflow activity gathers running processes using PowerShell to use in the workflow.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Operations System Command Integration- Get Running Processes flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get Running Processes via PowerShell activity

The Get Sensor ID workflow activity gathers running processes using PowerShell to use in the workflow.

The Get Running Processes via PowerShell workflow activity can be used with any workflow to retrieve processes to include in the workflow.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Found processes|
|Failure|No processes found. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|target|IP or fully-qualified domain name \(FQDN\) of the target CI.|
|processingScript|ECC script run on a Windows-based system.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|response|Raw output. Running processes data.|

**Parent Topic:**[Security Operations System Command Integration- Get Running Processes flow](../../security-incident-response-orchestration/task/obtain-WMI-retrieval-workflow.md)

