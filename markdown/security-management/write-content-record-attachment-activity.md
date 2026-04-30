---
title: Write content to record as attachment activity
description: This activity writes the content passed in from an input and creates a designated attachment to a given record.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Write content to record as attachment activity

This activity writes the content passed in from an input and creates a designated attachment to a given record.

The **Write content to record as attachment** activity can be used with any workflow to write content and attach it to a record.

## Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|tablename \[string\]|The table name for the record. This input field is mandatory.|
|sysid \[string\]|The system identifier \(sys\_id\) of a task record. This input field is mandatory.|
|payload|The plain text content to be written as an attachment. This input field is mandatory.|
|filename|The attachment file name.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|result \[string\]|Indicates whether the update was successful.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)

