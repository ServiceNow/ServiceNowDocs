---
title: Create a custom action to throw an error
description: Create an action that intentionally throws an error to test flow error handling.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Flow error handler, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a custom action to throw an error

Create an action that intentionally throws an error to test flow error handling.

## Before you begin

Role required: flow\_designer, action\_designer, or admin

## About this task

This custom action throws an error when the action input value is set to 1. Any other input value allows the action to run without throwing an error. You can add this custom action to a flow to test flow error handling.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    The system displays the Workflow Studio landing page.

2.  Select **New** &gt; **Action**

    The system displays the Action Properties dialog.

3.  Enter these sample values.

    |Field|Value|
    |-----|-----|
    |Name|Throw an error|
    |Application|Global|
    |Accessible From|All application scopes|

4.  Select **Build Action**.

    The system displays the Workflow Studio interface.

5.  From the Action Outline, select **Inputs** &gt; **Create Input**

    The system displays a new action input.

6.  Configure the action input with these values.

    |Field|Value|
    |-----|-----|
    |Label|Error Code|
    |Type|Integer|
    |Mandatory|True|

7.  From the Action Outline, select **Add a new step**.

    The system displays a list of available steps.

8.  Select **Script step**.

9.  From the **Input Variables** section, select **Create Variable**.

10. Configure the variable with these values.

<table id="table_cvp_l5p_lhb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

code

 **Note:** Make sure that this value is lower case so that it matches the script call reference in the next step.

</td></tr><tr><td>

Value

</td><td>

Select the data pill \[action-&gt;Error Code\]

</td></tr></tbody>
</table>11. In **Script**, enter this JavaScript code.

    ```
    (function execute(inputs, outputs) {
      if (inputs.code == 1) {
          throw 'My custom error message'
          }
    })(inputs, outputs);
    ```

12. Select **Save**.

    ![Action outline and configuration of the sample action Throw an error.](../images/create-action-throw-error.png)

13. Select **Test**.

    The system displays the Test Action dialog.

14. Enter the following test value:

    |Input|Value|
    |-----|-----|
    |Error Code|1|

15. Select **Run Test**.

    The system runs the action with the test values provided.

16. Select **Your test has finished running. View the action execution details.**

    The system displays the action execution details.

17. Verify that the action ran the Script step and threw your custom error message.

    The **Action Status** object should list an error on line 3 and display the text of your custom error message.

    ![Action execution details for a test run of Throw an error.](../images/test-action-throw-error.png)

18. Close the action execution details.

19. Select **Cancel** to stop testing the action.

20. Select **Publish** to make your custom action available to your flows.


## Result

You have a custom action that throws an error when you set the action input **Error Code** to 1.

## What to do next

Add this action to a flow to test the contents of the Error Handler section.

**Parent Topic:**[Flow error handler](../concept/flow-error-handler.md)

