---
title: Create a flow
description: Automate the workflow for the employee travel request application by creating a flow.Request approvals for any record by adding the Ask for Approval action to your flow.Use If flow logic to direct your flow to perform actions based on specific conditions.Integrate decision tables into your flow using Make a decision flow logic.For actions that repeat within your flow, save time by duplicating the actions and adjusting their values as needed.Automate record updates in a flow using the Update Record action.In flows with If flow logic, add Else flow logic to create alternate paths when conditions aren’t met.Automate sending email notifications using the Send Email action.Add End Flow flow logic to stop running the current flow.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 21
breadcrumb: [Adding logic and automation, App creation tutorial, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create a flow

Automate the workflow for the employee travel request application by creating a flow.

## Before you begin

Role required: admin or flow\_designer

## About this task

The second phase in adding logic and automation to the employee travel request application is to create a flow. The flow that we create automates the workflow for the application after an employee travel request is created.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Build a decision table](app-tutorial-create-decision-table.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Create a flow](app-tutorial-create-a-flow.md#)

</td></tr></tbody>
</table>For more information about flows, see [Building flows](https://www.servicenow.com/docs/access?context=flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

Use the following tutorial to create a flow for the employee travel request application.

Add logic and automation to your application. 

|Timestamp|Section|
|---------|-------|
|0:09|Add a flow to your application.|
|0:14|Build the flow from scratch.|
|0:17|Enter a unique name and description for the flow.|
|0:22|Continue setting up your flow.|
|0:25|Create a trigger.|
|0:41|[Add an Ask for Approval action](app-tutorial-create-a-flow.md#).|
|1:09|[Add If flow logic](app-tutorial-create-a-flow.md#).|
|1:25|[Integrate decision tables](app-tutorial-create-a-flow.md#).|
|1:48|[Duplicate repeating actions](app-tutorial-create-a-flow.md#).|
|2:17|[Add an Update Record action](app-tutorial-create-a-flow.md#).|
|2:38|[Add Else flow logic](app-tutorial-create-a-flow.md#).|
|2:50|[Add a Send Email action](app-tutorial-create-a-flow.md#).|
|4:14|[Add End Flow flow logic](app-tutorial-create-a-flow.md#).|
|4:19|View your flow as a diagram.|
|4:22|Save your changes.|

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  Open the employee travel request application.

3.  On the application dashboard, select **+ Add** next to **Logic and automation**.

4.  Select **Flow**, then select **Begin**.

5.  Select **Build your flow from scratch**.

    You can also choose to build your flow with Now Assist. For more information, see [Create a flow with Now Assist](https://www.servicenow.com/docs/access?context=create-flow-now-assist&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

6.  Define the properties of the flow.

    1.  In the **Name** field, enter `Approvals workflow`.

    2.  In the **Description** field, enter `Approval workflow for managers and regional heads`.

    3.  Select **Continue**.

7.  Select **Edit this flow** to continue setting up your flow.

8.  Add triggers to the flow.

    **Note:** A trigger specifies when to run the flow. When the trigger conditions are met, the system runs the flow using the data provided by the trigger.

    In our tutorial, we create a trigger that runs the flow whenever an employee submits a travel request.

    1.  In the **Trigger** section, select **+ Add a trigger**.

    2.  In the **Trigger** field, select **Record** &gt; **Created**.

        For more information about trigger types, see [Workflow Studio flow trigger types](https://www.servicenow.com/docs/access?context=flow-triggers&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

    3.  In the **Table** field, enter the name of the travel request table and select it from the list.

    4.  Select **Done**.

9.  Add actions, flow logic, and sublows to the flow.

    **Note:** You can add [actions](https://www.servicenow.com/docs/access?context=flow-actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US), [flow logic](https://www.servicenow.com/docs/access?context=flow-logic&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US), and [subflows](https://www.servicenow.com/docs/access?context=subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) to enable your flow to perform desired actions. For example, you can create an action that enables your application to send emails automatically.

    In our tutorial, we add several actions and branches of flow logic to automate the employee travel request process. The following diagram demonstrates the flow that we create in our tutorial.

    ![Diagram that](../image/app-tutorial-create-a-flow-diagram-v4.png)

    Instructions for adding the actions and flow logic demonstrated in the tutorial are outlined in the following topics.

10. See how your flow appears as a diagram by toggling the switch next to **View**.

11. Select **Save** to save your changes.


## Result

You have created a flow that will automate the end-to-end workflow for the employee travel request application.

## What to do next

Continue building the flow for the employee travel request application. Proceed to the next step: [Add an Ask for Approval action](app-tutorial-create-a-flow.md#).

## Add an Ask for Approval action

Request approvals for any record by adding the Ask for Approval action to your flow.

### Before you begin

Role required: admin or flow\_designer

### About this task

The Ask for Approval action is a ServiceNow Core action template that enables you to request approvals easily. You can specify which records require approval and assign users to approve or reject the record.

In our tutorial, we use the Ask for Approval action to request approvals from both managers and regional head for employee travel requests. This procedure outlines the Ask for Approval action that routes to the manager. The procedure for creating the Ask for Approval action that routes to the regional head is outlined in [Duplicate repeating actions](app-tutorial-create-a-flow.md#).

For more information about the Ask for Approval action, see [Ask for Approval action](https://www.servicenow.com/docs/access?context=ask-approval-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Procedure

1.  At the correct location in your flow, select **+ Add an Action, Flow Logic, or Subflow**.

    In our tutorial, the Ask for Approval action that routes to the manager occurs just after the trigger. To see where the Ask for Approval action occurs in the tutorial flow, see the diagram in [Create a flow](app-tutorial-create-a-flow.md#).

2.  Select **Action**.

3.  From the **ServiceNow Core** options, select **Ask for Approval**.

4.  Choose from one of the following options to connect the action to the appropriate trigger.

    **Note:** Some flows have multiple triggers, so you must specify which trigger corresponds to the action.

    In our tutorial, we add the travel request record trigger to the **Record** field, so that the action runs whenever an employee submits a travel request.

    -   To add your trigger within the Ask for Approval dialog, select the **Data Pill Picker** \(![Data pill picker icon](../../../administer/flow-designer/images/data_pill_picker.png)\), then select the trigger from the list.
    -   To add your trigger from the **Data** panel, drag the data pill that contains the trigger into the **Record** field.
    ![You can add your trigger by selecting the Data pill picker, or by dragging the data pill from the Data panel.](../image/app-tutorial-add-trigger-options.png)

5.  Set the rules for the action.

    **Note:** Rules determine which users can approve or reject requests, and what happens after approval or rejection. For more information about the rules available for the Ask for Approval action, see [Ask for Approval action](https://www.servicenow.com/docs/access?context=ask-approval-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

    In our tutorial, we configure the rules for the Ask for Approval action to send travel requests to the manager of the user who submitted the request. The manager can then approve or deny the request.

    1.  Select the **Approve** field, then select **Approve or Reject** from the list.

    2.  Select the **-Choose approval rule** field, then select **All users approve or reject**.

    3.  Choose which users or groups can complete the approval actions using the **Data Pill Picker** \(![Pill picker icon.](../../../administer/flow-designer/images/data_pill_picker.png)\), the add user icon \(![Add user icon](../image/app-tutorial-add-user-icon.png)\), add group icon \(![Add group icon](../image/app-tutorial-add-group-icon.png)\), the add manual approvers icon \(![Manual approvers icon](../../../administer/flow-designer/images/manual-users-icon.png)\), or by dragging data pills from the **Data** panel into the field.

        In our tutorial, we want the Ask for Approval action to route to the manager of the user who submitted the travel request. So we select **Trigger - Record Created** &gt; **Travel request Record** &gt; **Opened by** &gt; **Manager**.

        ![You can select which users can approve records using the Data pill picker button, then selecting the value that stores the correct user data.](../image/app-tutorial-add-manager-approval.png)

        The second Ask for Approval action, which you create in [Duplicate repeating actions](app-tutorial-create-a-flow.md#), routes the approval to the regional head.

6.  Select **Done**.

7.  Select **Save**.


### What to do next

Proceed to the next step: [Add If flow logic](app-tutorial-create-a-flow.md#).

## Add If flow logic

Use If flow logic to direct your flow to perform actions based on specific conditions.

### Before you begin

Role required: admin or flow\_designer

### About this task

Add If flow logic to your flow to have your application perform actions only when certain criteria are met. If flow logic creates a specific path, or branch, within a flow that runs only when the conditions are met.

In our tutorial, we use If flow logic to define what the application does if a travel request has been approved. For example, if a travel request has been approved by the regional head, the **State** of the travel request record should be changed to **Closed complete**.

There are two instances of If flow logic in the flow in the app creation tutorial: One that represents manager approval and another that represents regional head approval. This procedure covers creating the branch that represents manager approval. You can use this procedure to create the branch that represents the regional head approval and adjust the **Column label** and **Condition** field values accordingly.

For more information about using If flow logic, see [If flow logic](https://www.servicenow.com/docs/access?context=flow-logic-if&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Procedure

1.  At the correct location in your flow, select **+ Add an Action, Flow Logic, or Subflow**.

    The If flow logic that represents manager approval occurs just after the first Ask for Approval action. To see where If flow logic occurs in the tutorial flow, see the diagram in [Create a flow](app-tutorial-create-a-flow.md#).

2.  Select **Flow Logic**.

3.  Select **If**.

4.  In the **Condition label** field, enter a description to describe the conditions that the branch represents.

    In our tutorial, we enter `Manager Approved`, as this branch represents that a manager has approved the travel request.

5.  Select the condition under which the branch runs using the **Data Pill Picker** \(![Data pill picker icon](../../../administer/flow-designer/images/data_pill_picker.png)\) or by dragging the data pill from the **Data** panel into the **Condition 1** field.

    **Note:** The condition is the data container that the flow evaluates when determining whether to run the branch. You can define one or multiple conditions in If flow logic.

    In our tutorial, we want this branch of the flow to represent what happens if a manager has approved a travel request, so we set the condition to **Approval State**.

    ![Choose the condition or conditions that you want the flow to evaluate when determining whether to run branching actions or flow logic.](../image/app-tutorial-ask-for-approval-state.png)

6.  Define the condition state that enables the branch to run by selecting the fields beside **Condition 1**, then choosing the appropriate values.

    **Note:** The condition state is the actual value of the condition that defines when the branch should run.

    In our case, this branch should run when a travel request has been approved by a manager. So we set the condition state to **is** and **Approved**.

7.  Select **Done**.

8.  Select **Save**.


### Result

By default, If flow logic has no output. It simply evaluates whether a condition is met or unmet. To have your flow complete actions when the conditions in the If flow logic are met, you must add branching actions or flow logic.

### What to do next

Proceed to the next step: [Integrate decision tables](app-tutorial-create-a-flow.md#).

## Integrate decision tables

Integrate decision tables into your flow using Make a decision flow logic.

### Before you begin

Role required: admin or flow\_designer

### About this task

Make a decision flow logic enables you to integrate decision tables within flows easily. Make a decision flow logic runs the decision table and returns results, which can be displayed as branches in the flow or data pills in the **Data** panel.

In our tutorial, employee travel requests are sent to the regional heads after receiving manager approval. We use Make a decision flow logic to connect the flow to the regional head decision table and retrieve the correct regional information.

For more information about Make a decision flow logic, see [Make a decision flow logic](https://www.servicenow.com/docs/access?context=flow-logic-make-decision&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Procedure

1.  At the correct location in your flow, select **+ Add an Action, Flow Logic, or Subflow**.

    We add Make a decision flow logic beneath the branch of If flow logic that represents manager approval. To see where we add Make a decision flow logic in the tutorial flow, see the diagram in [Create a flow](app-tutorial-create-a-flow.md#).

2.  Select **Flow logic**.

3.  Select **Make a decision**.

4.  Select the **Decision table** field, then select the correct decision table from the list.

    In our tutorial, we select the regional head approvals decision table.

5.  Choose to select or deselect the check box for **Use Branches**.

    **Note:** If you select the check box for **Use Branches**, the flow displays each possible decision table result as a separate branch.

    In our tutorial, the approval process is the same for each of the regional heads, so we deselect **Use Branches**. If the employee travel request process was different for employees of a certain region, we could select **Use Branches** to represent the different processes based on region.

6.  Add the correct trigger to the **Decision table inputs** field using either the **Data Pill Picker**\(![Data pill picker icon](../../../administer/flow-designer/images/data_pill_picker.png)\) or by dragging the data pill from the **Data** panel into the field.

    **Tip:** When you integrate a decision table into a flow, you must specify the data values for the decision table to evaluate within the context of the flow.

    In our tutorial, we need the decision table to evaluate the user information that's associated with the travel request trigger. So we add our trigger to the **Decision table inputs** field.

7.  Select **Done**.


### Result

The Make a decision flow logic generates results from the decision table, which you can use in your flow.

### What to do next

Proceed to the next step: [Duplicate repeating actions](app-tutorial-create-a-flow.md#).

## Duplicate repeating actions

For actions that repeat within your flow, save time by duplicating the actions and adjusting their values as needed.

### Before you begin

Role required: admin or flow\_designer

### About this task

Duplicating actions enables you to build flows more quickly and efficiently.

In our tutorial, there are several actions that repeat within the employee travel request flow.

-   The Ask for Approval action repeats to request both the manager and regional head approvals for employee travel requests.
-   The Update Record action updates the travel request record at several places in the flow, such as when the request is rejected by a manager.
-   The Send Email action occurs in two places to notify employees that their travel requests have been rejected by either the manager or the regional head.

This procedure outlines duplicating the Ask for Approval action to request regional head approval. You can use the steps outlined here to duplicate the other actions that repeat and adjust the action location and field values accordingly.

### Procedure

1.  Hover over the action that you want to duplicate and select the Duplicate action icon \(![Duplicate action icon](../image/app-tutorial-duplicate-action-icon.png)\).

    In our tutorial, we duplicate the Ask for Approval action.

    ![You can select the Duplicate action icon to duplicate actions within your flow.](../image/app-tutorial-duplicate-action.png)

2.  Move the duplicated action into the correct place in the flow by hovering over the action, selecting the drag icon \(![Row drag and drop gripper icon](../../../administer/decision-table/image/Drag.png)\), and dragging the action into the correct place.

    We move the duplicated Ask for Approval action beneath the Make a decision flow logic that returns the regional head information.

    ![You can rearrange elements within your flow by selecting the drag icon and moving the element into the correct place.](../image/app-tutorial-drag-duplicated-action.png)

3.  Adjust values in the action as needed.

    1.  Select the duplicated action to open the action dialog.

    2.  Select the remove icon \(![Delete form element.](../../../administer/form-builder/image/fb-delete-icon.png)\) to remove any field values that you must change.

        In our tutorial, we must change the user that the Ask for Approval routes to. So we select the remove icon \( ![Delete form element.](../../../administer/form-builder/image/fb-delete-icon.png)\) in the data pill that contains the manager user information.

    3.  Provide the correct field values by selecting the **Data Pill Picker** \(![Pill picker icon.](../../../administer/flow-designer/images/data_pill_picker.png)\) or by dragging data pills from the **Data** panel into the fields.

        To route the Ask for Approval action to the correct regional head, we must add the data pill that contains the regional head information.

        -   Using the **Data Pill Picker** \(![Pill picker icon.](../../../administer/flow-designer/images/data_pill_picker.png)\), we select **Make a decision** &gt; **Decision Table Multiple Result Record** &gt; **Result elements** &gt; **Regional heads**.
        -   Using the **Data** panel, we select and drag the regional heads data pill into the field.

            ![The regional heads data pill appears in the Data panel in the Make a decision section.](../image/app-tutorial-make-a-decision-data-pill.png)

4.  Select **Save**.

5.  Repeat this procedure to duplicate as many actions as needed in your flow.

    In our tutorial, we also duplicate the Update Record and Send Email actions.


### What to do next

Proceed to the next step: [Add an Update Record action](app-tutorial-create-a-flow.md#).

## Add an Update Record action

Automate record updates in a flow using the Update Record action.

### Before you begin

Role required: admin or flow\_designer

### About this task

The Update Record action is a ServiceNow Core action template that you can add to your flow to update existing records.

In our tutorial, we use the Update Record action to update the travel request record after it has been approved or rejected. This procedure outlines creating the Update Record action if a travel request has been approved by the manager and regional head. You can use this procedure to create the other Update Record actions and change the fields and field values as needed.

For more information about the Update Record action, see [Update Record action](https://www.servicenow.com/docs/access?context=update-record-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Procedure

1.  At the correct location in your flow, select **+ Add an Action, Flow Logic, or Subflow**.

    We add the Update Record action that represents manager and regional head approvals beneath the If flow logic branch for regional head approval. To see where we add the Update Record action in the tutorial flow, see the diagram in [Create a flow](app-tutorial-create-a-flow.md#).

2.  Select **Action**.

3.  From the **ServiceNow Core** options, select **Update Record**.

4.  Select the record that you want to update by selecting the **Data Pill Picker** \(![Pill picker icon.](../../../administer/flow-designer/images/data_pill_picker.png)\) or by dragging the data pill from the **Data** panel into the **Record** field.

    In our tutorial, we want to update the travel request record, so we add the travel request trigger to the **Record** field.

5.  Choose the field or fields that you want to update in the record by selecting **Add a field value**, then selecting the field that you want to update from the list.

    In our tutorial, we must update several fields in our travel request record after the request has been approved by the manager and regional head. We select the following fields:

    -   **Approval**
    -   **Assignment group**
    -   **State**
6.  Set the desired value of each field that you added by selecting anywhere in the **Select** field, then selecting the correct value from the list.

    In our tutorial, we set the following values for the fields that we added:

    |Field|Value|
    |-----|-----|
    |Approval|Approved|
    |Assignment group|Travel desk|
    |State|Closed complete|

7.  Select **Done**.

8.  Select **Save**.


### What to do next

Proceed to the next step: [Add Else flow logic](app-tutorial-create-a-flow.md#).

## Add Else flow logic

In flows with If flow logic, add Else flow logic to create alternate paths when conditions aren’t met.

### Before you begin

Role required: admin or flow\_designer

### About this task

Add Else flow logic to define the actions that your flow performs when If flow logic conditions aren't met. Else flow logic creates a path in the flow that runs only when the If flow logic conditions aren’t met.

In our tutorial, we add Else flow logic to specify what happens when a travel request is rejected by either a manager or regional head.

### Procedure

1.  At the correct location in your flow, select **+ Add an Action, Flow Logic, or Subflow**.

    We add Else flow logic at two places in the flow: One beneath the branch of the flow that represents manager approval and another beneath the branch that represents regional head approval. To see where we add Else flow logic in the tutorial flow, see the diagram in [Create a flow](app-tutorial-create-a-flow.md#).

2.  Select **Flow logic**.

3.  In the **Search flow logics** list, select **Else**.

4.  Select **Save**.


### Result

By default, Else flow logic has no output. It just creates a branch for the flow to run when the If flow logic conditions aren't met. To have your flow complete actions in the Else flow logic block, you must add branching actions or flow logic.

### What to do next

Proceed to the next step: [Add a Send Email action](app-tutorial-create-a-flow.md#).

## Add a Send Email action

Automate sending email notifications using the Send Email action.

### Before you begin

Role required: admin

### About this task

The Send Email action is a ServiceNow Core action template that you can add to your flow to automate sending emails to specified users or groups.

In our tutorial, we add Send Email actions to notify employees that their travel requests have been rejected. This procedure covers the Send Email action that notifies employees that their travel request has been rejected by the regional head. You can use this procedure to create the other Send Email action for the manager rejection and adjust the field values accordingly.

For more information about the Send Email action, see [Send Email action](https://www.servicenow.com/docs/access?context=send-email-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Procedure

1.  At the correct location in your flow, select **+ Add an Action, Flow Logic, or Subflow**.

    We add the Send Email action beneath the Else flow logic that represents regional head rejection. To see where we add Send Email actions in the tutorial flow, see the diagram in [Create a flow](app-tutorial-create-a-flow.md#).

2.  Select **Action**.

3.  From the **ServiceNow Core** options, select **Send Email**.

4.  Add the record that the email is associated with to the **Target Record** field using the Data pill picker \(![Pill picker icon.](../../../administer/flow-designer/images/data_pill_picker.png)\), or by dragging the data pill from the **Data** panel.

    In our tutorial, we want the email to be associated with the travel request record in our trigger.

5.  Add recipients for the email in the **To** field using the Data pill picker \(![Pill picker icon.](../../../administer/flow-designer/images/data_pill_picker.png)\), or by dragging the data pill from the **Data** panel.

    In our tutorial, we want the user who created the travel request to receive the email. The user information is stored under **Trigger - Record Created** &gt; **Travel request Record** &gt; **Opened by**.

6.  Add additional recipients to the email in the **CC** and **BCC** fields.

    We don’t add additional recipients to the Send Email action in our tutorial.

7.  Enter a subject for the email in the **Subject** field.

    In our tutorial, we enter the following subject for the email: `Travel request rejected`.

8.  Enter the content for the email message in the **Body** field.

    **Tip:** You can add dynamically created content, or content that is generated within the flow, to the Send Email action. To add dynamic content, drag the data pills from the **Data** panel into the **Body** of the email.

    In our tutorial, the body of our email notifies the employee that their travel request has been rejected and to contact their manager for additional information.

9.  Select **Done**.

10. Select **Save**.


### What to do next

Proceed to the next step: [Add End Flow flow logic](app-tutorial-create-a-flow.md#).

## Add End Flow flow logic

Add End Flow flow logic to stop running the current flow.

### Before you begin

Role required: admin

### About this task

If you want your flow to end when certain conditions are met, you can add End Flow flow logic. End Flow flow logic can be contained within a conditional flow logic block, such as an If, Else If, or Else flow logic. End Flow flow logic stops running the current flow.

In our tutorial, we add End Flow flow logic to end the flow if a travel request has been rejected.

For more information about End Flow flow logic, see [End Flow flow logic](https://www.servicenow.com/docs/access?context=flow-logic-end-action&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

### Procedure

1.  At the correct location in your flow, select **+ Add an Action, Flow Logic, or Subflow**.

    We add End Flow flow logic in the branch that represents manager rejection of a travel request. To see where we add End Flow logic in the tutorial flow, see the diagram in [Create a flow](app-tutorial-create-a-flow.md#).

2.  Select **Flow Logic**.

3.  In the **Search flow logics** list, select **End Flow**.

4.  Select **Save**.


### What to do next

The logic and automation for the employee travel request application are complete. Proceed to the final step in the app creation tutorial: [Test your application](app-tutorial-test-app.md).

