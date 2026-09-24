---
title: Request an approval
description: Send an approval request for an issue or remediation task so designated approvers can review and respond to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/request-an-approval.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-16"
reading_time_minutes: 2
breadcrumb: [Issue approval flows, Common GRC features, Governance, Risk, and Compliance]
---

# Request an approval

Send an approval request for an issue or remediation task so designated approvers can review and respond to it.

## Before you begin

An approval must be configured directly on the table for the issue's or remediation task's current state. A due date extension approval must be configured for the source table. Approval configurations aren't inherited from parent tables. See [Configure approvals for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/configure-approvals-for-a-workflow.md).

Role required: sn\_grc\_appr.approver

## About this task

Approval requests can be submitted for a **State Change** approval or a **Due Date Extension** approval. The approval request shows the approvers and approval levels that will participate in the review process.

A **State Change** approval can also be requested from the playbook, where it appears as the last activity of a stage when an approval applies to the mapped state. The approval behaves the same way as it does on the record. A **Due Date Extension** approval isn't part of the playbook and is requested from the record only.

## Procedure

1.  Open the issue or remediation task.

2.  Select the approval that you want to request.

    An approval that was rejected or cancelled can be requested again. Requesting it again starts a new approval from the first approval level, and the earlier approval request remains in the approval history.

    An approval that is already awaiting a decision can't be requested again while it's in progress.

<table id="choicetable_approval_request_type"><thead><tr><th align="left" id="d82879e97">

Option

</th><th align="left" id="d82879e100">

Action

</th></tr></thead><tbody><tr><td id="d82879e106">

**__State Change__ approval**

</td><td>

Select **Request Approval**.

</td></tr><tr><td id="d82879e123">

**__Due Date Extension__ approval**

</td><td>

Select **Request due date extension**.

</td></tr></tbody>
</table>3.  If you're requesting a **Due Date Extension** approval, fill in the request fields.

    |Field|Description|
    |-----|-----------|
    |**Due date**|The current due date of the record.|
    |**Approved extensions**|The number of extensions that have been approved for the record. The maximum number of extensions allowed is set on the approval definition.|
    |**Proposed due date**|The requested due date.|
    |**Extension reason**|The reason for requesting the extension, selected from the configured list of extension reasons.|

4.  Review the approvers and approval levels.

    Approval levels indicate whether all approvers at a level must approve or whether any one approver can approve.

5.  Submit the request by selecting **Submit approval request**.


## Result

-   The approval request is submitted and routed to the configured approvers for review.
-   If no approvers are configured for the selected approval, the approval is marked as not required.
-   Approvers can review and respond to the request, and the requester receives a notification of the outcome when a decision is made. See [Review and respond to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/review-and-respond-to-an-approval-request.md).
-   When a **Due Date Extension** approval is approved, the proposed due date becomes the record's due date and the count of approved extensions increases. If it's rejected, the proposed due date is cleared, the count doesn't change, and the extension can be requested again.

**Parent Topic:**[Issue approval flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/issue-approval-flows.md)

