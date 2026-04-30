---
title: Getting started with actions
description: Transform the Ask for Approval action into a reusable action that always requires manager approval.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Building actions, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Getting started with actions

Transform the Ask for Approval action into a reusable action that always requires manager approval.

Demonstrates creating actions within a flow in the Flow Designer, and testing a flow.

## Before you begin

Role required: admin

**Note:** While Workflow Studio is designed to use the action\_designer and delegated\_developer roles in most scenarios, this tutorial uses the admin role to illustrate functionality without requiring additional roles to set up records and approve requests.

Complete the steps in [Getting started with flows](getting-started-flow.md). This tutorial replaces the Ask for Approval action in the Expense Approval flow.

## About this task

Actions are made up of:

-   Inputs: Data variables used in your action.
-   Steps: Operations on the inputs or results from a prior step that generate data that can be used in later steps.
-   Outputs: Data variables that represent the results of the action. These results are available to other actions in a flow.

Unlike the core Ask for Approval action where flow designers must manually configure the approval rules, this custom action always uses the same approval rules when added to a flow. You might create a reusable action if your flow designers often use an action with the same configuration. For example, if your flow designers always use the request manager approval and due date options, this action automatically uses them and therefore requires less flow configuration.

## Procedure

1.  Open the Expenses Getting Started application in Studio.

    Alternatively, you can navigate to **Process Automation** &gt; **Flow Designer** and select **New Action** to access Workflow Studio in the platform. In the Action Properties, select your scoped application in the **Application** field.

2.  Create an action.

    1.  Select **Create Application File**.

    2.  Under Workflow Studio, select Action and select **Create**.

    3.  In the **Name** field, enter `Ask for Manager Approval`.

    4.  In the **Description** field, enter `Approve or reject a request based on manager approval or rejection. Allow manual approvers to be added`.

    5.  Select **Submit**.

        An Ask for Manager Approval action is created in the Expenses Getting Started scope.

3.  Define the inputs in the Ask for Manager Approval action.

    1.  Select **+ Create Input** and add the following values.

        -   Name: **Request**
        -   Type: **Reference**
        -   Reference Table: **Expenses \[x\_expenses\_getting\_expenses\]**
        ![Add a Request input to the action.](../images/action-input.png)

    This input enables you to reference any field or record from the Expenses table. Use the data pills on the right-hand side to add the record or its fields to action steps.

4.  Add an Ask for Approval step.

    1.  Select the **+** underneath Inputs in the Action Outline.

    2.  Select **Ask for Approval**.

    3.  Complete the fields in the Ask for Approval step.

        -   Record: Under the **Input Variables** category, drag the **\[Request\]** data pill from the right-hand pane.
        -   Table: Set to **Expenses \[x\_expenses\_getting\_expenses\]**.
        -   Approval Field: Set to **Approval**.
        -   Journal Field: Set to **Approval history**.
        ![Add Ask for Approval step.](../images/ask-for-approve-getting-started-actions.png)

    4.  Define rules in the Ask for Approval step.

        You can use the data pill picker, or drag the data pills from the right-hand pane to select the data you need.

        -   **\[Approve\]** when **\[Anyone approves\]** from the field **\[action-&gt;Request-&gt;Requested for-&gt;Manager\]**, **\[OR\]**
        -   **\[Anyone approves\]** from the field **\[Manual User\(s\)\]**.
        Select **Add another OR rule set** to define rejection rules:

        -   **\[Reject\]** when **\[Anyone rejects\]** from the field **\[action-&gt;Request-&gt;Requested for-&gt;Manager\]**, **\[OR\]**
        -   **\[Anyone rejects\]** from the field **\[Manual User\(s\)\]**.
        ![Add rules to the Ask for Approval step.](../images/action-rules.png)

    5.  Define a due date in the Ask for Approval step.

        -   **\[Approve\]** if pending by **\[Relative date\]** **\[1\]** **\[Days\]** from **\[action-&gt;Request-&gt;Created\]**.
        -   Days schedule **\[8-5 weekdays excluding holidays\]**.
        This due date automatically approves all requests that haven’t been approved or denied within one day from when the request was created.

        ![Add a Due Date to the Ask for Approval step.](../images/action-due-date.png)

5.  Define the outputs in the Ask for Manager Approval action.

    Adding an output makes data available to a flow. For example, this action outputs the approval state of the record.

    1.  Select **+ Create Outputs** and add the following values.

        -   Name: **Approval state**
        -   Value: In the right-hand pane, expand the **Ask for Approval step** category and drag the **\[Approval State\]** data pill.
        ![Create outputs to the action.](../images/action-outputs.png)

    2.  Select **Save**.

6.  Add a custom icon for your application that displays in Workflow Studio.

    All actions in the application scope use the custom icon.

    1.  In Studio, navigate to **File** &gt; **Settings**.

        The application settings open.

    2.  In the **Logo** field, select **Click to add...**.

    3.  Upload an icon to use with your reusable actions.

7.  Test the reusable action within your flow.

    1.  Return to the Expense Approval flow.

    2.  Remove the 2.1 Ask for Approval action from the flow.

        This action is replaced by the reusable Ask for Manager Approval action.

    3.  Set **Show draft actions** to true.

    4.  Add the Ask for Manager Approval action to your flow.

    5.  In the right-hand pane, expand the **Trigger - Record Created** category and drag the **\[Expenses Record\]** data pill into the **Request \[Expenses\]** field.

    ![Add the action to the flow and enter an input.](../images/action-added-to-flow.png)

8.  Select **Save**.

9.  Test the flow using a record with an amount below the designated limit.

    1.  From the flow, select **Test**.

        The Test flow modal appears.

    2.  In the **Record** field, select a record that you created in earlier steps, has a value under the 100.00 limit in the **Amount** field, and you haven't used to run tests.

    3.  Select **Run Test**.

    4.  After the flow executes, select **Flow has been executed. To view the flow, click here**.

        The Execution Details open.

    Because the amount is less than 100.00, the first condition is met and the request is approved. The Else condition isn’t evaluated.

    ![Test result for first condition evaluated.](../images/action-test-1.png)

10. Test a record with an amount over the designated limit and verify that you have not already run a test on the test record.

    Because the amount is over the designated limit, the second condition is evaluated.

    ![Test result for second condition evaluated.](../images/test-action-waiting.png)

11. Approve the request.

    1.  Navigate to the test record and change the value of the **State** field in the Approvers related list to **Approved**.

    2.  Navigate back to the flow execution details and refresh the browser.

        Because the request is approved, the flow completes.

        ![Execution details showing a completed approval.](../images/action-test-completed.png)

12. Navigate to the Ask for Manager Approval action and select **Publish**.

    Publishing an action enables you to activate any flow that uses it.

13. Navigate to the flow and set **Show draft actions** to false.

14. Select **Activate**.

    Activating a flow sets it to run every time the trigger conditions are met.


## Result

The Expense Approval flow runs every time a record is created in the Expenses table. Now that the flow is activated and working as expected, you can publish it to the application repository and deploy it to other instances.

**Parent Topic:**[Building actions](../concept/actions.md)

