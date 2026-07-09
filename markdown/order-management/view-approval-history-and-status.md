---
title: View approval history and track status
description: Track the progress of submitted quote approval requests. View the complete history of approvals and rejections for audit and reference.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/view-approval-history-and-status.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 3
keywords: [approvals, history, status, tracking]
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# View approval history and track status

Track the progress of submitted quote approval requests. View the complete history of approvals and rejections for audit and reference.

## Before you begin

Role required: approval\_requester, approver, or approval\_request\_viewer.

## About this task

The approval history shows where a request is in the approval process. The history includes submitted requests, approver decisions, comments, and rejection reasons.

Approval requests can have the following statuses:

-   Pending: The request has been submitted and is awaiting an approver decision.
-   Approved: The approver has approved the request.
-   Rejected: The approver has rejected the request and returned it for revision.
-   Recalled: The requester withdrew the approval request before a decision was made.
-   Completed: All required approvals have been received and the approval process is complete.

The approval history records the following details for each approval action:

-   Timestamp of the approval action
-   Approver name or group that took the action
-   Action taken \(approved, rejected, recalled\)
-   Comments or notes provided by the approver
-   Approval rule or condition that triggered the approval
-   Approval request ID and version number

## Procedure

1.  Open the approval request for which you want to view approval history.

2.  Select **View Approval**.

    The approval panel opens showing the current approval status and a list of all approval requests for this quote or order.

3.  Review the current approval request details in the main approval panel.

    |Field|Description|
    |-----|-----------|
    |Request ID|Unique identifier for this approval request|
    |Status|Current state of the approval \(Pending, Approved, Rejected, Recalled, Completed\)|
    |Assigned Approvers|Names or groups that must approve this request|
    |Approval Progress|Visual indicator showing which approvers have acted and which are pending|
    |Trigger Conditions|The approval conditions that triggered this request \(for example, **Account Exception** or **Discount Tier 2**\)|
    |Request Date|Date and time when the request was submitted|

4.  View a specific approval request by selecting it from the list.

    The list shows all approval requests for the current quote or order, including:

    -   Request ID number
    -   Date submitted
    -   Final status \(Approved, Rejected, Recalled, or Active\)
    The approval panel updates to show the details of the selected approval request, including its complete history.

5.  Review the approval history timeline to see all actions taken on the request.

    The history shows a chronological record of:

    -   Request Submitted: Timestamp of the submission, including the requester name.
    -   Approvals Received: Each approval action taken, with timestamp and approver name.
    -   Approver Comments: Any notes or comments provided by approvers when they made their decision.
    -   Rejections and Recalls: Any rejection or recall actions, with reason documented by the requester or approver.
6.  View detailed comments from an approver by selecting the specific approval action in the history timeline.

    The approver's decision details appear, including:

    -   Approver name
    -   Decision made \(Approved, Rejected, Returned for Revision\)
    -   Approval rule applied
    -   Full text of the approver's comments or rejection reason
    -   Date and time of the decision
7.  If the request was rejected, review the rejection comments.

    The rejection comments explain:

    -   What specific issues need to be corrected
    -   What policy violations must be addressed
    -   What information is missing from the quote
    -   What actions you should take to get the quote approved
8.  Check the status of each assigned approver to monitor progress on pending requests.

    The approval panel shows:

    -   Which approvers have already acted on the request
    -   Which approvers are still pending
    -   The sequence of approvals \(if using approval chains\)
    -   How many approvals have been completed versus the total required

## What to do next

Based on the approval status and history, you can:

-   If approved: Proceed to complete the quote or order transaction
-   If rejected: Revise the quote to address the feedback from the approver and resubmit \(for more information, see [Reject or return a quote for revision](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/reject-or-return-quote-for-revision.md)\)
-   If pending: Wait for remaining approvers to complete their review, or contact them for status updates
-   If recalled: You can view previous approval requests to understand the decision history, then resubmit with updates

If your approval request is pending and has exceeded the expected approval timeframe:

1.  Check the approval panel for escalation status \(if escalations are configured\)
2.  Contact the pending approver directly to request an expedited review
3.  Escalate to your manager if the approval has been pending longer than your organizational SLA
4.  Contact your approval administrator for escalation options

**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-advanced-approval-management.md)

