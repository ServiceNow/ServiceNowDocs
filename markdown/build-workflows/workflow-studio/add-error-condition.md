---
title: Add error condition
description: Enable an action to return custom status information when specific conditions are met. Specify whether a flow considers your custom action status as an error or a successful run.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Action error evaluation, Create an action in Workflow Studio, Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Add error condition

Enable an action to return custom status information when specific conditions are met. Specify whether a flow considers your custom action status as an error or a successful run.

## Before you begin

-   Role required: flow\_designer, action\_designer, or admin
-   [Create an action in Workflow Studio](create-action.md)

## About this task

An action always returns an Action Status object. When an action runs, it evaluates the available error conditions from top to bottom looking for a possible match. An action returns the Action Status specified by the first matching error condition. If there is no matching error condition, the Action status is set to the Step Status of the last step run.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Actions** tab and select the custom action you want to edit.

3.  From the Action Outline, select **Error Evaluation**.

4.  Select **Add error condition** for each error condition you want to define.

    Workflow Studio adds an If block for configuration.

5.  Configure each error condition.

<table id="table_zp1_3mw_mpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

If

</td><td>

Description of your error condition. You can use this label to identify the error condition when the condition builder is not visible. Each error condition is equivalent to an else if flow logic block. Only one error condition can be true at a time.

</td></tr><tr><td>

Condition N

</td><td>

Condition builder to specify the matching criteria for the error condition. You can add conditions or condition sets to define the matching criteria.For each condition, select an action data pill to evaluate. For each data pill to evaluate, select an operator and matching value.

**Note:** Workflow Studio only displays the operators and values available for the type of data pill you selected.

</td></tr><tr><td>

Don't treat as error

</td><td>

Option to report the Action Status as an error or a success when returned to a flow.

</td></tr><tr><td>

Action Status Code

</td><td>

Integer value you want the action to return as part of the Action Status object. You can use this integer value as part of a [Flow error handler](../concept/flow-error-handler.md).

</td></tr><tr><td>

Action Status Message

</td><td>

String value you want the action to return as part of the Action Status object. You can use this string value as part of a [Flow error handler](../concept/flow-error-handler.md).

</td></tr></tbody>
</table>6.  Order error conditions from top to bottom in the order you want the action to evaluate them.

7.  Select **Save**.


## Result

Your custom action evaluates each error condition for matching conditions. The action returns the Action Status Code and Action Status Message for the first matching error condition. If there is no matching error condition, the Action status is set to the Step Status of the last step run.

**Parent Topic:**[Action error evaluation](../concept/action-error-evaluation.md)

