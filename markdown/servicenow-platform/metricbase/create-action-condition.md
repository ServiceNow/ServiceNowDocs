---
title: Execute triggers conditionally
description: MetricBase triggers execute based on a single metric. Condition Scripts impose additional requirements that determine whether a trigger kicks off a flow.
locale: en-US
release: yokohama
product: MetricBase
classification: metricbase
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Trigger flows, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Execute triggers conditionally

MetricBase triggers execute based on a single metric. Condition Scripts impose additional requirements that determine whether a trigger kicks off a flow.

## Before you begin

Role required: admin

## About this task

Condition Scripts execute when conditions for a trigger are met but before the trigger executes a Workflow Studio flow. In that way, Condition Scripts can prevent triggers from executing flows even when trigger conditions are met. For example, data often fluctuates over time. Small fluctuations can cause unwanted, duplicate triggering events. A Condition Script can prevent that erroneous duplication.

Condition scripts are sometimes also referred to as moderator scripts.

Condition Scripts always return *true* \(trigger\) or *false* \(do not trigger\). To learn how to write these scripts, see [Scripting in ServiceNow Fundamentals](https://www.servicenow.com/services/training-and-certification/scripting-in-servicenow-training.html). To experiment with scripts, see [Get familiar with MetricBase APIs](metricbase-data-explorer.md).

## Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **MetricBase Triggers** &gt; **Trigger Condition Script**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the Condition Script.|
    |Application|Scope of the Condition Script. The value, **Global**, means that the action applies to all applications.|
    |Description|Explanation of what the Condition Script does. When does it return True or False?|
    |Script|Field to enter the JavaScript. Make it returns *true* to execute a flow.|

4.  Write the Condition Script.

    When writing a script, think about the conditional statements \(what cases it should execute for and what cases it shouldn’t\). If all evaluate *true*, the script returns *true* and the flow executes, otherwise it does not. The following example script triggers a flow when a drone is traveling too fast at a low altitude \(defined by level 1\). The example shows a typical approach to writing a condition script.

    1.  Get the trigger definition, passed in as a filter function parameter.

    2.  Get the record \(*current*\) that is causing the triggering event, passed in as a filter function parameter.

    3.  Get the time from the record that the trigger conditions were satisfied, passed in as a filter function parameter.

    4.  Get the trigger level, passed in as a filter function parameter.

    5.  Use these parameters to return *true* if the level 1 trigger conditions are met and *travel\_state* equals traveling or speeding.

        ```
        function filter(/*GlideRecord*/ triggerDefinition, /*GlideRecord*/ current, /*GlideDateTime*/ start, /*int*/ level) {
        	// retrieve current travel state of drone
        	var travel_state = String(current.travel_state);
        	
        	// the drone is traveling at a significant speed, and the altitude just went below the threshold 
        	if (((travel_state === 'traveling') || (travel_state === 'speeding')) && (level === 1)){
        		return true; //process this trigger
        	}
        	
        	return false; // don't process this trigger
        }
        
        ```

    **Note:** Condition Scripts must execute quickly.

5.  Select **Submit**.


## What to do next

Use Workflow Studio to [associate a flow with a trigger](assign-trigger-to-workflow.md). When configuring a flow, you can select a Condition Script you created.

![Add Condition Script to a trigger definition.](../image/condition-script-flow-designer.png "Add a Condition Script to a trigger definition in Workflow Studio")

You can also associate a condition script with a trigger flow in the MetricBase Trigger Flows \[sys\_flow\_metric\_trigger\] table. If you associate a condition script with a trigger flow here, it won’t appear in Workflow Studio, but it will still execute with the trigger.

![Associate a Condition Script in MetricBase trigger flows table](../image/condition-script-trigger-flow.png "Associate a Condition Script in MetricBase Trigger Flows")

