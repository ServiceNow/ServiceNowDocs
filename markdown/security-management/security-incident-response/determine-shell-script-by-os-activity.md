---
title: Determine Shell Script by OS activity
description: The Determine Shell Script by OS workflow activity determines which operating system to use in the workflow
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Get Running Services workflow, Security Incident Response Orchestration workflows and activities, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Determine Shell Script by OS activity

The Determine Shell Script by OS workflow activity determines which operating system to use in the workflow

The Determine Shell Script by OS activity can be used with any workflow to determine which shell script to run based on the operating system running on the system containing the configuration item.

## Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|Found operating system.|
|Failure|No operating system found. More error information is available in the activity output error.|

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|ciSysId|System identifier of the configuration item.|
|processType|Internal identifier that defines which script to pull from the table.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|processScript|ECC agent that gathers the running process.|
|executionTemplate|Determines whether the script is run through a probe or using PowerShell.|
|enrichmentMappingId|System identifier of the enrichment mapping used to transform the response data.|

**Parent Topic:**[Security Incident Response - Get Running Services workflow](../../security-incident-response-orchestration/task/get-running-services-workflow.md)

