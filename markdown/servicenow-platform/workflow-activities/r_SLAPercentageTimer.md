---
title: SLA Percentage Timer workflow activity
description: The SLA Percentage Timer activity pauses the workflow for a duration equal to a percentage of an SLA.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Timer workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# SLA Percentage Timer workflow activity

The **SLA Percentage Timer** activity pauses the workflow for a duration equal to a percentage of an SLA.

A workflow must run on the Task SLA table to use this activity.

**Note:** Timer activities run as the System user because the system scheduler advances the workflow.

## Results

|Result|Description|
|------|-----------|
|Complete|The activity successfully reached the specified duration|
|Cancelled|The activity or workflow was canceled before the timer reached the specified duration|

## Input variables

Input variables determine the initial behavior of the activity.

|Field|Description|
|-----|-----------|
|Percentage|The duration to pause the workflow for, as a percentage of the current SLA|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The activity is in this state very briefly while initializing, after which it immediately changes to **Waiting**.|
|Waiting|The workflow engine waits until the SLA reaches the specified percentage. The engine then transitions the workflow to the next activity.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

