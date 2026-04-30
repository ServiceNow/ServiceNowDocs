---
title: Set up Notify with On-Call Scheduling
description: You can configure on-call scheduling to use Notify functionality to send SMS alerts and assign users to tasks based on the SMS responses.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Notify with On-Call Scheduling, Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up Notify with On-Call Scheduling

You can configure on-call scheduling to use Notify functionality to send SMS alerts and assign users to tasks based on the SMS responses.

## Before you begin

Ensure that the Notify and On-Call Scheduling plugins on your instance are activated.

Role required: notify\_view, or notify\_setup\_admin

## About this task

Set up Notify with On-Call Scheduling for the first time or migrate from On-Call Scheduling with NotifyNow.

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Numbers**.

2.  Select the phone number you want to use to send and receive on-call scheduling messages.

3.  In the **Notify group** field, select the **On-Call Group**.

    The On-Call Group is configured with the on-call workflows: **On-Call: Check Assignment Response**and **On-Call: Assign by Acknowledgement Voice** by default.

4.  Navigate to **Workflow** &gt; **Workflow Editor**.

5.  Select the **On-Call: Assign by Acknowledgement** workflow.

6.  Click the workflow menu icon in the title bar and select **Copy** to copy the **On-Call: Assign by Acknowledgement per rota** workflow.

    Save the copied workflow under a different name than what it is named by default.

    **Note:** You must avoid modifying default workflows and instead choose to copy and then modify the required workflow.

7.  Select a **Send SMS** activity.

8.  In the **To \(script\)** field, modify the getRecipientsAndNumberToSendFrom\(\) to use the correct value from getNotifyNumber\(\) notify number's sys ID.

9.  Close the **Workflow Editor**

10. Navigate to **On-Call Scheduling** &gt; **Trigger Rules**.

11. Select a trigger rule that launches an assignment workflow

12. In the **Trigger action** field, select **Workflow**.

13. In the **Trigger workflow** field, select the On-call: Assign by Acknowledgement workflow.

14. Click **Update.**

15. Repeat the previous 3 steps for each assignment trigger rule.

    Each time the conditions for one of these trigger rules is met, the On-call: Assign by Acknowledgement workflow runs.


**Parent Topic:**[Using Notify with On-Call Scheduling](../concept/c_NotifyWithOnCall.md)

**Related topics**  


[Controlling the on-call communication channel with Notify](../concept/c_OnCallNotifyForceCommChannel.md)

[Call a user from the WebRTC UI](t_CallfromWEBRTCUI.md)

[Key differences between on-call scheduling with NotifyNow and with Notify](../reference/r_OnCallNotifyNowNotifyDifferences.md)

[Workflow editor title bar](../../../administer/workflow/reference/r_WorkflowEditorTitleBar.md)

