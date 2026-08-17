---
title: Configure approval events
description: Configure the approval system events that control the approval buttons and stage transitions for a CPQ implementation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-approval-events.html
release: australia
topic_type: task
last_updated: "2026-06-29"
reading_time_minutes: 6
keywords: [approvals, approval events, event access, stage transition, configuration]
breadcrumb: [Set up the environment to manage approvals, Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure approval events

Configure the approval system events that control the approval buttons and stage transitions for a CPQ implementation.

## Before you begin

Role required: admin or sn\_adv\_appr\_mgmt.approval\_rule\_admin

The environment setup must be complete so that the approval system events, integrations, rules, and fields are seeded in your instance. For more information, see [Set up the environment to manage approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/setup-approvals-prerequisites.md).

## About this task

Configure these events. Do not create additional ones. The events fall into two groups based on how they are triggered.

|Event|Trigger type|What you configure|
|-----|------------|------------------|
|Preview Approval \(**txn.approval.preview**\)|Layout button|Event access rules that control when the button is visible, plus a layout button with a UI effect that opens the embedded SN approval component.|
|View Approval \(**txn.approval.view**\)|Layout button|
|Request Approval \(**txn.approval.request**\)|Fired by the embedded component|The stage transition that occurs after the action completes. No layout button is needed.|
|Approve Approval \(**txn.approval.approve**\)|Fired by the embedded component|
|Cancel Approval \(**txn.approval.cancel**\)|Fired by the embedded component|

## Procedure

1.  Configure the Preview Approval event \(**txn.approval.preview**\). The UI effect on the Preview Approval button opens the embedded SN approval component in Preview mode, showing the seller which approvals are triggered and who the approvers are before submitting. The **Request Approval** button inside this component triggers the Request Approval event.
2.  Configure the event access that controls when the Preview Approval button is visible.

    1.  Navigate to **CPQ Administration** &gt; **Transaction** &gt; **Events**.

    2.  Open the Preview Approval event \(**txn.approval.preview**\).

    3.  Select **Edit Event Access** in the top right.

    4.  Configure the visibility condition to show this event when txn.approvalState equals empty \(""\) or draft.

        The Preview button appears only when no approval is in progress.

    5.  Select **Save**.

    **Tip:** The preceding conditions reflect the default. Adjust them to match your stage structure—for example, if there are additional stages where the Preview button should or should not appear, add or modify conditions accordingly.

3.  Add the Preview Approval button to the layout.

    1.  Navigate to **Transaction** &gt; **Layouts** and open your layout.

    2.  In the **Header Buttons** section, add a new button and label it **Preview Approval** or a label of your choice.

    3.  In **Button Properties**, enable the **Event Button** toggle, then in the **Event** field select **Preview Approval**.

        This links the button visibility to the event access rules you configured.

    4.  Enable the **UI Effect Button** toggle, then set the UI effect properties:

        -   Set **UI Effect Type** to **Approvals**.
        -   Set **UI Effect Target** to **Modal** or **Slideout**, depending on your preferred display.
        -   Set **Mode** to **Preview**.
    5.  Select **Save**.

    The Preview Approval button appears in draft state and opens the embedded approval component in Preview mode.

4.  Configure the View Approval event \(**txn.approval.view**\). The UI effect on the View Approval button opens the embedded SN approval component in Status mode, showing the current approval status, approver details, history, and a **Recall** button for pending approvals. The **Recall** button inside this component triggers the Cancel Approval event.
5.  Configure the event access that controls when the View Approval button is visible.

    1.  Open the View Approval event \(**txn.approval.view**\).

    2.  Select **Edit Event Access** in the top right.

    3.  Configure the visibility condition to show this event when txn.approvalState is not empty and not draft—for example, when it equals requested, approved, recalled, or rejected.

        The View button appears only after an approval is initiated.

    4.  Select **Save**.

    **Tip:** You control which approval states cause this button to appear. For example, if you do not want the View button visible after an approval is fully completed, you can exclude the approved state from the condition.

6.  Add the View Approval button to the layout.

    1.  In your layout, go to **Header Buttons** and add a new button.

    2.  Label it **View Approval** or a label of your choice.

    3.  In **Button Properties**, enable the **Event Button** toggle, then in the **Event** field select **View Approval**.

    4.  Enable the **UI Effect Button** toggle, then set the UI effect properties:

        -   Set **UI Effect Type** to **Approvals**.
        -   Set **UI Effect Target** to **Modal** or **Slideout**.
        -   Set **Mode** to **Status**.
    5.  Select **Save**.

    The View Approval button appears after an approval is initiated and opens the embedded approval component in Status mode.

7.  Configure the stage transitions for the action events. The Request Approval, Approve Approval, and Cancel Approval events are fired automatically by the embedded SN component when the seller or approver takes an action. Each event runs **txn.approval.getState**—a built-in integration that fetches the current approval state from ServiceNow—and updates the **txn.approvalState** field. No layout button is needed for these events.
8.  Configure the stage transition for the Request Approval event \(**txn.approval.request**\).

    This event is triggered when the seller selects **Request Approval** inside the embedded SN component.

    1.  Navigate to **Transaction** &gt; **Events**.

    2.  Open the Request Approval event \(**txn.approval.request**\).

    3.  Scroll to the **Stage Transition** section.

    4.  Enable the **Transition after actions** toggle.

    5.  Set **After all actions run, transition to** **forward**.

    6.  Select **Add New Action**.

    7.  To add rule group to an event, select the **Rule grouping** and then assign the **txn.approval.submission** rule grouping.

    8.  Select **Save**.

    **Tip:** If your stage sequence differs from the default, verify the forward transition points to the correct next stage. You can also add a Rule Grouping action on this event if additional rules need to run at submission time.

    When a seller submits a request, the transaction moves forward to the Pending Approval stage.

9.  Configure the stage transition for the Approve Approval event \(**txn.approval.approve**\).

    This event is triggered when all required approvers approve the request, either inside the embedded SN component or by email. It updates **txn.approvalState** to approved.

    1.  Open the Approve Approval event \(**txn.approval.approve**\).

    2.  Scroll to the **Stage Transition** section.

    3.  Enable the **Transition after actions** toggle.

    4.  Set **After all actions run, transition to** **forward**.

    5.  Select **Add New Action**.

    6.  To add rule group to an event, select the **Rule grouping** and then assign the **txn.approval.completion** rule grouping.

    7.  Select **Save**.

    **Tip:** If you have additional stages between Pending Approval and Approved, verify the forward transition lands on the correct destination. Entry criteria on the Approved stage validates the state before allowing entry regardless.

    When all approvers approve, the transaction moves forward to the Approved stage.

10. Configure the stage transition for the Cancel Approval event \(**txn.approval.cancel**\).

    This event is triggered when the seller selects **Recall** inside the embedded SN component \(Status mode\), or when an approver rejects the request, ending the approval cycle. It updates **txn.approvalState** to recalled or rejected accordingly.

    1.  Open the Cancel Approval event \(**txn.approval.cancel**\).

    2.  Scroll to the **Stage Transition** section.

    3.  Enable the **Transition after actions** toggle.

    4.  Set **After all actions run, transition to** **backward**.

    5.  Set **If available from current stage, go back to** **Draft**.

    6.  Select **Add New Action**.

    7.  To add rule group to an event, select the **Rule grouping** and then assign the **txn.approval.revision** rule grouping.

    8.  Select **Save**.

    **Tip:** If you want the transaction to return to a different stage on recall or rejection—for example, a dedicated Rejected stage rather than Draft—change the target stage here and verify that stage exists in your blueprint with appropriate entry criteria.

    On recall or rejection, the transaction returns to the Draft stage so the seller can make changes and resubmit.


## Result

All five approval events are configured. The Preview and View buttons appear in the layout according to the approval state, and each action event moves the transaction to the correct stage.

## What to do next

Configure the stages and entry criteria that validate each approval state transition. For more information, see [Configure stages and entry criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-stages-entry-criteria.md).

