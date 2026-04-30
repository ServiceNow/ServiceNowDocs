---
title: Template post-processing fields
description: From the Post Processing form in the activity designer you can define a script to run after the activity executes.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, Workflow Data Fabric]
---

# Template post-processing fields

From the **Post Processing** form in the activity designer you can define a script to run after the activity executes.

## Post-processing fields

To use the results returned by the activity, append the `executionResult.` prefix to these parameters.

|Field|Description|
|-----|-----------|
|Output process script|Script to run after the activity executes.|
|Variables|Input variables that are available to use as building blocks in the output process script. Click the arrow above the field to open the variables list. Click an item in the tree to add it to your script in the appropriate syntax. The list displays execution results and the variables you passed into the activity on the **Inputs** form. All activity variables added in the **Inputs** form are read-only and are expressed in the post-processing script with this syntax: `activityInput.variable`. For parameter descriptions, refer to the table in the post-processing parameters topic for this activity.|

## Logging

Activity designers can add logging to the post-processing script using the **ActivityLogger** API, which works for scoped or global applications. Logged data from the script appears in the **Workflow Log** related list in the context records for any workflow that uses the activity. The **Source** for these messages in the workflow log is **ACTIVITY**.

**Important:** To display the debug messages in the workflow log, set the **glide.workflow.log.debug** property to **true**.

The supported messages are:

-   `ActivityLogger.debug("Post Processing Log Message");`
-   `ActivityLogger.info ("Post Processing Log Message");`
-   `ActivityLogger.warn ("Post Processing Log Message");`
-   `ActivityLogger.error("Post Processing Log Message");`

![ActivityLogger API](../image/Post-ProcessLoggingAPI.png "ActivityLogger API")

**Parent Topic:**[Create custom activities using custom activity designer templates](../task/create-custom-activities.md)

