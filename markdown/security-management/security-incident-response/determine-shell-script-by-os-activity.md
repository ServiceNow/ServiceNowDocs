---
title: Determine Shell Script by OS Flow Action
description: The Determine Shell Script by OS flow action determines which operating system to use in the flow.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Incident Response - Get Running Services Flow, Security Incident Response Orchestration flows and actions, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Determine Shell Script by OS Flow Action

The Determine Shell Script by OS flow action determines which operating system to use in the flow.

The Determine Shell Script by OS flow action can be used with any flow to determine which shell script to run based on the operating system running on the system containing the configuration item.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Found operating system.|
|Failure|No operating system found. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

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

**Parent Topic:**[Security Incident Response - Get Running Services Flow](../../security-incident-response-orchestration/task/get-running-services-workflow.md)

