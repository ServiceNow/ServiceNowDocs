---
title: Configure the fields to appear on task cards or in the contextual side panel
description: Add fields to task cards or the contextual side panel so more information is available to dispatchers so they can make decisions faster.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Configure the fields to appear on task cards or in the contextual side panel

Add fields to task cards or the contextual side panel so more information is available to dispatchers so they can make decisions faster.

## Before you begin

Role required: admin, wm\_admin

## About this task

Task cards provide a brief summary of the work order task in the Dispatcher Workspace. By default, these details include the work order task number, short description, scheduled start, assignment group, location, and SLA value.

**Note:** If you add a field to the contextual side panel that contains date or time information, then it shows in the Planned/ Actual times section in the contextual side panel.

## Procedure

1.  Choose to update the data in the task cards or in the CSP.

    |Update|Navigation|
    |------|----------|
    |**To update the CSP**|Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Task Info Fields**.|
    |**To update the task card**|Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Task Panel Card Fields**.|

2.  Choose the following:

    -   To add a new field, select **New.**
    -   To edit an existing field, select the field you want to edit.
3.  Fill in the form.

    |Field|Description|
    |-----|-----------|
    |Field name|Field that to be displayed on the card or contextual side panel.|
    |Name|Name for the field.|
    |Always show|Option for determining whether the field displays on the task card or contextual side panel and can’t be removed by the dispatcher in the Dispatcher Workspace.|
    |Default show field|Option for determining whether the field shows by default in the task card or contextual side panel. The dispatcher won’t be able to remove this field in the Dispatcher Workspace.|
    |Order|The order number for the field. Fields assigned lower-order numbers appear higher in the order.|

4.  Select **Submit**.


