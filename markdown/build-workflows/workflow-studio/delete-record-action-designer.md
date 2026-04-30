---
title: Delete Record step
description: Deletes a record on any table.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Delete Record step

Deletes a record on any table.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

|Field|Description|
|-----|-----------|
|Record|The record to be deleted. Drag-and-drop a record data pill or use the data pill picker to select a record.|
|Table|Read-only. Set to the table associated with the record.|

## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

