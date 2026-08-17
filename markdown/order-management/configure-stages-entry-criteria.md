---
title: Configure stages and entry criteria
description: Configure the stages and entry criteria that validate each approval state transition, ensuring a transaction can enter a stage only when its approval state confirms it belongs there.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-stages-entry-criteria.html
release: australia
topic_type: task
last_updated: "2026-06-29"
reading_time_minutes: 4
keywords: [approvals, stages, entry criteria, rule groups, configuration]
breadcrumb: [Set up the environment to manage approvals, Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure stages and entry criteria

Configure the stages and entry criteria that validate each approval state transition, ensuring a transaction can enter a stage only when its approval state confirms it belongs there.

## Before you begin

Role required: admin or sn\_adv\_appr\_mgmt.approval\_rule\_admin

Configure the approval events and their stage transitions. For more information, see [Configure approval events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-approval-events.md).

## About this task

Stage entry criteria act as the validation gate for each approval state transition. When an action event fires and updates txn.approvalState, the stage transition configured on that event attempts to move the transaction. The destination stage accepts the transaction only if its entry criteria conditions are met—ensuring the transaction cannot enter a stage unless the approval state confirms it belongs there. Rule groups are assigned to events to run the appropriate approval validation rules each time an event is triggered. For more information, see [Configure approval events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-approval-events.md).

Stages are fully customizable and managed by your admin. You can create as many stages as your process requires and name them as needed. This guide uses the following example structure: Draft → Pending Approval → Approved → Completed.

|Stage|Entry criteria \(txn.approvalState\)|
|-----|------------------------------------|
|Draft|None \(initial stage\)|
|Pending Approval|Equals requested|
|Approved|Equals approved|
|Completed|Per your process|

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Stages**.

    The Stages list opens.

2.  Create or confirm your stages, then configure each one with its entry criteria.

    For the example structure, ensure the following stages are present: Draft, Pending Approval, Approved, and Completed. Configure each stage and its associated event as described in the following substeps.

    1.  Configure the Draft stage and assign the **Cancel Approval** event \(txn.approval.revision\) and then select **Save**.

        No entry criteria are required because the Draft stage is the initial stage. The Draft stage is the starting point and the stage a transaction returns to after a recall or rejection. The Approval Revision rule group is assigned to the Cancel Approval event so that the correct validation rules run whenever that event fires and returns the transaction to Draft.

        **Tip:** If you have chosen a different stage as the recall or rejection destination, point the Cancel Approval event's stage transition at that stage. The Approval Revision rule group remains on the event.

    2.  Configure the Pending Approval stage.

        1.  Open the stage.
        2.  Set **Allow Entry When** to **All Conditions Are Met** with the condition Approval State \(txn.approvalState\) Equals requested.
        3.  Assign the **Request Approval** event \(txn.approval.submission\) on the stage.
        4.  Select **Save**.
        The transaction enters this stage after the seller submits a request for approval. The entry criteria validates that txn.approvalState has been set to requested by the Request Approval event before allowing entry—preventing a transaction from being manually moved to this stage without a legitimate approval request in flight. The Approval Submission rule group is assigned to the Request Approval event so its validation rules run when the event fires.

        **Tip:** Set this entry condition on whichever stage you designated as the submission destination in the Request Approval event transition, and keep the Approval Submission rule group on the event. You can also add further entry conditions here if your process requires additional validation before an approval request can proceed.

    3.  Configure the Approved stage.

        1.  Open the stage.
        2.  Set **Allow Entry When** to **All Conditions Are Met** with the condition **Approval State** \(**txn.approvalState**\) **Equals** **approved**.
        3.  Assign the **Approve Approval** event \(**txn.approval.completion**\) on the stage.
        4.  Select **Save**.
        The transaction enters this stage after all required approvers have approved. The entry criteria validates that txn.approvalState has been set to approved by the Approve Approval event. The Approval Completion rule group is assigned to the Approve Approval event so its validation rules run when the event fires.

        **Tip:** Set this entry condition on whichever stage you designated as the approval completion destination in the Approve Approval event transition, and keep the Approval Completion rule group on the event.

    Each stage accepts a transaction only when its entry criteria are met, and the assigned rule group runs its validation rules each time the stage is entered.


## Result

The approval stages are configured with entry criteria and rule groups. Each stage accepts a transaction only when the approval state confirms it belongs there, and the appropriate validation rules run on entry.

## What to do next

After approvals are configured, end users can submit approval requests using the approval interface. For user-facing tasks, see [Submit a quote for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/submit-quote-for-approval-process.md) and [Review and approve a submitted quote](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/review-and-approve-quote.md).

