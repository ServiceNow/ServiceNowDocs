---
title: Activity designer template pre-processing fields
description: Use the Pre Processing form of the activity designer to define a script to run before the activity executes.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ActivityLogger, ActivityLogger.info, ActivityLogger.debug, ActivityLogger.warn, ActivityLogger.error, activity logger, activity logging]
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, Workflow Data Fabric]
---

# Activity designer template pre-processing fields

Use the **Pre Processing** form of the activity designer to define a script to run before the activity executes.

## Pre-processing fields

|Field|Description|
|-----|-----------|
|Input process script|Script to run before the activity executes.|
|Variables|Input variables that are available to use as building blocks in the input process script. Click the arrow above the field to open the variables list. Click an item in the tree to add it to your script in the appropriate syntax. The list displays execution parameters and input variables you passed into the activity on the **Inputs** form. All activity variables added in the **Inputs** form are read-only and are expressed in the pre-processing script with this syntax: `activityInput.variable`. Before the activity executes and makes a call to the service or host, you can override the effective execution value of this variable by assigning values to the `executionParam.variable_name` execution parameter. Refer to the specific execution parameters for your template.|

## Logging

Activity designers can add logging to the pre-processing using the **ActivityLogger** API, which works for scoped or global applications. Logged data from the script appears in the **Workflow Log** related list in the context records for any workflow that uses the activity. The **Source** for these messages in the workflow log is **ACTIVITY**.

**Important:** To display the debug messages in the workflow log, set the **glide.workflow.log.debug** property to **true**.

The supported messages are:

-   `ActivityLogger.debug("Pre Processing Log Message");`
-   `ActivityLogger.info ("Pre Processing Log Message");`
-   `ActivityLogger.warn ("Pre Processing Log Message");`
-   `ActivityLogger.error("Pre Processing Log Message");`

![ActivityLogger API](../image/Pre-ProcessLoggingAPI.png "ActivityLogger API")

**Parent Topic:**[Create custom activities using custom activity designer templates](../task/create-custom-activities.md)

