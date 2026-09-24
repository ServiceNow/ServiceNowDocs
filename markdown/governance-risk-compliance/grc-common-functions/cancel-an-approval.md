---
title: Cancel an approval
description: Withdraw a pending approval request that is no longer needed so the approval can be requested again.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/cancel-an-approval.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-16"
reading_time_minutes: 1
breadcrumb: [Issue approval flows, Common GRC features, Governance, Risk, and Compliance]
---

# Cancel an approval

Withdraw a pending approval request that is no longer needed so the approval can be requested again.

## Before you begin

A pending approval request must exist.

You must have requested for the approval.

Role required: sn\_grc\_appr.approver

## About this task

Cancelling an approval request does not affect the issue or remediation task itself. Only the approval request is withdrawn.

Cancelling an approval request doesn't allow the issue or remediation task to move forward. A state change still requires an approved approval, so a new approval request must be submitted.

## Procedure

1.  Open the issue or remediation task.

2.  Withdraw the approval request by selecting **Cancel approval**.

3.  If more than one approval request is pending, select the approval request that you want to cancel.

4.  Review the approval request and confirm the cancellation.

    A confirmation message asks whether you want to cancel the approval request.


## Result

-   The approval request is cancelled and approvers can no longer take action on it.
-   The cancellation is recorded in the approval history and on the associated issue or remediation task.
-   A work note is added to the issue or remediation task indicating that approval cancellation was requested.
-   The option to request the approval again becomes available.
-   If the cancelled approval request has more than one approval level, the levels that haven't been requested yet are marked as no longer required.

**Parent Topic:**[Issue approval flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/issue-approval-flows.md)

**Related topics**  


[Request an approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/request-an-approval.md)

[Review and respond to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/review-and-respond-to-an-approval-request.md)

