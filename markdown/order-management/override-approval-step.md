---
title: Override an approver
description: Override the approver in an approval step if the approval is no longer required, to help prevent the approval workflow from being blocked.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Override an approver

Override the approver in an approval step if the approval is no longer required, to help prevent the approval workflow from being blocked.

## Before you begin

Role required: approval\_admin \(platform role\) and sn\_adv\_appr\_mgmt.approval\_request\_writer

## About this task

As an approval admin with the approval request writer role, use this procedure to bypass or override the approver in an approval step that is no longer needed. The approval step must be in the Requested state.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the ![](../../../reuse/icons/product-icons/list-outline-24.svg)List icon.

3.  Navigate to the approval request.

    Access the request by navigating to the transaction entity and selecting the Approvals tab for the transaction. For example, navigate to **Quotes** &gt; **All**, select the quote, and select the Approvals tab to open the approval workflow.

4.  In the approval step card, select the More options menu and select **Override**.

5.  In the Override approval dialog box, select **Approve** or **Reject** in the **Approval decision** field.

    1.  If you select **Approve**, enter a comment and select **Submit**.

        The step record is updated and the workflow advances to the next step, which is in a requested state.

    2.  If you select **Reject**, enter a comment explaining the reason for rejection and select **Submit**.

        The step record is updated and the step state changes to Canceled, and the workflow stops. A rejection notification is sent to the requester, to change the approval request as needed and resubmit.


