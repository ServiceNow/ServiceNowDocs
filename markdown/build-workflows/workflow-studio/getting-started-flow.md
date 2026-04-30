---
title: Getting started with flows
description: Create a sample flow with a trigger and base system actions that requires an approval.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Getting started with flows

Create a sample flow with a trigger and base system actions that requires an approval.

Introduction to spokes, setting up an application, granting access, creating a flow, setting up an ATF test, and publishing the flow.

Watch this 11-minute video for an introduction to using Workflow Studio.

## Before you begin

Role required: admin

**Note:** While Workflow Studio is designed to use the flow\_designer and delegated\_developer roles in most scenarios, this tutorial uses the admin role to illustrate functionality without requiring additional roles to set up records and approve requests.

The ITSM application is required to access the Task table.

## About this task

A flow can include these components:

-   Trigger: An activity that initiates the flow, such as a record created in a specified table or a scheduled job.
-   Conditions: Statements that determine when or how an action runs. For example, run an action only if a field is over a certain value.
-   Actions: Operations executed by the system, such as a field value updated, approval requested, or a value logged.

To understand basic flows, create an expense approval flow. This flow:

1.  Runs when an Expenses record is created.
2.  Uses the total amount to determine which action to run.
3.  Approves the request if it is under the specified dollar amount.
4.  Requires manager approval if it is over a specified dollar amount. Another approver can be manually added.

## Procedure

1.  Create a custom application for the flow. Creating flows and actions within an application enables you to publish flows and actions to an application repository and deploy them on other instances. While this example does not use delegated development, you can optionally delegate action and flow designer development by assigning developers to the application.

    1.  Navigate to **System Applications** &gt; **Studio**.

    2.  Create a custom application called **Expenses Getting Started**.

2.  In Studio, create an Expenses table.

    1.  Click **Create Application File**.

    2.  Under Data Model, select Table and click **Create**.

        A Table form opens.

    3.  Complete the form with the following values.

        -   Label: **Expenses**
        -   Extends table: **Task**
    4.  Save the form.

    5.  Add three additional columns to the table.

        |Column label|Type|Reference|
        |------------|----|---------|
        |Amount|Floating point number|None|
        |Destination|String|None|
        |Requested for|Reference|User \[sys\_user\]|

3.  Add four records to the Expenses table to use in Workflow Studio tests.

    When you test your flow in later steps, you can specify which record is used as the trigger, enabling you to test specific record values.

    1.  On the Expenses table record, click the **Show list** related link.

    2.  Click **New**.

    3.  Configure the form to add the **Amount**, **Destination**, and **Requested for** fields, and the **Approvers** related list.

    4.  Complete the **Destination** and **Requested for** fields.

        Make sure that the user in the **Requested for** field in the test record has a manager assigned in the system. If the user in the test record does not have a manager, configure the User form to add the **Manager** field, and assign a manager to the user.

    5.  In the **Amount** field, add a value under 100.00.

    6.  Submit the form.

    7.  Add another record to the table with an amount under 100.00.

    8.  Add two more records to the table with a value over 100.00 in the **Amount** field.

4.  In Studio, create a new flow.

    1.  Click **Create Application File**.

    2.  Under Workflow Studio, select Flow and click **Create**.

    3.  Select the **Flow** option, click **Next**.

    4.  In the **Flow Name** field, enter `Expense Approval`.

    5.  Click **Submit**.

        An Expense Approval flow is created in the Expenses Getting Started scope.

5.  Create a trigger that runs the flow when a record is created in the Expenses table.

    -   Trigger: **Created**
    -   Table: **Expenses \[x\_expenses\_getting\_expenses\]**
    ![Record trigger in a flow.](../images/get-start-trigger.png)

6.  Add an if condition to the flow.

    1.  Select **Flow Logic** &gt; **If**.

    2.  In the right-hand pane, expand the **Trigger - Record Created** category and the **\[Expenses Record\]** pill.

    3.  Drag-and-drop the **\[Amount\]** pill into **Condition 1**.

        A data pill represents the value of a record or a field at a particular stage in your flow. Dragging the **\[Amount\]** data pill from the trigger populates the condition with the value of the field in the triggering record.

    4.  Set Condition 1 to **\[Trigger-&gt;Expenses Record-&gt;Amount\]** **\[less than\]** **\[100.00\]**.

    ![Example if condition in a flow.](../images/if-condition-flow-getting-started.png)

7.  Underneath action 1, click **+** to add an action that runs when the If condition is met.

    ![Icon to add an action or flow logic within an If condition.](../images/sub-action-plus-sign.png)

8.  Create an Update Record action that approves the request.

    -   Action: **Update Record**
    -   Record: Expand the **Trigger - Record Created** category and drag the **\[Expenses Record\]** data pill from the right-hand pane.
    -   Table: Set to **Expenses \[x\_expenses\_getting\_expenses\]**.
    -   Fields:
        -   Approval: **Approved**
        -   Work notes: `Auto-approved. Amount less than $100.00`
    ![Update Record action to approve the request.](../images/approved-flow-getting-started.png)

9.  Add an else condition to the flow.

    1.  Select **Flow Logic** &gt; **Else**.

10. Underneath action 2, click **+** to add an Ask for Approval action that runs when the Else condition is met.

    1.  Complete the fields in the Ask for Approval step.

        -   Action: **Ask for Approval**
        -   Record: Expand the **\[Trigger - Record Created\]** category and drag the **\[Expenses Record\]** data pill from the right-hand pane.
        -   Table: Set to **Expenses \[x\_expenses\_getting\_expenses\]**.
        -   Approval Field: Set to **Approval**.
        -   Journal Field: Set to **Approval history**.
        ![Add an Ask For Approval action that evaluates in the Else clause.](../images/action-fields-flow-getting-started.png)

    2.  Define the rules in the Ask for Approval step.

        -   **\[Approve\]** when **\[Anyone approves\]** from the field **\[Trigger-&gt;Expenses Record-&gt;Requested for-&gt;Manager\]**, **\[OR\]**
        -   **\[Anyone approves\]** from the **\[Manual User\(s\)\]** list. Select Manual approvers ![Manual approvers icon](../images/manual-users-icon.png) to allow a manual approver to process an approval or rejection. A manual approver is a user manually added to the Approvers related list who can then approve the request. For example, you can manually add a subject matter expert to a task to approve the request. To learn more about adding manual approvers, see [Generate approvals using the approvers related list](../../service-administration/concept/c_GenApprovalsUsingApprsRelList.md).
        Select **Add another OR rule set** to define rejection rules. When defining approvals, make sure to include rejection rules to avoid creating flows that remain in a waiting state if there are no matching approval rules.

        -   **\[Reject\]** when **\[Anyone rejects\]** from the field **\[Trigger-&gt;Expenses Record-&gt;Requested for-&gt;Manager\]**, **\[OR\]**
        -   **\[Anyone rejects\]** from the **\[Manual User\(s\)\]** list.
        ![Rules in the Ask for Approval step.](../images/rule-fields-flow-getting-started.png)

    3.  Define a due date to automatically approve, cancel, or reject an approval if the request is not approved or denied by the designated time.

        Adding a due date ensures that the flow does not remain in a waiting state.

        -   **\[Approve\]** if pending by **\[Relative date\]** **\[1\]** **\[Days\]** from **\[Trigger-&gt;Expenses Record-&gt;Created\]**.
        -   Days schedule **\[8-5 weekdays excluding holidays\]**.
        This due date automatically approves all requests that have not been approved or denied within one day from when the request was created.

        ![Due date in the Ask for Approval step.](../images/due-date-flow-getting-started.png)

11. Click **Save**.

12. Test the flow using a record with an amount below the designated limit.

    1.  From the flow, click **Test**.

        The Test flow modal appears.

    2.  In the **Record** field, select a record you created in earlier steps that has value in the **Amount** field under the 100.00 limit.

        This field is a reference to the table defined in the trigger.

        **Note:** Testing a flow bypasses the trigger conditions and immediately runs it. To test a flow with a record-based trigger, you must select a specific record to act as the trigger.

    3.  Select **Run Test**.

    4.  After the flow executes, click **Flow has been executed. To view the flow, click here**.

        The Execution Details open.

    Because the amount is less than 100.00, the first condition is met and the request is approved.

    ![Execution details showing the If clause evaluated and completed.](../images/get-start-test.png)

13. Navigate back to the flow and run the test again using a record with an amount over the designated amount.

14. After the flow executes, open the flow Execution Details.

    Because the amount is over the designated limit, the request must be approved. Until a manager or a manual approver approves the request, the state is **Waiting**.

    ![Execution details showing the Else clause evaluated and waiting for approval.](../images/flow-test-waiting.png)

15. Approve the request.

    In an active flow, a user from the Approvers list would approve or reject the request. However, because the flow is being tested, an admin can approve the flow.

    1.  Navigate to the test record.

        The associated manager appears in the Approvers related list with **Requested** in the **State** field. Alternatively, you can edit the list to add manual approvers.

    2.  Change the value of the **State** field in the Approvers related list to **Approved**.

    3.  Navigate back to the flow Execution Details and refresh the browser.

        Because the request is approved, the flow completes.

        ![Execution details showing the Else clause evaluated and completed.](../images/flow-test-approved.png)


## What to do next

Transform the Ask for Approval action into a reusable action using Workflow Studio. Actions enable flow designers to add complex actions to multiple flows with minimal configuration. See [Getting started with actions](getting-started-action.md).

-   **[Build your first flow in Workflow Studio](build-your-first-flow.md)**  
Step through an example of how to build, test, and activate a sample flow in Workflow Studio.
-   **[Build a flow from a template in App Engine Studio](build-flow-from-template.md)**  
Step through an example of how to build, test, and activate a flow using a flow template in App Engine Studio.
-   **[Use the Workflow Studio help panel](use-flow-designer-help-panel.md)**  
Browse topics in the side help panel to learn more about building flows and actions, working with data and spokes, and stepping through guided tours in Workflow Studio.

**Parent Topic:**[Exploring flows](../../workflow-studio/concept/exploring-flows.md)

