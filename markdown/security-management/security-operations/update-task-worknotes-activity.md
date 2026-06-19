---
title: Update Task Worknotes activity
description: The Security Common Orchestration - Update Task Worknotes workflow activity updates the Activity section \(work notes\) of a task record. This is useful for logging information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/update-task-worknotes-activity.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Update Task Worknotes activity

The **Security Common Orchestration - Update Task Worknotes** workflow activity updates the **Activity** section \(work notes\) of a task record. This is useful for logging information.

The **Update Task Worknotes** activity can be used with any workflow to update the work notes of any task record.

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|task\_id \[string\]|The system identifier \(sys\_id\) of a task record.|
|content \[string\]|The data written into the work notes of a task.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|result \[string\]|Indicates whether the update was successful.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/common-wf-activities.md)

