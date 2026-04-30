---
title: Create a run script activity
description: Create an activity that runs any script.Use the Run Script custom template Script form to enter a script to call and use with other activities.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a run script activity

Create an activity that runs any script.

## Before you begin

Role required: activity\_creator or workflow\_admin

## Procedure

1.  Create a [custom activity](https://www.servicenow.com/docs/access?context=create-custom-activities&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    This action creates a custom activity using a template.

2.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the Run Script Execution Command:

    Create a script for this activity to execute.

    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](automap-output-variable-inputs.md).


## What to do next

-   Use [auto-mapping](automap-output-variable-inputs.md) to generate outputs and parsing rules
-   If you do not use auto-mapping, you can manually [create output variables](t_CreateAnOutputVariable.md#) and [create parsing rules](t_CreateAParsingRule.md#)

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

## Run Script template processing script

Use the Run Script custom template Script form to enter a script to call and use with other activities.

|Field|Description|
|-----|-----------|
|Processing script|Script that the activity runs.|
|Variables|Input variables that are available to use as building blocks in the input process script. Click the arrow above the field to open the variables list. Click an item in the tree to add it to your script in the appropriate syntax. The list displays input variables you passed into the activity on the **Inputs** form. All activity variables added in the **Inputs** form are read-only and are expressed in the processing script with this syntax: `activityInput.variable`.|

