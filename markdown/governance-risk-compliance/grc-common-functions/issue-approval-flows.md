---
title: Issue approval flows
description: Issue approval flows require review and approval before an issue or remediation task moves past a specific state, or before its due date is extended.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/issue-approval-flows.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-09-16"
reading_time_minutes: 3
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Issue approval flows

Issue approval flows require review and approval before an issue or remediation task moves past a specific state, or before its due date is extended.

## Benefits of approval flows

Issue approval flows provide the following benefits:

-   Add a review checkpoint before an issue or remediation task advances.
-   Track approval status directly on the record instead of relying on email or spreadsheets.
-   Enable approvers to review and respond to approval requests from the approval record.

## What triggers an approval

An approval is triggered by an approval configuration attached to an issue workflow or remediation task workflow.

Approval configurations support two approval types.

|Approval type|Description|
|-------------|-----------|
|**State Change**|Prevents an issue or remediation task from moving beyond a specified state until approval is granted.|
|**Due Date Extension**|Requires approval before a due date extension request can be processed. This approval type is not associated with a specific state.|

**Note:**

Only one **Due Date Extension** approval configuration can be active at a time for a given combination of workflow and applicable table. A workflow can therefore have one active **Due Date Extension** approval for issues and one for remediation tasks. There is no such limit on **State Change** approval configurations.

Attaching approvals to a workflow is an administrative task. See [Configure approvals for a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/configure-approvals-for-a-workflow.md).

## Approval process

An approval flow tracks the review process from the time an approval is requested until a decision is made. Approval requests and their status are displayed on the record, allowing stakeholders to monitor progress throughout the approval process.

When an approval is required, the assigned approver is notified, and an approval request is created. The approval request appears on the record and in the approver's work queue. The approver reviews the request and either approves or rejects it.

Approval requests can include one or more approval levels, depending on how the approval configuration is defined.

More than one approval can apply to the same state. When several approval configurations target one state, all of them are presented together when an approval is requested. Each runs as an independent approval with its own approvers and its own history. Approving or rejecting one has no effect on the others. Every approval that applies to a state must be approved before the issue or remediation task can move beyond that state.

## How approvals affect state changes

An issue or remediation task can move forward only when every **State Change** approval between its current state and the target state has been approved or determined not to be required. If an approval is still awaiting a decision, or was rejected or cancelled, the move is blocked. The message identifies the state and approval that is outstanding.

This applies even when the state model permits a state to be skipped. If an intermediate state has an approval that applies to the issue, that state can't be bypassed.

Moving an issue or remediation task backward is blocked while approvals at or above the target state are awaiting a decision. Those approvals must be cancelled first. Once the move is complete, the earlier approvals no longer count toward the approval requirement, so the approvals must be requested again when the issue moves forward.

A **Due Date Extension** approval doesn't block a state change, and it isn't affected by a backward state change.

## Approval history

Approval requests and approval decisions are recorded on the issue or remediation task. Approval records include information such as the approval state, approver, approval level, comments, and approval history, providing an audit trail that can be reviewed later.

-   **[Request an approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/request-an-approval.md)**  
Send an approval request for an issue or remediation task so designated approvers can review and respond to it.
-   **[Cancel an approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/cancel-an-approval.md)**  
Withdraw a pending approval request that is no longer needed so the approval can be requested again.
-   **[Review and respond to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/review-and-respond-to-an-approval-request.md)**  
Respond to an approval request assigned to you so the issue or remediation task can continue through its workflow.

**Parent Topic:**[Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/common-grc-features.md)

