---
title: Reject or return a quote for revision
description: As an approver, reject or return a submitted quote when it does not meet organizational requirements. The quote requester can then revise and resubmit for approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/reject-or-return-quote-for-revision.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [approvals, quote, reject, revision]
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Reject or return a quote for revision

As an approver, reject or return a submitted quote when it does not meet organizational requirements. The quote requester can then revise and resubmit for approval.

## Before you begin

Role required: Approver

## About this task

Reject an approval request when:

-   Pricing or discounts violate company policies
-   Customer account does not meet qualification criteria
-   Terms or conditions don't meet legal or contractual requirements
-   Required information is missing from the quote
-   Business conditions have changed since the quote was submitted

When you reject an approval request:

-   The quote status changes to Rejected, or to a customized status if configured.
-   The approval request is marked as rejected and removed from active approval workflows
-   The quote requester receives a notification with your rejection comments
-   The requester can make changes and resubmit the quote
-   When resubmitted, the quote goes through the complete approval process again , starting from the first approver

## Procedure

1.  Open the approval request for the quote you want to reject.

2.  Review the quote details and approval context to identify the reasons for rejection.

    Review the following:

    -   The specific approval conditions that aren't met
    -   Policy violations or non-conformance issues
    -   Missing information or required clarifications
3.  Select **Reject**.

    A form appears to document your rejection decision.

4.  In the **Comments** field, enter the reason for rejection and provide specific guidance for the requester.

    Provide clear, actionable feedback, for example, Discount exceeds approval threshold by 5%. Reduce by at least 6% for tier compliance.

5.  Select **Submit** to send the rejection.

    The rejection is processed. The system:

    -   Changes the quote status to **Returned for Revision**
    -   Records the rejection with timestamp and comments
    -   Sends a notification to the quote requester with your rejection reason
    -   Returns the quote to the requester for editing

## What to do next

-   The requester makes revisions based on your feedback
-   The requester resubmits the quote for approval by selecting **Request Approval**
-   The revised quote goes through the complete approval workflow from the beginning
-   You receive another approval request for the revised quote
-   You can track all previous rejection comments in the approval history

The **View Approval** panel shows:

-   All previous approval requests for the same quote
-   Status of each request \(approved, rejected, recalled\)
-   Your rejection comments and the requester's responses
-   Timestamp of each approval action

**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-advanced-approval-management.md)

