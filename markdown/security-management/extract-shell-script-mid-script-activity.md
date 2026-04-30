---
title: Extract Shell Script from MID Script activity
description: The Extract Shell Script from MID script workflow activity pulls a MID server shell script to use with in the workflow.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations System Command Integration- Get Running Processes flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Extract Shell Script from MID Script activity

The Extract Shell Script from MID script workflow activity pulls a MID server shell script to use with in the workflow.

The Extract Shell Script from MID Script activity can be used with any workflow to extract a MID server shell script to include in the workflow.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Found shell script|
|Failure|No shell script found. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|sysId|System identifier|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|scriptValue|Script, as a string value, executed on a Unix system.|

**Parent Topic:**[Security Operations System Command Integration- Get Running Processes flow](../../security-incident-response-orchestration/task/obtain-WMI-retrieval-workflow.md)

