---
title: Closing tasks on Mobile Agent
description: A work order is automatically closed when all work order tasks associated with it have been closed.Close a work order task as complete after you finish the work required for the task. You can close the work order task as incomplete and optionally create a follow-on task to complete.Respond to a task that was sent back to you for review. Update the work order task with the requested details and submit the task back to reviewer.Receive a digital signature and confirmation from a customer that a work order has been completed.Enable customers to digitally sign and confirm a work order on the Mobile Agent application after it has been closed.Cancel a work order if it is no longer needed or suspend a work order if you want to work on it later.Record a break from a work order task on Mobile Agent if you are unable to continue the work for any reason. You can resume the work order task when you start working on it again. The system automatically tracks and calculates the actual time taken to complete the task even though you worked at different intervals.Record the duration for executing a task using the Mobile Agent application.Record incidental expenses associated with your business travel through the Mobile Agent application to execute work order tasks.Edit or delete your logged incidentals from WOT forms or from My Incidentals applets.Generate a summary directly from the work order task record.Generate work order task closure summaries in the ServiceNow Agent app to create detailed notes and close tasks faster.Use the Parts Manager AI agent to track and validate parts usage when closing a work order task on the ServiceNow Agent mobile application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/work-order-management/close-wo-wot-mobile.html
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 15
keywords: [Parts Manager, validate parts, AI agent, generative AI for Field Service Management]
breadcrumb: [ServiceNow Agent mobile app, Use, Field Service Management]
---

# Closing tasks on Mobile Agent

A work order is automatically closed when all work order tasks associated with it have been closed.

## Close a work order task

Close a work order task as complete after you finish the work required for the task. You can close the work order task as incomplete and optionally create a follow-on task to complete.

### Before you begin

Agents can only close the work order tasks assigned to them. The work order task must be in the **Work in Progress** state.

Role required: wm\_agent or wm\_dispatcher

### Procedure

1.  Open the Now Mobile Agent application.

2.  Tap **My Work**.

3.  In the **My Tasks** section, tap **See All**.

4.  Select the work order task you want to close.

5.  Do one of the following.

<table id="choicetable_rb4_1gc_qfb"><thead><tr><th align="left" id="d69207e164">

To

</th><th align="left" id="d69207e167">

Do this

</th></tr></thead><tbody><tr><td id="d69207e173">

**Close a work order task after you complete the work on the task**

</td><td>

1.  Select **Close Complete**.
2.  In the **Close Complete** page, select **Closure Note**.
3.  Provide the work completion details.
4.  Select **Done** to save the details.
5.  Automatically create and route a new work order task when the current task is closed as complete by turning on the **Has follow-on task** option.
 **Note:** Your **Work agent status** is automatically updated as **On Shift** to determine that you are available to work on a task.

</td></tr><tr><td id="d69207e224">

**Close a work order task if a follow-on task is pending completion**

</td><td>

Do the following:

1.  Select **Close Incomplete**.
2.  Optionally, turn the **Has follow-on task** button on.
3.  Select **Closure Note** and enter the reason for closing the task as incomplete. The text entered is copied into the **Work notes** field.
4.  Do one of the following to close the work order task:

    -   On an iOS device, tap **Submit**.
    -   On an Android device, tap the done icon.
A clone of the work order task set to **Draft** state is created and the originally created work order task changes to the **Closed Incomplete** state.

5.  Do one of the following to return to the work order task:
    -   On an iOS device, tap **Submit**.
    -   On an Android device, tap the done icon.


</td></tr></tbody>
</table>    When all work order tasks associated with a work order are closed, the work order is automatically closed.


### What to do next

You can view the closed work order tasks of last seven days by navigating to **My Work** &gt; **Recently Closed Tasks** in the Now Mobile Agent application.

You can change the time period for displaying the last closed work order tasks in the Recently Closed Tasks list. For more information, see [Configure the recently closed work order tasks list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/mobile-experience-for-field-service-management-glide-family/configure-recently-closed-di.md).

**Related topics**  


[Closing work orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/work-order-management/c_CloseAWorkOrder.md)

[System properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/r_InstalledWithFSM.md)

## Respond to a reviewed task

Respond to a task that was sent back to you for review. Update the work order task with the requested details and submit the task back to reviewer.

### Before you begin

Role required: wm\_agent

Ensure that the Field Service Quality Management plugin is active. For more information, see [Activate Field Service Quality Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/work-order-management/activate-quality-mgmt.md).

### About this task

When you close a work order task, the task is sent to a reviewer. The reviewer can either mark the task as complete or request more information. For more information, see [Review a task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/work-order-management/review-send-task-back.md). You will receive a notification about the work order task that needs review.

### Procedure

1.  Open the Now Mobile Agent application.

2.  Navigate to the work order task.

    -   Navigate to **Notifications** and select the work order task that needs review.
    -   Navigate to **My work** &gt; **Closed tasks** &gt; **Needs Information** and select the work order task that needs review.
3.  Add the information that was requested.

    **Note:** The required information depends on what was requested.

4.  Tap **Update work order task**.

5.  Provide details about what was updated in the **Notes** field.

6.  Tap **Submit**.


### Result

The work order task is sent back to the reviewer. The reviewer can either close the task or send back to you for review.

### Add the time worked

The reviewer sent the work order task requesting that you add the time worked. You navigate to the work order task through notifications. In the Time worked related list, you select **Record time** and fill out the form to record the time worked. You navigate back to the work order task details and tap **Update work order task**. You enter "I have entered my time worked" in the **Notes** field and submit the task.

## Complete a work order

Receive a digital signature and confirmation from a customer that a work order has been completed.

### Before you begin

The **Sign and Confirm** button must be enabled to receive digital confirmation from a customer after a work order is closed.

The signed PDF summaries capability must be enabled to generate a work order summary and get the customer signature on the work order after it has been closed. For more information on enabling the PDF summaries capability, see [Signed PDF summaries for closed work orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/work-order-management/work-order-sign-and-confirm-pdf.md).

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

<table id="choicetable_jfb_1sy_cgb"><thead><tr><th align="left" id="d69207e871">

To

</th><th align="left" id="d69207e874">

Complete these steps

</th></tr></thead><tbody><tr><td id="d69207e880">

**Enable the Sign and confirm option to display when you swipe a work order from a list**

</td><td>

1.  Select the **Master Items** tab.
2.  Select **Work Order**.
3.  Select the **Button Instances belonging to Master Item** tab.


</td></tr><tr><td id="d69207e910">

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

7.  Tap the more actions \(\[Omitted image "OverflowIcon.png"\] Alt text: More actions icon\) icon and cancel or suspend the work order.

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

5.  Tap the more actions \(\[Omitted image "OverflowIcon.png"\] Alt text: More actions icon\) icon and then select **Record Time**.

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


## Generate a work order task summary

Generate a summary directly from the work order task record.

### Before you begin

Role required: wm\_qualifier, wm\_dispatcher, wm\_agent

### Procedure

1.  Navigate to a work order task.

2.  Select **Summarize**.


### Result

A summary is generated for the work order task.

### Generate a summary for a work-in-progress task

Alex the agent is finishing a printer repair task. To wrap up the task, they generate a summary using the procedure.

\[Omitted image "generate-summary-na.png"\] Alt text: Summary generated for the work order task.

### What to do next

You can mark the summary as helpful or unhelpful, copy the summary, or refresh to generate the summary again.

## Generate work order task closure summaries in ServiceNow Agent

Generate work order task closure summaries in the ServiceNow Agent app to create detailed notes and close tasks faster.

### Before you begin

Agents can only generate summaries for the work order tasks that are assigned to them. The work order task must be in the **Work in Progress** state. Work notes must have at least 200 words to generate a summary.

For more information on how to close work order tasks, see [Close a complete work order task on a mobile device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/work-order-management/close-complete-wot-fsc.md).

Role required: agent

### Procedure

1.  Navigate to **My work**.

2.  In the My Tasks section, select the work order task that you want to close.

    \[Omitted image "mobile-my-work.png"\] Alt text: My Work tab with work order tasks.

3.  Tap **Close Complete**.

    \[Omitted image "mobile-close-complete.png"\] Alt text: Close complete action on Work In Progress task.

4.  Tap the **Closure notes** field.

5.  Tap \[Omitted image "icon-ai-sparkle.png"\] Alt text: Generate closure notes icon. **Generate closure notes**.

    \[Omitted image "mobile-generate-closure-notes.png"\] Alt text: Generate closure notes action on the Closure summary screen.


### Result

A closure summary is generated for the work order task. You can edit the summary after it's generated. Because the information in these fields is automatically generated, it’s a good idea to review the text and make sure that it's accurate.

## Validate parts on ServiceNow Agent using the Parts Manager AI agent

Use the Parts Manager AI agent to track and validate parts usage when closing a work order task on the ServiceNow Agent mobile application.

### Before you begin

Before validating parts, verify that comments or work notes describing the parts used during the task have been added to the work order task activity stream. The Parts Manager AI agent references these notes to identify and validate parts.

Role required: wm\_agent

### About this task

The Parts Manager AI agent analyzes your work notes to identify which parts were used during a service task. You can use the agent to swap, install, or decline required parts through a conversational AI interaction. After validation, the agent automatically updates inventory and parts statuses.

**Note:** Review the AI-generated parts summary before confirming. AI-generated results may not be accurate in all cases.

### Procedure

1.  Navigate to **My Work**.

2.  Tap a work order task under **My Tasks**.

3.  Tap the Now Assist icon \[Omitted image "now-assist-panel-icon.png"\] Alt text: in the navigation bar to open Now Assist Virtual Agent.

4.  Ask Now Assist to validate parts for the work order task.

    \[Omitted image "now-assist-mobile-validate-parts.png"\] Alt text: The validate parts conversation in Now Assist Virtual Agent on the mobile app.

    If the Parts Manager AI agent cannot determine the work order task, provide the work order task number when prompted.

    The Parts Manager AI agent analyzes the work notes and work order task details, then presents a summary of parts used, parts removed, and parts not used.

5.  Review the validated parts summary and confirm the results.

    The parts statuses and inventory are updated based on the validated results.


### What to do next

To verify the updated parts for the task, open the work order task and tap the more options icon next to **Related**, then tap **Parts**.

