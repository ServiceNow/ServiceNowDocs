---
title: Approve or reject exception requests for Scan Engine findings
description: Exception approvers can review exception requests submitted by developers and approve or reject them. Approved exceptions exclude findings from technical debt calculations and unblock form submission.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/approving-exception-requests-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [Prevent technical debt with real-time code fixes, Platform Health, Using Impact, Impact]
---

# Approve or reject exception requests for Scan Engine findings

Exception approvers can review exception requests submitted by developers and approve or reject them. Approved exceptions exclude findings from technical debt calculations and unblock form submission.

## Before you begin

You must be assigned the Exception Approver role to approve or reject exception requests. Exception approvers receive notifications when new exception requests are submitted and have access to the exception approval interface.

Role required: sn\_se.scan\_engine\_exception\_approver

## Procedure

1.  When a developer submits an exception request, you receive a notification with the exception details and a link to the request.

    The notification includes:

    -   The finding definition that triggered the exception
    -   The severity level \(Suggest, Review, Recommend, or Act\)
    -   The exception reason provided by the developer
    -   The scanned record affected by the finding
2.  Select the notification link or navigate to the Findings panel and select the finding card with the Exception requested badge.

3.  On the finding card, select **View exception reason** to open the exception details.

    \[Omitted image "se-view-exception-reason-approver.png"\] Alt text: Exception reason submitting modal with the View exception reason button available.

4.  Review the exception reason and finding details provided by the developer.

5.  Determine whether the exception is justified based on your organization's policies.

    Consider the following when evaluating an exception:

    -   Is the finding out of scope for your application or team?
    -   Is this a pre-existing issue with a remediation plan?
    -   Is the risk acceptable for your use case?
    -   Does the exception reason align with your organization's governance standards?
6.  Select **Approve/reject exception** to open the approval modal.

    \[Omitted image "se-view-exception-reason.png"\] Alt text: The exception approval modal showing the definition, description, and exception reason with Approve and Reject buttons.

    |Decision|Action|
    |--------|------|
    |**Approve**|The exception is granted. The finding is excluded from technical debt calculations and no longer blocks form submission. The finding card displays the Approved badge with the approval date.|
    |**Reject**|The exception is denied. The developer receives notification and can submit a new exception request with different rationale or work to resolve the finding. The finding card displays the Rejected badge.|

    The exception request is processed and the developer receives notification of your decision. If approved, the finding is immediately excluded from technical debt calculations. The finding card updates to display the Approved or Rejected badge with the decision date.


