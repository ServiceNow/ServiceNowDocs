---
title: Closing tasks on Mobile Agent
description: A work order is automatically closed when all work order tasks associated with it have been closed.Close a work order task as complete or as incomplete with optionally a follow-on task to complete.Respond to a task that was sent back to you for review. Update the work order task with the requested details and submit the task back to reviewer.Receive a digital signature and confirmation from a customer that a work order has been completed.Enable customers to digitally sign and confirm a work order on the Mobile Agent application after it has been closed.Cancel a work order if it is no longer needed or suspend a work order if you want to work on it later.Record a break from a work order task on Mobile Agent if you are unable to continue the work for any reason. You can resume the work order task when you start working on it again. The system automatically tracks and calculates the actual time taken to complete the task even though you worked at different intervals.Record the duration for executing a task using the Mobile Agent application.Record incidental expenses associated with your business travel through the Mobile Agent application to execute work order tasks.Edit or delete your logged incidentals from WOT forms or from My Incidentals applets.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Closing tasks on Mobile Agent

A work order is automatically closed when all work order tasks associated with it have been closed.

## Close a work order task

Close a work order task as complete or as incomplete with optionally a follow-on task to complete.

### Before you begin

Technicians can close only the work order tasks assigned to them. The work order task must be in the **Work in Progress** state.

Role required: wm\_agent

### Procedure

1.  Open the Now Mobile Agent application.

2.  Tap **My Work**.

3.  In the **My Tasks** section, tap **See All**.

4.  Select the work order task you want to close.

5.  Either close the task after work is complete or close it with a follow-on task pending.

<table id="choicetable_rb4_1gc_qfb"><thead><tr><th align="left" id="d71443e163">

To

</th><th align="left" id="d71443e166">

Do this

</th></tr></thead><tbody><tr><td id="d71443e172">

**Close a work order task after work has been completed**

</td><td>

Select **Close Complete**.**Note:** Your **Work agent status** is automatically updated as On Shift to indicate that you are available to work on another task.

</td></tr><tr><td id="d71443e190">

**Close a work order task as incomplete**

</td><td>

1.  Select **Close Incomplete**.
2.  If the task has a follow-on task, select **Has follow-on task**.
3.  Select **Closure Note** and enter the reason for closing the task as incomplete.

The text will appear in the **Work notes** field.

4.  Close the work order task.

    -   iOS: Tap **Submit**.
    -   Android: Tap the done icon.
A clone of the work order task set to **Draft** state is created and the originally created work order task changes to the Closed Incomplete state.

5.  Return to the work order task.
    -   iOS: Tap **Submit**.
    -   Android: Tap the done icon.


</td></tr></tbody>
</table>6.  Generate a signed PDF summary for the work order task by tapping **Preview Work Summary**.

    The PDF summary captures the details of the task, and the responses submitted in the smart assessment questionnaire along with the score. For more information, see [Enable PDF summaries at work order task level](../task/enable-pdf-summary.md).


### Result

When all work order tasks associated with a work order are closed, the work order is automatically closed. You can view the signed PDF summary in the activity stream.

**Related topics**  


[Closing work orders](../../planning-and-policy/concept/c_CloseAWorkOrder.md)

[System properties](../../planning-and-policy/reference/r_InstalledWithFSM.md)

## Respond to a reviewed work order task

Respond to a task that was sent back to you for review. Update the work order task with the requested details and submit the task back to reviewer.

### Before you begin

Ensure that the Field Service Quality Management plugin is active. For more information, see [Activate Field Service Quality Management](../task/activate-quality-mgmt.md).

Role required: wm\_agent

### About this task

When you close a work order task, the task is sent to a reviewer. The reviewer can either mark the task as complete or request more information. For more information, see [Review a task](../task/review-send-task-back.md). You will receive a notification about the work order task that needs review.

### Procedure

1.  Open the Now Mobile Agent application.

2.  Navigate to the work order task using either of two methods.

    -   Navigate to **Notifications** and select the work order task that needs review.
    -   Navigate to **My work** &gt; **Closed tasks** &gt; **Needs Information** and select the work order task that needs review.
3.  Add the information that was requested.

4.  Tap **Update work order task**.

5.  Provide details about what was updated in the **Notes** field.

6.  Update a previously submitted smart assessment questionnaire responses to match the information added for the task.

    1.  Navigate to **Questionnaires** &gt; **Completed**.

    2.  Tap the Retake icon ![](../image/retake-questionnaire.png).

    3.  Edit the responses.

    4.  Tap **Submit** to resubmit the questionnaire.

7.  Tap **Submit** to update and submit the work order task with the requested details.


### Result

The work order task is sent back to the reviewer. The reviewer can either close the task or send back to you for review.

### Add the time worked

The reviewer sent the work order task requesting that you add the time worked. You navigate to the work order task through notifications. In the Time worked related list, you select **Record time** and fill out the form to record the time worked. You navigate back to the work order task details and tap **Update work order task**. You enter "I have entered my time worked" in the **Notes** field and submit the task.

## Complete a work order

Receive a digital signature and confirmation from a customer that a work order has been completed.

### Before you begin

The **Sign and Confirm** button must be enabled to receive digital confirmation from a customer after a work order is closed.

The signed PDF summaries capability must be enabled to generate a work order summary and get the customer signature on the work order after it has been closed. For more information on enabling the PDF summaries capability, see [Signed PDF summaries for closed work orders](work-order-sign-and-confirm-pdf.md#).

When all work order tasks associated with the work order are closed, the work order is automatically closed.

Role required: wm\_agent or wm\_dispatcher

### Procedure

1.  Open the Now Mobile Agent application.

2.  Locate the work order you want to complete.

    1.  Tap **My Work**.
    2.  In the **My Tasks** section, tap **See All**.
    3.  Select the work order task associated with the work order you want to close.
    4.  Select the work order number.
    5.  Select the work order to view the details.
3.  Receive the signature and confirmation from the customer for completing the work order.

    1.  Select the **Details** tab.
    2.  Tap **Preview** to review the details of closed work order.
    3.  Tap **Sign &amp; Confirm**.
    4.  Tap the **Signature** field.
    5.  In the signature pad, receive the signature from the customer to confirm the completed work.
    6.  Accept the signature.

        -   On an iOS device, tap **Submit**.
        -   On an Android device, tap the done icon.
        The signed PDF summary is generated and attached to the work order form. You can view the signed PDF summary in the activity stream.

        **Note:** Click the trash icon to cancel the signature.


### Enable customers to sign and confirm work orders on your mobile device

Enable customers to digitally sign and confirm a work order on the Mobile Agent application after it has been closed.

#### Before you begin

Role required: admin

#### Procedure

1.  On your desktop Field Service instance, navigate to **System Mobile** &gt; **Mobile Applications**.

2.  Select **Field Service**.

3.  From the Folders related list, select **My Work**.

4.  From the Screens belonging to the Folder related list, select **Work Order**.

5.  Do one of the following to enable the **Sign and Confirm** button.

<table id="choicetable_jfb_1sy_cgb"><thead><tr><th align="left" id="d71443e871">

To

</th><th align="left" id="d71443e874">

Complete these steps

</th></tr></thead><tbody><tr><td id="d71443e880">

**Enable the Sign and confirm option to display when you swipe a work order from a list**

</td><td>

1.  Select the **Master Items** tab.
2.  Select **Work Order**.
3.  Select the **Button Instances belonging to Master Item** tab.


</td></tr><tr><td id="d71443e910">

**Enable the Sign and confirm option to display when you open a work order form**

</td><td>

Select the **Function instances belonging to Screen** tab.

</td></tr></tbody>
</table>6.  Select **Sign &amp; Confirm**.

7.  Enable the **Active** check box.

8.  Select **Update**.


## Cancel or suspend a work order

Cancel a work order if it is no longer needed or suspend a work order if you want to work on it later.

### Before you begin

You can cancel or suspend a work order that has not been closed.

Role required: wm\_agent or wm\_dispatcher

### Procedure

1.  Open the Mobile Agent application.

2.  Tap **My Work**.

3.  In the **My Tasks** section, tap **See All**.

4.  Select the work order task.

5.  Select the work order number associated with the task.

    The work order number, work order state, and the short description for the work order appear.

6.  Select the work order to view the details.

7.  Tap the more actions \(![More actions icon](../image/OverflowIcon.png)\) icon and cancel or suspend the work order.

    -   To cancel the work order, select **Cancel Work Order**.
    -   To suspend the work order:

        1.  Select **Suspend**.
        2.  Select **Suspend Note**.
        3.  Enter the reason to suspend this work order.
        4.  Cancel the work order.
            -   On an iOS device, tap **Back**.
            -   On an Android device, tap the back icon.
        5.  Go back to the work order screen.
            -   On an iOS device, tap **Back**.
            -   On an Android device, tap the done icon.
        When you are ready to work on it again, tap the overflow icon and select **Resume**.


## Pause a work order task

Record a break from a work order task on Mobile Agent if you are unable to continue the work for any reason. You can resume the work order task when you start working on it again. The system automatically tracks and calculates the actual time taken to complete the task even though you worked at different intervals.

### Before you begin

Role required: wm\_agent

### About this task

The work order task must be in the Work in Progress state to pause the timer.

### Procedure

1.  Open the Mobile Agent application.

2.  Tap **My Work**.

3.  In the **My Tasks** section, tap **See All**.

4.  Open the work order task that you want to pause.

5.  Click **Pause Work**.

    The button toggles to **Resume Work** automatically. A pause on the work order task disables mobile actions such as Use Part, Close Complete, Edit, Questionnaires, Remove Part, Create Part Requirement, Record Time, and Close Incomplete on the work order task. Your **Work agent status** is automatically updated as **Work paused** to determine that you have paused working on a task.

6.  Click **Resume Work** when you are ready to work on the activity again.

    Your **Work agent status** is automatically updated as **On site** to determine that you have resumed working on a task.


### Result

Each time you pause or resume work on the task, a timestamp is captured in the activity stream and the actual time you worked on the task is automatically calculated. An entry for the time worked is created in the **Time Worked** related list.

## Record time worked on a work order task

Record the duration for executing a task using the Mobile Agent application.

### Before you begin

Role required: wm\_agent or wm\_dispatcher

### Procedure

1.  Open the Mobile Agent application.

2.  Tap **My Work**.

3.  In the **My Tasks** section, tap **See All**.

4.  Select a work order task to record the time.

5.  Tap the more actions \(![More actions icon](../image/OverflowIcon.png)\) icon and then select **Record Time**.

6.  Select the desired items from any of the following fields:

    |Field|Description|
    |-----|-----------|
    |Work Date|Date the task was executed.|
    |Category|Category for the accomplished task.|
    |Time Worked \(Hours\)|Number of hours worked on the task.|
    |Time Worked \(Minutes\)|Number of minutes worked on the task.|
    |Comments|Additional notes about the task.|

7.  Record the task duration.

    -   On an iOS device, tap the **Submit** button.
    -   On an Android device, tap the send icon.

## Record an incidental expense for a work order task

Record incidental expenses associated with your business travel through the Mobile Agent application to execute work order tasks.

### Before you begin

Role required: wm\_agent

### About this task

Log incidentals to manage your expenses such as car rental cost, mileage, and vendor costs that you spend through the mobile application to execute your work order task. You can attach a receipt for a logged incidental.

### Procedure

1.  Open the Mobile Agent application.

2.  From the **My Work** tab, select a work order task to record related expenses.

3.  Tap the top-right menu and tab **Log Incidental**.

4.  From the **Type** field, select the type of this incidental.

5.  From the **Currency** field, select the currency you used for the expense.

6.  In the **State** field, indicate whether the expense has already occurred \(**Incurred**\) or has not yet occurred \(**Pending**\).

7.  In the **Description** field, enter a description for the incidental you want to record.

8.  Upload files or photos as attachment if applicable.

9.  Record the expense for the incidental.

    -   On an iOS device, tap the **Submit** button.
    -   On an Android device, tap the send icon.

## Edit or delete an incidental expense for a work order task

Edit or delete your logged incidentals from WOT forms or from My Incidentals applets.

### Before you begin

Role required: wm\_agent

### Procedure

1.  Open the Mobile Agent application.

2.  Navigate to your incidentals in one of the following ways:

    -   From WOT forms:
        1.  From the **My Work** tab, select a work order task.
        2.  Tap the **Related** tab.
        3.  Scroll down to the **Incidentals** tab.
    -   From My Incidentals applets:
        1.  Tap **More** at the bottom-right corner.
        2.  Tap **My Incidentals**.
3.  Tap an incidental to see details.

4.  Tap the top-right menu and tap **Edit** or **Delete**.

5.  Save the record.


