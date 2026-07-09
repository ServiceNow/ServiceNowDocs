---
title: Review and approve a submitted quote
description: As an approver, review the details of a submitted quote and approve the request when it meets your organization's requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/review-and-approve-quote.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 3
keywords: [approvals, quote, approve, review]
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Review and approve a submitted quote

As an approver, review the details of a submitted quote and approve the request when it meets your organization's requirements.

## Before you begin

Role required: Approver

**Important:** You can receive approval requests through multiple channels:

-   Email notifications
-   Approval dashboard or approval center in your workspace
-   Direct on the quote record

## About this task

Approvers are responsible for reviewing submitted quotes and either approving or rejecting them based on organizational policies such as pricing guidelines, legal requirements, and discount thresholds. Your approval decision routes the request to the next approver in the approval chain, or completes the approval process if you are the final approver.

As an approver, you must:

-   Review quote details and verify that they comply with company policies
-   Check the approval conditions that triggered the approval request \(for example, "Account Exception" or discount percentage\)
-   Make an approval decision: approve, reject, or request revision
-   Document your decision with comments if needed
-   Complete the approval within the expected timeframe \(escalations may be configured for overdue approvals\)

Approval requests may be configured to work in different ways:

-   **Sequential approvals:** Your approval must be completed before the request moves to the next approver. The quote remains pending until all required approvals are received.
-   **Parallel approvals:** Multiple approvers review the request simultaneously. The quote can proceed when any one approver approves it \(OR logic\) or when all assigned approvers approve it \(AND logic\).
-   **Multi-level chains:** Different approval rules may be assigned to different approvers based on the approval sequence \(for example, Sales Manager first, then Finance Manager\).

## Procedure

1.  Open the approval request notification or navigate to your approval dashboard to find pending approval requests.

    You can access approval requests from:

    -   Email notification from the approval system
    -   Approval section in your CSM/FSM Configurable Workspace
    -   Dedicated approval dashboard or approval center
    -   Directly on the quote record by clicking **View Approval**
2.  Click on the approval request to open the quote details.

    The quote record displays with:

    -   All quote fields and line items
    -   Customer account information
    -   Pricing and discount details
    -   Any other relevant business information
3.  Select **View Approval**.

    The approval panel appears and displays:

    -   The trigger conditions that required this approval \(for example, "Account Exception" or "Discount Tier 2: 70-89.99%"\)
    -   The approval rule that applies to your decision
    -   Other approvers in the chain and their status
    -   Any comments from the requester or previous approvers
4.  Verify that the quote meets your organization's approval criteria.

    Review the following based on your role and the approval rule:

    -   Sales team approvers: Verify customer information, special terms, and account status
    -   Finance approvers: Verify pricing, discount levels, and financial terms
    -   Legal approvers: Verify compliance, contract terms, and regulatory requirements
5.  Click **Approve** to approve the quote.

    The approval action is recorded, and the system:

    -   Documents your approval with the current timestamp
    -   Routes the request to the next approver in the chain \(if applicable\)
    -   Completes the approval process if you are the final required approver
    -   Notifies the quote requester and other approvers of the status change
6.  Add comments to document your approval decision.

    Use the comments field to:

    -   Document your approval rationale
    -   Flag any issues or concerns that the requester should address in future quotes
    -   Provide guidance to other approvers in the chain
    -   Record business context for audit purposes

## What to do next

After approving a quote:

-   If you were the final required approver, the quote moves to the "Approved" state and the requester can proceed to complete the transaction
-   If additional approvers are required, the request is routed to the next approver in the approval chain
-   If the requester resubmits a previously rejected quote with changes, you may receive another approval request for review
-   Track all your approval decisions in your approval history

**Tip:** If you cannot complete the approval within your assigned timeframe, contact your administrator about delegation or escalation options.

**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-advanced-approval-management.md)

