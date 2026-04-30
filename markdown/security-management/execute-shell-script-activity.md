---
title: Execute Shell Script activity
description: The Execute Shell Script workflow activity runs a MID server shell script within the workflow.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security Operations System Command Integration- Get Running Processes flow, Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Execute Shell Script activity

The Execute Shell Script workflow activity runs a MID server shell script within the workflow.

The Execute Shell Script activity can be used with any workflow to execute a MID server shell script in the workflow.

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
|target|IP or fully-qualified domain name \(FQDN\) of the target CI.|
|scriptValue|Script, as a string value, executed on a Unix system.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|response|Raw output. Running processes data.|

**Parent Topic:**[Security Operations System Command Integration- Get Running Processes flow](../../security-incident-response-orchestration/task/obtain-WMI-retrieval-workflow.md)

