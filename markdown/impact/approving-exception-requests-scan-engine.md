---
title: Approve or reject exception requests for Scan Engine findings
description: Exception approvers can review exception requests submitted by developers and approve or reject them. Approved exceptions exclude findings from technical debt calculations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/approving-exception-requests-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 2
breadcrumb: [Prevent technical debt with real-time code fixes, Platform Health, Using Impact, Impact]
---

# Approve or reject exception requests for Scan Engine findings

Exception approvers can review exception requests submitted by developers and approve or reject them. Approved exceptions exclude findings from technical debt calculations.

## Before you begin

You must be a member of an approval group or hold the Exception Approver role to approve or reject exception requests. Approvers have access to the exception approval interface.

Role required: sn\_se.scan\_engine\_exception\_approver, or membership in an approval group

## Procedure

1.  Receive a notification with the exception details and a link to the request when a developer submits an exception request.

    The notification includes:

    -   The finding definition that triggered the exception
    -   The severity level \(Suggest, Review, Recommend, or Act\)
    -   The exception reason provided by the developer
    -   The scanned record affected by the finding
    **Note:** Notifications are sent from the production instance only. The approval group needs a member with an email address, and the email properties must be on. If a notification doesn't arrive, check the email logs for an entry for it.

2.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **All exceptions**.

    \[Omitted image "se-exception-reasons.png"\] Alt text: The Exception Reasons list with the State, Raised By, Source Record, and Definition columns.

    You can also navigate to **All** &gt; **Impact** &gt; **Scan Engine** &gt; **Exceptions**. Select **Approved**, **Pending**, or **Rejected**.

    The **Exception Reasons** table opens the list of exceptions.

3.  Locate an exception and select the record link in the **Source Record** column.

    Records in the **Requested** state are pending approval.

4.  Select **View finding details** to open the findings panel.

5.  In the **Findings** panel, on the finding card with the Exception requested badge, select **View exception reason**.

    \[Omitted image "se-view-findings-panel.png"\] Alt text: The Findings panel with a finding card that has the Exception requested badge and the View exception reason button.

6.  Review the exception reason and finding details provided.

7.  Determine whether the exception is justified based on your organization's policies.

    Consider the following when evaluating an exception:

    -   Is the finding out of scope for your application or team?
    -   Is this a pre-existing issue with a remediation plan?
    -   Is the risk acceptable for your use case?
    -   Does the exception reason align with your organization's governance standards?
8.  In the **View exception** panel, select **Approve/reject exception**.

    \[Omitted image "view-exception-reason-approve-reject.png"\] Alt text: The View exception panel with the Return and Approve/reject exception buttons.

    The Exception Reason record opens.

9.  On the Exception Reason record, from the **State** list, select **Approved** or **Rejected**.

    \[Omitted image "se-exception-reject.png"\] Alt text: The State list on the exception record with Rejected selected and the Rejection Comments field.

    |Decision|Action|
    |--------|------|
    |**Approved**|The exception is granted. The finding is excluded from technical debt calculations and no longer blocks form submission. The finding card displays the Exception approved badge with the approval date.|
    |**Rejected**|The exception is denied. The developer receives notification and can submit a new exception request with different rationale or work to resolve the finding. The finding card displays the Exception rejected badge.|

    Based on your selection, the corresponding required Approval Comments or Rejection Comments field becomes available.

10. Enter your comments, and then select **Update**.

    -   The exception request is processed and the developer receives notification of your decision.
    -   The Findings list is updated with the Approved or Rejected exceptions.
    -   The finding card updates to display the Exception approved or Exception rejected badge.
    -   If approved, the finding is excluded from technical debt calculations.

