---
title: Turnstile workflow activity
description: The Turnstile activity limits how many times a workflow can pass through the same point.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Turnstile workflow activity

The **Turnstile** activity limits how many times a workflow can pass through the same point.

Use this activity to prevent infinite loops. This activity is useful alongside the [Rollback To workflow activity](https://www.servicenow.com/docs/access?context=r_RollbackTo&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) activity.

## Results

You can assign a result value using the *activity.result* variable from within a script field of the activity. By default, the activity script evaluates if the activity should continue to iterate or stop.

|Result|Description|
|------|-----------|
|Continue|The **Allowed iterations** value is greater than the number of times the workflow accessed this activity.|
|Cancel|The workflow accessed this activity more times than the **Allowed iterations** value.|

## Input variables

Input variables determine the initial behavior of the activity.

|Field|Description|
|-----|-----------|
|Allowed iterations|Number of times the workflow can pass through this activity before the turnstile ends the loop.|

## Conditions

The conditions determine which transition comes after this activity.

|Field|Description|
|-----|-----------|
|Continue|If the workflow has returned to this point an amount of times less than the allowed iteration.|
|Cancel|If the workflow has returned to this point an amount of times more than the allowed iteration.|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine knows to start the onExecute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is triggered.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

**Parent Topic:**[Utility workflow activities](../concept/c_UtilityActivities.md)

